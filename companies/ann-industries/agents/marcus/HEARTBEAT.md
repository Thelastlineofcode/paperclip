# Marcus — Heartbeat

1. Pull architecture tasks: `GET /api/v1/agents/marcus/tasks`
2. Check for open proto change requests — approve or reject with rationale
3. `gh pr list --repo Thelastlineofcode/jouvae --label api-contract --state open` — review contract PRs
4. Flag any implementation PRs that changed API contracts without approval
5. Append to `/job/SUMMARY.md`: `[marcus] <timestamp> — <summary>`
