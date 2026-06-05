# Decisions

This file records public-safe product and ecosystem decisions. Keep entries short, dated, and factual.

## Decision Log

### 2026-06-05 - Create Builder Journal as a Public Command Center

**Status:** Accepted

Builder Journal will serve as a public-safe builder journal and ecosystem command center for ambitions, active builds, upcoming builds, repository status, maintenance tasks, and decisions.

**Reason:** The ecosystem needs a shared orientation point before more repositories and agents begin parallel work.

**Boundary:** This repository must not contain private implementation details, sensitive operational data, credentials, private betting information, personal records, or unsupported security/compliance claims.

### 2026-06-05 - Treat ecosystem-standards as Canonical

**Status:** Accepted

The `ecosystem-standards` repository is the source of truth for documentation structure, repository hygiene, security practices, public/private boundaries, release practices, and agent governance.

**Reason:** A single standards source reduces drift across repositories and agents.

**Boundary:** If Builder Journal guidance conflicts with `ecosystem-standards`, update Builder Journal to match the standards.

### 2026-06-05 - Keep Chess by Sparsh Implementation Separate

**Status:** Accepted

Chess by Sparsh will be planned in Builder Journal but implemented in a separate public repository named `openboard-chess`.

**Reason:** Builder Journal should remain a planner and ecosystem command center, not a product implementation repository.

**Boundary:** Builder Journal may track the chess roadmap, public-safe status, decisions, build sequencing, and agent handoff notes only. Application code, package files, tests, deployments, and release assets belong in `openboard-chess`.
