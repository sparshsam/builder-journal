# Release Checklist Template

Use this template when preparing a new release for any ecosystem repository.

---

## Repo: `{{repo-name}}`

**Release Version:** {{vX.Y.Z}}  
**Release Type:** {{Major / Minor / Patch / Pre-release}}  
**Target Date:** {{YYYY-MM-DD}}  
**Release Manager:** {{name}}

## Pre-Release Checklist

### Code & Build

- [ ] All PRs for this release are merged to `main`.
- [ ] Build passes on `main` (CI/CD green).
- [ ] Test suite passes (unit + integration).
- [ ] No known regressions against the previous release.

### Documentation

- [ ] `CHANGELOG.md` updated with release notes under the new version heading.
- [ ] `README.md` updated if installation instructions, badges, or feature lists changed.
- [ ] Version bumped in canonical location (e.g., `Cargo.toml`, `package.json`, version file).

### Security

- [ ] No unaddressed security advisories for this release.
- [ ] Dependencies are at least patch-level current.
- [ ] Secrets scan performed (no credentials leaked).

### Artifacts

- [ ] Git tag created (`vX.Y.Z`).
- [ ] GitHub Release created with release notes.
- [ ] Binary/package published (npm, crates.io, Docker, etc.) — if applicable.
- [ ] Release artifact verified (install from registry works).

### Post-Release

- [ ] Release entry added to `release-status.md` in builder-journal.
- [ ] If this is a public-facing release, update `CURRENT_STATUS.md` or repo status as needed.
- [ ] Announcement drafted (if warranted).

### Release Blocker Check

| Blocker | Status | Notes |
|---------|--------|-------|
| _List known blockers_ | Resolved / Open / N/A | |

---

## Release Notes Outline

```markdown
## vX.Y.Z — YYYY-MM-DD

### Added
- 

### Changed
- 

### Fixed
- 

### Security
- 
```

---

## Related

- [Release Status](../repos/release-status.md) — version tracking table
- [Repo Health Checks](../repos/repo-health-checks.md) — pre-release health verification
- [Maintenance Log](../repos/maintenance-log.md) — log this release
