# TW Oracle Personal Lab — Build Roadmap

## Purpose

A private, personal analytics and recordkeeping tool for tracking and reviewing personal sports-related observations. TW Oracle Personal Lab is designed as a single-user application for structured personal recordkeeping and retrospective analysis. It is not a public advisory product, not a betting recommendation service, and not a shared sports intelligence platform.

## MVP Scope

- Manual entry of personal observations and notes
- Tagging and categorization of entries
- Basic search and filter by date, tag, or category
- Personal dashboard with summary views
- CSV export of personal records

## Non-Goals

- Public-facing predictions or recommendations
- Automated data scraping or external data ingestion
- Betting edge calculations or performance formulas
- Multi-user access or collaboration features
- Integration with betting platforms or payment systems
- Real-time data feeds or alerts
- API access for third-party consumers
- Any form of public advisory or recommendation output

## Risk Classification

**Risk Level:** Medium

Private recordkeeping tool. The primary risk is misuse as a public advisory product or disclosure of personal analytics methodology. All public references must frame it as a personal tool, not a betting advisory service. Implementation details (edge calculations, methodology, formulas) must remain private.

## Privacy / Security Boundaries

- All data is private to the single user.
- No data is transmitted to external services unless explicitly exported by the user.
- No personal analytics methodology, edge calculations, or performance formulas are disclosed in public documentation.
- The application does not connect to betting platforms, payment systems, or public data feeds.
- See `ecosystem-standards/standards/public-private-boundary.md` for what can and cannot be disclosed publicly.
- This is a private tool. Its public name, purpose, and boundaries are all that appear in the ecosystem. Implementation details remain private.

## Target: v0.1.0

**Estimated:** Q3 2026

## Future Versions

- **v0.2.0:** Enhanced visualization, advanced filtering, recurring entry templates
- **v0.3.0:** Custom tagging taxonomies, structured review workflows

## Agent Notes

- This is a **private** system. All public references must use boundary language only.
- Do not describe methodology, edge calculations, formulas, or analytical approaches in any public-facing file.
- The private repository should include `PRIVATE_NOTICE.md`.
- Implementation agents must read `ecosystem-standards/standards/public-private-boundary.md` before working on this project.
- All roadmap entries in this file are public-safe. Do not expand them with private details.

## Release Readiness Checklist

- [ ] All MVP items complete
- [ ] Tests pass
- [ ] Private system boundaries documented
- [ ] PRIVATE_NOTICE.md in place
- [ ] Public-facing README uses boundary language only
- [ ] No implementation details disclosed
- [ ] No secrets committed
- [ ] Public-safe language verified
