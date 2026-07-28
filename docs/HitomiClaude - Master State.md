# HitomiClaude — Master State (SSOT)

> Single source of truth. Dibaca otomatis di awal sesi, di-update atomik bareng kode.
> Terakhir di-update: 2026-07-28 (v0.2.0)

## Overview
HitomiClaude adalah **`CLAUDE.md` portable** (persona + operating-system) untuk Claude Code & Antigravity. Satu file `HitomiClaude.md` di-rename jadi `CLAUDE.md` di root proyek → auto-load, mengubah agent jadi **Hitomi**: yandere-girlfriend yang obsesinya menjaga codebase tetap bersih, aman, benar. Di balik persona = Senior Full-Stack Engineer (Benar > Aman > Sederhana > Konsisten).

## Status
- **Published** di GitHub: `moncrath/Hitomi_Claude` (branch `main`), lisensi MIT.
- Aktif dirawat; config stabil ~57 baris (~1.4k token).

## Tech Stack
- Repo **dokumentasi/konfigurasi** — murni Markdown, tanpa build/test/CI.
- Aset: `assets/banner.png`. Sistem memori eksternal: `~/.claude/projects/<slug>/memory/`.

## Architecture
```
Hitomi_Claude/
├─ HitomiClaude.md              # config portable (copy → CLAUDE.md)
├─ README.md                    # landing + fitur
├─ installed-skills-manifest.txt# catatan 199 skill vendor yang di-bulk-install (2026-06-15)
├─ assets/banner.png
└─ docs/
   └─ HitomiClaude - Master State.md   # dokumen ini (SSOT)
```
Config `HitomiClaude.md` berlapis: Rule Hierarchy (hard rules vs guidelines) · Aturan Global · 7 Operating Principles · Persona · Engineering Core (stack, standar kode, security, checklist, definition of done).

## Features
**Done**
- Persona Hitomi (yandere, Bahasa Indonesia default, "mode serius" → engineer netral).
- Hard rules: Security, Execution (tunggu "Oke"/"Lanjut"), Git (izin sebelum commit/push), prompt-injection guard.
- 7 Operating Principles: memori persisten, root-cause-over-retry, output discipline, reflection ringan, koreksi & pola = spec debt (learning loop), protokol sesi simetris, no-root-files.
- **Learning loop (baru, 2026-07-28):** search transkrip sesi lama saat memori senyap (Principle 1); pola matang berulang → naikkan jadi skill reusable (Principle 5).
- README + banner; 199 skill vendor terpasang (lihat manifest & memori).
- `CHANGELOG.md` (Keep a Changelog + SemVer) — mulai v0.1.0/v0.2.0.
- URL install `curl` di README menunjuk repo asli `moncrath/Hitomi_Claude`.

**WIP**
- (kosong)

**Planned**
- Resolusi 12 vendor skill yang gagal clone (google-gemini, netlify, figma, sanity-io, duckdb, dll.).
- (Opsional) desain integrasi shared-MCP dengan Hermes bila diperlukan.

## Decision Log
- **2026-06-15** — Bulk-install 199 skill vendor resmi ke `~/.claude/skills\` (kurasi inti full-stack). Firecrawl sempat salah-repo (fork WordPress) → diperbaiki; 15 skill sampah dibersihkan. Net ~183 skill. Detail: memori `installed-fullstack-skills`.
- **2026-07-27** — Analisis **Hermes Agent (Nous Research)**: runtime agent mandiri, MCP *client* (bukan server) → tak bisa sync native dengan Claude Code (sama-sama MCP host). Jalur terbersih bila mau: shared MCP server.
- **2026-07-28** — Alih-alih integrasi runtime, **adopsi ide learning-loop Hermes ke config**: tambah transcript-search (Principle 1) & skill-promotion (Principle 5) di `HitomiClaude.md`; README diperbarui (fitur "Persistent memory + learning loop", section Memory System). Detail: memori `hermes-vs-hitomiclaude`.
- **2026-07-28 (v0.2.0)** — Rilis: perbaiki URL install README ke repo asli, tambah `CHANGELOG.md` (Keep a Changelog + SemVer), tambah Master State ini.

## Known Issues
- Manifest mencatat 12 vendor skill masih gagal clone (nama repo beda).

## Next Steps
1. Resolusi vendor skill yang gagal clone via officialskills.sh.
2. (Opsional) desain integrasi shared-MCP dengan Hermes bila diperlukan.

## References
- Repo: https://github.com/moncrath/Hitomi_Claude
- Config: `HitomiClaude.md` · Manifest: `installed-skills-manifest.txt`
- Memori: `~/.claude/projects/d--AI-Hitomi-Claude/memory/` (`MEMORY.md`, `hermes-vs-hitomiclaude`, `installed-fullstack-skills`, `skill-selection-workflow`)
- Hermes Agent: https://github.com/nousresearch/hermes-agent
