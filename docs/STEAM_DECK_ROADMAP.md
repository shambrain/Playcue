# Steam Deck and Linux Roadmap

Steam Deck/Linux is a roadmap target, not a current compatibility claim.

## Why later
Windows-first implementation must first stabilize Win32 Orb behavior, Steam detection, process observation, global shortcuts, tray and packaging. Linux/SteamOS has different compositor, desktop-session, paths, Flatpak permissions and controller UX.

## Deck Mode
Do not shrink the floating mouse-first Orb. Build a fullscreen controller-first view with clear focus, large buttons, D-pad/analog/touch support, minimal text entry, recent/favorites/WishVault access, offline and suspend/resume handling.

## Packaging
Investigate Flatpak for SteamOS Desktop Mode and required portals/permissions. Valve's current Deck desktop FAQ describes Discover/Flatpak and cautions about system modifications outside it. Do not modify SteamOS read-only system files or require random pacman scripts.

## Integration
Desktop Mode app first. User may optionally add it as a Non-Steam game. Do not claim Gaming Mode overlay/Quick Access integration without a documented supportable mechanism. Decky is a separate optional research item.

## Tests
Physical Deck LCD/OLED if available; stable SteamOS; Desktop and Gaming Mode separate; gamepad/touch/keyboard/on-screen keyboard; Flatpak install/update/uninstall; suspend/resume; SD library; external display; offline behavior. No automatic shader cache/Proton prefix/save deletion.
