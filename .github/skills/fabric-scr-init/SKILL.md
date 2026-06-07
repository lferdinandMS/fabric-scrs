---
name: fabric-scr-init
description: "Initialize a new Fabric SCR deal workspace. USE WHEN: starting a new Fabric SCR for a customer who does not yet have a wip/<customer>/ folder structure. Creates the deal folder, input config, and output placeholder, then instructs the human on what to drop in. Triggers on 'init scr', 'new scr', 'create scr workspace', 'scaffold bosch scr', or any request to set up a new deal for the SCR workflow."
---

# Fabric SCR — Initialize deal workspace (Phase 0)

Scaffold a new deal folder so the **Fabric SCR Author** agent can run Phase 1
(populate the data file) as soon as the SOW and supporting files are dropped in.

---

## PHASE 0 — Initialize

### 0a. Identify the deal
Collect the following (from the user prompt or, if missing, ask before proceeding):

| Field | Source |
|----|----|
| `customer_short` | Short name / filename-safe identifier (e.g. `bosch`, `ford`) |
| `customer` | Full legal customer name |
| `engagement_name` | Short engagement description |

### 0b. Create the folder structure
```
wip/
  <customer_short>/
    inputs/           ← human drops SOW + staffing plan here
```

Create `wip/<customer_short>/inputs/` (and `wip/<customer_short>/` if needed).

### 0c. Scaffold the input config
Copy `templates/scr-config.template.yml` to
`wip/<customer_short>/inputs/scr-<customer_short>.yml` and pre-fill:
- `customer` ← from step 0a
- `customer_short` ← from step 0a
- `engagement_name` ← from step 0a
- `inputs.sow_docx` ← `"wip/<customer_short>/inputs/<< Statement of Work .docx >>"`
- `inputs.supporting` ← `["wip/<customer_short>/inputs/<< Staffing plan .xlsx >>"]`

Leave all business fields (`msx_id`, `deal_value_usd`, `date`, etc.) as `<< ... >>`
placeholders — these are filled by the human before handing off to Phase 1.

### 0d. Hand off to the human
Report:
- Paths created
- Files the human must drop into `wip/<customer_short>/inputs/`:
  - Statement of Work (`.docx`)
  - Staffing plan (`.xlsx`, if available)
  - CompassOne screenshot (optional but recommended)
- Fields in `scr-<customer_short>.yml` that need filling before the agent can populate the
  data file: `customer_short`, `date`, `opportunity.*`, `team.*`, `commercials.*`
- Command to kick off Phase 1 once ready:
  ```
  @Fabric SCR Author wip/<customer_short>/inputs/scr-<customer_short>.yml populate
  ```

---

## Constraints
- Do NOT populate the data file or read a SOW as part of init — this phase is scaffolding only.
- Do NOT invent MSX IDs, deal values, or team names — leave `<< ... >>` placeholders.
- The output folder (`wip/output/`) is shared; per-customer inputs live under `wip/<customer_short>/inputs/`.
