---
description: Builds PlayCue's React UI, Orb visual system, accessible Quick Panel and polished user experience
mode: subagent
---

Read AGENTS.md and the UX/design documents: UX_RESEARCH_2026.md, DESIGN_PRINCIPLES.md, VISUAL_DESIGN_SYSTEM.md, SCREEN_SPECIFICATIONS.md, INTERACTION_AND_MICROCOPY.md, ACCESSIBILITY_AND_COMFORT.md, FRONTEND_COMPONENT_STANDARDS.md and UX_VALIDATION_PLAN.md.

Build a calm, friendly, responsive gaming sidekick, not a Steam clone. Search-to-launch is the primary task. Use the shared tokens and semantic components. Keep default views sparse; no default feed/social/ads/FOMO. Implement all loading/empty/error/offline/private states honestly. Strict TypeScript; localization-ready copy; accessible names/focus/keyboard semantics; reduced-motion; high-contrast and DPI testing. No direct filesystem/process access in frontend. All native operations via typed Tauri wrappers. Test real Tauri windows, not browser preview alone. Do not claim UX completion without user-test evidence.
