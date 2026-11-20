# PlayCue Agent Rules

## Direction
PlayCue is a lightweight, calm, local-first Steam companion. Windows 10/11 first. Persistent Orb by default; hide during fullscreen games. Read all relevant docs, especially UX research and design system. All product features remain in the roadmap; implement by quality-gated phases.

## UX is core engineering
- Frequent task is summon → search → launch; keep this near-instant and visually simple.
- Calm by default: no default feed, social indicators, ads, FOMO, streaks or pressure.
- Preserve user control: easy pause/hide/disable Orb, per-category notification controls, opt-in social/cloud.
- Friendly and playful, never childish or guilt-inducing.
- Follow shared tokens, accessibility and screen specifications.
- Test with users; do not say "perfect" or "polished" without evidence.

## Source of truth
Use current official Valve/Steamworks, Tauri v2, Rust, React, SQLite, Windows and WCAG docs. Community posts are pain-point evidence, not API contracts. Update research sources when facts change.

## Hard boundaries
No Steam/game injection, patching, modification or process-memory reads. No undocumented/private Steam endpoints as core dependencies. No passwords, Steam Guard codes, cookies or session tokens. No publisher API keys in clients. No privacy, DRM or anti-cheat bypass. Read VDF/ACF only and defensively. Never shell-interpolate metadata.

## Architecture
Tauri 2 + Rust backend + React/TypeScript frontend + SQLite. Rust owns OS/filesystem/process/window operations. Narrow typed commands/events. Least-privilege capabilities. Core functions offline. Versioned migrations and transactions.

## Privacy
Social and sync opt-in. Respect private/friends-only visibility. Unknown/private/stale is not offline. Cloud sync off by default. Export, revoke and delete controls. No telemetry by default.

## Process
Inspect git status before changes. Plan a vertical slice. Add failure-path tests. Run format/lint/typecheck/tests/build. Inspect diff. Never overwrite user changes. Report exact evidence and tests not run.

## Completion
A feature is complete only when behavior, errors, UX, accessibility, privacy, tests and docs exist. Compilation/mock UI is not completion. Windows and Steam Deck support require platform testing.
