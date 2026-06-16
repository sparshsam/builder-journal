[![License: MIT](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Standard](https://img.shields.io/badge/status-stable-green)]()

# Builder Journal

**Your public builder journal and ecosystem command center.** This is the shared orientation point for you and your AI agents — a single place to understand what you're building, why it matters, what order work should happen in, and where public/private boundaries sit.

Builder Journal tracks the direction of your software ecosystem at a public-safe level: ambitions, active builds, upcoming builds, repository health, maintenance priorities, product decisions, and agent notes that can be shared without exposing sensitive details.

## Status

Early foundation. Not a product, not a production system, and not a source of private operational truth. The initial goal is a stable documentation structure before deeper planning, repo health tracking, and agent-specific workflows are added.

## What This Repo Is For

Builder Journal supports your ecosystem by:

- recording strategic direction without oversharing private details;
- distinguishing public, private, sensitive, and experimental projects;
- tracking build order and maintenance priorities;
- preserving key product decisions and tradeoffs;
- giving your agents shared context before they work in individual repositories.

The canonical standards for repository hygiene, documentation, security, releases, public/private boundaries, and agent behavior live in [`ecosystem-standards`](https://github.com/sparshsam/ecosystem-standards). When this repository and the standards disagree, the standards repository wins.

## How You and Your Agents Should Use This Repo

You (and any agent working on your behalf) may use Builder Journal to:

- understand current ecosystem priorities before changing another repository;
- update public-safe status notes when work lands;
- add restrained decision records after meaningful product or architecture choices;
- record maintenance tasks without exposing secrets, credentials, infrastructure details, or private workflows;
- keep README, changelog, status, and boundary docs consistent with `ecosystem-standards`.

**What not to put here:** private plans, credentials, raw operational data, private betting data, personal documents, or implementation details for private systems. This is a public journal — describe purposes and boundaries, not internals.

## Repository Map

| File | Purpose |
|------|---------|
| `AMBITIONS.md` | Public-safe ambitions and direction |
| `CURRENT_STATUS.md` | Snapshot of ecosystem project status |
| `BUILD_PIPELINE.md` | Recommended build order and sequencing |
| `ECOSYSTEM_MAP.md` | High-level public/private project map |
| `PRINCIPLES.md` | Operating principles for the ecosystem |
| `SECURITY_BOUNDARIES.md` | Public/private and sensitive-data rules |
| `DECISIONS.md` | Product and ecosystem decisions |
| `MAINTENANCE.md` | Maintenance model and recurring care |
| `CHANGELOG.md` | Versioned history |
| `agents/` | Agent coordination, handoff templates, and agent-specific rules |
| `plans/` | Build roadmaps for upcoming ecosystem projects |
| `templates/` | Reusable templates for build plans, handoffs, and decision logging |

## Limitations

Builder Journal is a planning and coordination repository. It does not replace private project documentation, legal review, security audits, financial records, or operational runbooks. Public entries may stay intentionally high-level when the underlying project is private, sensitive, or experimental.

## License

MIT License. See [`LICENSE`](LICENSE).

---

*Last updated: June 2026*
