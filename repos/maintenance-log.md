# Maintenance Log

Dated log of all maintenance actions performed across ecosystem repositories. This log is the operational record — it captures what was done, why, and what the outcome was.

---

## Log Format

Each entry follows this structure:

```markdown
### YYYY-MM-DD — Short Title

**Trigger:** Monthly / Pre-release / Incident / Ad-hoc  
**Scope:** Repos affected  
**Summary:** What was done  
**Findings:** What was discovered (drift, issues, config changes)  
**Actions Taken:** What was fixed or updated  
**Outcome:** Healthy / Needs follow-up / Needs discussion  
**Follow-up Items:**
- [ ] Item with owner or deadline
```

---

## Entries

_No entries yet. The first maintenance action should create the first entry._

---

## Log Maintenance Rules

1. **Date every entry** with the actual date of the maintenance action. Use ISO 8601 (YYYY-MM-DD).
2. **One entry per session.** If you do three things on one day, group them under one entry.
3. **Link to related files.** If a health check triggered a change to `repo-inventory.md`, link to it.
4. **Be concise but specific.** "Updated deps" is too vague. "Upgraded express from 4.18 to 4.19 to fix CVE-2024-xxxxx" is good.
5. **Flag SParsh review items** with a `[Sparsh]` prefix in the Follow-up Items.

---

## Related

- [Repo Health Checks](./repo-health-checks.md) — the monthly health check procedure
- [Repo Inventory](./repo-inventory.md) — current lifecycle status of all repos
