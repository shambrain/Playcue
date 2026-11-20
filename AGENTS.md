# PlayCue Agent Rules

## Direction
PlayCue is a lightweight local-first Steam companion. Windows 10/11 first. Persistent Orb by default; hide during fullscreen games. All features in docs/PRODUCT_SPECIFICATION.md belong to the product roadmap; implement by phase, not by silently dropping them.

## Source of truth
Use current official Valve/Steamworks, Tauri v2, Rust, React, SQLite and OpenCode documentation for technical contracts. Community posts are pain-point evidence, not API contracts. Update docs/RESEARCH_SOURCES.md when contracts change.

## Hard boundaries
- Never patch, inject into, hook, modify or read memory from Steam/game processes.
- No undocumented/private Steam endpoints as core dependencies.
- No Steam passwords, Steam Guard codes, browser cookies, session tokens or browser profile extraction.
- Never embed a publisher Web API key in desktop/extension/installer code.
- Do not bypass privacy, DRM, anti-cheat or publisher launcher requirements.
- Read Steam VDF/ACF files only; parse defensively and treat as best-effort compatibility data.
- Use validated AppID + normal Steam launch handoff; never shell-interpolate untrusted metadata.
- Do not claim complete session history unless the source actually provides it.

## Architecture
Tauri 2 + Rust backend + React/TypeScript frontend + SQLite. Rust owns filesystem/process/native window operations. Frontend uses narrow typed Tauri commands/events. Least-privilege Tauri capabilities. Versioned migrations and transactions. Windows-specific code behind platform interfaces. Core workflows work offline; no account/backend required.

## Privacy
Social and sync are opt-in. Respect private/friends-only visibility. Unknown/private/stale are not offline. Cloud sync off by default with export, revoke, deletion and retention controls. No telemetry by default.

## Process
Inspect tree and dirty status before changes. Plan one vertical slice. Add tests for success and failure. Run format/lint/typecheck/tests/build. Inspect diff. Never overwrite user changes or reset a dirty tree without consent. Report exact evidence and tests not run.

## Completion
A feature is complete only when behavior, error handling, privacy, tests, UX and docs exist. Compilation or mock UI is not completion. Never claim Windows 10/11 or Deck support without those platforms being tested.
