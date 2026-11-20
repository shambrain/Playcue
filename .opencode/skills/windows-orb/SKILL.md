---
name: Windows Orb and Multi-Monitor UX
description: Use for PlayCue Orb, transparent window, placement, fullscreen suppression, DPI and Windows desktop behavior.
---

Read docs/ORB_UX_WINDOWS.md. Separate Orb rendering, placement and visibility policy. Persist monitor + normalized work-area coordinates. Handle missing monitor and DPI changes. Prefer foreground/window events and throttled fallback, not a busy polling loop. Test taskbar, focus, snap, fullscreen, display sleep and mixed DPI. No game injection, input hooks or Steam patching. Document uncertain fullscreen detection.
