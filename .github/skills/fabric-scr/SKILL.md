---
name: fabric-scr
description: "Generate a Fabric Special Conditions Review (SCR) document from a per-deal YAML config. USE WHEN: creating a new Fabric SCR, populating the SCR data file from a SOW, scaffolding an SCR document in wip/output, converting an SCR markdown to a styled Word docx, or running the SCR pandoc workflow. Two-phase: populate a reviewable data file, then render markdown + docx with GFM table flattening and the SCR template."
---

# Fabric SCR Skill

Produce a **Fabric Special Conditions Review (SCR = Special Conditions Review)** document
from a per-deal config plus the deal's Statement of Work (SOW). Full reference:
[RUNBOOK.md](../../../RUNBOOK.md).

## Three files, three roles

| File | Role | Who writes it |
|----|----|----|
| `wip/<customer_short>/inputs/scr-<short>.yml` | **Input config** — deterministic facts + pointers to the SOW. Pristine; never overwritten. | Human |
| `wip/output/<short>-scr.data.yml` | **Data work product** — the structured SCR with all three tiers + per-field provenance. The single source of truth and the human review surface. | Agent populates, human reviews |
| `wip/output/Fabric-SCR-<short>-<YYYYMMDD>.md` / `.docx` | **Render targets** — generated FROM the data file. | Agent (render) |

Data-file schema: [templates/scr-data.template.yml](../../../templates/scr-data.template.yml).
Input schema: [templates/scr-config.template.yml](../../../templates/scr-config.template.yml).

## Data-flow model — every section is one of three tiers

| Tier | Sections | Source |
|----|----|----|
| **1. Config-sourced** | Opportunity Overview, Pre-Conditions | the input config |
| **2. Document-extracted** | Project Overview, SCR Risk Types (incl. workloads) | thorough review of `inputs.sow_docx` |
| **3. Synthesized** | Review Summary, Key Points Considered, Key Risk Factors | summary of tiers 1 + 2 |

Each Tier-2 / Tier-3 field in the data file carries a `status`:
`extracted` · `synthesized` · `verified` · `unverified` · `human-edited` · `approved`.

---

## PHASE 0 — Initialize a new deal workspace

If the deal folder and input config do not yet exist, run the **fabric-scr-init** skill
(`.github/skills/fabric-scr-init/SKILL.md`) to scaffold `wip/<customer_short>/inputs/` and
the starter config before proceeding to Phase 1.

---

## PHASE 1 — Populate the data file

### 1. Read and validate the input config
- Load `wip/<customer_short>/inputs/scr-<short>.yml`.
- Confirm required fields: `customer`, `customer_short`, `date`, `commercials.deal_value_usd`,
  `inputs.sow_docx`.
- Data-file path = `wip/output/<customer_short>-scr.data.yml`. If it already exists, do NOT
  clobber — load it and refresh only fields whose `status` is still `extracted`/`synthesized`/
  `unverified` (never overwrite `human-edited` or `approved` without confirmation).

### 2. Convert the SOW for review
```powershell
pandoc "<inputs.sow_docx>" -f docx -t gfm --wrap=none -o "wip/output/_sow-<short>.md"
```
Read the whole converted SOW before extracting — do not skim.

### 3. Fill the data file by tier
Start from [templates/scr-data.template.yml](../../../templates/scr-data.template.yml).

- **Tier 1 (copy from config):** `identity`, `opportunity`, `commercials`, `output`. Compute
  `pre_conditions` as bare **Yes/No**:
  - `fabric_and_prod_under_10m` → Yes if `fabric_in_scope` AND `deal_value_usd < 10,000,000`.
  - `fabric_10m_or_above_triggers_scr` → Yes only if `deal_value_usd >= 10,000,000`.
- **Tier 2 (extract from SOW):** `project_overview`, `workloads`, and each `risk.*` field. Set
  `status: extracted`. Workloads come from the SOW, NOT the config. Never invent names — leave
  `<< Confirm name / alias >>`.
- **Tier 3 (synthesize):** `review_summary`, `key_points`, `key_risk_factors` from tiers 1–2
  only. Set `status: synthesized`.

