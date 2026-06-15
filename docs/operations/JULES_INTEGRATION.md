# Jules Integration — paperclip

**Active:** Yes
**Scope:** Code improvement suggestions from Jules (Google Gemini)
**Channel:** jules@levite.live → CF Email → AgentMail → agents
**AgentMail inbox:** gracefulservice932@agentmail.to

## Scope Policy
Jules suggestions should be evaluated against:
- Current AGENT_OPS_BOARD.md priorities for this repo
- Open issues and PRs
- Code quality, security, and dependency health

## Safe Tasks (auto-apply)
- Dependency patch updates
- Test fixes
- Documentation corrections
- Code formatting

## Review Required
- Architecture changes
- New features
- Security pattern changes
- Any file deletion

## Context
- Base project: paperclip
- AgentMail inbox: gracefulservice932@agentmail.to — Jules suggestions land here
- Poll endpoint: api.agentmail.to/v0/inboxes/gracefulservice932%40agentmail.to/messages

## Activation
1. CF Dashboard → levite.live → Email → Email Routing
2. Add rule: jules@levite.live → gracefulservice932@agentmail.to
3. Agents start polling — no other setup needed.

