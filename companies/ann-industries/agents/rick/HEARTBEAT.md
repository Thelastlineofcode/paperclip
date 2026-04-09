# Rick — Heartbeat Tasks

On each tick, in order:

1. `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/api/v1/agents/rick/tasks` — pull assigned tasks
2. If tasks exist: pick the highest-priority open task, read the linked issue or file, and begin work
3. If no tasks: check `http://localhost:9000/api/v1/missions?status=blocked&assignee=rick` — unblock any blocked missions
4. If nothing blocked: query Neo4j for open ADRs — `MATCH (a:ADR {status:"draft"}) RETURN a LIMIT 3` — pick one to review
5. Emit DAIR signal on completion: `POST http://localhost:9000/api/v1/learn` with job summary

## Branch Protocol

Every job that writes files:
1. `git checkout -b rick/job-<slug>-<date>`
2. Do the work
3. `git commit -m "rick: <summary>"`
4. Open PR → `main`

## Done Signal

Append to `/job/SUMMARY.md`:
```
[rick] <timestamp> — <one-line summary of what was done>
```
