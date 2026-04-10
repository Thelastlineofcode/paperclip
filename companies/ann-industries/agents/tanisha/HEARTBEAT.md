# Tanisha — Heartbeat

1. Pull QA tasks: `GET /api/v1/agents/tanisha/tasks`
2. Run test suite: `go test ./... 2>&1` — report any failures as GitHub issues
3. Check contract test coverage — flag any endpoint missing a contract test
4. Validate edge cases and regressions on recently merged PRs
5. Append to `/job/SUMMARY.md`: `[tanisha] <timestamp> — <summary>`
