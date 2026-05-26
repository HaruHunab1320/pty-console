# Changelog

All notable changes to `pty-console` will be documented in this file.

## [0.3.2] - 2026-05-26

### Changed
- Repository extracted from the parallax monorepo into its own standalone repo at `github.com/HaruHunab1320/pty-console`. Package metadata (`repository`, `homepage`) updated accordingly. No source code changes.

## [0.3.1] - 2026-02-25

### Added
- CHANGELOG.md

## [0.3.0] - 2026-02-25

### Added
- `tool_running` event forwarding — `PTYConsoleBridge` now listens for `tool_running` from the manager and emits it as a `SessionStatusEvent` with `kind: 'tool_running'` and `toolInfo`
- `toolInfo?: ToolRunningInfo` field on `SessionStatusEvent`

## [0.2.0] - 2026-02-25

### Added
- `PTYManagerAsyncLike` interface for async manager support (e.g. `BunCompatiblePTYManager`)
- `PTYConsoleBridge` now accepts both `PTYManagerLike` (sync) and `PTYManagerAsyncLike` (async) managers
- `writeRaw()` method on `PTYConsoleBridge`
- `PTYManagerAsyncLike` export from package index
