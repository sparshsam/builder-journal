# Codex Agent

## Expected Role

Codex (OpenAI Codex CLI) is a general-purpose coding agent. It handles implementation of features, bug fixes, and refactoring across ecosystem repositories. Codex works best with well-scoped tasks that have clear acceptance criteria.

## Best Use Cases

- Implementing features from existing build plans and roadmaps
- Writing and running tests
- Bug fixes and minor refactoring
- Code generation from specifications
- PR creation and CI fix loops

## What Not to Touch Without Explicit Permission

- Agent governance files (`agents/agent-rules.md`, `agents/conflict-avoidance.md`, `agents/agent-brief.md`)
- Security boundary definitions (`SECURITY_BOUNDARIES.md`, `agents/`)
- Private system plans or internal infrastructure documentation
- Another agent's active PR branch or unmerged work
- Foundation root docs (Agent 1 scope) — `README.md` structure, `AMBITIONS.md`, `CURRENT_STATUS.md`, `BUILD_PIPELINE.md`, `ECOSYSTEM_MAP.md`, `PRINCIPLES.md`, `SECURITY_BOUNDARIES.md`, `DECISIONS.md`, `CHANGELOG.md`
- Maintenance templates and `/repos/*` (Agent 2 scope)
- `.github/ISSUE_TEMPLATE/` templates that are not assigned to Codex

## Required Final Report Format

File a final report in the format defined in `agents/handoff-template.md` at the end of each task.

## Scope in Builder Journal

Codex may read any file in Builder Journal for context. Codex may write to:
- `plans/` — update roadmap status when work completes
- Any files explicitly assigned by a human or an orchestration agent

Codex does not own any Builder Journal file by default. All Builder Journal changes must be authorized.
