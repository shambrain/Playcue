# PlayCue Visual Design System

Status: proposed design baseline for the first high-fidelity prototype. Validate with users and contrast tooling before shipping.

## Visual character
A modern, calm gaming accessory: warm-dark surfaces, restrained indigo/ice-blue accent, soft teal success, clear typography and generous spacing. It must not look like a neon RGB dashboard, a clone of Steam, or a mobile app stretched to desktop.

## Themes
- Dark (default): ink/navy surfaces and soft near-white text.
- Light: warm near-white surface, deep slate text, restrained blue actions.
- Windows High Contrast: respect OS/system colors; do not force custom colors.
- Accent presets: Indigo (default), Teal, Amber; accent is decorative and never the only state signal.

## Initial token proposal
Dark:
- app background #111722
- surface #192231
- elevated surface #202B3C
- primary text #F5F7FC
- secondary text #B9C3D4
- accent #AFC2FF
- success #A9E8D0
Light:
- app background #F6F7FB
- primary text #1B2230
- secondary text #536174
- primary action #405FC5

Calculated contrast for the proposed pairs: #F5F7FC on #111722 ≈16.75:1; #B9C3D4 on #111722 ≈10.11:1; #1B2230 on #F6F7FB ≈14.88:1; #536174 on #F6F7FB ≈5.89:1; #405FC5 on #F6F7FB ≈5.36:1. Recalculate after opacity, overlays, gradients and actual font weights/sizes. Do not place body text on uncontrolled artwork.

## Typography
- Prefer native/system UI font stack (Segoe UI Variable where available; system fallback) for readable Windows rendering.
- Avoid thin weights for body text and small metadata.
- Body text should remain comfortably readable; secondary metadata must not become tiny.
- Use tabular numerals for playtime, dates, counts and price.
- Support Windows text scaling and high DPI without clipping.

## Spacing and shape
- 4px spacing base; use consistent 8/12/16/24/32px rhythm.
- Cards use modest radius (10–14px), not pills everywhere.
- Maintain clear visual grouping and generous whitespace.
- Avoid nested cards inside cards; avoid decorative dividers for every row.
- Icons always have labels or accessible names when not obvious.

## Imagery
- Use Steam AppID/game metadata artwork only when available and permitted by source/terms.
- Preserve aspect ratios; use predictable capsule/header crops.
- Add neutral fallback artwork with game initial/icon and title.
- Avoid screenshots or artwork as the only way to identify a game.
- Use lazy loading and size limits; don't load the full library's art at once.

## Orb
- Default visual diameter target: 44–48 logical px, user adjustable (suggested 36–64).
- Circular, recognizable PlayCue glyph; subtle material depth and restrained accent edge.
- Idle state is static. Optional low-amplitude attention hint only for user-requested events; never a permanent pulse.
- Hover/focus reveals concise label and tooltip; no hover-only essential action.
- Clear focus ring and high-contrast equivalent.
- Hit target target ≥44 logical px, even if visual glyph is smaller.
- Position respects work area/taskbar, monitor bounds and DPI.
- Opacity/compact mode adjustable; no automatic movement across displays.

## Quick Panel
- Suggested width 400–460 logical px; height 540–640, constrained to work area.
- Header: PlayCue wordmark + Steam/local status + settings affordance.
- Search row at top and receives focus when opened.
- Primary section: one “Continue”/last-played action.
- Secondary section: 3–5 recent games, horizontally compact or vertically stacked depending on width.
- Up Next/favorites visible without scrolling where possible.
- WishVault/Friends are small navigation destinations, not competing dashboards.
- Do not put a live news/community feed in this panel.
- Use text labels for primary actions; icon-only controls need accessible name and tooltip.

## Full application
- Reference desktop size 1180×760 logical px; responsive min layout 760×560.
- Navigation rail: Home, Library, WishVault, Gift Watchlist, History, Collections; Social may appear only when opted in.
- Main content width constrained for readability; search and current context preserved.
- Use detail side panel for game actions/notes rather than nested modal stacks.

## States
Every screen has loading, populated, empty, unavailable/offline, permission denied, malformed data and recovery states. State must be textual and not color-only.
