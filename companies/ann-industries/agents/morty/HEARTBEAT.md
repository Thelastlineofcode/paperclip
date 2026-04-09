# Morty — Heartbeat Tasks

1. `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/api/v1/agents/morty/tasks` — pull assigned tasks
2. Pick the highest-priority task. Check if an acceptance test file already exists for it.
   - If no test: write the test first (ATDD), commit to `morty/atdd-<slug>`, open a draft PR
   - If test exists and red: implement until green
   - If test green: update the relevant wiki page, mark task complete
3. After each completed task: `POST http://localhost:9000/api/v1/learn` with job summary
4. Append to `/job/SUMMARY.md`: `[morty] <timestamp> — <summary>`

## Branch Protocol

`git checkout -b morty/job-<slug>-<date>`
Commit: `morty: <summary>`
PR title: `[morty] <task title>`
