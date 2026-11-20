# PlayCue UX Research — 2026 Snapshot

**Research date:** 2026-11-21  
**Purpose:** Ground PlayCue's experience in current Steam capabilities, current player complaints and established human-computer interaction evidence.  
**Important:** Community posts indicate reported pain points, not prevalence across all Steam users. They are qualitative signals, not market-size estimates.

## 1. What Steam already does well (do not rebuild it)
Valve's Library documentation describes:
- Home shelves for updates, recently played games, friends' activity and custom collections.
- Game detail pages with developer/community material, post-game summaries, achievements/screenshots/trading cards, friends who play and friends' posts.
- Dynamic collections and custom shelves.
- Wishlist categories, improved search/autocomplete, sharing, demo indicators and demo-release notifications are documented in Steam's newer wishlist updates.
- Steam's Nov 11, 2026 news says Achievement Sets are generally available, with independent DLC/achievement sets and comparison with up to three friends.

Implication: PlayCue must not position itself as a replacement library, friend feed, achievement manager or wishlist category manager. The differentiated experience is a fast desktop entry point, a quiet personal command surface, durable personal context and carefully controlled optional social features.

Sources:
- https://store.steampowered.com/libraryupdate/
- https://store.steampowered.com/news/posts/?enddate=1788390000
- https://steamcommunity.com/app/593110/allnews

## 2. 2026 pain-point signals

### A. Social UI should respect user intent
A Jan 5, 2026 Steam Client Beta feature request reports library friend indicators still appearing when a user is Offline/Invisible, with no switch to suppress the visual indicators. The author describes duplicated activity and persistent visual noise and requests a control.
PlayCue response: no unsolicited social presence in the main Quick Panel. SquadPulse is opt-in, independently hideable, and never treats inaccessible presence as offline.

Source: https://steamcommunity.com/groups/SteamClientBeta/discussions/3/688619956215133813/

### B. Spoiler control
A Steam Suggestions thread from Sep 2025, with replies in May 2026, describes friends' achievement activity exposing spoilers in game detail pages and asks for the ability to hide that activity.
PlayCue response: friend activity summaries must be spoiler-safe by default. Do not surface achievement names, story screenshots, game posts or activity details without per-game/per-feature permission and an explicit reveal action.

Source: https://steamcommunity.com/discussions/forum/10/601914519534635657/

### C. Steam Deck virtual keyboard friction
r/SteamDeck posts in Apr and Oct 2026 describe keyboard overlays obscuring content, awkward resizing/positioning, delayed appearance, failed focus, missed/duplicated keystrokes and inconsistent behavior. These reports are not all reproducible defects, but demonstrate the cost of forcing text entry into frequent flows.
PlayCue response: controller-first Deck Mode later; reduce typing using recent queries, tags, pinned actions, controller focus and visible focus rings. Do not claim to fix SteamOS keyboard defects.

Sources:
- https://www.reddit.com/r/SteamDeck/comments/1ss1dgy/my_biggest_complaint/
- https://www.reddit.com/r/SteamDeck/comments/1x3aaab/issues_with_the_onscreen_keyboard/

### D. Gaming identity and backlogs
PC Gamer's Jan 9, 2026 editorial requests a currently-playing section and better context such as playtime/progress, noting that a recent shelf does not feel like a personal command center. The article also raises wishlist price history and improved organization. These are editorial opinions, not representative surveys.
Steam has since added wishlist categories and better search, so PlayCue should provide personal intent and context rather than another category feature.
Source: https://www.pcgamer.com/software/platforms/9-big-things-steam-needs-to-improve-in-2026/

### E. Notification fatigue
A 2026 peer-reviewed study on instant messaging notifications reports that controllability and non-mandatory interaction affect cognitive load/time perception; it recommends transient, auto-dismissing and non-mandatory notification patterns. A June 2026 Computers in Human Behavior paper reports transient processing slowdown after social notifications. These studies are not tests of PlayCue, but support restraint and user control.
Sources:
- https://doi.org/10.1080/10447318.2026.2700022
- https://doi.org/10.1016/j.chb.2026.108926

## 3. Human-computer interaction principles
Use Nielsen Norman Group heuristics: system status visibility, real-world language, user control/freedom, consistency, error prevention, recognition rather than recall, expert efficiency, minimalist presentation and understandable recovery.
Source: https://www.nngroup.com/articles/ten-usability-heuristics/

Windows inclusive design guidance updated Sep 14, 2026 calls for logical structure/order, high contrast, system fonts, DPI scaling, sufficient contrast, and not using color alone.
Source: https://learn.microsoft.com/en-us/windows/apps/design/accessibility/designing-inclusive-software

WCAG 2.2 covers focus not obscured, focus appearance, target size and input modalities.
Source: https://www.w3.org/TR/WCAG22/

## 4. Product opportunity
PlayCue should make the *frequent action* effortless:
1. Summon Orb/Quick Panel.
2. Type or recognize the game.
3. Launch using the normal Steam handoff.
4. Understand whether Steam received the request or the game process was actually observed.
5. Return to the user's own next-up queue or session note.

Its *ambient experience* should be quiet: no feed by default, no pressure, no streaks, no engagement traps, and no surprise overlays.

## 5. Claims we must not make
- Do not say Steam lacks Recent, collections, friend activity, achievements or wishlist categories.
- Do not say every reported Reddit issue affects all players.
- Do not claim PlayCue can change Steam client UI or fix Steam Deck OS behavior.
- Do not claim notification research proves one exact animation timing or one theme is psychologically optimal.
- Validate PlayCue through usability tests with real players, including disabled users and different display/input setups.
