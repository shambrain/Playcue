# PlayCue Experience Principles

## Design promise
**A friendly gaming sidekick that gets out of your way.** PlayCue should feel immediately understandable, soothing rather than sterile, playful without being childish, and fast without feeling rushed.

## 1. Calm by default
- One clear primary action per view.
- No news feed, ads, social feed, random recommendations or animated counters on the default panel.
- No attention-grabbing pulsing, flashing, forced onboarding or urgency language.
- Hide optional modules until users enable them.
- Empty states explain one useful next step; never shame a player for a backlog.

## 2. Respect agency
- Orb can be moved, resized, dimmed, paused, hidden or disabled.
- Notifications are opt-in by category; quiet hours and fullscreen suppression.
- Every suggestion has a visible reason and a dismiss/disable action.
- No automatic launch, purchase, follow, invite, friend request, save upload or cloud sharing.
- Undo/recovery for destructive archive edits and collection changes.

## 3. Reduce cognitive load
- Recognition over recall: artwork, clear labels, recent games, aliases, pinned actions and visible shortcuts.
- Search is the main interaction, not a menu maze.
- Progressive disclosure: Quick Panel first, full app for deeper tasks.
- Do not show every metadata field at once.
- Keep social context separated from private library/search by default.

## 4. Make state legible
Every important state has a label, not only a color:
- Steam: Connected / Not running / Not found / Needs attention.
- Launch: Request sent / Process observed / Exited / Unknown.
- WishVault: Present / Not seen in later snapshot / Unavailable (verified) / Unknown.
- Social: Shared / Private / Stale / Unknown.
Do not present unknown as failed, offline, deleted or delisted.

## 5. Be friendly, not manipulative
- Voice: warm, concise, peer-like, never patronizing.
- Examples: “Ready when you are.” “Pick up where you left off?” “Want to find something for tonight?”
- Avoid: “You are falling behind,” “Your streak is broken,” “Your friends are waiting,” countdown pressure, shame or false urgency.
- Do not gamify app usage, daily opens, streaks or time spent in PlayCue.
- User may disable all coaching/suggestions.

## 6. Playfulness with restraint
- Character comes from the Orb, subtle transitions, expressive but sparse iconography and tasteful game artwork.
- No mascot that blocks content or demands attention.
- Micro-interactions should confirm intent (launch accepted, item saved, snapshot created), not decorate every click.
- Use reduced-motion aware transitions and no continuous animation in idle state.

## 7. Predictable and forgiving
- Consistent placement and naming across panel/full app.
- Esc closes temporary surfaces; clicking outside behavior is consistent and never loses unsaved input.
- Confirm only consequential/destructive actions. Prefer undo for reversible actions.
- Preserve filters, search context and scroll position when navigating back.

## 8. Fast and low effort
- Orb click or shortcut -> focused search.
- Enter launches selected installed game.
- Arrow keys navigate, Tab reaches secondary actions, Esc closes.
- Game search works offline and does not wait for Steam Web API.
- Show skeleton/placeholders rather than freezing the surface.
- Cache local artwork carefully and load large images lazily.

## 9. Privacy is a UX property
- Social hidden until enabled; status is never inferred from silence.
- Wishlist capture is visible and user-triggered.
- Online sync is off by default, with clear categories and participants.
- Never ask for Steam credentials, Steam Guard codes, cookies or session tokens.

## 10. Validate outcomes, not taste
Measure launch time, search success, task completion, false-launch confusion, notification dismissals, accidental panel openings and user trust. "Looks premium" is not a substitute for testing.
