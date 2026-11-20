# PlayCue Interaction and Microcopy Specification

## Core summon flow
1. Orb click or global shortcut opens Quick Panel.
2. Panel becomes visible without stealing focus before explicit open; search receives focus after explicit activation.
3. Search field accepts title/alias fragments; results appear locally and quickly.
4. Arrow keys move selection; Enter sends launch request; Esc closes; Ctrl+Enter may open details if consistent.
5. Show honest launch state: “Opening Steam…” then “Steam received the request” or “Game detected” only when observed.
6. On failure, preserve query and offer safe next steps.

## Orb pointer/keyboard
- Click: open/close panel.
- Drag: move; snap only on release.
- Right-click: Pause Orb, Settings, Open full app, Exit.
- Keyboard: Orb has an accessible name; users can reach it through the panel/tray and keyboard.
- Double-click is configurable, not an unexpected default launch action.
- Do not implement hidden gesture-only commands.

## Search
- Search installed game titles, user aliases, AppIDs and later WishVault records.
- Show source/status chips: Installed, Not installed, Saved, Missing locally.
- Ranking favors exact title, prefix, recent, pinned; expose predictable ordering.
- Empty result offers “Search WishVault” or “Add manually”; no forced internet query.
- Avoid fuzzy false positive launch; require selection if ambiguous.

## Recent and next-up
- Continue is explicit and based on the latest observed session, not guessed Steam history.
- Users can pin a game, mark currently playing/paused/finished, hide from recents and set next-up.
- Session Notes are optional reminders without streaks or guilt.

## Friends and privacy
- Social module is hidden/disabled until enabled.
- No friend presence dots in the default Orb.
- Per-friend hide, status pause and global quiet mode.
- Spoilers hidden by default: achievement names, story text and screenshots do not appear in Quick Panel.
- Game Night Matcher only uses lists participants intentionally share.
- Never translate unknown/private/stale into Offline.

## Notification policy
- Default notifications: security/backup error or explicit user-created reminder only; other categories disabled or quiet by default.
- Categories individually controlled: WishVault changes, friend invitations (future opt-in), sync failures, release/price events (future opt-in).
- Quiet hours, fullscreen/game session suppression and Windows Focus Assist/Do Not Disturb respect where possible.
- Toasts are non-modal, brief, non-obstructive, actionable only when needed and user-dismissable.
- No repeated messages for same event; aggregate into a digest.
- No audio/haptics unless user enables them.
- Provide “why am I seeing this?” and “turn this off” affordances.

## Friendly copy
Preferred:
- “Ready when you are.”
- “Pick up where you left off?”
- “Saved to WishVault.”
- “This game wasn’t in your latest snapshot.”
- “Steam received the launch request.”
- “We couldn't confirm the game started. View details.”
Avoid:
- “You have been away too long.”
- “Your streak is at risk.”
- “Everyone is waiting for you.”
- “Your friend is ignoring you.”
- “You missed out!”
Never imply certainty where state is unknown.

## Error recovery
Use plain language, explain impact, one safe next action and a details link. Preserve user work. Avoid raw error codes as the only message. Do not automatically change Steam configuration, Proton, game files or publisher launcher settings.
