# Repo Health Check Template

Use this template to run a monthly health check on a single repository. Copy this file and fill it out per repo, or use it as a reference during the monthly check.

---

## Repo: `{{repo-name}}`

**Check Date:** {{YYYY-MM-DD}}  
**Checked By:** {{your-name-or-agent-id}}  
**Current Status in Inventory:** {{active / maintained / needs review / etc.}}

### Checklist

| # | Check | Pass/Fail | Notes |
|---|-------|-----------|-------|
| 1 | **Build status** — CI/CD pipeline passes? | ✅ / ❌ / N/A | |
| 2 | **Tests pass** — Test suite green? | ✅ / ❌ / N/A | |
| 3 | **Dependencies current** — No critical/high outdated deps? | ✅ / ❌ / N/A | |
| 4 | **Security advisories** — Any unaddressed advisories? | ✅ / ❌ / N/A | |
| 5 | **Secrets check** — No committed secrets or credentials? | ✅ / ❌ | |
| 6 | **README accuracy** — Purpose, status, maturity current? | ✅ / ❌ | |
| 7 | **Changelog status** — Present and up to date? | ✅ / ❌ / N/A | |
| 8 | **Release status** — Latest release tagged and published? | ✅ / ❌ / N/A | |
| 9 | **Open issues** — Triage OK, no stale criticals? | ✅ / ❌ | |
| 10 | **Active decision** — Should lifecycle status change? | ✅ (stay) / ❌ (change) | |

### Score

**{{X}}/10** — {{Healthy / Acceptable / Needs intervention / Critical}}

### Findings

_Describe any failures, drift, or notable observations:_

### Actions Taken

_List what was fixed or updated during this check:_

### Follow-up Items

- [ ] _Item or issue to track_

---

## Related

- [Repo Health Checks](../repos/repo-health-checks.md) — full monthly procedure
- [Repo Inventory](../repos/repo-inventory.md) — current lifecycle status
- [Maintenance Log](../repos/maintenance-log.md) — log this check
