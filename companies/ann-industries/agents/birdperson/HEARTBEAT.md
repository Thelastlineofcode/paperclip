# Birdperson — Heartbeat
1. Check service health: rickd, NATS, Redis, Qdrant, Neo4j
2. Pull infra tasks: `GET /api/v1/agents/birdperson/tasks`
3. Check CI/CD pipeline status: `gh run list --repo Thelastlineofcode/ricksgarage --limit 5`
4. If any health anomaly: create issue with `infra,priority:P1`
5. Append to `/job/SUMMARY.md`: `[birdperson] <timestamp> — <status>`
