# UAT changes

Every change made in this UAT copy, so exactly these can be moved to the live plugin (`shubhankargarg-lang/poc-studio`) after testing.

Starting point: live POC Studio **1.42.3** (commit `c2ff52c`), renamed to `poc-studio-uat` / marketplace `unifyapps-poc-uat`. The renaming itself is **not** moved to live.

| # | Date | Change | Commits | Tested | Moved to live |
|---|---|---|---|---|---|
| U-01 | 2026-11-13 | UAT keeps its run flags in `.poc-studio-uat/` (live keeps `.poc-studio/`), so with both plugins installed each plugin's hooks act only on its own runs. **UAT-only: never moved to live.** | see git log "UAT run flags" | Hooks checked both ways (question routing, stop reminder, Observability) | No (UAT-only) |

## Syncs from live

| Date | Live version | What |
|---|---|---|
| 2026-11-14 | 1.45.0 (commit `0f17a65`) | UAT brought level with live 1.42.3 → 1.45.0 (session logs, real tokens, orchestrator rows, sample redaction, no lost write-backs). Same transform as the first copy: `poc-studio-uat` names, `unifyapps-poc-uat`, the UAT repo URL, `.poc-studio-uat/` run folders (U-01). Also fixed 3 places the first copy had missed (`poc-studio:` → `poc-studio-uat:` in asset-run, poc-orchestrator and skill_run_row.py). |
| 2026-11-16 | 1.48.0 (commit `767654a`) | UAT brought level with live 1.45.0 → 1.48.0: wireframes as one clickable HTML with slop rules and the new design system (1.46.0), gate feedback as context on iterations (1.47.0), the AI PM build walk fixes (1.48.0). Same transform: UAT names, the UAT repo URL, `.poc-studio-uat/` run folders. |
| 2026-11-16 | 1.49.0 (commit `75e4563`) | UAT brought level with live 1.48.0 → 1.49.0: the 11 low-risk loop optimisations (AI PM blockers and one verdict, waiting flag, retry once, collateral toolkit in `assets/kit/` and scoping checker as files, leaner BRD, collateral limits, research caps and reuse, notes once, RG second run, less bookkeeping, fewer Drive checks). Same transform: UAT names, the UAT repo URL, `.poc-studio-uat/` run folders (the waiting flag is `.poc-studio-uat/waiting`). |
| 2026-11-16 | 1.49.2 (commit `8718019`) | UAT brought level with live 1.49.0 → 1.49.2: the leaner-BRD change removed completely, and no caps on solution content (workflows, vendors, research questions). |
| 2026-11-16 | 1.49.3 (commit `fca5e84`) | Skills and tools load fresh at every use again (load-once removed). |
| 2026-11-16 | 1.50.0 (commit `a815d28`) | Before-and-after feedback check from the AI PM's kept review screenshots (local only). |
| 2026-11-16 | 1.50.1 (commit `3b12c47`) | AI PM sizing follows the guide-not-cap rule, seed lessons refresh on every run, stale waiting flag ignored. |
| 2026-11-16 | 1.50.2 (commit `89826ae`) | 14 rules from the POC Build Loop skill proposals, added on the current skills. |
| 2026-11-17 | 1.51.0 (commit `d931c43`) | Anti-slop rules inside every skill's writing step (shared `references/anti-slop.md`, per-skill Quality rules, AI PM slop section 6). |
