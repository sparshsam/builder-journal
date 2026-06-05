# Current Status

This file is a public-safe snapshot. It should describe status, maturity, and next direction without exposing private implementation details, sensitive operational data, or unsupported claims.

## Project Status

| Project | Visibility | Status | Public-Safe Notes |
|---------|------------|--------|-------------------|
| PDFReader | Public or public-intended | Needs review | Local document reading and workflow support. Status should be verified against the repository before claims expand. |
| Hisstastic | Public or experimental | Needs definition | Project purpose and maturity need a clear public-safe description before deeper planning. |
| OpenProof | Public or public-intended | Needs review | Proof and verification work. Avoid claims about legal validity, audit status, or compliance unless documented. |
| OpenSprout | Public or public-intended | Needs review | Care-system tooling. Avoid personal, household-specific, or private family details. |
| QuietLedger | Public or public-intended | Needs review | Finance-adjacent tooling. Do not commit personal financial data or account details. |
| Elora Vault | Public or public-intended | Needs review | Behavioral finance and vault mechanics. Keep claims practical and documented. |
| TW Oracle Personal Lab | Private / sensitive | High-level only | Private decision-support lab. Do not disclose methodology, picks, prompts, data, infrastructure, or performance details. |
| FridgeWise | Public or public-intended | Upcoming build | Food and household inventory tooling. Keep user data and household specifics out of public docs. |
| OpenBoard Chess | Public or public-intended | Upcoming build | Chess-related build. Use accurate status language and avoid overstating engine strength or completeness. |
| LexiBoard | Public or public-intended | Upcoming build | Language, writing, or board-style tooling. Needs sharper project definition before launch claims. |
| StreamDock | Public or public-intended | Upcoming build | Streaming/workflow support. Avoid exposing platform tokens, account details, or private setup. |

## Monthly Health Check

First monthly ecosystem health check completed on **2026-06-05**. All 8 tracked repositories verified.

### High-Priority Follow-Up

- **Batch-merge Dependabot PRs** — 20 open across openproof (8), elora-vault (4), pdfreader-by-sparsh (3), opensprout (3), quietledger (2)
- **Create initial releases/tags** — hiss-tastic, opensprout, quietledger, openproof, elora-vault have changelogs and active CI but no GitHub releases
- **Consider tagging ecosystem-standards** as v1.0.0 baseline

See [`repos/health-checks/2026-06-first-monthly-health-check.md`](./repos/health-checks/2026-06-first-monthly-health-check.md) for full results.
| QuietVault | Public or public-intended | Upcoming build | Personal vault or records tooling. Privacy and security claims must remain conservative unless proven. |

## Status Rules

- Use "needs review" when a repository has not been checked recently.
- Use "upcoming build" for planned work that is not yet active.
- Use "active build" only when there is current implementation work.
- Use "maintained" only when README, changelog, security boundaries, and release practices are current.
- Use "private / sensitive" when public notes must stay high-level.
