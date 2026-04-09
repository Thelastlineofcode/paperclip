# Unity — Heartbeat Tasks

1. Pull cross-project coordination queue: `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/api/v1/agents/unity/tasks`
2. Check for blocked missions across all agents: `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/api/v1/missions?status=blocked`
3. For each blocked mission: determine if it can be unblocked by reassignment, context injection, or escalation
4. If any mission has been blocked > 4h: escalate to Evil Morty via `POST /api/v1/agents/evil-morty/tasks`
5. Emit DAIR signal for any completed missions: `POST http://localhost:9000/api/v1/learn`
6. Append to `/job/SUMMARY.md`: `[unity] <timestamp> — <mesh status>`
