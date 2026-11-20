# PlayCue Product Specification

Status: approved product direction for implementation planning. Research snapshot: 2026-11-20.

## Product promise
A quick, lightweight gaming sidekick: launch a game without navigating Steam Library; preserve wishlist intent; keep personal gaming context nearby. PlayCue complements Steam and does not replace Steam Store, downloads, overlay, chat, achievements or DRM.

## Audience
Steam users with large libraries; users who cycle among recent games; users who want historical wishlist memory; groups who want to find common games; players who prefer one compact utility instead of a full launcher.

## UX pillars
Summonable (Orb, shortcut, tray); fast (local indexed search); quiet (low idle activity); trustworthy (data provenance); local-first; optional (disable Orb/network/notifications).

## Navigation
Home: recent/pinned/up-next. Library: detected games/search/filters/collections. WishVault: snapshots/diffs/missing items. Gift Watchlist: games intended as gifts. History: observed/imported sessions. Settings: Orb, shortcut, autostart, privacy, export, diagnostics. Social later: SquadPulse and Game Night.

## 1.0
- PlayCue Orb: persistent by default, draggable, edge snap, saved location, auto-hide during fullscreen; user can disable.
- Quick Panel: global shortcut, search focus, Escape close, predictable keyboard navigation.
- Steam discovery: read-only install/library scan, multiple libraries/drives, resilient error states.
- Instant Game Search: local fuzzy search across installed games.
- Recently Played and favorites.
- Quick Launch via Steam handoff; show launch-request vs confirmed-process state.
- Play History: record only sessions PlayCue can observe, with provenance/confidence.
- WishVault: manual/import entries, dated snapshots, comparison, archive, export; never infer delisted status from absence alone.
- Gift Watchlist: separate user-curated list, note/recipient nickname/target price/reminder.
- Unified Game Search across installed games and WishVault.
- SQLite migrations, tray, optional autostart, data export, offline operation.

## 1.1
Gaming Collections; Game Session Notes and next-step reminders; Launch Doctor diagnostics with no silent repair; optional browser companion for user-triggered wishlist capture (narrow permissions, no cookies/tokens).

## 2.x
SquadPulse with public/voluntarily shared presence; Game Night Matcher from explicitly shared game lists; optional Cloud Sync, off by default, with category consent, encryption model, export and deletion.

## 3.x
Steam Deck/Linux Deck Mode: controller-first full-screen UI and Flatpak feasibility. Not supported until tested on real hardware.

## Non-goals
No Steam UI replacement, launcher universalization in 1.0, DRM bypass, game/process injection, private data extraction, automatic cache deletion, or fake history.

## Success metrics
Time from Orb to launch request; local search p95; installed AppID resolution correctness; fullscreen false-positive/negative rate; WishVault capture/diff correctness; export/restore success; measured idle CPU/RAM; crash-free sessions; optional social/sync opt-in without forced account.
