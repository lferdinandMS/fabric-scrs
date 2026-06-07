# Fabric SCR Runbook

How to produce a **Fabric Special Conditions Review (SCR = Special Conditions Review)**
Word document from a deal's source material. This process runs several times a year,
once per qualifying opportunity.

## Repository layout

| Folder | Purpose |
|----|----|
| `templates/` | The Word styling template (`Fabric-SCRTemplate-<date>.docx`). Used as the pandoc `--reference-doc` so output inherits Microsoft house styles (fonts, headings, table styles, margins). |
| `wip/inputs/` | Source material for the deal under review — Statement of Work (SOW), staffing plan, CompassOne screenshots, etc. |
| `wip/output/` | Generated artifacts per deal: the working `.md` and the final `.docx`. |

**Naming convention:** `Fabric-SCR-<Customer>-<YYYYMMDD>` for both the `.md` and `.docx`
(e.g. `Fabric-SCR-Ford-20260606`).

## Two ways to run this

This runbook covers **both**:

- **Manual pandoc workflow** (Steps 0–4) — convert/edit/style by hand.
- **Agentic workflow** (the [Fabric SCR Author](.github/agents/fabric-scr.agent.md) agent +
  `fabric-scr` skill) — the agent populates a structured **data file** from the config + SOW
  for you to review, then renders the `.md`/`.docx` from it. See *Agentic data-file model* below.

## Agentic data-file model

The agent splits the work across **three files** so that machine extraction and human review
stay cleanly separated:

| File | Role | Who writes it |
|----|----|----|
| `wip/inputs/<short>.yml` | **Input config** — deterministic deal facts + pointers to the SOW. Pristine; the agent never overwrites it. Schema: [templates/scr-config.template.yml](templates/scr-config.template.yml). | Human |
| `wip/output/<short>-scr.data.yml` | **Data work product** — the structured SCR holding all three data tiers with **per-field provenance** (`status` + `sources`). This is the single source of truth and the human review surface. Schema: [templates/scr-data.template.yml](templates/scr-data.template.yml). | Agent populates → human reviews |
| `wip/output/Fabric-SCR-<short>-<YYYYMMDD>.md` / `.docx` | **Render targets** — generated FROM the approved data file only. | Agent (render phase) |

**Three data tiers** (every section maps to exactly one):

1. **Config-sourced** → Opportunity Overview, Pre-Conditions (copied/derived from the input config).
2. **Document-extracted** → Project Overview, SCR Risk Types, workloads (thorough SOW review).
3. **Synthesized** → Review Summary, Key Points Considered, Key Risk Factors (summary of tiers 1+2).

**Per-field `status`** in the data file:
`extracted` · `synthesized` · `verified` · `unverified` · `human-edited` · `approved`.

**Two-phase flow:**

- **Phase 1 — Populate.** Agent reads the input config, converts + thoroughly reads the SOW,
  and fills `<short>-scr.data.yml` tier by tier. Risk-Type claims (preview/GA status, connectors,
  SLAs) are checked against **authoritative sources only** (Microsoft Learn / official docs /
  the SOW / first-party ISV docs), recorded in `references:` and cited by id in each field's
  `sources:`. Anything unconfirmed is left `status: unverified`. The agent then **stops for review**.
- **Phase 2 — Human review.** You edit the data file: fix values, resolve every `<< ... >>` and
  `unverified`, and flip `status` to `human-edited` / `approved`. Re-running Phase 1 only
  refreshes still-unreviewed fields.
- **Phase 3 — Render.** Agent generates the `.md` (GFM tables, inline `[n]` citations) and the
  styled `.docx` **from the data file only** — no new facts at render time.

The manual Steps 1–4 below are exactly what the agent's render phase automates.

## Prerequisites (one-time)

- **pandoc** — document converter (installed via scoop). Check: `pandoc --version`.
- **Microsoft Word** — only needed to unprotect the template (see step 0).
- **Python venv** — the workflow's Python deps (`pyyaml` for YAML validation,
  `openpyxl` for reading the staffing `.xlsx`; pandoc cannot read Excel) live in a
  repo-local `.venv`. Create it once:
  ```powershell
  python -m venv .venv
  .\.venv\Scripts\python.exe -m pip install -r requirements.txt
  ```
  Verify: `.\.venv\Scripts\python.exe -c "import yaml, openpyxl; print('deps OK')"`.
  Use `.\.venv\Scripts\python.exe` wherever a step calls `python`.

