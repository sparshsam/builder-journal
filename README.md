# Builder Journal

**Public builder journal and ecosystem command center for Sparsh Sam's software projects.**

Builder Journal tracks the direction of Sparsh Sam's software ecosystem at a public-safe level: ambitions, active builds, upcoming builds, repository health, maintenance priorities, product decisions, and agent notes that can be shared without exposing sensitive details.

This repository exists to keep the ecosystem legible. It gives humans and AI agents a single place to understand what is being built, why it matters, what order work should happen in, and where public/private boundaries sit.

## Status

Early foundation. Not a product, not a production system, and not a source of private operational truth.

The initial goal is to establish a stable documentation structure before deeper planning, repo health tracking, and agent-specific workflows are added.

## Ecosystem Role

Builder Journal supports the broader software ecosystem by:

- recording strategic direction without oversharing private details;
- distinguishing public, private, sensitive, and experimental projects;
- tracking build order and maintenance priorities;
- preserving key product decisions and tradeoffs;
- giving agents shared context before they work in individual repositories.

The canonical standards for repository hygiene, documentation, security, releases, public/private boundaries, and agent behavior live in [`ecosystem-standards`](https://github.com/sparshsam/ecosystem-standards). When this repository and the standards disagree, the standards repository wins.

## How Agents Should Use This Repo

Agents may use Builder Journal to:

- understand current ecosystem priorities before changing another repository;
- update public-safe status notes when work lands;
- add restrained decision records after meaningful product or architecture choices;
- record maintenance tasks that do not expose secrets, credentials, infrastructure details, or private workflows;
- keep README, changelog, status, and boundary docs consistent with `ecosystem-standards`.

Agents must not use this repository as a place to store private plans, credentials, raw operational data, private betting data, personal documents, or implementation details for private systems.

## What Should Never Be Committed

Never commit:

- secrets, API keys, auth tokens, passwords, or credentials;
- wallet seed phrases, private keys, recovery phrases, or signing material;
- `.env`, `.env.*`, local config files, or real environment values;
- personal address, phone number, government ID documents, tax records, or financial account details;
- private betting picks, edge calculations, raw betting logs, or sensitive business data;
- private repository internals, schemas, prompts, deployment URLs, infrastructure addresses, or operational runbooks;
- claims that a project is compliant, audited, production-secure, enterprise-grade, or externally validated unless that is documented and true.

## Repository Map

| File | Purpose |
|------|---------|
| `AMBITIONS.md` | Public-safe ambitions and direction |
| `CURRENT_STATUS.md` | Snapshot of ecosystem project status |
| `BUILD_PIPELINE.md` | Recommended build order and sequencing |
| `ECOSYSTEM_MAP.md` | High-level public/private project map |
| `PRINCIPLES.md` | Operating principles for the ecosystem |
| `SECURITY_BOUNDARIES.md` | Public/private and sensitive-data rules |
| `DECISIONS.md` | Initial product and ecosystem decisions |
| `MAINTENANCE.md` | Maintenance model and recurring care |
| `CHANGELOG.md` | Versioned history |

## Limitations

Builder Journal is a planning and coordination repository. It does not replace private project documentation, legal review, security audits, financial records, or operational runbooks.

Public entries may intentionally stay high-level when the underlying project is private, sensitive, or experimental.

## License

MIT License. See [`LICENSE`](LICENSE).
