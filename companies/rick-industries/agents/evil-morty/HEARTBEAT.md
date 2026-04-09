# Ann (Evil Morty) — Heartbeat Tasks

1. Check for P0 escalations: `curl -s -H "X-API-Key: $RICKD_API_KEY" http://localhost:9000/api/v1/missions?status=escalated`
2. Check for blocked missions > 8h: `GET /api/v1/missions?status=blocked&blocked_hours_gte=8`
3. For each escalation: read the mission context, make a decision, update the mission with a resolution directive
4. Check approval gates: `GET /api/v1/approvals?status=pending` — approve or reject tasks waiting on CEO sign-off
5. Append to `/job/SUMMARY.md`: `[ann] <timestamp> — <decisions made or "all clear">`
