# Changelog

All notable changes to the Codey project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [3.5.1] - 2026-06-18

### Added
- Integrated self-update CLI logic pointing directly to the unified `Codey-Community` release hub.
- Added platform-specific CLI bundles supporting Apple Silicon, Intel macOS, x86_64 Windows, and glibc/musl Linux targets.
- Created beautiful unified `install` script supporting TTY progress indicators, architecture auto-detection, and local binary installations.

### Changed
- Rebranded and updated all repository distribution paths and package names from legacy references to `Codey-Community` and the CLI binary name `codey`.
- Streamlined configuration path locations: remote/custom skills now load correctly from `~/.codey/skills/`.

### Fixed
- Fixed release publishing pipelines in Tauri and main workflows to ensure seamless asset distribution (`latest.json` configurations).

---

## [3.5.0] - 2026-06-01

### Added
- First public distribution release of Codey CLI and Desktop App versions.
- Initial release of Model Context Protocol (MCP) tool integration.
- Custom prompts and agent templates configuration.

[Unreleased]: https://github.com/fares-moustafa/Codey-Community/compare/v3.5.1...HEAD
[3.5.1]: https://github.com/fares-moustafa/Codey-Community/releases/tag/v3.5.1
[3.5.0]: https://github.com/fares-moustafa/Codey-Community/releases/tag/v3.5.0
