# Archive Candidates

This file lists repositories recommended for archival and documents the criteria that trigger an archive recommendation.

---

## When to Archive Instead of Leaving Stale

A repo should be **archived** (made read-only on GitHub) rather than left stale when it meets any of these criteria:

### 1. No commits in 6+ months
   - If a repo has received no commits, PR merges, or meaningful activity for six consecutive months, flag it as an archive candidate.
   - **Exception:** The repo is explicitly `maintained` with no active development needed (e.g., a stable, finished tool).

### 2. Superseded or replaced
   - Another repo now serves the same purpose. The old repo should be archived with a redirect note in its README pointing to the replacement.
   - **Exception:** The old repo is still used as a dependency by active repos.

### 3. Abandoned experiment
   - The repo was created as a prototype or experiment and is no longer being worked on. There is no plan to resume.
   - **Exception:** The experiment is referenced in a paper, talk, or published research.

### 4. Security risk from neglect
   - The repo has unpatched critical security advisories and no one is actively maintaining it. Archival at least signals it is unsupported.
   - **Exception:** The repo is automatically deprecated by GitHub, which leaves the source visible with a warning banner.

### 5. No longer aligned with ecosystem goals
   - The repo's purpose no longer fits the builder's current direction or stated project categories.
   - **Exception:** The repo is widely used by others, even if the builder no longer works on it personally.

---

## What Archival Means

- `git archive` is run, or the GitHub "Archive repository" setting is enabled.
- The README is updated with an archival notice banner.
- The repo is removed from any CI/CD pipelines.
- The repo is marked `archived` in `repo-inventory.md`.
- Issues and PRs are closed with a brief explanation.
- Dependabot alerts and automated security scanning are left running (if applicable) — archival does not mean ignoring security issues.

---

## Archive Candidates Table

| Repo | Reason | Recommended Date | Status |
|------|--------|-----------------|--------|
| – | – | – | Under review / Approved / Rejected |

---

## Archived Repos

Repos that have been archived. Keep these listed here for reference.

| Repo | Archived Date | Reason | Notes |
|------|---------------|--------|-------|
| – | – | – | – |

---

## Unarchival

A repo can be unarchived if:

- The builder decides to resume work on it.
- An external contributor submits a well-motivated PR and the builder agrees to maintain again.
- The repo is the canonical reference for a standard or specification and needs updates.

Unarchival should be documented in `maintenance-log.md`.

---

## Related

- [Repo Inventory](./repo-inventory.md) — current lifecycle status
- [Repo Health Checks](./repo-health-checks.md) — monthly check that may identify archive candidates
- [Maintenance Log](./maintenance-log.md) — record archivals here
