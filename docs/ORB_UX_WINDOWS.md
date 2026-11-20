# PlayCue Orb and Windows UX

## Default
Persistent, small desktop Orb near a chosen edge. User may move it, edge-snap it, change size/opacity or disable it. It hides during detected fullscreen games. Tray and global shortcut remain alternative entry points.

## Interaction
Click: open Quick Panel. Drag: move and snap. Shortcut: toggle panel and focus search. Escape: close panel. Right-click: settings, pause, disable, open full app, exit. Double-click is configurable; default should not surprise-launch a game.

## Visual
Premium gaming accessory, restrained glass/metal treatment, crisp vector glyph, subtle idle animation, configurable accent, reduced-motion and high-contrast options. Avoid heavy bloom/particles and unnecessary animation.

## Native behavior
Use a dedicated transparent, frameless Tauri window and current v2 APIs. Test real Windows compositor behavior. Handle z-order, focus, taskbar presence, monitor work area, mixed DPI, unplug/reconnect, display sleep/resume and single-instance lifecycle. Never rely on browser preview alone.

## Fullscreen suppression
Prefer event-driven foreground/window notifications with throttled verification. Detect probable fullscreen/borderless fullscreen from foreground window/monitor bounds; ignore PlayCue windows; avoid hiding for an ordinary maximized app unless configured. Do not use a tight polling loop. If detection is uncertain, expose a user control and document limitations.

## Performance/acceptance
Measure idle CPU/RAM on a named reference PC. No busy loop. Test 100–200% scaling, multi-monitor mixed DPI, taskbar on different edges, hotkey conflict, focus restore, fullscreen game start/exit, monitor removal and auto-hide off. Orb must never intercept game input.
