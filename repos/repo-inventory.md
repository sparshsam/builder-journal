# Repo Inventory

This file is the canonical inventory of all ecosystem repositories tracked by the Builder Journal. It is the source of truth for repo lifecycle status, active branches, sensitivity, and next actions.

> **How to update:** After any meaningful repo lifecycle change (archived, reactivated, new repo added), update this file. Do not let it drift more than one month stale.

---

## Inventory Table

|| Repo | Category | Visibility | Status | Sensitivity | Latest Known Version | Current Priority | Next Action |
||------|----------|------------|--------|-------------|---------------------|------------------|-------------|
|| [pdfreader-by-sparsh](https://github.com/sparshsam/pdfreader-by-sparsh) | Local documents | Public | active | public-safe | v0.3.2 | Low | Dependabot backlog cleared (0 open). Normal development cycle. |
|| [hiss-tastic](https://github.com/sparshsam/hiss-tastic) | Focus and interfaces | Public | active | public-safe | – | Low | Retro arcade game (Snake-inspired). Active commits. Consider creating initial release/tag. |
|| [openproof](https://github.com/sparshsam/openproof) | Proof and verification | Public | active | public-safe | v2 (receipt schema) | Medium | Continue MVP refinement; see memory notes on receipt schema |
|| [opensprout](https://github.com/sparshsam/opensprout) | Care and household systems | Public | active | public-safe | – | Low | Privacy-first plant care. Active commits. Dependabot backlog cleared (0 open). |
|| [quietledger](https://github.com/sparshsam/quietledger) | Behavioral finance | Public | active | public-safe | – | Low | Local-first finance tooling. Active commits. Dependabot backlog cleared (0 open). |
|| [elora-vault](https://github.com/sparshsam/elora-vault) | Behavioral finance | Public | active | betting-sensitive | v0.9 | High | Continue Phase 5/6 development; see memory notes |
|| [ecosystem-standards](https://github.com/sparshsam/ecosystem-standards) | Standards | Public | maintained | public-safe | – | High | Canonical source; update only when standards change |
|| [builder-journal](https://github.com/sparshsam/builder-journal) | Command center | Public | active | public-safe | – | High | Ongoing; current sprint |
|| [tw-oracle-personal](https://github.com/sparshsam/tworacle) | Private decision support | Private | sensitive | betting-sensitive | – | Medium | Maintain high-level-only public posture; do not disclose methodology |
|| fridgewise | Care and household systems | – | planned | public-safe | – | Low | Upcoming build; not yet created |
|| chess-by-sparsh | Focus and interfaces | – | planned | public-safe | – | Low | Upcoming build; not yet created |
|| lexiboard | Focus and interfaces | – | planned | public-safe | – | Low | Upcoming build; needs sharper definition |
|| streamdock | Focus and interfaces | – | planned | privacy-sensitive | – | Low | Upcoming build; avoid platform tokens and account details |
|| quietvault | Behavioral finance | – | planned | security-sensitive | – | Low | Upcoming build; privacy/security claims must remain conservative |

---

## Lifecycle Status Definitions

| Status | Meaning |
|--------|---------|
| **active** | Current implementation work underway. Regular commits. |
| **maintained** | Stable. No active development but receives updates, security patches, and issue responses. |
| **planned** | Not yet built. Listed as a future project. |
| **needs review** | Exists but has not been checked recently. Status should be verified. |
| **needs definition** | Repo exists but purpose or maturity is unclear. Needs scoping. |
| **experimental** | Early exploration. May be deleted or rewritten. |
| **paused** | Work has stopped intentionally. May resume later. |
| **archived** | Read-only. No further work planned. |
| **sensitive** | Active but requires special handling. See `sensitive-repos.md`. |

## Sensitivity Definitions

| Label | Meaning |
|-------|---------|
| **public-safe** | Safe to publish source, docs, issues, and releases freely. |
| **privacy-sensitive** | Contains or may contain user data, personal information, or private configuration. |
| **security-sensitive** | Involves authentication, secrets, passwords, or cryptographic operations. |
| **finance-sensitive** | Touches financial data, transactions, or account information. |
| **betting-sensitive** | Related to wagering, predictions, or gambling-adjacent systems. Requires legal framing. |
| **legal-framing-needed** | Operates in a legally ambiguous area and needs explicit terms/conditions. |

## Repo Addition Criteria

A repo is added to this inventory when it:

- Is owned by the `sparshsam` GitHub account (any visibility), **or**
- Is a canonical dependency of an ecosystem project (e.g., a forked library with custom patches).

Repos not in this table are not tracked by Builder Journal maintenance. If a repo should be tracked, add it above with an appropriate status, category, and sensitivity.

## Maintenance Rules for This File

- Do **not** include private operational details, methodology, or architecture for sensitive repos.
- Prefer linking to public repos over duplicating their documentation.
- Use "needs review" when status is uncertain.
- When a repo transitions to `archived`, move it to `archive-candidates.md` and keep a note here.
