---
name: Steam Library Discovery
description: Use for Steam root, libraryfolders.vdf, appmanifest files and installed AppID discovery.
---

Discover Steam roots robustly; parse library folders and appmanifest_<appid>.acf defensively. Handle multiple libraries/drives, Unicode, malformed/partial files, duplicate IDs, disconnected storage and concurrent Steam updates. Use fixture tests. VDF/ACF is best-effort compatibility, not stable official API. Read-only; do not mutate manifests, config or registry; do not infer ownership.
