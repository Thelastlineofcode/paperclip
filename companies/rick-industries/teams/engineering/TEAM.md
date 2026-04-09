---
schema: agentcompanies/v1
kind: team
slug: engineering
name: Engineering
description: Product and platform engineering — Levite, Jouvae, Ann Engine
manager: ../../../agents/rick/AGENTS.md
includes:
  - ../../../agents/morty/AGENTS.md
  - ../../../agents/beth/AGENTS.md
tags:
  - engineering
  - team
---

# Engineering Team

Rick leads. Morty builds. Beth ships.

**Stack:** Rust/Axum · Leptos/WASM · Go · PostgreSQL · Neo4j · Qdrant · Fly.io

**Key practices:**
- ATDD first — acceptance tests before implementation code
- Domain-locked agents — backend workers stay in `api/src/`, frontend workers in `levite-web/src/`
- Damage control mandatory — force pushes, DROP TABLE, fly destroy all require confirmation gate
- Wiki updates on every task — two-output rule enforced
