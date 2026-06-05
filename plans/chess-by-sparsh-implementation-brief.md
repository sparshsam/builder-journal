# Chess by Sparsh — Implementation Brief

## Canonical Setup

- **Implementation repository:** `openboard-chess`
- **Public product name:** Chess by Sparsh
- **Repository description:** Open-source chess board focused on clean local play, accurate rules, move history, and portable game records.

## Repository Boundary

Do not build Chess by Sparsh inside `builder-journal`.

Builder Journal is only responsible for:

- roadmap
- public-safe status
- decisions
- build sequencing
- agent handoff notes

All application source code, package files, tests, release workflows, demo deployments, and implementation assets must live in `openboard-chess`.

## v0.1.0 Product Goal

Ship a clean local chess board that lets two people play on the same device with accurate rules, visible move history, and portable game state.

The first release should feel small, correct, calm, and reliable.

## v0.1.0 Required Scope

- Local two-player chess board
- Accurate legal move validation
- Castling, en passant, promotion, check, checkmate, and stalemate support
- Legal move highlighting
- Move history
- New game / reset flow
- FEN import/export
- Basic responsive layout
- README with purpose, scope, non-goals, and local development instructions
- Tests covering critical rule behavior

## v0.1.0 Non-Goals

- Online multiplayer
- User accounts
- Database storage
- AI opponent
- Engine analysis
- Opening explorer
- Ratings, ladders, or matchmaking
- Monetization
- Telemetry

## Suggested Stack

- React
- Vite
- TypeScript
- chess.js or another mature chess rules library
- Vitest
- Vercel or GitHub Pages for a public demo

## Agent Instructions

- Start from the separate `openboard-chess` repository once it exists.
- Keep commits small and reviewable.
- Do not add features outside the v0.1.0 scope without a decision entry.
- Use restrained public language. Do not claim engine strength, competitive readiness, or advanced analysis.
- Keep the chess rules layer testable and separated from visual board components where practical.
- Prefer correctness and simplicity over visual novelty.

## Initial Repository Creation Settings

Use these settings when creating the repo manually in GitHub:

| Field | Value |
|-------|-------|
| Owner | `sparshsam` |
| Repository name | `openboard-chess` |
| Description | `Open-source chess board focused on clean local play, accurate rules, move history, and portable game records.` |
| Visibility | Public |
| Initialize with README | Yes |
| License | MIT |
| Product name in README | Chess by Sparsh |

## First Implementation Milestone

Create the repo foundation only:

- README.md
- LICENSE
- package setup
- TypeScript config
- app shell
- test runner
- basic board placeholder
- no online features
- no engine features
