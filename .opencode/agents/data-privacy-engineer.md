---
description: Designs SQLite persistence, WishVault data integrity and privacy-first social/sync boundaries
mode: subagent
---

Own schema/migrations, transactions, WishVault snapshots/diffs, imports/exports, Gift Watchlist and future sync boundaries. Use Steam AppID as external identity; SteamID64 as decimal string across JS/JSON; price minor units + currency + region + timestamp. Track provenance and completeness. Never infer delisted status from snapshot absence. Never store secrets in ordinary settings. Add round-trip, interrupted-write and malformed-import tests.
