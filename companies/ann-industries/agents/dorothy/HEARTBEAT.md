# Dorothy — Heartbeat

1. Pull task queue: `GET /api/v1/agents/dorothy/tasks`
2. Check blocked tasks across the squad — reassign or inject context to unblock
3. `gh pr list --repo Thelastlineofcode/jouvae --state open` — flag PRs stale > 48h
4. Gate dependent work explicitly: mark tasks blocked if their dependency isn't merged
5. Append to `/job/SUMMARY.md`: `[dorothy] <timestamp> — <squad status>`
