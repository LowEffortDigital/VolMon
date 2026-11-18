# VolMon v2.1.0 for macOS (Build 23)

## What's New in v2.1.0
- **Interactive Top 50 Non-Overlapping Folder Ring Gauge & Concentric Sunburst**: Added `FolderRingGaugeView` with three interactive ring modes (`Sunburst (Parent + Top 50)`, `Single Ring (Top 50 Exclusive)`, and `Parent Roots Only`), strictly partitioning parent vs. top-50 sub-folder footprints so slice percentages never double-count parent and child directories.
- **Accurate POSIX FTS Physical Block Footprints**: Upgraded `VolumeScannerEngine` to compute true on-disk physical block usage via low-overhead POSIX `fts` traversal with inode/clone deduplication and zero Spotlight overcounting.
- **APFS Purgeable Space Telemetry & Boot-First Progressive Scan**: Prioritizes your active boot volume first for sub-second initial insights, surfaces live APFS purgeable capacity alongside physical used and free space, and continues scanning secondary/external volumes non-blockingly in the background.
- **Unified Per-Page Volume Switcher, Tactile `LowEffortButtonStyle` & Multi-Monitor Widgets**: Switch active volumes across every action page with already-offloaded folder guards, high-affordance tactile controls, and active-screen multi-display desktop HUD placement.
