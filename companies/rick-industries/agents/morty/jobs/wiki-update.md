# Daily Wiki Update

Every day at 18:00.

1. `git log --since="24 hours ago" --oneline` — list today's commits
2. For each commit that changed a source file: check if the corresponding wiki page in `wiki/` is stale
3. Update stale wiki pages — L2 budget (2-5K tokens each)
4. Check `wiki/index.md` — update the index if any new pages were added
5. Commit to `morty/wiki-<YYYY-MM-DD>` and open a PR
