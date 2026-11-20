# Security and Privacy

- Core app requires no account and works offline.
- Telemetry off by default. Diagnostic export is user-reviewed and user-initiated.
- Never request Steam password, Steam Guard code, cookies or browser tokens.
- Never embed publisher keys/service secrets in app, extension, installer or repo.
- Read Steam roots/manifests only; canonicalize paths and guard symlinks/path traversal.
- Do not shell-interpolate titles/paths or execute metadata-derived files.
- Keep Tauri capabilities least-privilege; narrow typed commands; CSP; no remote content in privileged WebView.
- Browser bridge, if added, must authenticate extension messages, validate origin/schema/size, and reject replay; no unauthenticated localhost HTTP API.
- Logs redact SteamIDs when unnecessary, personal paths, recipient labels, keys and tokens.
- Provide export and permanent local deletion.
- Cloud later: consent per category, encryption/key ownership, remote deletion, retention, unlink, incident response and conflict rules.
- Threat model: malicious VDF/ACF, malformed archive imports, path traversal, URI injection, XSS from metadata, extension spoofing, IPC spoofing, leaked tokens, account enumeration, API rate abuse and deletion failures.
