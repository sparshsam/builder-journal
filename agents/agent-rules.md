# Agent Rules

All AI agents operating on ecosystem repositories must follow these rules. Violations involving secret exposure or boundary leakage are treated as high-severity incidents.

## 1. Always Pull Latest Main

Before starting any work, verify you are on the latest `main`:

```bash
git checkout main && git pull origin main
```

This prevents conflicts with work committed by other agents or humans between sessions.

## 2. Always Create a Feature Branch

- Never commit directly to `main` or `master`.
- Branch naming: `<type>/<short-description>` (e.g., `feat/user-auth`, `fix/login-bug`, `setup/agent-roadmaps`).
- Types: `feat`, `fix`, `docs`, `refactor`, `security`, `chore`, `setup`.
- Branch names must be lowercase with hyphens.

## 3. Never Overwrite Another Agent's Scope

- Each agent has a defined scope in its individual agent page (`agents/codex.md`, `agents/claude-code.md`, etc.).
- Do not modify files outside your assigned scope unless explicitly authorized.
- If a file exists and belongs to another agent's scope, do not edit it.
- If overlapping files are unavoidable, follow the conflict resolution process in `agents/conflict-avoidance.md`.

## 4. Never Make Public Claims That Are Not True

- All public-facing content must be accurate and verifiable.
- Do not claim a project is compliant, audited, production-secure, enterprise-grade, or externally validated unless that is documented and true.
- Do not describe private systems with more detail than the high-level description in `ECOSYSTEM_MAP.md`.
- Use restrained, non-hype language. No "revolutionary," "cutting-edge," "seamless," "next-generation."

## 5. Never Commit Secrets

- Never commit `.env`, `.env.*`, or any file containing real credentials.
- Never commit API keys, tokens, passwords, or auth credentials.
- Never commit wallet seed phrases, private keys, or recovery phrases.
- If a secret is accidentally exposed, report it immediately. Do not attempt to fix silently.
- Validate `.gitignore` coverage before every commit.

## 6. Update Docs When Behavior Changes

- When a build completes, a decision is made, or agent behavior changes, update the relevant documentation.
- Update the agent's individual page if scope, rules, or constraints change.
- Update the relevant roadmap in `plans/` when a project advances.
- Keep changelog entries restrained and factual.

## 7. Follow Ecosystem Standards

The `ecosystem-standards` repository is the canonical source of truth:

| Standard | File |
|----------|------|
| Agent discipline and behavior | `standards/agent-governance.md` |
| Naming conventions | `standards/naming-conventions.md` |
| Public/private boundaries | `standards/public-private-boundary.md` |
| Security and credentials | `standards/security-standard.md` |
| Repository structure | `standards/repository-structure.md` |
| Profile integration | `standards/github-profile-integration.md` |

## 8. Update GitHub Profile Repo When a Meaningful Public-Facing Ecosystem Change Is Merged

When a meaningful public-facing change is merged — new public repo, new capability in an existing public repo, updated agent governance — update the profile README at `github.com/sparshsam/sparshsam`:
- Add the repo to the Public Ecosystem table if it meets maturity requirements.
- Update or add a note about new agent coordination capabilities.
- Do not duplicate existing references.
- Keep the profile update concise: one sentence or bullet per change.
