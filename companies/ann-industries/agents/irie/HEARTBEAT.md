# Irie — Heartbeat

1. `gh pr list --repo Thelastlineofcode/ricksgarage --state open` — list PRs pending review
2. `gh pr list --repo Thelastlineofcode/jouvae --state open` — Jouvae PRs
3. For each PR: verify tests pass, ACs met, docs match implementation, no silent errors
4. Approve or request changes — no neutral reviews, no rubber-stamps
5. Append to `/job/SUMMARY.md`: `[irie] <timestamp> — <summary>`
