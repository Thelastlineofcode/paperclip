# Irie — Heartbeat

1. `gh pr list --repo Thelastlineofcode/jouvae --state open` — list PRs pending review
2. For each PR: check tests pass, docs updated, ACs met, no regressions
3. Approve or request changes — no neutral reviews
4. Append to `/job/SUMMARY.md`: `[irie] <timestamp> — <summary>`
