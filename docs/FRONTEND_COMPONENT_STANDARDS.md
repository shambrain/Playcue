# PlayCue Frontend Component Standards

## Core components
AppShell, OrbWindow, QuickPanel, CommandSearch, GameResult, GameArtwork, GameStatus, RecentGameRow, ContinueCard, UpNextList, WishSnapshotTimeline, SnapshotDiff, GiftItemCard, EmptyState, ErrorRecovery, StatusBadge, Toast, SettingsGroup, FocusRing.

## Rules
- Components have explicit loading/empty/error/disabled/focus states.
- Use shared design tokens; no inline one-off colors/sizing for product components.
- Avoid nested card stacks and dashboard clutter.
- Use semantic buttons/inputs; icon-only controls require accessible names.
- Never use color alone for installed/playing/private/unknown.
- Keep game artwork decorative; title remains selectable/readable text.
- Lists virtualize only when needed; avoid complex virtualization for short recents.
- Search results stable across metadata updates and support keyboard navigation.
- Avoid layout shift when artwork loads; reserve dimensions.
- Do not animate list reorder or status changes unless useful and reduced-motion aware.
- Toasts do not cover search, primary action or keyboard focus.
- All UI strings live in a localization-ready resource layer.
