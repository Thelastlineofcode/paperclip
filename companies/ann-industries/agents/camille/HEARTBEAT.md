# Camille — Heartbeat

1. Check service health: rickd, NATS, Qdrant, Neo4j, Redis
2. `fly status --app levite` — check deploy health
3. Pull ops tasks: `GET /api/v1/agents/camille/tasks`
4. Every deployment needs a rollback plan before it starts — validate before executing
5. Open GitHub issue for any anomaly with `infra,priority:P1`
6. Append to `/job/SUMMARY.md`: `[camille] <timestamp> — <health status>`
