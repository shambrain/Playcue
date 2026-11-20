# Research Sources

Research snapshot: 2026-11-20. Re-check before implementation because APIs and policies change.

## Valve / Steam
- Steamworks ISteamApps: https://partner.steamgames.com/doc/api/ISteamApps — launch URI behavior and app interface.
- Steamworks ISteamFriends: https://partner.steamgames.com/doc/api/ISteamFriends — client-context friend state functions.
- IPlayerService: https://partner.steamgames.com/doc/webapi/iplayerservice — recent games and owned games; API key, SteamID and visibility requirements.
- ISteamUser: https://partner.steamgames.com/doc/webapi/isteamuser — GetFriendList and private-list HTTP 401.
- Steam Deck Desktop FAQ: https://help.steampowered.com/en/faqs/view/671A-4453-E8D2-323C — Discover/Flatpak and cautions around system changes.
- Steam Deck troubleshooting: https://help.steampowered.com/en/faqs/view/69E3-14AF-9764-4C28

## SteamBrew / Millennium
- Overview: https://docs.steambrew.app/users/index
- Plugin submission policy: https://docs.steambrew.app/developers/submitting-plugins
- Repository/license: https://github.com/SteamClientHomebrew/Millennium
- MIT license: https://github.com/SteamClientHomebrew/Millennium/blob/main/LICENSE.md

## Tauri / OpenCode
- Global shortcut: https://v2.tauri.app/plugin/global-shortcut/
- Autostart: https://v2.tauri.app/plugin/autostart/
- Single instance: https://v2.tauri.app/plugin/single-instance/
- Window state: https://v2.tauri.app/plugin/window-state/
- Window API: https://v2.tauri.app/reference/javascript/api/namespacewindow/
- OpenCode agents: https://opencode.ai/docs/agents/
- OpenCode skills: https://opencode.ai/docs/skills/

## Alternatives
- Playnite: https://playnite.link/
- Augmented Steam: https://augmentedsteam.com/
- SteamBrew: https://steambrew.app/

## Interpretation
Official docs are the contract. Community posts are pain-point evidence only. Local VDF/ACF are compatibility formats, not stable official APIs. No source reviewed confirmed a stable public Steam wishlist API or a Millennium plugin payment system. Steam OpenID is identity, not private-data authorization.
