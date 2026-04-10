# Ox — Heartbeat

1. Pull fix/refactor tasks: `GET /api/v1/agents/ox/tasks`
2. Write failing test first. Implement the fix. Verify GREEN. Open PR.
3. Minimal surface area — implement exactly what the issue asks, nothing more
4. Branch: `ox/job-<slug>-<date>`
5. Append to `/job/SUMMARY.md`: `[ox] <timestamp> — <summary>`
