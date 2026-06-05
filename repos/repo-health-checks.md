# Repo Health Checks

This document defines the repeatable monthly health check procedure for all tracked ecosystem repositories. The goal is to catch drift early and keep every repo in a known, documented state.

---

## Monthly Health Check Procedure

**Frequency:** Monthly (first week of each month).  
**Trigger:** Also run after major ecosystem changes, before a release, or when adopting a new repo into the ecosystem.  
**Owner:** Builder Journal maintainer (Sparsh Sam or delegated agent).

### Check Items

Run each check against every repo in `repo-inventory.md` with status `active`, `maintained`, `needs review`, or `sensitive`.

| # | Check | Pass/Fail | Notes |
|---|-------|-----------|-------|
| 1 | **Build status** | CI/CD pipeline passes (if configured). If no CI exists, note that. | Run `gh run list --repo <org/repo> --limit 5` or check Actions tab. |
| 2 | **Tests pass** | Test suite passes (if any). If no test suite, note that. | `npm test`, `cargo test`, `pytest`, etc. depending on stack. |
| 3 | **Dependencies current** | No critical or high-severity outdated dependencies. | Run `npm outdated`, `deps.dev`, or Dependabot tab. Note any overdue patch-level updates. |
| 4 | **Security advisories** | No unaddressed security advisories or dependabot alerts. | Check GitHub Security tab for each repo. Critical/high must be addressed within 14 days. |
| 5 | **Secrets check** | No committed secrets, API keys, tokens, or credentials in the repo. | Run `trufflehog` or `gitleaks` scan. If not available, manually audit recent commits for secret-like strings. |
| 6 | **README accuracy** | README reflects current purpose, status, maturity, and excludes stale or inaccurate claims. | Compare README with `CURRENT_STATUS.md` and actual repo state. |
| 7 | **Changelog status** | CHANGELOG.md is present (if repo maturity requires it) and has entries for each release. | No gaps between releases. Each entry has a date. |
| 8 | **Release status** | Latest release is tagged and published. Release notes are present. | `git tag --list` and GitHub Releases page. |
| 9 | **Open issues** | At least triaged — no critical unlabeled/uncommented issues older than 30 days. | Scan open issues. Add labels, assign priority, or close stale ones. |
| 10 | **Active decision** | Should this repo remain in its current lifecycle status? | Either confirm status or propose a change (archive, pause, promote). |

### Scoring

| Result | Meaning |
|--------|---------|
| **All pass (10/10)** | Healthy. No action needed. |
| **7–9 pass** | Acceptable but needs attention on failing items within 30 days. |
| **4–6 pass** | Needs intervention. Schedule a maintenance session. |
| **0–3 pass** | Critical. Consider pausing or archiving the repo until resolved. |

---

## Health Check Log

Each monthly run appends a summary row here:

| Date | Repos Checked | Pass Rate | Notable Failures | Action Taken |
|------|---------------|-----------|------------------|--------------|
| _(first run)_ | – | – | – | – |

---

## Per-Repo Health Notes

Use this section for repo-specific health concerns that don't fit the generic checklist.

_None yet._

---

## Automation Ideas

- [ ] Set up a monthly GitHub Action that opens an issue with the health checklist pre-filled.
- [ ] Integrate Dependabot or Renovate for automated dependency updates.
- [ ] Use `gh repo list --json name,updatedAt` to detect stale repos automatically.

---

## Related

- [Release Status](./release-status.md) — version and release tracking
- [Maintenance Log](./maintenance-log.md) — dated log of all maintenance actions
- [Archive Candidates](./archive-candidates.md) — repos recommended for archival
