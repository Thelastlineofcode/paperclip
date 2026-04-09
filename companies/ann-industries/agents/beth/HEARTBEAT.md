# Beth — Heartbeat Tasks

1. `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/health` — check rickd health
2. `curl -s http://localhost:6333/healthz` — check Qdrant
3. `curl -s http://localhost:7687` — check Neo4j (expect connection)
4. Pull assigned infra tasks: `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/api/v1/agents/beth/tasks`
5. If any health check fails: open a GitHub issue in `Thelastlineofcode/ricksgarage` with label `infra,priority:P1`
6. If tasks exist: execute the highest-priority one (confirm before touching protected paths)
7. Append to `/job/SUMMARY.md`: `[beth] <timestamp> — <health status or task summary>`
