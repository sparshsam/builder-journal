# Maintenance

Builder Journal should remain useful because it is current, restrained, and easy to scan.

## Maintenance Cadence

| Cadence | Task |
|---------|------|
| After each meaningful repo change | Update `CURRENT_STATUS.md` if project state changed. |
| After product or architecture decisions | Add a short entry to `DECISIONS.md`. |
| Before releases | Confirm `CHANGELOG.md`, README status, and security boundaries are current. |
| Monthly or after major ecosystem work | Review project statuses, build pipeline order, and public/private classifications. |

## Maintenance Rules

- Keep public notes factual and concise.
- Do not add private operational details for sensitive systems.
- Do not turn status files into raw logs.
- Prefer linking to public repositories over duplicating their documentation.
- Use "needs review" when current status is uncertain.
- Update the changelog for user-visible or ecosystem-visible changes.

## Repo Health Checklist

- README explains purpose, status, ecosystem role, agent usage, and exclusions.
- `.gitignore` excludes environment files and local artifacts.
- Security boundaries are explicit.
- Changelog has an entry for each release.
- Decision records are dated and public-safe.
- Project status table does not overclaim maturity.
