# Agent Brief

## Purpose of Builder Journal

Builder Journal is your public-safe builder journal and ecosystem command center. It tracks strategic direction, active builds, upcoming builds, repository health, maintenance priorities, product decisions, and agent coordination notes — all at a level that does not expose sensitive details.

This repository exists so you and your agents have a single place to understand:
- What is being built and why
- What order work should happen in
- Where public, private, and experimental boundaries sit
- How agents should coordinate across repositories

The canonical source of truth for all documentation, repository hygiene, naming, security, and agent behavior is [`ecosystem-standards`](https://github.com/sparshsam/ecosystem-standards). When Builder Journal and the standards disagree, the standards win.

## How Agents Should Read This Repo Before Acting

Before making any change to an ecosystem repository:

1. Pull the latest `main` branch of Builder Journal.
2. Read `CURRENT_STATUS.md` for live project state.
3. Read `BUILD_PIPELINE.md` for build sequencing.
4. Read `ECOSYSTEM_MAP.md` to confirm public/private classification.
5. Read `SECURITY_BOUNDARIES.md` for what must never be exposed.
6. Check the relevant `plans/` roadmap for the project you are working on.
7. Check `agents/` for agent-specific rules and current handoffs.
8. Refer to your specific agent page (`codex.md`, `claude-code.md`, `openclaw.md`, `hermes.md`) for role-specific constraints.

## How to Avoid Exposing Sensitive Information

- Never commit secrets, API keys, tokens, passwords, or credentials.
- Never commit wallet seed phrases, private keys, or signing material.
- Never commit `.env`, `.env.*`, or real environment values.
- Never commit personal identifying documents, financial records, or tax information.
- Never commit private repository internals, schemas, prompts, deployment URLs, infrastructure addresses, or operational runbooks.
- Never claim a project is compliant, audited, production-secure, enterprise-grade, or externally validated unless that is documented and true.
- Keep all entries public-safe. If you must reference a private system, use only the high-level description from `ECOSYSTEM_MAP.md`.
- When in doubt, leave the detail out.

## How to Report Work

When a build or coordination task is complete, create an agent final report:

1. Verify the work — run lint, checks, or CI if applicable.
2. Summarize: what was done, what branch, what PR, merge commit hash, files changed.
3. Note any known issues or next recommended actions.
4. Update the relevant `plans/` roadmap file if the build state changed.
5. Update your individual agent page in `agents/` if behavior or scope changed.

The canonical final report format is in `agents/handoff-template.md`.

## How to Coordinate with Other Agents

- Always pull latest `main` before starting work.
- Always create a feature branch. Never commit to `main`.
- Respect file ownership: each agent has a defined scope in its agent page.
- If another agent's PR touches the same files, pause, review, and coordinate before committing.
- Document conflicts in `agents/conflict-avoidance.md`.
- Update `agents/` handoff templates when a task passes from one agent to another.
- Follow the merge sequence rules in `agents/conflict-avoidance.md`.

## Ecosystem Standards

All agent work must follow the standards in `ecosystem-standards`:

| Standard | What it governs |
|----------|----------------|
| agent-governance.md | Branch discipline, secret handling, public/private boundaries |
| naming-conventions.md | Branch names, commit messages, file naming |
| public-private-boundary.md | What can and cannot be said about private systems |
| security-standard.md | .env policy, credential handling |
| repository-structure.md | Canonical file layout |
| github-profile-integration.md | When and how to update the profile README |
