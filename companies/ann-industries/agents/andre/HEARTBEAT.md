# Andre — Heartbeat

1. Pull doc tasks: `GET /api/v1/agents/andre/tasks`
2. `git log --since="24 hours ago" --oneline` — find merged PRs with no doc update
3. Update wiki pages for any merged feature — L2 budget per page (2-5K tokens)
4. Update `wiki/index.md` if new pages were added
5. Append to `/job/SUMMARY.md`: `[andre] <timestamp> — <summary>`
