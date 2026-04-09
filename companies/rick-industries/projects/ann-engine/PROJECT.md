---
schema: agentcompanies/v1
kind: project
slug: ann-engine
name: Ann Engine
description: 20-agent orchestration mesh — rickd API, dual RAG brain, agent hierarchy
owner: rick
tags:
  - ann
  - infrastructure
  - active
---

# Ann Engine

**Repo:** Thelastlineofcode/ricksgarage  
**Status:** Active — P0 tracks in progress

## Active Tracks

| Track | Status | Issues |
|-------|--------|--------|
| Paperclip Integration | P0 active | #622–#631 |
| MCP CLI Config | P0 active | #632 |
| Security Audit | In progress | #610, #612 |
| Parity Framework | Bootstrapped | #642–#663 |
| GStack Integration | Empathize | #664 |

## Architecture

- **rickd** — Go API server, port 9000
- **rick-agent** — executor, port 9001
- **NATS JetStream** — event bus, port 4222
- **Neo4j** — skills graph + agent memory graph, bolt port 7687
- **Qdrant** — vector memory, port 6333
- **Redis** — heartbeat state cache, ports 6379/6380
- **Ollama** — local inference (phi4-mini, gemma3:4b, qwen3.5:0.8b), port 11434
