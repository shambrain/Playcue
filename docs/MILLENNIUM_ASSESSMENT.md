# SteamBrew / Millennium Assessment

**Decision: do not make Millennium a PlayCue dependency.** Consider a narrow, separately maintained optional integration only if users demand a Steam-client entry point.

## What it is
SteamBrew is the community/documentation ecosystem. Millennium is an open-source Windows/Linux modding framework for Steam desktop-client themes and plugins; it is not Valve or Steamworks.

## Possible benefit
A plugin could add a Steam-client-specific action such as “Save this game to PlayCue” or an entry point to open PlayCue for the current AppID. It does not improve the external Orb, launch workflow, WishVault DB, local discovery or fullscreen detection.

## Constraints discovered
- The framework is unofficial and Steam client updates can change its compatibility.
- Plugin updates require an update PR and successful merge into its plugin database; code is reviewed/tested and review timing is not guaranteed.
- Published submission rules say a plugin must not be primarily AI-generated; AI assistance must be disclosed. This is a significant constraint for an OpenCode-heavy implementation.
- Plugins must provide Steam-client-specific functionality and look native using Steam components where available. A generic web-page button belongs in a browser extension instead.
- Millennium repository LICENSE.md is MIT: it permits use/modification/distribution/sale of covered code subject to keeping the copyright and permission notice. That does not imply Valve endorsement or resolve Steam trademark/terms issues.
- No reviewed source establishes a built-in Millennium plugin payment/marketplace revenue system. Do not assume plugin-directory monetization.

Sources:
https://docs.steambrew.app/users/index
https://docs.steambrew.app/developers/submitting-plugins
https://github.com/SteamClientHomebrew/Millennium
https://github.com/SteamClientHomebrew/Millennium/blob/main/LICENSE.md

## Recommendation
Build and sell/distribute PlayCue independently. Do not bundle the patcher or copy Millennium code in core. If an optional plugin is later pursued, keep it in a separate package/repository, identify a human maintainer who can support it, disclose AI assistance as policy requires, and treat review/Steam-update compatibility as external risks. Do not use Millennium for Orb, local VDF parsing, launch handoff, WishVault or friend scraping.
