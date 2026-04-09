# Daily Infra Audit

Every day at 07:00.

1. `fly status --app levite` — check Levite app status
2. `fly status --app levite-db` — check DB status
3. Check machine count vs expected (1 running machine for levite)
4. Check Fly.io billing: flag any stopped machines still accruing charges
5. Check GitHub Actions runner: `systemctl --user status github-runner` on c-137
6. If any anomaly: open issue in `Thelastlineofcode/Levite` with label `infra,priority:P1`
7. Commit audit log to `beth/infra-audit-<YYYY-MM-DD>` branch
