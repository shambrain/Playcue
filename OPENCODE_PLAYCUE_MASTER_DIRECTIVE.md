# OpenCode Master Directive — PlayCue

Build PlayCue into a polished, efficient Windows-first gaming companion for Steam. The user's core interaction is effortless: a stylish, unobtrusive Orb remains at the desktop edge; one click or global shortcut opens a calm Quick Panel; search and launch a game immediately; WishVault remembers games the user wanted. PlayCue should feel like a thoughtful gaming sidekick, not a noisy dashboard or Steam clone.

## Required reading
Read AGENTS.md, all relevant docs including UX_RESEARCH_2026.md, DESIGN_PRINCIPLES.md, VISUAL_DESIGN_SYSTEM.md, SCREEN_SPECIFICATIONS.md, INTERACTION_AND_MICROCOPY.md, ACCESSIBILITY_AND_COMFORT.md and UX_VALIDATION_PLAN.md. Use product-ux-designer and ux-researcher agents for UI tasks.

## Decisions
- Product: PlayCue; signature feature WishVault; desktop interaction PlayCue Orb.
- Windows 10/11 first.
- Tauri 2 + Rust + React + TypeScript + SQLite.
- Persistent Orb by default, hide during fullscreen games; disable option; tray and global shortcut alternatives.
- All features in PRODUCT_SPECIFICATION.md remain in roadmap.
- Local-first; no login/backend needed for MVP.
- Steam Deck/Linux is roadmap only.
- Millennium is not a core dependency.
- UI/UX, accessibility and comfort are engineering requirements, not optional polish.

## UX non-negotiables
- Calm by default, low cognitive load, progressive disclosure, recognition over recall.
- Search and launch is the first task; do not build a cluttered dashboard.
- No default social feed, ads, guilt, FOMO, streaks, nagging or autoplay.
- Social and notifications are opt-in and easy to pause.
- Spoilers hidden by default.
- User can move, dim, pause, hide or disable Orb.
- Visible focus, keyboard navigation, screen-reader semantics, reduced motion, high contrast and DPI behavior are first-class.
- Warm concise peer-like copy; friendly not childish.
- Use shared design tokens and test real rendered contrast.
- No design marked complete based on mockup alone; run formative usability tests.

## First-release scope
Steam discovery read-only; standard launch handoff; Orb/Quick Panel/shortcut/tray; search; recents; favorites; WishVault snapshots/import/export; Gift Watchlist; Play History; Unified Game Search; polished design system, accessibility and validation.

## Later
Collections; Session Notes; Launch Doctor; optional user-triggered browser capture; SquadPulse; Game Night Matcher; optional Cloud Sync; Deck Mode; optional separately maintained Millennium experiment.

## Steam and privacy requirements
Verify Valve docs. No undocumented/private endpoints, credentials/cookies, client modification, process memory reads, DRM or anti-cheat bypass. Steam OpenID is identity, not authorization. Unknown/private/stale is never offline. Local VDF/ACF is read-only best-effort. No secrets in client.

## Engineering quality
Tauri 2 capabilities least-privilege. Rust owns filesystem/process/window operations. SQLite migrations and transactions. No hot loops. Measure idle CPU/RAM, search p95 and startup. Preserve user changes. Run formatting, lint, typecheck, tests and production build. Record exact commands/results and untested cases. No false feature/support claims.
