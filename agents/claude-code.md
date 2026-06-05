# Claude Code Agent

## Expected Role

Claude Code is a focused coding agent suited for implementation tasks, code review, and documentation. It excels at tasks requiring careful reasoning about code structure and correctness.

## Best Use Cases

- Code review and quality analysis
- Feature implementation with test coverage
- Documentation generation and maintenance
- Complex refactoring with correctness guarantees
- Integration work and build pipeline fixes

## What Not to Touch Without Explicit Permission

- Agent governance files (`agents/agent-rules.md`, `agents/conflict-avoidance.md`, `agents/agent-brief.md`)
- Security boundary definitions (`SECURITY_BOUNDARIES.md`)
- Another agent's active PR branch or unmerged work
- Foundation root docs (Agent 1 scope) without explicit authorization
- Maintenance templates and `/repos/*` (Agent 2 scope)
- Private system plans or internal infrastructure documentation

## Required Final Report Format

File a final report in the format defined in `agents/handoff-template.md` at the end of each task.

## Scope in Builder Journal

Claude Code may read any file in Builder Journal for context. Claude Code may write to:
- `plans/` — update roadmap status when work completes
- Any files explicitly assigned by a human or an orchestration agent

Claude Code does not own any Builder Journal file by default. All Builder Journal changes must be authorized.
