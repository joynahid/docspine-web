---
title: "Changelog"
description: "Release notes and version history for Nexus"
---

# Changelog

All notable changes to Nexus are documented here.

## [2.4.1] - 2024-01-15

### Fixed

- Fixed path resolution on Windows with spaces in directory names
- Corrected sourcemap generation for minified builds
- Resolved hot reload failing after multiple file saves

## [2.4.0] - 2024-01-08

### Added

- New `nexus deploy --preview` for preview deployments
- Support for Cloudflare Pages deployment
- Bundle analyzer with `--analyze` flag
- Workspace filtering with `--filter` option

### Changed

- Improved build performance by 40%
- Better error messages for configuration issues
- Updated default Node.js target to 18

### Fixed

- Memory leak in watch mode
- Incorrect exit codes on build failure

## [2.3.0] - 2023-12-15

### Added

- Monorepo support with workspaces
- Custom scripts in `nexus.config.js`
- Shell completion for Fish

### Changed

- Migrated to Rust for core CLI (3x faster)
- Simplified configuration format

### Deprecated

- `nexus.json` config format (use `nexus.config.js`)

## [2.2.0] - 2023-11-20

### Added

- TypeScript support out of the box
- `nexus add` and `nexus remove` commands
- Environment-specific `.env` files

### Fixed

- HMR not triggering for CSS changes
- Incorrect dependency resolution in monorepos

## [2.1.0] - 2023-10-30

### Added

- `nexus test` command with Vitest integration
- Coverage reporting with `--coverage`
- Test UI with `--ui`

### Changed

- Faster dev server startup
- Reduced memory usage in watch mode

## [2.0.0] - 2023-10-01

### Breaking Changes

- Minimum Node.js version is now 18
- Config file renamed from `.nexusrc` to `nexus.config.js`
- `nexus start` renamed to `nexus dev`

### Added

- Complete rewrite with improved architecture
- Plugin system for extensibility
- Multi-platform deployment support

### Removed

- Legacy `nexus serve` command
- Support for Node.js 14 and 16

## [1.x] - Legacy

For changes prior to version 2.0, see the [legacy changelog](https://github.com/nexus-cli/nexus/blob/v1/CHANGELOG.md).

---

## Versioning

Nexus follows [Semantic Versioning](https://semver.org/):

- **Major** (X.0.0) — Breaking changes
- **Minor** (0.X.0) — New features, backwards compatible
- **Patch** (0.0.X) — Bug fixes, backwards compatible

## Release Schedule

- **Patch releases** — As needed for bug fixes
- **Minor releases** — Monthly
- **Major releases** — Annually (with migration guides)

## Upgrade Guides

- [Upgrading from 1.x to 2.x](https://github.com/nexus-cli/nexus/blob/main/docs/migration-v2.md)

