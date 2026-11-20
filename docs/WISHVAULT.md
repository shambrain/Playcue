# WishVault Specification

WishVault is PlayCue's durable local memory of games the user wanted to buy or revisit.

## States
Use explicit states: present_in_snapshot, not_present_in_later_snapshot, store_page_unavailable, region_unavailable, user_archived, unknown. Store source, check time, region and confidence. Missing from a later snapshot does not prove removal or delisting.

## Capture
MVP: manual add and JSON/CSV import with validation and preview; snapshot local records. Later: explicit user-triggered browser extension capture from visible Steam wishlist page. No background scraping, cookies, browser DB, password or token access. Do not depend on undocumented wishlist endpoints.

## Data
Stable UUID; Steam AppID when known; title; store URL; developer/publisher if sourced; image reference and source; note/tags; first saved and last seen timestamps; capture method; region/currency/price only with source and observation timestamp.

## Snapshots
Store capture time/source/region/completeness/schema version/item count. Diff by AppID first; fuzzy title matching is low-confidence and must be reviewed. Partial capture never replaces a complete snapshot. Preview large imports before mutation.

## Gift Watchlist
Separate user-curated list with game reference, recipient nickname (local/private), note, target price/currency/region, reminder and status. Do not infer ownership from hidden data or installed files.

## Export/testing
JSON with schema version and stable IDs; CSV with limitations documented. Test round trip, duplicate records, missing AppID, changed title, partial capture, malformed files, unknown schema, interrupted writes and same-day snapshots.
