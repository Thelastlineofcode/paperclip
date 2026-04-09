# Meeseeks — Heartbeat
1. Check spawn queue: `GET /api/v1/agents/meeseeks/tasks`
2. Execute assigned QA task — four lenses: correctness, security, performance, observability
3. Report results, mark task complete
4. Append to `/job/SUMMARY.md`: `[meeseeks] <timestamp> — DONE: <task>`
