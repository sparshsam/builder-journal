# Security Boundaries

Builder Journal is public. Treat every commit, issue, pull request, release, and profile reference as visible to the internet.

## Never Commit

Never commit:

- secrets, API keys, tokens, credentials, passwords, or session values;
- wallet seed phrases, private keys, recovery phrases, or signing material;
- `.env`, `.env.local`, `.env.production`, `.env.development`, or any real environment file;
- personal ID documents, passports, driver's licenses, tax records, or government forms;
- private address, phone number, financial account details, or personal finance records;
- private betting data, raw picks, edge calculations, logs, performance formulas, or methodology;
- private business data, client data, user records, operational metrics, or internal runbooks;
- deployment URLs, infrastructure addresses, database schemas, prompt chains, or orchestration logic for private systems.

## Claims Boundary

Never claim that a project is fully compliant, audited, production-secure, enterprise-grade, legally validated, financially reliable, or externally certified unless that claim is documented and true.

Prefer narrower language:

- "early foundation"
- "prototype"
- "needs review"
- "public-safe summary"
- "security boundaries documented"

## Public / Private Project Boundary

| Project Class | Public Notes May Include | Public Notes Must Exclude |
|---------------|--------------------------|---------------------------|
| Public | Purpose, status, docs, releases, known limitations. | Secrets, personal data, unsupported claims. |
| Private | High-level purpose and boundary only. | Source, architecture, prompts, schemas, data, URLs, workflows. |
| Sensitive | Category and safety boundary. | Raw records, private analysis, identifiers, financial or betting details. |
| Experimental | Idea, scope, current uncertainty. | Launch claims, production claims, invented maturity. |

## Agent Rules

- Check `.gitignore` before committing.
- Do not read, print, or summarize real secret files.
- If a secret appears in output or git history, stop and report it.
- Do not broaden private-system descriptions beyond approved high-level language.
- When unsure whether something is safe to publish, leave it out.

## Local Files

Use `.env.example` only for placeholder values. Real local files belong outside git and must stay ignored.
