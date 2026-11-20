# Accessibility and Comfort Requirements

Accessibility is a product-quality requirement, not a late polish task.

## Standards and references
- WCAG 2.2: https://www.w3.org/TR/WCAG22/
- Microsoft inclusive Windows design (updated 2026-09-14): https://learn.microsoft.com/en-us/windows/apps/design/accessibility/designing-inclusive-software
- Microsoft accessible text: https://learn.microsoft.com/en-us/windows/apps/design/accessibility/accessible-text-requirements
- Steam accessibility announcement (Big Picture/SteamOS): https://store.steampowered.com/news/posts/?enddate=1753914937

## Visual
- Target ≥4.5:1 contrast for normal text and ≥3:1 for large text under WCAG AA; aim ≥5:1 for ordinary text where practical per Microsoft's guidance. Verify actual rendered combinations.
- Never use color alone for state. Add labels/icons/patterns.
- Support light/dark and Windows High Contrast/System colors.
- Honor system font/smoothing settings; allow UI scale. Test 100%, 125%, 150%, 175%, 200% and mixed-DPI multi-monitor.
- No tiny metadata as primary information; no low-contrast disabled text for essential actions.
- Ensure focus rings remain visible and not obscured; use strong, consistent focus treatment.
- Respect reduced motion; avoid flash/strobe and persistent animation.

## Pointer/touch
- Design major targets at 40–44 logical px or larger; comply with WCAG 2.2 target-size requirements and exceptions.
- Provide spacing between adjacent destructive/launch actions.
- No essential hover-only content. Tooltips supplement labels.
- Orb's visible icon can be smaller than its accessible hit target.

## Keyboard/gamepad
- Full operation by keyboard: logical tab order, visible focus, shortcuts, escape, arrow navigation where appropriate.
- Shortcuts configurable and conflict-aware.
- Controller navigation planned for Deck Mode: obvious focus, large targets, no text-heavy required flows.
- Do not trap focus. Restore focus to the invoking control when a panel closes.
- Screen-reader semantic labels/roles and predictable announcement of launch/snapshot status.

## Cognitive and sensory comfort
- Progressive disclosure, plain language and limited visible choices.
- No auto-playing media, sound or background video.
- Reduced-motion mode; transitions can be turned off.
- Notification control, quiet hours, full-screen suppression and digest options.
- No guilt-based gamification, streaks, FOMO countdowns or manipulative scarcity.

## Validation
Run automated accessibility checks and manual keyboard/screen-reader tests. Include users with low vision, color-vision differences, motor needs and screen-reader use where feasible. Record issues and test environment. Automated WCAG checks do not replace user testing.
