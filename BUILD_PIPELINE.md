# Build Pipeline

This is the recommended public-safe build order for the ecosystem. It is a sequencing guide, not a promise of release dates.

## Recommended Order

| Order | Build | Reason |
|-------|-------|--------|
| 1 | Builder Journal | Establish the command center, status language, decision log, and public/private boundaries first. |
| 2 | Repo health / maintenance system | Make repository upkeep visible before expanding the number of active builds. |
| 3 | FridgeWise | Begin a practical household/care-oriented build with clear public boundaries. |
| 4 | Chess by Sparsh (`openboard-chess`) | Create a standalone chess board repository after planning is clear. Keep Builder Journal as planner only. |
| 5 | TW Oracle Personal Lab | Keep private lab references high-level in public documents. |
| 6 | StreamDock | Add workflow tooling after baseline repo health and early product work are stable. |
| 7 | LexiBoard | Develop once purpose, scope, and relation to other language/writing tools are clearer. |
| 8 | QuietVault | Approach after privacy, safety, and data-boundary expectations are mature. |

## Pipeline Rules

- Do not start a new build by weakening security or documentation standards.
- Do not use public docs to expose private architecture, prompts, data, or operational workflows.
- Prefer finishing foundation and maintenance work before adding new surface area.
- Record meaningful product decisions in `DECISIONS.md`.
- Update `CURRENT_STATUS.md` after major milestones, releases, pauses, or deprecations.
- Do not build standalone applications inside Builder Journal; use it only for roadmap, public-safe status, decisions, build sequencing, and agent handoff notes.
