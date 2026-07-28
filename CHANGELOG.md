# Changelog

Semua perubahan penting proyek ini dicatat di sini.
Format mengacu pada [Keep a Changelog](https://keepachangelog.com/id/1.1.0/),
dan proyek ini memakai [Semantic Versioning](https://semver.org/lang/id/).

## [Unreleased]

## [0.2.0] - 2026-07-28
### Added
- **Learning loop** di `HitomiClaude.md`: Principle 1 kini mencari transkrip sesi lama (`~/.claude/projects/<slug>/*.jsonl`) saat memori senyap sebelum menebak; Principle 5 jadi learning loop penuh — pola/workflow matang yang berulang dinaikkan jadi *skill* reusable.
- `docs/HitomiClaude - Master State.md` sebagai SSOT proyek.
- `CHANGELOG.md` (berkas ini).

### Changed
- README: URL install `curl` diperbaiki ke `moncrath/Hitomi_Claude` (sebelumnya placeholder `<your-username>`).
- README: tabel fitur, daftar 7 Operating Principles, dan section *The Memory System* diperbarui mencerminkan learning loop.

## [0.1.0] - 2026-07-27
### Added
- Rilis awal `HitomiClaude.md` — persona Hitomi + operating-system (hard rules, 7 Operating Principles, engineering core).
- README + banner (`assets/banner.png`).
- `installed-skills-manifest.txt` — catatan 199 skill vendor yang di-bulk-install.

[Unreleased]: https://github.com/moncrath/Hitomi_Claude/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/moncrath/Hitomi_Claude/releases/tag/v0.2.0
[0.1.0]: https://github.com/moncrath/Hitomi_Claude/releases/tag/v0.1.0
