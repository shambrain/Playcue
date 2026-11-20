# PlayCue Architecture

Proposed design; confirm exact dependency versions/APIs during implementation.

## Stack
Tauri 2 shell; Rust native/domain backend; React + TypeScript frontend; SQLite local source of truth; official Tauri v2 plugins where appropriate; no mandatory online service.

## Boundaries
Frontend: presentation, accessible interactions, local search UI. Rust: Steam discovery, safe launch, process observation, database, OS windows, Orb policy and file imports/exports. Keep pure domain logic independent of Tauri commands.

## Proposed modules
- steam_discovery: locate Steam root, libraries, manifests, normalize AppIDs.
- steam_launch: validate AppID, invoke registered Steam URI handler, report launch stages.
- process_observer: best-effort process lifecycle and confidence.
- orb: window placement, snap, visibility, fullscreen policy, monitor/DPI handling.
- catalog/search: local indexed game records and Unified Game Search.
- wishvault: snapshots, diffs, status confidence, import/export.
- history/gifts/collections/notes: separate domain services.
- social/sync: interfaces only until threat model and consent design are approved.

## Tauri command boundary
Use narrow typed commands (e.g. scan_steam_libraries, list_installed_games, search_local_games, launch_steam_app, get_recent_sessions, create_wishlist_snapshot, compare_wishlist_snapshots, export_user_data, set_orb_position). Validate all inputs in Rust. Do not expose broad shell/filesystem access. Emit coarse lifecycle events, not high-frequency UI telemetry.

## Steam discovery
Read Steam library configuration and appmanifest files only. Support multiple libraries, malformed/missing data, stale paths, external drive absence and concurrent client updates. These local formats are best-effort compatibility inputs, not stable public API guarantees.

## Launch lifecycle
Resolve game to validated numeric AppID. Dispatch standard Steam URL via safe OS URL opener, commonly steam://run/<appid>. Record request separately from process observation. Publisher launchers/anti-cheat may create child processes; do not assume first child is the game. Report outcome as handoff_only, process_observed, exited or unknown.

## Orb
Use a dedicated transparent, frameless Tauri window with least-privilege capabilities. Separate display, placement, and visibility state. Persist monitor identity + normalized work-area coordinates. Recover when monitor disappears or DPI changes. Avoid focus stealing at startup. Prefer foreground/window events plus throttled verification for fullscreen detection, not a busy loop. Tray/shortcut must recover the panel.

## Database
SQLite with migrations, foreign keys, transactional snapshot/import, prepared queries and integrity tests. Use FTS5 only after verifying bundled SQLite support. SteamID64 crosses JS/JSON as decimal string to avoid precision loss. Prices are integer minor units + ISO currency + region + observed timestamp.

## Optional browser bridge
Later extension: user-initiated visible wishlist capture. Narrow host permissions, bounded authenticated native-messaging payloads and schema validation. No cookies, browser DB or open localhost API.

## Optional cloud
No backend for MVP. Future service must define consent, authentication, encryption/key ownership, retention, conflict merge, export, account unlink, remote deletion and abuse controls before deployment.
