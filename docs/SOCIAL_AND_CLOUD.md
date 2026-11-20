# SquadPulse, Game Night Matcher and Cloud Sync

## Principle
Social and cloud are optional. Core PlayCue needs no account. User sees exactly what is shared, with whom and for how long.

## SquadPulse
Local friend shortcuts can store user-entered Steam profile links/SteamIDs and labels. Later, show public/authorized profile information and opt-in PlayCue availability. Presence states: steam_observed, playcue_shared, stale, private, unknown. Never turn inaccessible data into “offline.”

## Game Night Matcher
Create a group and invite participants. Each participant deliberately shares a selected or complete game list and optional platform/party preferences. Compare only the shared lists. Explain why a game matches; let participants revoke and delete shared data. Manual export/import is fallback.

## Backend
No MVP backend. Before deployment define authentication, consent, invite/group membership, key management, access control, retention, deletion, export, rate limits, abuse controls, backups and incident response. Steam OpenID identifies a user but does not authorize access to private data. Never embed publisher Web API keys in clients.

## Cloud Sync
Off by default. Per-category controls; no sensitive recipient nicknames/notes synced by default. Encryption in transit and at rest; do not claim end-to-end encryption unless the key model supports it. Deterministic visible conflict resolution. Provide pause, export, remote deletion and account unlink. No sale of gaming data or targeted advertising profiles.
