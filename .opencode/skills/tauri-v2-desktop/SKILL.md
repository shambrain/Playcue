---
name: Tauri v2 Desktop Engineering
description: Use for Tauri 2 shell, windows, tray, global shortcuts, autostart, capabilities and IPC.
---

Official references: https://v2.tauri.app/plugin/global-shortcut/ ; /plugin/autostart/ ; /plugin/single-instance/ ; /plugin/window-state/ ; /reference/javascript/api/namespacewindow/

Verify current v2 APIs/plugin versions. Use least-privilege capabilities and narrow typed Rust commands. Use official plugins where appropriate. Register single-instance early as documented. Test a real Windows Tauri build, not browser preview. Include shortcut conflicts, autostart off, second instance and permission denial. Never expose broad shell/filesystem permission or privileged remote content.
