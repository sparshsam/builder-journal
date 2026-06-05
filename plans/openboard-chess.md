# Chess by Sparsh — Build Roadmap

## Repository

- **Planned repository name:** `openboard-chess`
- **Public product name:** Chess by Sparsh
- **Repository description:** Open-source chess board focused on clean local play, accurate rules, move history, and portable game records.

## Purpose

Chess by Sparsh is an open-source chess board application focused first on clean local play, accurate rules, move history, and portable game records.

The project should begin as a restrained, testable local chess experience. Online play, engine analysis, and richer study tools can be considered later only after the core board, rules, and game-state handling are stable.

## Builder Journal Boundary

Do not build the chess application inside `builder-journal`.

Builder Journal should only track:

- roadmap
- public-safe status
- decisions
- build sequencing
- agent handoff notes

Implementation work belongs in the future `openboard-chess` repository.

## MVP Scope

- Full chess rules support through a reliable chess logic layer
- Local two-player mode on the same device
- Legal move validation and legal move highlighting
- Move history display using standard chess notation where practical
- Game state export/import using FEN first, with PGN as a follow-up if needed
- Clear reset/new-game flow
- Public-safe README, license, and basic contribution notes
- Automated tests for rule-critical behavior

## Non-Goals for v0.1.0

- AI/engine integration for move suggestions
- Online matchmaking server
- User accounts or profiles
- Time controls and tournament modes
- Opening book or database integration
- Analysis board with engine evaluation
- Claims about engine strength, training quality, ratings, or competitive performance

## Risk Classification

**Risk Level:** Low

Standard local-first chess application. The first version should not require accounts, payments, telemetry, private user data, or server-side storage.

## Privacy / Security Boundaries

- Local games require no data transmission.
- No user telemetry collection.
- No credentials, tokens, or private configuration should be committed.
- Online play, if added later, must be designed separately with clear privacy and security boundaries.
- Avoid storing game data server-side unless the user explicitly opts in.

## Suggested Initial Stack

- React + Vite + TypeScript
- `chess.js` or another mature chess rules library
- Vitest for rule and component tests
- Local browser storage only where useful
- Vercel or GitHub Pages for public demo deployment

## Target: v0.1.0

**Estimated:** Q3 2026

## Future Versions

- **v0.2.0:** PGN export, saved local games, board themes
- **v0.3.0:** Game clock/timer and simple practice conveniences
- **v0.4.0:** Optional engine-backed analysis, clearly labelled as engine-assisted
- **v0.5.0:** Optional online multiplayer after privacy/security design is documented

## Agent Notes

- Treat `builder-journal` as the planner only.
- Create implementation work in `openboard-chess`, not here.
- Prefer using a mature chess rules library rather than reimplementing chess rules from scratch.
- Keep the chess logic isolated from UI components where possible.
- Prioritize readable UI, correct legal moves, and reliable tests over feature volume.
- Keep claims restrained until the app is actually built and validated.

## Release Readiness Checklist

- [ ] `openboard-chess` repository created
- [ ] README states the product name as Chess by Sparsh
- [ ] Repository description matches the approved wording
- [ ] All MVP items complete
- [ ] Tests pass for legal moves, edge cases, and core rules
- [ ] Security boundaries documented
- [ ] README updated
- [ ] No secrets committed
- [ ] Public-safe language verified