## Step 0 — Unprotect the template (only if encrypted)

The template may ship with a **Microsoft sensitivity label / IRM (Information Rights
Management) encryption**. pandoc cannot read an encrypted file as a reference document.

**How to tell:** check the first bytes of the template.

```powershell
$f = 'templates/Fabric-SCRTemplate-20250605.docx'
($([System.IO.File]::ReadAllBytes($f)[0..3]) | ForEach-Object { $_.ToString('X2') }) -join ' '
```

- `50 4B 03 04` (PK) → plain OOXML `.docx`. **Good — skip to Step 1.**
- `D0 CF 11 E0` → OLE2 wrapper = **encrypted/protected**. Unprotect it first:
  1. Open the template in **Word**.
  2. **File → Info → Protect Document → Restrict Access → Unrestricted Access**
     (or change the sensitivity label to a non-encrypted one).
  3. **Save As** a plain `.docx` (overwrite the template or save a working copy).

> Stripping protection is a rights/policy decision. Only do it if you are permitted to.

## Step 1 — (Optional) Convert an existing SCR docx to markdown for review

If you are reviewing/editing an existing SCR `.docx`, convert it to markdown first:

```powershell
pandoc "wip/output/<file>.docx" -f docx -t gfm --wrap=none `
  --extract-media="wip/output/media" -o "wip/output/<file>.md"
```

- `--extract-media` pulls any embedded images into `wip/output/media/`.
- If there are no images, no media folder is created.

## Step 2 — Edit the markdown

Edit `wip/output/<file>.md` as the single source of truth for content.

### Critical: tables with bullet lists

pandoc renders a Word table cell that contains a bulleted list as a **raw HTML
`<table>` block**, not a GitHub-flavored-markdown (GFM) pipe table.

> **HTML `<table>` blocks are silently dropped when converting markdown back to
> `.docx`.** The table will vanish from the Word output with no error.

**Fix — flatten any HTML table into a GFM pipe table:**

- Use pipe syntax: `| Header | Header |` with a `|----|----|` separator row.
- Represent in-cell line breaks with `<br>`.
- Represent former bullet points as `<br>`-separated lines, each prefixed with `–`.

This keeps all content and round-trips cleanly into Word (in-cell bullets become
line-broken text rather than native Word list items — content preserved, only the
bullet glyph formatting changes).

## Step 3 — Generate the final styled Word document

```powershell
pandoc "wip/output/<file>.md" -f gfm -t docx `
  --reference-doc="templates/Fabric-SCRTemplate-20250605.docx" `
  -o "wip/output/<file>.docx"
```

`--reference-doc` applies the template's **styles only** (fonts, heading and table
styles, margins). It does **not** copy any boilerplate body text from the template —
the document body comes entirely from your markdown.

## Step 4 — Verify the output

Spot-check that key sections and the (formerly HTML) table survived:

```powershell
pandoc "wip/output/<file>.docx" -f docx -t plain --wrap=none |
  Select-String -Pattern "SCR Risk Type|Review Summary|Key Risk Factors"
```

Then open the `.docx` in Word to confirm styling and table rendering.

## Quick reference

| Task | Command |
|----|----|
| Check template encryption | `([System.IO.File]::ReadAllBytes('templates\Fabric-SCRTemplate-20250605.docx')[0..3] | %{ $_.ToString('X2') }) -join ' '` |
| docx → markdown | `pandoc in.docx -f docx -t gfm --wrap=none --extract-media=wip/output/media -o out.md` |
| markdown → styled docx | `pandoc out.md -f gfm -t docx --reference-doc=templates/Fabric-SCRTemplate-20250605.docx -o out.docx` |
| Verify docx text | `pandoc out.docx -f docx -t plain --wrap=none | Select-String "<pattern>"` |

## Known gotchas

- **HTML tables drop on md → docx.** Always flatten to GFM pipe tables (Step 2).
- **Encrypted template.** pandoc can't read an IRM/sensitivity-labelled template;
  unprotect it first (Step 0).
- **Word COM automation to strip encryption is unreliable** from PowerShell and may
  hang or hold a file lock — prefer unprotecting through the Word UI.
- **`~$` lock files** in `templates/` mean the file is open in Word; harmless for
  pandoc (read-only) but don't commit them.
