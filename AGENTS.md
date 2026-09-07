# Agent Guidelines - Omnix Tauri

## Build and Test Commands

- Setup: `npm ci`
- Run app: `npm run tauri:dev`
- Frontend development: `npm run dev`
- Frontend checks: `npm run lint && npm run build`
- Rust format: `cargo fmt --manifest-path src-tauri/Cargo.toml --check`
- Rust check: `cargo check --manifest-path src-tauri/Cargo.toml --locked`
- Desktop build: `npm run tauri:build`

## Code Style and Architecture

- Use TypeScript for frontend code and Rust for all native/backend behavior.
- Keep UI code in `src/` and Tauri commands, persistence, and integrations in
  `src-tauri/src/`.
- Access backend behavior through typed Tauri `invoke` calls and events.
- Format Rust with `rustfmt`; follow the repository ESLint configuration for TypeScript.
- Preserve cross-platform behavior across Windows, Linux, and macOS.

## Security and Data

- Never commit secrets or local user data.
- Store application data under `~/.gaming_ai_assistant` on Unix and
  `%USERPROFILE%\.gaming_ai_assistant` on Windows.
- Validate external URLs and any identifier used in a filesystem path.
- Keep Tauri capabilities limited to permissions the application actually needs.

## Repository Boundary

This repository contains only the Rust/Tauri edition of Omnix. The Python/PyQt6 edition
is maintained at https://github.com/shingoku2/Omnix-All-knowing-gaming-companion. Do not
copy Python application code into this repository or add Tauri code to the Python repo.
