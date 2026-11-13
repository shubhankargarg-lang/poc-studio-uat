# UAT changes

Every change made in this UAT copy, so exactly these can be moved to the live plugin (`shubhankargarg-lang/poc-studio`) after testing.

Starting point: live POC Studio **1.42.3** (commit `c2ff52c`), renamed to `poc-studio-uat` / marketplace `unifyapps-poc-uat`. The renaming itself is **not** moved to live.

| # | Date | Change | Commits | Tested | Moved to live |
|---|---|---|---|---|---|
| U-01 | 2026-11-13 | UAT keeps its run flags in `.poc-studio-uat/` (live keeps `.poc-studio/`), so with both plugins installed each plugin's hooks act only on its own runs. **UAT-only: never moved to live.** | see git log "UAT run flags" | Hooks checked both ways (question routing, stop reminder, Observability) | No (UAT-only) |
