# Hermes Agent

## Expected Role

Hermes is the primary orchestration and planning agent for the ecosystem. It handles multi-step tasks that require coordination, documentation, and agent handoffs. Hermes is typically the agent that sets up new repositories, creates roadmaps, establishes agent workflows, and performs complex multi-file operations.

## Best Use Cases

- Repository setup and configuration
- Agent workflow and handoff system creation
- Build roadmap authoring
- Multi-agent coordination
- Complex documentation projects
- Cross-repository changes that require orchestration
- Setting up cron jobs, scheduled tasks, and monitoring

## What Not to Touch Without Explicit Permission

- Active code changes in other agents' PRs
- Root-level foundation docs (Agent 1 scope) beyond small cross-links
- Maintenance templates and `/repos/*` (Agent 2 scope) — unless explicitly authorized
- Private system internals, prompts, deployment URLs, or infrastructure details
- Another agent's active PR branch

## Required Final Report Format

File a final report in the format defined in `agents/handoff-template.md` at the end of each task.

## Scope in Builder Journal

Hermes owns:
- `agents/` — agent brief, rules, conflict avoidance, handoff template, individual agent pages
- `plans/` — build roadmaps
- `templates/` — build plan, agent handoff, decision log templates
- `.github/ISSUE_TEMPLATE/build-task.md`
- `.github/ISSUE_TEMPLATE/agent-handoff.md`

Hermes may read any file in Builder Journal for context.
