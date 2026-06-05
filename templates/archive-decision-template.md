# Archive Decision Template

Use this template when evaluating a repository for archival. Fill out one per repo under consideration.

---

## Repo: `{{repo-name}}`

**Evaluation Date:** {{YYYY-MM-DD}}  
**Evaluated By:** {{name-or-agent-id}}  
**Current Status:** {{current lifecycle status}}

### Archive Criteria Check

| Criterion | Applies? | Details |
|-----------|----------|---------|
| No commits in 6+ months | ☐ Yes / ☐ No | Last commit: |
| Superseded or replaced | ☐ Yes / ☐ No | By: |
| Abandoned experiment | ☐ Yes / ☐ No | |
| Security risk from neglect | ☐ Yes / ☐ No | |
| No longer aligned with ecosystem goals | ☐ Yes / ☐ No | |

### Counterarguments

_Why should this repo NOT be archived?_

### Impact Assessment

- **Users/contributors affected:** {{none / list}}
- **Dependent repos in ecosystem:** {{none / list}}
- **Documentation or references that need updating:**
- **CI/CD removal needed:** {{yes / no}}
- **Secret scanning still needed:** {{yes / no}}

### Decision

**Recommendation:** {{Archive / Keep / Pause (revisit in N months)}}

**Rationale:**

### Archival Actions (if approved)

- [ ] Update README with archival notice banner.
- [ ] Close all open issues and PRs with explanation.
- [ ] Remove from CI/CD pipelines.
- [ ] Update `repo-inventory.md` status to `archived`.
- [ ] Add entry to `archive-candidates.md` Archived Repos table.
- [ ] Log in `maintenance-log.md`.

---

## Related

- [Archive Candidates](../repos/archive-candidates.md) — criteria and candidate table
- [Repo Inventory](../repos/repo-inventory.md) — lifecycle status
- [Maintenance Log](../repos/maintenance-log.md) — log archival here
