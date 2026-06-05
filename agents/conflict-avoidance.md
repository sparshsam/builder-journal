# Conflict Avoidance

Defines how multiple agents coordinate work in the Builder Journal repository to prevent collisions, lost work, and contradictory state.

## Branch Naming Conventions

All agents must use the following branch format:

```
<type>/<scope>-<description>
```

Where:
- `type` is one of: `feat`, `fix`, `docs`, `refactor`, `security`, `chore`, `setup`
- `scope` identifies the primary agent or area (e.g., `agent-roadmaps`, `foundation`, `build-plans`)
- `description` is a short hyphenated summary

Examples:
- `setup/agent-roadmaps` — Agent 3: agent handoff system and build roadmaps
- `setup/foundation-builder-journal` — Agent 1: foundation documents
- `feat/maintenance-framework` — Agent 2: maintenance templates

If an agent arrives and the branch it wants to use already exists, append a counter: `setup/agent-roadmaps-2`.

## File Ownership Rules

| Scope | Owner | Files |
|-------|-------|-------|
| Foundation / Root docs | Agent 1 | `README.md`, `AMBITIONS.md`, `CURRENT_STATUS.md`, `BUILD_PIPELINE.md`, `ECOSYSTEM_MAP.md`, `PRINCIPLES.md`, `SECURITY_BOUNDARIES.md`, `DECISIONS.md`, `CHANGELOG.md` |
| Maintenance / Repos | Agent 2 | `MAINTENANCE.md`, `/repos/*` |
| Agent handoff / Roadmaps | Agent 3 | `/agents/*`, `/plans/*`, `.github/ISSUE_TEMPLATE/build-task.md`, `.github/ISSUE_TEMPLATE/agent-handoff.md`, `templates/build-plan-template.md`, `templates/agent-handoff-template.md`, `templates/decision-log-template.md` |

Shared files (cross-agent):
- `README.md` — may receive small cross-links from Agent 3 to reference agents/ or plans/ directories.
- `.github/ISSUE_TEMPLATE/` — Agent 3 adds build-task and agent-handoff templates. Agent 2 adds maintenance templates. Do not overwrite each other's.
- `templates/` — Agent 3 creates build-plan, agent-handoff, and decision-log templates. Agent 2 creates maintenance templates. Do not overwrite each other's.

## Merge Sequence Rules

1. **Foundation first.** Root-level foundation docs (Agent 1 scope) should be merged before dependent files (agent pages, roadmaps, templates).
2. **Least-dependent first.** PRs that touch fewer shared files should merge first.
3. **Conflict resolution.** If two PRs touch the same file, the first PR to merge wins. The second PR must rebase and resolve conflicts manually.
4. **No force push.** Never force push to shared branches. Use `--force-with-lease` only if explicitly authorized.

## How to Handle Overlapping Files

If you need to write a file that another agent's PR also touches:

1. **Do not overwrite.** Read the other agent's file first (on their branch or in their PR).
2. **Add, do not replace.** Append your content rather than replacing theirs.
3. **Document the overlap.** Add a note in the file explaining which sections belong to which agent.
4. **Notify.** Update the conflict log in this file.

## How to Document Conflicts

When a conflict is identified, add an entry to this section:

```
### Conflict Log

| Date | Agent | Branches | Files | Resolution |
|------|-------|----------|-------|------------|
| -- | -- | -- | -- | -- |
```

If no conflicts have occurred, leave the log empty.

## What to Do When Another PR Is Already Touching the Same Files

1. Identify the conflicting PR (check open PRs against `main`).
2. Review the diff to understand what the other agent changed.
3. If the changes are compatible, rebase your branch on the other agent's branch and add your content alongside theirs.
4. If the changes conflict structurally, coordinate via the PR comments or a handoff note. Do not silently overwrite.
5. If you cannot resolve, leave both changes intact but separated by clear section headers and note the situation in the PR description.
