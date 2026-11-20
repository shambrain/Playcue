---
name: Steam Integration
description: Use for Steam launch, Steamworks/Web API, friend, ownership, recent-played and browser integration.
---

Read docs/STEAM_INTEGRATION.md. Verify exact methods in Valve docs: ISteamApps, ISteamFriends, IPlayerService, ISteamUser. Classify official API vs local file vs unsupported behavior. Validate AppID and use standard Steam URL handoff. Distinguish launch handoff from process success. Respect profile privacy; GetFriendList can return 401 for private lists. No passwords/cookies/private scraping/client patching/keys in client. Add failure tests.
