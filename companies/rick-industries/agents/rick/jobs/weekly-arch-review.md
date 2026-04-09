# Weekly Architecture Review

Every Monday at 09:00.

1. `gh issue list --repo Thelastlineofcode/ricksgarage --label architecture --state open` — list open arch issues
2. For each issue scored P0 or P1: read the issue, check if a linked ADR exists in `docs/adr/`
3. If no ADR: draft one in `docs/adr/YYYY-MM-DD-<slug>.md` using the standard ADR template
4. Check for any `agent:rick` issues that have been open > 7 days with no comment — add a triage comment
5. Check `parity/PARITY_SOURCE_REGISTRY.md` — flag any source scoring 80+ without an open port issue
6. Commit any ADR drafts to branch `rick/arch-review-<YYYY-MM-DD>` and open a PR
