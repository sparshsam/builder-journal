# Release Status

Tracks current releases, artifacts, and blockers across all ecosystem repositories.

---

## Release Tracking Table

| Repo | Current Version | Latest Release Date | Release Type | Artifact Status | Known Release Blockers | Next Release Target |
|------|----------------|---------------------|-------------|----------------|----------------------|---------------------|
| pdfreader-by-sparsh | _to verify_ | – | – | – | – | – |
| hiss-tastic | _to verify_ | – | – | – | – | – |
| openproof | v2 (receipt schema) | _to verify_ | Minor | Source tag | None known | TBD |
| opensprout | _to verify_ | – | – | – | – | – |
| quietledger | _to verify_ | – | – | – | – | – |
| elora-vault | v0.9 | _to verify_ | Pre-release | Source tag | Phase 5/6 pending | v1.0 |
| ecosystem-standards | _to verify_ | – | – | – | None known | TBD |
| builder-journal | – | – | – | – | None known | TBD (initial setup) |
| tw-oracle-personal | – | – | – | – | Private; internal only | – |
| fridgewise | – | – | – | – | Not yet created | – |
| openboard-chess | – | – | – | – | Not yet created | – |
| lexiboard | – | – | – | – | Not yet created | – |
| streamdock | – | – | – | – | Not yet created | – |
| quietvault | – | – | – | – | Not yet created | – |

---

## Release Type Definitions

| Type | Meaning |
|------|---------|
| **Major** | Breaking changes. Requires migration guide. |
| **Minor** | Backward-compatible feature additions. |
| **Patch** | Bug fixes, security patches, documentation. |
| **Pre-release** | Alpha, beta, or release candidate. Not production-ready. |
| **Rolling** | Continuous delivery; no versioned releases. |

---

## Artifact Status Definitions

| Status | Meaning |
|--------|---------|
| `source tag` | Only a git tag exists. No binary/package published. |
| `npm` | Published to npm registry. |
| `crates.io` | Published to crates.io. |
| `docker` | Docker image published. |
| `pypi` | Published to PyPI. |
| `github releases` | Published via GitHub Releases with assets. |

---

## Release Blockers

A release blocker is any issue, dependency, or decision that prevents shipping a new version.

### Current Blockers

_None tracked._

### Blocker Resolution Process

1. Document the blocker in the table above.
2. If external (depends on another repo's release), link to that repo's release status.
3. If internal (feature or decision pending), link to the relevant issue or plan.
4. Review blockers weekly during active development sprints.

---

## Release Cadence Guidelines

| Repo Maturity | Suggested Cadence |
|---------------|-------------------|
| Active build | As needed per feature completion |
| Maintained | Every 1–3 months |
| Stable / low churn | Every 6 months or security-triggered |
| Archived | No releases |

---

## Related

- [Repo Health Checks](./repo-health-checks.md) — build, test, and dependency verification
- [Maintenance Log](./maintenance-log.md) — dated log of maintenance and release actions
