# Health Checks

This directory contains dated health check reports for ecosystem repositories, organized by month.

## Structure

```
repos/health-checks/
├── README.md                    # This file
├── YYYY-MM-first-monthly-health-check.md   # Standard monthly checks
└── YYYY-MM-adhoc-<reason>.md               # Ad-hoc triggered checks
```

## File Naming

- Monthly checks: `YYYY-MM-first-monthly-health-check.md`
- Ad-hoc checks: `YYYY-MM-adhoc-<reason>.md` (e.g., `2026-06-adhoc-pre-release.md`)

## Contents

Each health check file follows the template in `templates/repo-health-check-template.md` and includes:

- A per-repo checklist (build, tests, deps, security, README, changelog, releases, issues)
- A cross-repo summary table
- Key findings and actionable follow-up items
- Recommended lifecycle status changes

## Related

- [Repo Health Checks](../repo-health-checks.md) — the monthly procedure definition
- [Repo Inventory](../repo-inventory.md) — current lifecycle status of all repos
- [Maintenance Log](../maintenance-log.md) — log this check
