# Quality Gates

## Engineering
- cargo fmt --check
- cargo clippy --all-targets --all-features -- -D warnings
- cargo test
- Frontend lint/typecheck/tests/build
- Tauri production build
- dependency/license audit and secret scan

## Steam discovery/launch
- Default and custom Steam roots; multiple libraries/drives; malformed VDF; missing/partial manifest; duplicate/stale AppID; unplugged library; Steam not installed/running.
- Valid launch, missing URI handler, app removed, publisher launcher and process-observation ambiguity.
- No writes to Steam files/registry and no arbitrary command execution.

## Orb
- Startup focus, click/drag/snap, global shortcut conflict, tray recovery, auto-hide, monitor removal, mixed DPI, taskbar placement, display sleep/resume and disable mode.

## Data
- Snapshot transactionality; partial capture; import preview; duplicate handling; missing AppID; unknown schema; interrupted write; JSON/CSV round-trip; data deletion.

## Privacy/security
- No credential/cookie access; no publisher key in clients; Tauri least privilege; path traversal tests; import limits; redacted logs; cloud/social disabled by default.

## UX
- Keyboard-only navigation, focus order, screen reader names, reduced motion, high contrast, empty/error/offline/private states and provenance labels.

## Release evidence
Record OS build/hardware, Steam client branch/build, commit, dependencies, test commands/results, manual Orb/fullscreen evidence, installer/signing, limitations and untested platforms. Compilation is not release acceptance.
