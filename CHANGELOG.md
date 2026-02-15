# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.0.3](https://github.com/YazanAmmar/SyncEveryThing/releases/tag/1.0.3) - 2025-08-22

### Added
- Performance control modes (`--ultra-speed`, `--minimum-speed`) to manage process priority.

### Changed
- Implemented semaphore-based concurrency throttling to prevent I/O saturation on slower systems.

## [v1.0.2](https://github.com/YazanAmmar/SyncEveryThing/releases/tag/1.0.2) - 2025-08-22

### Added
- Size-based conditional hashing using `--sha256-min` and `--sha256-max` flags.

### Changed
- The `--sha256` flag now applies to all files by default unless a size range is explicitly specified.

## [v1.0.1](https://github.com/YazanAmmar/SyncEveryThing/releases/tag/1.0.1) - 2025-08-21

### Fixed
- Critical logic bug where variable shadowing caused incorrect file size comparisons.
- Crash when adding the tool to Windows PATH if the registry value was missing.

### Maintenance
- Added `<cstdint>` include for improved cross-compiler compatibility.

## [v1.0.0](https://github.com/YazanAmmar/SyncEveryThing/releases/tag/1.0.0) - 2025-08-21

### Added
- Initial public release.
- Core synchronization logic for directories (`--dir`) and single files (`--file`).
- FNV64 fingerprinting for fast content comparison.
- Windows-only SHA-256 support via CNG.
- Essential utilities: `--dry-run`, `--delete` (mirror mode), `--ignore`, and colored output.
