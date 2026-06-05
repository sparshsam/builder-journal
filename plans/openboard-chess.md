# OpenBoard Chess — Build Roadmap

## Purpose

An open-source chess application with support for local play, online multiplayer, and game analysis. Designed for casual and intermediate players.

## MVP Scope

- Full chess rules implementation (moves, castling, en passant, promotion, check, checkmate, stalemate)
- Local two-player mode on the same device
- Basic move validation and legal move highlighting
- Move history display (algebraic notation)
- Game state export/import (PGN or FEN)

## Non-Goals

- AI/engine integration for move suggestions (future consideration)
- Online matchmaking server (future consideration)
- Time controls and tournament modes (future consideration)
- Opening book or database integration
- Analysis board with engine evaluation

## Risk Classification

**Risk Level:** Low

Standard chess application. No financial transactions, no personal data beyond what is needed for online play.

## Privacy / Security Boundaries

- Local games require no data transmission.
- Online play (future) should use encryption and avoid storing game data server-side unless the user opts in.
- No user telemetry collection.

## Target: v0.1.0

**Estimated:** Q3 2026

## Future Versions

- **v0.2.0:** AI opponent with configurable difficulty, PGN export
- **v0.3.0:** Online multiplayer, game clock/timer

## Agent Notes

- Chess logic should be implemented as a standalone library with full test coverage.
- Consider using a well-known chess library (e.g., chess.js) to avoid reimplementing rules.
- The UI can be web-based (React) or native depending on the target platform.

## Release Readiness Checklist

- [ ] All MVP items complete
- [ ] Tests pass (move validation, edge cases, rules)
- [ ] Security boundaries documented
- [ ] README updated
- [ ] No secrets committed
- [ ] Public-safe language verified
