# Maintenance Check Template

Use this template for routine maintenance sessions that do not involve a repo health check or a release (e.g., dependency bumps, config updates, CI fixes, documentation cleanups). For full repo health checks, use `repo-health-check-template.md`. For releases, use `release-checklist-template.md`.

---

## Session: {{short-title}}

**Date:** {{YYYY-MM-DD}}  
**Scope:** {{repos-affected}}  
**Trigger:** {{Routine / Dependency update / Security fix / Cleanup / Other}}

### Work Items

| # | Task | Repo | Done | Notes |
|---|------|------|------|-------|
| 1 | | | ☐ | |
| 2 | | | ☐ | |
| 3 | | | ☐ | |

### Dependencies Updated

| Dependency | From | To | Reason |
|------------|------|----|--------|
| | | | |

### Issues Found

_Issues discovered during maintenance that were not the primary task:_

### Actions Taken

_Summary of what was changed:_

### Follow-up Items

- [ ] _Item with owner or deadline_

---

## Related

- [Maintenance Log](../repos/maintenance-log.md) — log this session
- [Repo Inventory](../repos/repo-inventory.md) — current lifecycle status
- [Repo Health Checks](../repos/repo-health-checks.md) — if you discover health issues
