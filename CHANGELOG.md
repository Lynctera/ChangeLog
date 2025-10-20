# Changelog

All notable changes to this project will be documented in this file.

This project follows the [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) format and [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- GitHub mirror configured at [github.com/mike-ybl/Lynctera](https://github.com/mike-ybl/Lynctera).
- Email Listener V2: Introduced action system scaffolding (entities, repositories, EF configuration) and migration `2025-10-14_add_action_system.sql`.

### Changed
- Email Listener V2 AI: Updated classification agent, category service, and priority scoring models/configuration.
- Ops: Tuned WAF rate-limit script in `increase-waf-rate-limits.sh`.
- Observability: Refined `monitoring-queries/429-analysis.kql`.
- Docs: Updated AI framework architecture, deployment verification, request telemetry fix, and function config comparison docs.

## [0.1.0] - 2025-10-20

### Added
- Initial public changelog scaffold.

[Unreleased]: https://github.com/mike-ybl/Lynctera/compare/v0.1.0...HEAD
[0.1.0]: https://github.com/mike-ybl/Lynctera/releases/tag/v0.1.0
