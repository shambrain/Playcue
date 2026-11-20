# PlayCue

**A Windows-first gaming sidekick for Steam.** Open your games quickly. Keep track of what you love. Never lose a game you wanted.

PlayCue is a lightweight, local-first companion. A persistent desktop Orb opens a compact Quick Panel for installed-game search, launch, recent sessions and WishVault. It complements Steam; it does not replace the Steam client, store, overlay or chat.

- Name: PlayCue
- Signature feature: WishVault
- Desktop affordance: PlayCue Orb
- First platform: Windows 10/11
- Proposed stack: Tauri 2 + Rust + React + TypeScript + SQLite
- Repository status: planning/docs kickoff; no executable application implemented yet.

## Principles
1. Fast, low-friction launch; do not become another heavyweight launcher.
2. Steam-friendly: supported launch handoff and read-only local discovery.
3. Local-first: no sign-in required for core functions.
4. Evidence/provenance: distinguish observed facts from inferred/unavailable data.
5. Optional: Orb, autostart, online social and sync can be disabled.
6. No false Deck compatibility claims.

## Feature map

| Feature | Phase |
|---|---|
| PlayCue Orb, Quick Panel, global shortcut, tray | 1.0 |
| Instant Game Search, Recently Played, favorites | 1.0 |
| WishVault snapshots, missing-item history, import/export | 1.0 |
| Gift Watchlist, Play History, Unified Game Search | 1.0 |
| Gaming Collections, Game Session Notes, Launch Doctor | 1.1 |
| Optional browser companion for user-triggered wishlist capture | 1.1/2.x |
| SquadPulse and Game Night Matcher | 2.x |
| Optional privacy-first Cloud Sync | 2.x |
| Steam Deck/Linux Deck Mode | 3.x |
| Optional Millennium bridge | research gate only |

See docs/ for requirements and release gates. Start OpenCode with OPENCODE_PLAYCUE_MASTER_DIRECTIVE.md. AGENTS.md applies to all agents.

## Relationship disclaimer
PlayCue is independent and is not affiliated with, endorsed by or sponsored by Valve or Steam. Never request Steam passwords, Steam Guard codes or session cookies.

## Current status
This is a product/engineering documentation commit only. Do not describe planned features as implemented.
