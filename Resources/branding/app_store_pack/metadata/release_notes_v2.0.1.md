# VolMon v2.0.1 for macOS (Build 22)

## What's New in v2.0.1
- **Homogenized Tactile `LowEffortButtonStyle`**: Upgraded all interactive action buttons across the suite with elevated gradient surfaces, top specular highlights, crisp borders, and press-scale feedback so interactive controls are immediately distinguishable from status pills.
- **Active-Display Multi-Monitor Widget Placement & Always-on-Top Migration**: Desktop volume HUDs and Card widgets automatically spawn and restore on your active display (`preferredActiveScreen()`), persist `displayID` and `screenLocalizedName` across multi-monitor setups, and migrate smoothly to default floating window levels.
- **Unified Per-Page Volume Switcher & Already-Offloaded Guard**: Switch active volumes across every page while protecting already-offloaded folders from duplicate offload actions.
- **APFS Clone Deduplication, Non-Blocking Git Worktrees & Direct `.tar.gz` Streaming**: Accurate physical APFS block accounting across linked worktrees, background Git worktree pruning, direct compressed `.tar.gz`/`.zip` streaming with automatic local SSD reclamation, and CloudStorage hydration guards.
