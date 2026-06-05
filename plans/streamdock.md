# StreamDock — Build Roadmap

## Purpose

A media player application designed for playback of legally obtained IPTV and Xtream-compatible subscriptions. StreamDock provides a unified interface for managing and viewing media from authorized sources only.

## MVP Scope

- Playlist import (M3U, Xtream API)
- Channel list with search and filter
- EPG (Electronic Program Guide) integration
- Video playback with basic controls (play, pause, seek, volume)
- Favorites list

## Non-Goals

- Content discovery, recommendation, or promotion
- Bittorrent, P2P, or peer-to-peer streaming support
- Download or offline storage of streamed content
- DRM circumvention or piracy-enabling features
- Unofficial or unauthorized IPTV provider support
- Any mechanism to find, search, or recommend content sources

## Risk Classification

**Risk Level:** Medium

Media player. The primary risk is misuse for unauthorized content. The application must never provide, sell, recommend, or facilitate access to unauthorized content. All documentation must use precise, safe framing.

## Privacy / Security Boundaries

- StreamDock does not provide content. It only plays content from sources the user configures.
- No content is stored, cached, or redistributed by the application.
- No telemetry or usage data is collected about what the user watches.
- The application does not maintain a directory or index of IPTV providers.
- The user is solely responsible for ensuring their content sources are legally authorized.

## Target: v0.1.0

**Estimated:** Q4 2026

## Future Versions

- **v0.2.0:** Multi-playlist support, catch-up TV, recording scheduler (for authorized content)
- **v0.3.0:** Multi-device sync, parental controls, customizable UI themes

## Agent Notes

- All public documentation must clearly state that StreamDock is for legally obtained subscriptions only.
- Do not reference specific IPTV providers, content sources, or unauthorized services in any documentation.
- Avoid language that could be interpreted as encouraging or facilitating piracy.
- The app should not include a browser for discovering IPTV services.
- If implementing a recording feature, frame it as DVR for authorized content only.

## Release Readiness Checklist

- [ ] All MVP items complete
- [ ] Tests pass
- [ ] Public-facing language audited — no piracy-facilitating framing
- [ ] No content source recommendations or provider directories
- [ ] Security boundaries documented
- [ ] README updated
- [ ] No secrets committed
- [ ] Public-safe language verified
