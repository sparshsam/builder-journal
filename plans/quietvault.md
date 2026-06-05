# QuietVault — Build Roadmap

## Purpose

A local-first encrypted vault experiment for storing, organizing, and retrieving small pieces of encrypted data. QuietVault is an exploration in client-side encryption, local storage, and privacy-focused application design. It is a prototype and experiment — not a production security product.

**Important:** QuietVault is not compliant, professionally secure, enterprise-grade, or production-audited. It is an experiment. Do not use it for sensitive real-world data without independent security review.

## MVP Scope

- Local-first data storage (IndexedDB or similar)
- Client-side encryption (AES-GCM or similar symmetric encryption)
- Entry creation: title, content, tags
- Search within decrypted entries
- Import/export of encrypted vault (single file)
- Password-based vault access

## Non-Goals

- Cloud sync or backup (future consideration)
- Multi-user access (future consideration — design for single-user)
- Key management or recovery beyond password
- Audit logging or compliance features
- End-to-end encryption claims (encryption is client-side only)
- Any representation of being a production-ready security product

## Risk Classification

**Risk Level:** Medium

Encrypted data storage. The primary risk is users trusting the application with data that requires production-grade security. The application is explicitly an experiment. All documentation must make this clear and avoid overclaiming security properties.

## Privacy / Security Boundaries

- All encryption and decryption happens client-side in the browser.
- No data is transmitted to any server unless the user explicitly exports.
- The encryption mechanism has not been independently audited.
- The application makes no guarantees about key derivation strength, side-channel resistance, or forward secrecy.
- Users should not store critical secrets (passwords, recovery phrases, private keys) in QuietVault.
- Do not use QuietVault to store data whose compromise would cause harm.

## Target: v0.1.0

**Estimated:** Q4 2026

## Future Versions

- **v0.2.0:** Biometric unlock (where platform supports), encrypted attachment support
- **v0.3.0:** Vault format versioning, integrity verification, entry categories

## Agent Notes

- All documentation must include the disclaimer that this is an experimental vault, not a production security product.
- Do not claim compliance, audit status, enterprise-grade security, or professional-grade encryption.
- Use precise language: "encrypted vault experiment" rather than "secure vault."
- Do not recommend QuietVault for storing sensitive real-world data without independent security review.
- The vault format should be open (documented in the repo) even if the application is an experiment.
- Consider using the Web Crypto API for encryption rather than a third-party library.
- Add a prominent warning on the application's landing/start page.
- The export file format should include a version header for future format migration.

## Release Readiness Checklist

- [ ] All MVP items complete
- [ ] Tests pass
- [ ] Prominent disclaimer present on landing page and in README
- [ ] No compliance/audit/enterprise claims made
- [ ] Encryption mechanism documented (not audited)
- [ ] Usability warning about experimental status
- [ ] No secrets committed
- [ ] Public-safe language verified
