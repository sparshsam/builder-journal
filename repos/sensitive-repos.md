# Sensitive Repos — Special Care Rules

Some ecosystem repositories involve betting/financial systems, authentication, user data, or onchain transactions. These repos require stricter operational discipline and must not be treated as routine public repositories.

---

## General Rules for All Sensitive Repos

1. **No secrets in source.** API keys, tokens, passwords, private keys, mnemonics, or credentials must never be committed. Use environment variables, secret managers, or hardware wallets.
2. **No private user data.** Do not commit logs, database dumps, or user-submitted content to any repository (even private ones).
3. **No methodology disclosure.** For private sensitive repos, do not describe operational methodology, prompt engineering, data pipelines, or architecture details in public contexts.
4. **Audit commits before push.** Scan for accidentally included secrets, config files, or `.env` overrides before pushing.
5. **Keep `.gitignore` tight.** Ensure `.env`, `*.log`, `node_modules/`, `target/`, `dist/`, and IDE config are always excluded.
6. **Enable branch protection** on all sensitive repos (requires PR for `main`, no direct pushes).
7. **Enable secret scanning** (GitHub Advanced Security or equivalent).
8. **Restrict collaborator access** to only those who need it. Audit quarterly.

---

## Per-Repo Care Rules

### Elora Vault

| Attribute | Rule |
|-----------|------|
| Risk category | **betting-sensitive** |
| Visibility | Public (source) / Private (internal notes) |
| Special rules | • No real-money betting data in any repo.<br>• Prediction market terminology must use clear disclaimers (not financial advice).<br>• Smart contract code must go through security review before mainnet deployment.<br>• Keep user vault data out of public docs and issues.<br>• Terms of service must disclaim any investment or gambling advice. |
| Legal framing | Required. See `CURRENT_STATUS.md` for current posture. |

### TW Oracle / The Wager Tools

| Attribute | Rule |
|-----------|------|
| Risk category | **betting-sensitive** |
| Visibility | Private |
| Special rules | • **Zero public methodology disclosure.** Do not describe how predictions are made, what data feeds are used, or model architecture.<br>• **No performance data.** Do not publish win rates, ROI, accuracy stats, or pick history.<br>• Keep repo access to a strict need-to-know list.<br>• No public issues mentioning specific picks, outcomes, or methods.<br>• Internal documentation must not be committed with prediction-specific data that could reconstruct methodology. |
| Legal framing | Required. The Wager brand carries legal exposure — ensure terms of service, disclaimers, and regulatory review are current. |

### QuietVault Password Manager

| Attribute | Rule |
|-----------|------|
| Risk category | **security-sensitive** |
| Visibility | Planned (public) |
| Special rules | • **Cryptography must use audited, standard libraries only.** No rolling your own crypto.<br>• Zero-knowledge architecture (if planned) must be documented and verified.<br>• No password data, vault contents, or derived keys may appear in commits, logs, or error messages.<br>• A security audit must be completed before the first release.<br>• Follow OWASP guidelines for credential storage. |
| Legal framing | Privacy policy and security disclosure process needed before release. |

### StreamDock IPTV Player

| Attribute | Rule |
|-----------|------|
| Risk category | **privacy-sensitive** |
| Visibility | Planned (public) |
| Special rules | • Do not commit streaming tokens, API keys, or account credentials.<br>• User playback data must not be logged or transmitted without explicit consent.<br>• No hardcoded URLs to unlicensed content sources.<br>• Must include a clear privacy policy explaining what data the app collects and why. |
| Legal framing | Due to IPTV's legal gray area, include explicit terms of service and DMCA compliance notice. |

### Any Wallet or Onchain Repository

| Attribute | Rule |
|-----------|------|
| Risk category | **finance-sensitive** (may overlap with security-sensitive) |
| Visibility | As appropriate for each project |
| Special rules | • Private keys, mnemonics, and seed phrases must **never** be stored in or derived from source code.<br>• Smart contracts must follow established patterns (OpenZeppelin, Solmate) and be verified on-chain.<br>• Use hardware wallets or secure key management for any production onchain operations.<br>• Test with testnet funds only. Never use mainnet funds in development.<br>• All transaction construction must be reviewed for correctness before broadcast. |

### Any Repo Using Authentication or User Data

| Attribute | Rule |
|-----------|------|
| Risk category | **privacy-sensitive** or **security-sensitive** |
| Visibility | As appropriate for each project |
| Special rules | • Authentication tokens, session secrets, and OAuth credentials must be treated as secrets.<br>• User data exposure must be minimized. Anonymize or pseudonymize where possible.<br>• Add a `PRIVACY.md` or `docs/privacy-model.md` that documents data handling.<br>• Follow data minimization principles: collect only what you need, retain only as long as needed. |

---

## Sensitive Repo Lifecycle

| Phase | Requirements |
|-------|-------------|
| Creation | Add to this file before or immediately after repo creation. Document risk category and special rules. |
| Active development | Follow all special rules above. Security review before any production release. |
| Pre-release | Legal review for betting/security-sensitive repos. Terms of service published. |
| Maintenance | Quarterly access audit. Secret scanning logs reviewed. |
| Archival | Confirm no secrets remain. Update README with archival notice including security context. |

---

## Related

- [Repo Inventory](./repo-inventory.md) — sensitivity column for every repo
- [Archive Candidates](./archive-candidates.md) — archival process
- [SECURITY_BOUNDARIES.md](../SECURITY_BOUNDARIES.md) — project-wide security boundaries
