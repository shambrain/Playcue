# PlayCue UX Validation Plan

Do not declare the UX “perfect” based on developer taste or a rendered mockup. Iterate with representative players.

## Research questions
1. Can a new user launch a known installed game without a tutorial?
2. Does the Orb feel useful rather than intrusive?
3. Can users understand launch-request vs game-start status?
4. Can users save and recover a wishlist snapshot without fear of losing data?
5. Do privacy, spoiler and notification controls feel understandable?
6. Can keyboard-only, high-DPI, high-contrast and screen-reader users complete core tasks?

## Formative sample
Recruit 8–12 varied PC players for first usability rounds, then repeat after changes. This is formative qualitative testing, not statistically representative research. Include large-library users, keyboard-first users, users with accessibility needs and users who dislike persistent overlays. Deck usability requires separate Steam Deck participants/device.

## Tasks
- Open Orb and search a game.
- Launch one known game.
- Recover after a missing Steam install/URI handler.
- Pin and queue a game.
- Create a WishVault snapshot and compare two snapshots.
- Explain difference between missing from snapshot and delisted.
- Add a gift item and export.
- Disable Orb and notifications.
- Find and change a privacy/spoiler setting.
- Navigate with keyboard only.

## Measures
- Task success/completion.
- Time to first successful launch request.
- Mislaunch and ambiguity rate.
- Search correction rate.
- Accidental Orb opens and dismissals.
- Error recovery completion.
- SUS or UMUX-Lite as a supplemental measure.
- Single Ease Question after tasks.
- Qualitative comfort/trust/interruption rating; ask users whether Orb presence is welcome or distracting.
- Performance: idle CPU/RAM and local search latency measured separately from subjective UX.

## Acceptance targets (initial hypotheses; validate, do not market as established facts)
- ≥90% of participants complete “open panel → search → request launch” without help after brief orientation.
- Median time from panel open to launch request ≤5 seconds for a known installed game.
- 0 destructive wishlist overwrites during test suite; partial snapshots never replace complete snapshots.
- Users can find Orb disable and notification controls without assistance.
- No critical keyboard trap, focus loss or clipped content at supported DPI scales.
- No default intrusive sound, media, social feed or repeated notification.

## Iterate
Observe silently, record friction, separate preference from usability defect, prioritize repeated/severe problems, update design and retest. Document sample, device, OS, app build, task results and known bias.
