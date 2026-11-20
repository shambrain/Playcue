# PlayCue Screen and Component Specifications

## 1. Orb
Purpose: always-available access without dominating the desktop.
An unobtrusive 44–48px default icon, edge snapped and user movable. Static at rest; hover/focus may reveal a label. One click opens Quick Panel. It hides during true fullscreen games by default. No notification badge for non-actionable events. Context menu includes pause/disable/settings/exit.

## 2. Quick Panel
Purpose: launch in seconds.
- Top: search field, app status and settings.
- “Continue” card: last PlayCue-observed game, launch action and last session note if any.
- Recent row/list: maximum 3–5 entries, clear timestamps, favorites/pin.
- Up Next: optional short queue.
- Bottom shortcuts: Library, WishVault, Gift Watchlist; Friends only when enabled.
No infinite feed, community activity or store news.

## 3. Home
Purpose: gentle orientation, not a dashboard wall.
- “Good to see you”/“Ready when you are” style greeting optional and dismissible.
- Continue, Currently Playing, Up Next.
- A small personal recap: sessions captured this week only if the user opts in.
- Quick actions: search, save wishlist snapshot, add note.
No daily engagement score or streak.

## 4. Library
- Local detected games, status and last observed session.
- Filters for installed, favorites, hidden, collection and platform.
- Dense list and visual grid options.
- Search is persistent. Sort options obvious.
- Bulk actions are reversible where possible.
Steam remains source of truth for installation/update/purchase state; PlayCue's local scan may be stale and must show scan time.

## 5. WishVault
- Snapshot timeline with capture source, timestamp, region and completeness.
- Diff view: added, no longer seen, changed metadata; “not seen” is neutral, not “delisted.”
- Manual add/import, merge preview, export.
- Price history only with trustworthy observations and region/currency/time labels.
- No alarmist red alerts for missing items.

## 6. Gift Watchlist
- Game, private recipient nickname (optional), note, target price/region and reminder.
- Private by default, not synced unless explicitly included.
- No automatic gift purchase or friend messaging.

## 7. Friends / SquadPulse (opt-in)
- Default view is compact, user-curated friends.
- Status freshness timestamp; stale/private/unknown states explicit.
- Hide individual/all status; pause social module.
- Spoilers concealed by default.
- Game Night matcher shows the source and overlap of voluntarily shared lists.
- No friend activity in Quick Panel unless the user opts in.

## 8. Launch Doctor
- Timeline of launch stages and detected processes.
- Distinguish OS handoff from game process observed.
- Show relevant logs with redaction preview.
- Suggestions reversible, user-approved and linked to evidence.
- No auto-repair of Steam, game or publisher launcher.

## 9. Settings
Grouped: Appearance, Orb & Shortcuts, Notifications & Quiet Hours, Steam & Libraries, Privacy & Social, Data & WishVault, Accessibility, Advanced/Diagnostics.
Use plain labels, setting descriptions, immediate preview for visual settings and Reset to defaults. Do not bury Orb disable/autostart controls.

## 10. Responsive/window modes
- Quick panel: constrained to available monitor work area, no off-screen spawn.
- Full app: resizable; minimum size respects usable layout.
- Compact mode retains labels for primary controls.
- Remember per-monitor location carefully; recover if monitor removed.
