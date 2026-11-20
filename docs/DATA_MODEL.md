# PlayCue Local Data Model (Proposed)

Conceptual schema; choose exact SQL types after selecting the SQLite binding. Use versioned migrations, foreign keys, indexes and transactions.

- games: UUID, Steam AppID, title/normalized title, developer, publisher, store URL, install state/path, scan timestamp, metadata provenance.
- steam_libraries: ID, root path, source and last scan state/time.
- wish_items: UUID, AppID, title, store URL, metadata, first/last seen, state/source/confidence, region/currency, notes.
- wish_snapshots: ID, captured time, source, region, completeness, item count, schema version, import hash.
- wish_snapshot_items: snapshot/item IDs, observed title, optional integer price minor units, currency, region, source hash.
- gift_items: ID, game reference, recipient label, target price minor/currency/region, note, reminder, status.
- play_sessions: ID, game ID, start/end, launch source, observation method, confidence, process ID nullable, status.
- collections/collection_games/tags: user-created metadata and memberships.
- session_notes: ID, game/session reference, body, next action, reminder and timestamps.
- settings: schema-validated versioned values; no secrets.

Future only: social_groups, group_members, shared_library_snapshots, consent_grants, sync_devices and deletion_requests.

Rules: SteamID64 crosses JS/JSON as decimal string; timestamps UTC; prices integer minor units + ISO currency + region + observed timestamp; provenance for imported/remote fields; never replace complete snapshot with partial capture; use transactions for import and migration.
