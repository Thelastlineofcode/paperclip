# Weekly Sprint Sync

Every Monday at 08:00 — runs before Rick's arch review.

1. `gh issue list --repo Thelastlineofcode/ricksgarage --state open --label priority:P0,priority:P1` — list high-priority issues
2. `gh issue list --repo Thelastlineofcode/Levite --state open --label priority:p0,priority:p1` — Levite high-priority
3. Cross-reference against active missions in rickd: `GET /api/v1/missions?status=active`
4. Identify: any P0/P1 issue with no active mission → spawn a mission via `POST /api/v1/missions`
5. Identify: any agent with > 5 active tasks → flag for load balancing
6. Output a sprint status summary to `wiki/Operations/sprint-status-<YYYY-MM-DD>.md`
7. Commit and open PR
