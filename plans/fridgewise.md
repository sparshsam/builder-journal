# FridgeWise — Build Roadmap

## Purpose

A food inventory and expiration tracking application to help reduce food waste. Users can log groceries, track expiration dates, and receive notifications before items expire.

## MVP Scope

- Item entry: name, quantity, expiration date, category
- Dashboard view of all tracked items sorted by expiration
- Expiration alerts (via in-app notification or push)
- Search and filter by category
- Basic CRUD for items

## Non-Goals

- Barcode scanning or OCR-based entry (future consideration)
- Recipe suggestions (future consideration)
- Multi-user household sharing (future consideration)
- Nutritional tracking
- Integration with grocery delivery services

## Risk Classification

**Risk Level:** Low

This is a standard CRUD application. No financial transactions, no PII beyond what the user chooses to enter, no third-party data sharing.

## Privacy / Security Boundaries

- Item data is stored locally or under the user's own account.
- No food or consumption data is shared with third parties.
- The application does not collect or transmit telemetry without user consent.

## Target: v0.1.0

**Estimated:** Q3 2026

## Future Versions

- **v0.2.0:** Barcode scanning, push notifications, category presets
- **v0.3.0:** Recipe suggestions based on expiring items, household sharing

## Agent Notes

- Consider local-first architecture (IndexedDB or SQLite) with optional cloud sync.
- Expiration notification timing should be configurable (24h, 48h, 7d before expiry).

## Release Readiness Checklist

- [ ] All MVP items complete
- [ ] Tests pass
- [ ] Security boundaries documented
- [ ] README updated
- [ ] No secrets committed
- [ ] Public-safe language verified
