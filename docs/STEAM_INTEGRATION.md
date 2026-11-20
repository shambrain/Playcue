# Steam Integration Contract

## Source classes
- Steam URL launch handoff: standard client scheme; test handler availability.
- Local library VDF/ACF: read-only best-effort compatibility data, not a stable published Web API.
- Steamworks SDK client interfaces: official but context-bound; not automatically callable from a standalone Tauri utility.
- Steam Web API: official but key/privacy constrained.
- Wishlist page capture: later user-initiated browser feature; DOM may change.
- Millennium: unofficial mod framework, optional only.

## Launch
Validate numeric AppID from local catalog. Open the standard Steam launch URI (commonly steam://run/<appid>) with a safe OS URL-opening API. Never build a shell command from user-controlled values. Test Steam running/not running, missing URI handler, stale AppID, disconnected library and third-party publisher launcher. URI dispatch is not proof of game startup.

Official reference: https://partner.steamgames.com/doc/api/ISteamApps

## Local discovery
Read Steam install/library config and appmanifest_<appid>.acf. Support multiple libraries/drives and malformed VDF/ACF. Do not write files, assume order, infer ownership or trust stale manifests. Use fixtures from more than one real client install.

## Official Web API limits
IPlayerService GetRecentlyPlayedGames and GetOwnedGames require Web API key and SteamID; results depend on visible profile/game details. ISteamUser GetFriendList requires key and SteamID; Valve documents HTTP 401 for private friend lists. Publisher-key methods explicitly requiring a secure server must never be called from the desktop binary. Steam OpenID authenticates identity, not private-data authorization.

Sources:
- https://partner.steamgames.com/doc/webapi/iplayerservice
- https://partner.steamgames.com/doc/webapi/isteamuser

## Steamworks Friends
ISteamFriends GetFriendPersonaState/GetFriendGamePlayed are Steamworks client API functions. A standalone Tauri application is not automatically a Steamworks game/client context. Do not assume they expose the user's entire friends list externally.

Reference: https://partner.steamgames.com/doc/api/ISteamFriends

## Wishlist
No stable public wishlist API was confirmed in this research. MVP manual entry/import/snapshot. A future extension can read visible wishlist content only on explicit user action, with narrow permissions and no cookie/session access. Distinguish missing-from-snapshot from confirmed delisting.

## Hard prohibitions
No password/session cookie/Steam Guard access; no private endpoint scraping; no client patching/injection/memory reads; no privacy/DRM/anti-cheat bypass; no automatic changes to game launch settings.
