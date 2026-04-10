---
schema: agentcompanies/v1
kind: company
slug: ann-industries
name: Ann Industries
description: Adriatic Neural Network — 11-agent orchestration mesh powering Levite, Jouvae, and the portfolio control plane
version: 2.0.0
authors:
  - name: Thelastlineofcode
goals:
  - Operate a fully autonomous multi-project engineering organization
  - Route all work through the Adriatic Neural Network agent hierarchy with cost governance
  - Run zero-idle infrastructure — heartbeats, not servers
includes:
  - agents/dorothy/AGENTS.md
  - agents/marcus/AGENTS.md
  - agents/keisha/AGENTS.md
  - agents/ox/AGENTS.md
  - agents/tanisha/AGENTS.md
  - agents/camille/AGENTS.md
  - agents/irie/AGENTS.md
  - agents/andre/AGENTS.md
  - agents/sister-nancy/AGENTS.md
  - agents/lois/AGENTS.md
  - agents/curtis/AGENTS.md
requirements:
  secrets:
    - ANTHROPIC_API_KEY
    - GITHUB_TOKEN
    - NEO4J_URI
    - QDRANT_URL
    - RICKD_API_KEY
metadata:
  ann:
    rickd_url: http://localhost:9000
    nats_url: nats://localhost:4222
    topology:
      studio: http://localhost:9000      # Mac mini c-137 — primary orchestration
      c137: http://localhost:9001        # Linux server — continuous workers + Ollama
      portal: http://localhost:9002      # Dell laptop — mobile ops + dev
    memory:
      qdrant_url: http://localhost:6333
      neo4j_bolt: bolt://localhost:7687
      unity_kernel_context: true
---

# Ann Industries

Adriatic Neural Network is an 11-agent orchestration mesh built on Paperclip. It manages three active products — Levite (astrology SaaS), Jouvae (Caribbean platform), and xcellent1 — across a three-machine physical topology.

## Hierarchy

```
Dorothy (Platform Orchestrator, L4)
├── Marcus (Platform Architect, L4)
├── Keisha (Go+gRPC Dev, L3)
├── Ox (Code Fix & Refactor, L3)
├── Tanisha (QA & Test Automation, L3)
├── Camille (Platform Operations, L3)
├── Irie (Quality Gate, L3)
├── Andre (Documentation, L3)
├── Sister Nancy (Design & UX, L3)
├── Lois (Guest Concierge, L3)
└── Curtis (Partner Operations, L3)
```

## Capability Map (from deprecated ricksgarage agents)

| Deprecated | Ann Agent | Capability |
|------------|-----------|------------|
| unity | dorothy | Cross-team coordination, sprint sync, dependency gating |
| rick | marcus | Architecture review, ADRs, contract sign-off |
| morty | keisha + ox | TDD implementation, code fix, refactoring |
| meeseeks | tanisha | Ephemeral QA workers, regression suites |
| birdperson | camille | Infra health checks, deployments, rollback |
| beth | irie | Quality gate, PR merge control |
| (new) | andre | Wiki synthesis, docs from merged PRs |
| (new) | sister-nancy | Design tokens, WCAG-AA accessibility |
| (new) | lois | Guest support, escalation paths |
| (new) | curtis | Partner onboarding, workflow ops |

## Adriatic Neural Network Extensions

This company package extends Paperclip with four Ann-specific layers:

1. **Unity Kernel Memory** — every agent task envelope is injected with Qdrant + Neo4j context before execution
2. **Portal Gun Topology Routing** — heartbeats are topology-aware; tasks route to STUDIO/c-137/PORTAL based on capability and availability
3. **LLM Cost Registry** — every agent role has an assigned model tier; tasks > $0.50 estimated cost require approval gate
4. **DAIR Signal Loop** — completed missions emit learning signals to `/api/v1/learn`; successful workflows become versioned Skill nodes

## Active Projects

| Project | Status | Owner |
|---------|--------|-------|
| Adriatic Neural Network (Thelastlineofcode/ricksgarage) | Active | Marcus / Dorothy |
| Levite | Active — Dashboard shipped | Keisha / Camille |
| Jouvae | Empathize | Dorothy |
| Portfolio Control Plane | Active | Dorothy |
