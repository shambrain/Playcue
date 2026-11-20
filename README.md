# PlayCue

**Your little gaming sidekick.** Launch games in seconds. Keep your gaming life in order. Never lose a game you wanted.

PlayCue is a lightweight, calm, local-first companion for Steam. A small desktop Orb opens a focused Quick Panel for instant game search and launch. WishVault preserves the user's personal wishlist history. Optional social and sync features come later.

## Product direction
- Windows 10/11 first; Steam Deck/Linux on roadmap.
- Tauri 2 + Rust + React + TypeScript + SQLite.
- Persistent Orb by default; auto-hide during fullscreen; fully optional.
- Local-first; no account required for core features.
- Not a Steam client replacement and not affiliated with Valve.

## UX identity
Warm, modern, playful but restrained. Calm by default. Search-to-launch is the primary task. No default social feed, ads, streaks, FOMO or nagging. Accessible scaling, high contrast, reduced motion, keyboard/screen-reader support and user testing are release requirements.

## Feature plan
1.0: Orb, Quick Panel, Instant Game Search, Recently Played, favorites, WishVault, Gift Watchlist, Play History, Unified Game Search.
1.1: Collections, Session Notes, Launch Doctor, optional browser capture.
2.x: opt-in SquadPulse, Game Night Matcher and optional Cloud Sync.
3.x: controller-first Deck Mode and Linux packaging.
Research-gated: optional Millennium plugin; never a core dependency.

## Start here
- [Product Specification](docs/PRODUCT_SPECIFICATION.md)
- [2026 UX Research](docs/UX_RESEARCH_2026.md)
- [Design Principles](docs/DESIGN_PRINCIPLES.md)
- [Visual Design System](docs/VISUAL_DESIGN_SYSTEM.md)
- [Screen Specifications](docs/SCREEN_SPECIFICATIONS.md)
- [UX Validation Plan](docs/UX_VALIDATION_PLAN.md)
- [OpenCode Master Directive](OPENCODE_PLAYCUE_MASTER_DIRECTIVE.md)

## Repository status
This repository contains product and engineering specifications; it does not yet contain an executable PlayCue application. Do not describe planned features as implemented.
