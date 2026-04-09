---
schema: agentcompanies/v1
kind: company
slug: rick-industries
name: Rick Industries
description: Adriatic Neural Network — 20-agent orchestration mesh powering Levite, Jouvae, and the portfolio control plane
version: 1.0.0
authors:
  - name: Thelastlineofcode
goals:
  - Operate a fully autonomous multi-project engineering organization
  - Route all work through the Adriatic Neural Network agent hierarchy with cost governance
  - Run zero-idle infrastructure — heartbeats, not servers
includes:
  - agents/evil-morty/AGENTS.md
  - agents/rick/AGENTS.md
  - agents/unity/AGENTS.md
  - agents/morty/AGENTS.md
  - agents/beth/AGENTS.md
  - teams/engineering/TEAM.md
  - teams/lifeos/TEAM.md
  - projects/adriatic-neural-network/PROJECT.md
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

# Rick Industries

Adriatic Neural Network is a 20-agent orchestration mesh built on Paperclip. It manages three active products — Levite (astrology SaaS), Jouvae (Caribbean platform), and xcellent1 — across a three-machine physical topology.

## Hierarchy

```
Evil Morty (CEO, L5)
├── Rick (CTO/Architect, L5)
│   ├── Beth (Infra, L4)
│   │   └── Birdperson (DevOps, L3)
│   ├── Morty (Dev, L3)
│   ├── Poopybutthole (Security, L4)
│   ├── Pencilvester (Tech Debt, L3)
│   └── Meeseeks (Ephemeral workers, L2)
└── Unity (LifeOS Orchestrator, L5)
    ├── Summer (Product, L3)
    ├── Dr. Wong (Coach, L3)
    ├── Squanchy (Growth, L3)
    └── Jerry (Admin, L2)
```

## Adriatic Neural Network Extensions

This company package extends Paperclip with four Ann-specific layers:

1. **Unity Kernel Memory** — every agent task envelope is injected with Qdrant + Neo4j context before execution
2. **Portal Gun Topology Routing** — heartbeats are topology-aware; tasks route to STUDIO/c-137/PORTAL based on capability and availability
3. **LLM Cost Registry** — every agent role has an assigned model tier; tasks > $0.50 estimated cost require approval gate
4. **DAIR Signal Loop** — completed missions emit learning signals to `/api/v1/learn`; successful workflows become versioned Skill nodes

## Active Projects

| Project | Status | Owner |
|---------|--------|-------|
| Adriatic Neural Network (Thelastlineofcode/ricksgarage) | Active | Rick |
| Levite | Active — Dashboard shipped | Morty/Beth |
| Jouvae | Empathize | Summer |
| Portfolio Control Plane | Active | Unity |
