---
name: fabric-scr-finalize
description: "Finalize a completed Fabric SCR deal by archiving its workspace. USE WHEN: an SCR is done/approved/signed off and should be moved out of the active working area. Moves wip/<customer_short>/ to completed_scrs/<customer_short>/, preserving git history. Triggers on 'finalize scr', 'complete scr', 'archive scr', 'mark scr done', 'move bosch to completed', or any request to close out / archive a finished deal."
---

# Fabric SCR — Finalize deal (Phase 4)

Archive a finished deal by moving its self-contained workspace from the active
`wip/` area into `completed_scrs/`, keeping inputs and outputs together and
preserving git history.

```
wip/<customer_short>/            →    completed_scrs/<customer_short>/
  inputs/   outputs/                    inputs/   outputs/
```

---

## PHASE 4 — Finalize

### 4a. Identify the deal
Resolve `customer_short` from the user prompt (e.g. `bosch`, `ford`). Confirm the
source folder `wip/<customer_short>/` exists; if not, list the folders under `wip/`
and stop.

### 4b. Pre-flight checks (stop and report if any fail)
- The deal's data file `wip/<customer_short>/outputs/<short>-scr.data.yml` exists.
- A rendered SCR markdown `wip/<customer_short>/outputs/Fabric-SCR-<short>-*.md` exists
  (the deal has actually been rendered, not just populated).
- The destination `completed_scrs/<customer_short>/` does NOT already exist (never
  overwrite a previously archived deal — stop and ask if it does).
- There are no uncommitted changes inside `wip/<customer_short>/` that the user has
  not been told about. Surface `git status --short wip/<customer_short>/` and confirm
  before moving.

### 4c. Move the folder (preserve history)
Create `completed_scrs/` if it does not yet exist, then move the whole deal folder.
Use `git mv` for tracked files so history follows the rename; move any git-ignored
files (e.g. the `.docx`) with a regular move.

```powershell
New-Item -ItemType Directory -Force -Path "completed_scrs" | Out-Null

# Tracked files (history-preserving)
git mv "wip/<customer_short>" "completed_scrs/<customer_short>"

# If git mv leaves ignored files behind (e.g. *.docx, media/), move them too:
if (Test-Path "wip/<customer_short>") {
  Get-ChildItem "wip/<customer_short>" -Recurse -File | ForEach-Object {
    $dest = $_.FullName -replace [regex]::Escape("\wip\<customer_short>\"), "\completed_scrs\<customer_short>\"
    New-Item -ItemType Directory -Force -Path (Split-Path $dest) | Out-Null
    Move-Item $_.FullName $dest -Force
  }
  if ((Get-ChildItem "wip/<customer_short>" -Recurse -File | Measure-Object).Count -eq 0) {
    Remove-Item "wip/<customer_short>" -Recurse -Force
  }
}
```

> If a file inside the folder is locked (e.g. the `.docx` is open in Word), stop and
> ask the user to close it, then retry — do not force-delete in-progress work.

> Only ever remove the specific `wip/<customer_short>/` subfolder. NEVER remove the
> `wip/` parent directory — it is kept under version control by `wip/.gitkeep` so the
> active work area is always present, even when no deals are in flight.

### 4d. Fix internal path references
Anything inside the moved files that points at `wip/<customer_short>/` must now point
at `completed_scrs/<customer_short>/`. Update:
- The data file header comments, `meta.source_config`, and any `references[].url`
  that referenced `wip/<customer_short>/inputs/...`.
- The input config `inputs.sow_docx` and `inputs.supporting` paths.
- The rendered markdown footer (`… from wip/<customer_short>/outputs/<short>-scr.data.yml`)
  and any in-body source citations that referenced `wip/<customer_short>/inputs/...`.

Grep the moved folder for `wip/<customer_short>` and replace each hit with
`completed_scrs/<customer_short>`.

### 4e. Validate and report
- Re-parse the moved data file (and input config) to confirm the YAML still loads.
- Report: source → destination paths, the files moved, whether the `.docx` came along,
  and any remaining `wip/<customer_short>` references that still need attention.
- Do NOT commit or push unless the user asks. Leave the staged `git mv` for review.

---

## Constraints
- This phase **moves**, it does not regenerate — never re-render or re-populate here.
- NEVER overwrite an existing `completed_scrs/<customer_short>/`.
- Preserve git history: use `git mv` for tracked files; only fall back to a plain move
  for git-ignored files (`.docx`, `media/`).
- Do not delete the source folder until every file has been moved.
- Remove only `wip/<customer_short>/`; never remove the `wip/` parent (kept by `wip/.gitkeep`).
- Do not commit/push as part of finalize unless explicitly asked.
