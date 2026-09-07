# Changelog

All notable changes to the standalone Omnix Tauri application are documented
in this file.

## [Unreleased]

### Added

- Created the standalone `shingoku2/Omnix-Tauri` repository while preserving
  the Tauri directory's project history.
- Added root-level GitHub Actions CI for Rust formatting/checks, frontend lint
  and builds, and a full Tauri build.
- Added npm, Cargo, and GitHub Actions Dependabot configuration.
- Added standalone contributor guidance and the MIT license.

### Fixed

- Updated React state initialization to satisfy current React hooks lint rules
  without disabling the checks.
- Formatted inherited Rust sources and made `cargo fmt --check` a CI gate.
- Updated npm and Cargo lockfiles to patched compatible dependency versions.

## Historical changes

Earlier Tauri changes retain their original filtered Git history from
`Omnix-All-knowing-gaming-companion`.
