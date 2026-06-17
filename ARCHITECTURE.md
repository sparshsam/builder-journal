# Architecture

Builder Journal is a documentation-and-planning repository. There is no runtime application, build system, or deployment pipeline.

## Structure

| Layer | Path | Purpose |
|-------|------|---------|
| Orientation | `README.md` | Entry point, purpose, usage |
| Direction | `AMBITIONS.md`, `PRINCIPLES.md`, `ECOSYSTEM_MAP.md` | High-level direction and boundaries |
| Status | `CURRENT_STATUS.md`, `BUILD_PIPELINE.md`, `MAINTENANCE.md` | Current and planned work |
| Records | `DECISIONS.md`, `CHANGELOG.md` | Past decisions and release history |
| Agents | `agents/`, `AGENTS.md`, `CLAUDE.md` | Agent coordination and task context |
| Plans | `plans/` | Per-project build roadmaps |
| Templates | `templates/` | Reusable document templates |

## Key Design Decisions

- **Public-first:** All content is written for public consumption. Private details are kept in private repos or scratch files.
- **Standards-driven:** This repo defers to `ecosystem-standards` for canonical rules on documentation, security, releases, and agent behavior.
- **Minimal tooling:** No build step, no CI pipeline — plain Markdown with basic linting.
