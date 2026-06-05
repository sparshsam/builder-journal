# LexiBoard — Build Roadmap

## Purpose

A word tile board game where players place letter tiles on a grid to form words. LexiBoard is a word game in the tile-placement puzzle genre. It does not use the Scrabble brand, Scrabble rules, or Scrabble trademarked elements.

## MVP Scope

- Tile-based word placement on a grid board
- Turn-based gameplay (local, single device)
- Word validation against a standard dictionary
- Score tracking per player
- Tile rack management with pass and swap options

## Non-Goals

- Real-time multiplayer over the network (future consideration)
- Scrabble compatibility or adherence to Scrabble rules
- AI opponent (future consideration)
- Dictionary editor or custom word lists
- Branded elements or trademark-encumbered terminology

## Risk Classification

**Risk Level:** Low

Word game. The primary risk is trademark confusion with Scrabble. All documentation and code must avoid using "Scrabble" as a descriptor, comparison, or reference point. Use "word tile board game" or similar original phrasing.

## Privacy / Security Boundaries

- Local games require no data transmission.
- No user data is collected or transmitted.
- The dictionary is bundled with the application; no network calls for word lookup.

## Target: v0.1.0

**Estimated:** Q4 2026

## Future Versions

- **v0.2.0:** Pass-and-play on the same device, custom board sizes
- **v0.3.0:** Online asynchronous play, themed tile sets, timer modes

## Agent Notes

- Do not use the word "Scrabble" in any documentation, code comments, or commit messages.
- Board dimensions, tile distribution, and scoring should be original — not copied from Scrabble or any other trademarked game.
- Use original terminology: "word tile board game" or "tile-placement word game."
- The dictionary should be a standard open-source word list (e.g., SCOWL, ENABLE, or similar).
- Verify no trademark-encumbered assets, names, or terminology are used.

## Release Readiness Checklist

- [ ] All MVP items complete
- [ ] Tests pass
- [ ] No Scrabble-branded terminology or assets
- [ ] Original board and scoring design verified
- [ ] Open-source dictionary attribution included
- [ ] Security boundaries documented
- [ ] README updated
- [ ] No secrets committed
- [ ] Public-safe language verified