### 3a. Staffing-plan analysis (Tier 2)
Read the staffing plan from `inputs.supporting` (the `.xlsx`). This needs **openpyxl**
(pandoc cannot read Excel), which lives in the repo `.venv`. Ensure the venv exists:
```powershell
if (-not (Test-Path .venv)) { python -m venv .venv; .\.venv\Scripts\python.exe -m pip install -r requirements.txt }
```
Then convert/read it, e.g.:
```powershell
.\.venv\Scripts\python.exe -c "import openpyxl,sys; wb=openpyxl.load_workbook(sys.argv[1],data_only=True); [print('--',ws.title) or [print(','.join('' if c is None else str(c) for c in r)) for r in ws.iter_rows(values_only=True)] for ws in wb.worksheets]" "<inputs.supporting staffing .xlsx>"
```
```
- Fill `staffing.roles` and judge `staffing.data_engineering.adequate` (Yes/No/Borderline):
  are **data-engineering resources present in the numbers required to deliver the projected
  workloads/outcomes**? Note any gap, under-, or over-staffing in `assessment`.
- Add the staffing **boilerplate bullet** to `key_points` (completed with the adequacy summary).
- If `adequate` is **No**/**Borderline**, add a matching **risk** to `key_risk_factors`
  (e.g. insufficient data-engineering coverage for the projected workloads).

### 4. Authoritative sources + provenance (Risk Types)
For Risk Types — especially Non-GA / preview status, connector availability, and SLAs — rely
ONLY on **authoritative sources**: Microsoft Learn / official product docs, Fabric/Azure
release notes or roadmap, the SOW itself, or first-party ISV documentation. Never assert
preview/GA status from memory or third-party blogs.
- Add each source to the `references:` list with `id`, `title`, `url`, `accessed`.
- Reference them by id in each risk field's `sources: [n, …]`.
- If a status cannot be confirmed, set that field's `status: unverified` and leave a
  `<< unverified — confirm against Microsoft Learn >>` marker. Do not guess.

### 5. Hand off for human review
Report: data-file path, the derived Pre-Conditions Yes/No, a per-field `status` summary, the
count of references, and every `<< ... >>` / `unverified` field still needing a human. STOP
here unless the user asks to render.

---

## PHASE 2 — Human-in-the-loop (no agent action)

The human edits the data file: corrects values, resolves `<< ... >>` and `unverified`, and
flips `status` to `human-edited` / `approved`. Re-run Phase 1 to refresh only un-reviewed
fields, or proceed to render when satisfied.

---

## PHASE 3 — Render markdown + Word from the data file

### 6. Scaffold the markdown
Render `wip/output/Fabric-SCR-<short>-<YYYYMMDD>.md` from the data file ONLY (do not re-read
the SOW). Section order (must mirror the SCR template — no extra sections):
Opportunity Overview → Project Overview → Team Involved → Pre-Conditions →
Special Conditions Review Criteria (SCR Risk Type) → Review Summary → Key Points Considered →
Key Risk Factors → References. Emit inline `[n]` citations matching `references`.

> **Render only template sections.** `workloads` and `staffing` are analysis inputs that live
> in the data file (they feed the SCR Risk Type "workloads" row and the synthesized Review
> Summary / Key Points / Key Risk Factors) — they are NOT standalone sections in the template,
> so do NOT emit "Workloads in Scope" or "Staffing & Data-Engineering Adequacy" headings/tables.

> **References is required.** The template defines a `References` heading, so always close the
> document with a `### References` numbered list. Every entry MUST be authoritative — Microsoft
> Learn / official Microsoft docs, the deal SOW, or first-party ISV docs (never blogs, forums,
> or third-party tutorials). Every `references` entry must be cited by at least one inline `[n]`,
> and every inline `[n]` must resolve to a `references` entry (no orphans either way).

End the markdown with a self-identifying footer (so any printout/export is traceable without
filename suffixes). The filename stays stable across revisions — git is the version history:
```markdown
---
*Revision `<meta.revision>` · generated `<meta.generated_utc>` · rendered `<output.rendered_utc>` from `wip/output/<short>-scr.data.yml`.*
```

**Indent body content one level under its heading.** Indentation is template-driven, not
hand-applied:
- **Prose paragraphs and bullet/number lists** under a heading are prefixed with a blockquote
  marker `> ` on *every* line. Pandoc maps `>` to the template's **Block Text** style, which
  the SCR template defines with a left indent.
- **Pipe tables are NOT blockquoted** — leave them flush in the markdown. They indent via the
  template's **Table** style (which carries a matching `tblInd` plus borders).
- Headings and the footer line stay flush-left; a new heading resets the indent.

> The indent only appears because the reference template defines indented `Block Text` and
> `Table` styles (paragraph `w:ind w:left` and table `w:tblInd`, ~360 twips / 0.25"). If a
> future template lacks them, body content renders flush — add the styles to the template
> rather than hand-indenting the markdown.

### 7. Tables — ALWAYS use GFM pipe tables
> Raw HTML `<table>` blocks are silently dropped on markdown → docx.

- Build every table as a GFM pipe table (`| col | col |` + `|----|----|`), flush-left (no `>`).
- For multi-line / bulleted cell content use `<br>` for line breaks and prefix former bullets
  with `–`. Never emit a `<table>` element.

### 8. Generate the styled Word document (if `output.generate_docx: true`)
Confirm the reference template is unencrypted (PK magic `50 4B 03 04`; if `D0 CF 11 E0` it is
IRM-encrypted — stop and ask the user to unprotect it). Then:
```powershell
pandoc "wip/output/<filename>.md" -f gfm -t docx `
  --reference-doc="<output.reference_template>" `
  -o "wip/output/<filename>.docx"
```

### 9. Verify
```powershell
pandoc "wip/output/<filename>.docx" -f docx -t plain --wrap=none |
  Select-String -Pattern "SCR Risk Type|Review Summary|Key Risk Factors|References"
```
Report the created file paths and any remaining `<< ... >>` / `unverified` fields.

### 10. Stamp render provenance
In the data file set `output.rendered_utc` (now, UTC ISO-8601) and
`output.rendered_from_revision: <meta.revision>`. Bump `meta.revision` by 1 whenever the data
file is re-populated or human-edited before a re-render; the `.md` is the committed artifact
and the `.docx` is git-ignored (reproducible via pandoc).

## Guardrails
- Do NOT strip template encryption automatically — that is a rights/policy decision.
- Do NOT overwrite `human-edited` / `approved` data-file fields, or any existing render output,
  without explicit confirmation.
- Do NOT invent deal facts, names, or product statuses — extract from the SOW or cite an
  authoritative source; otherwise leave a `<< ... >>` placeholder and `status: unverified`.
- The render phase reads the data file ONLY — never inject new facts at render time.
