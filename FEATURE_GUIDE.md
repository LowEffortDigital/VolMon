# VolMon Feature Guide (v2.0.0)

**VolMon (`MacVolumeManager`)** is a native Swift 6 / AppKit / SwiftUI macOS utility for inspecting drive capacity, locating large files & folders, offloading heavy workloads to external storage, building structured backup/archive trees, and safely cleaning reclaimable caches as part of the Low Effort Suite v2.0 (`PerfMon`, `EventMon`, `VolMon`, `WebMon`).

---

## 1. Overview Dashboard
- **Mounted Volumes Grid**: Shows every mounted internal APFS volume, external Thunderbolt/USB4 SSD, and network/NAS share with segmented 5-category usage bars, free/purgeable capacity, bus speed, and S.M.A.R.T. health.
- **5 Storage Categories**:
  1. `Apps & Frameworks`
  2. `Developer & Caches`
  3. `Media & Creative`
  4. `Documents & Datasets`
  5. `Archives & Installers`
- **60-Second Rolling Waveforms**: Live index scan throughput (`MB/s`) and reclaimable/offloadable capacity (`GB`).
- **Interactive Spotlight Tables**: Sortable, resizable, and drag-to-reorder spotlight tables for top space consumers and recommended offload/archive/cleanup actions.

## 2. Large Files & Folders Explorer
- Scan any user directory via `Scan Folder…` (`NSOpenPanel`) or explore indexed volumes.
- Filter by category, access temperature (`Active Hot`, `Warm Recent`, `Cold (>90d)`, `Offload Ready`, `Reclaimable`), minimum size (`500 MB`, `5 GB`, `20 GB`), or full-text search.
- Right-click any item to queue for **External Storage Offload**, add to **Structured Backup & Archive**, stage for **Smart Cleanup**, bookmark (`★`), copy its POSIX path, or reveal in Finder.
- Inspect any selected item in the bottom 3-tab inspector (`General & Space`, `Offload / Archive / Clean`, `XML & JSON Manifest`).

## 3. Storage Flow Map & Directory Hierarchy Tree
- **3-Column Cubic Bezier Flow Map**: Connects `1. Mounted Volumes & Containers` → `2. Storage Categories & Hot Folders` → `3. Action & Destination Tiers`.
- **Directory Hierarchy Tree**: Expandable category-by-category directory tree with proportional footprint bars.

## 4. External Storage Offload Planner
- Select a target external drive or custom destination folder.
- Choose between three offload strategies:
  - **Move & Symlink Back (Transparent)**
  - **Copy & Verify Only (Mirror)**
  - **Move & Leave `.volman-stub`**
- Supports **SHA-256 checksum verification** and **Dry-Run Verification** before live execution.

## 5. Structured Backup & Archive Builder
- Choose from three deterministic archive folder hierarchy templates:
  - `VolMan_Archive/YYYY/YYYY-MM/Category/Item`
  - `VolMan_Archive/Category/YYYY-MM/SourceVolume/Item`
  - `VolMan_Archive/Snapshot_YYYY-MM-DD/Category/Item`
- Choose between **Structured Folder Hierarchy + Manifest**, **Compressed `.tar.gz` Archive Bundle**, or **ZIP Archive + SHA-256 Index**.
- Live destination tree preview and SHA-256 `archive_manifest.json` catalog.

## 6. Smart Delete & Cleanup Reclaim Suite
- Scans 6 safe cleanup rule groups (`Xcode DerivedData & Simulators`, `Package Manager Caches`, `User Application & Browser Caches`, `Orphaned .dmg & .pkg Installers`, `Old Diagnostic Logs & Crash Dumps`, `Stale Temp & Incomplete Downloads`).
- Protected by **`SystemPathGuard`**, which blocks `/`, `/System`, `/Library`, `/Applications`, `/usr`, `/bin`, `/sbin`, and `/private/var/db`.
- Supports **Move to macOS Trash (Reversible)**, **Dry-Run Simulation (Preview Only)**, and **Permanent Delete (Confirmation Required)**.

## 7. Desktop HUD Widgets, Card Gallery, Menu Bar Designer & Themes
- **4 Built-in Desktop HUDs** + **Custom Modular HUD Builder** + **Widget Gallery** (6 Card presets × 8 chart styles).
- **Menu Bar Token Designer** with customizable `VM` badge and live storage metrics.
- **9 Low Effort Studio Themes** (`Follow System` default) with live Dock icon switching (`VM`, `VO`, `LE`).
