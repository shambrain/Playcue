# OpenCode Master Directive — PlayCue

Build PlayCue into a polished, efficient Windows-first gaming companion for Steam. The user's core interaction should be effortless: a stylish Orb remains at the desktop edge; one click or a global shortcut opens the compact panel; search and launch a game immediately; WishVault remembers games the user wanted. The app is local-first. Social, sync, browser extension and Steam Deck follow later.

## Start
Read AGENTS.md and all relevant docs/. Inspect the working tree, history and toolchain. Verify current official framework/API docs. Produce a short plan with risks and tests, then implement a small complete vertical slice. Do not ask the user to repeat decisions recorded here.

## Decisions
- Product: PlayCue; signature feature WishVault; desktop interaction PlayCue Orb.
- Windows 10/11 first.
- Tauri 2 + Rust + React + TypeScript + SQLite.
- Persistent Orb by default; automatic hide for fullscreen games; disable option; tray and global shortcut alternatives.
- All features in docs/PRODUCT_SPECIFICATION.md remain in the roadmap.
- Local-first; no login/backend needed for MVP.
- Steam Deck/Linux is roadmap only.
- Millennium is not a core dependency.

## First-release scope
Steam root/library detection read-only; robust multi-library game catalog; standard Steam AppID launch handoff; Orb/Quick Panel/shortcut/tray/autostart setting/fullscreen suppression; local indexed search; favorites/recent games; PlayCue-observed session history; WishVault manual/import snapshots and comparison; Gift Watchlist; Unified Game Search; JSON/CSV export; offline workflows.

## Later scope
Gaming Collections; Session Notes; Launch Doctor with safe evidence-based advice; optional browser wishlist capture; SquadPulse; Game Night Matcher based on voluntarily shared lists; optional encrypted Cloud Sync; Deck Mode; optional separately maintained Millennium experiment.

## Steam requirements
Consult current Valve docs before each integration. Treat VDF/ACF files as read-only best-effort data. Use a validated numeric AppID and normal Steam URL handoff (commonly steam://run/<appid>) via safe OS URL opening, not shell concatenation. A successful handoff is not proof the game reached its menu. Never patch Steam, read process memory, scrape private endpoints, collect cookies/tokens, bypass privacy or ship publisher keys. Web API GetFriendList may return 401 for a private list; GetOwnedGames/GetRecentlyPlayedGames depend on profile visibility. Steamworks ISteamFriends is not a general Tauri desktop API.

## Orb requirements
Separate transparent frameless Tauri window; move/snap to screen edge; remember position across monitor/DPI changes; no focus stealing at startup; panel gets predictable focus only after explicit activation; Escape closes; tray/shortcut recover hidden UI; conservative fullscreen detection; no high-frequency polling; no input interception; auto-hide can be disabled.

## WishVault semantics
AppID is the stable external key when available. Store capture source, timestamp, region, currency, completeness and confidence. Differentiate not-in-later-snapshot, unavailable, region-unavailable, user-archived and unknown. Never equate missing snapshot item with delisted. Gift list is separate and user-curated. No invented prices/dates.

## Optional social and browser
Steam OpenID proves identity, not authorization to see private data. Share only voluntarily selected game lists/status with named people. The browser extension may capture visible page data only after a user-initiated action, with narrow permissions and no cookies/tokens. Use an authenticated native-messaging bridge; no open localhost API.

## Quality
Measure idle CPU/RAM and local search p95 on a named reference machine. No hot loops. Offline launch/search/archive must work. Validate malformed manifests, stale AppIDs, missing Steam, multiple libraries, fullscreen, mixed-DPI displays, imports, interrupted DB writes and export round trips. Windows 10 and 11 need separate manual acceptance. Deck requires physical device tests.

## Work phases
A foundation/CI/schema; B Steam discovery/launch; C Orb/Windows behavior; D search/recent/session history; E WishVault/Gift/Unified Search; F accessibility/performance/release; G collections/notes/Launch Doctor; H optional browser; I social/cloud; J Linux/Deck; K optional Millennium.

Use the PlayCue specialist agents/skills. Preserve uncommitted work. Every completion claim must have exact commands, results, known limits and evidence.
