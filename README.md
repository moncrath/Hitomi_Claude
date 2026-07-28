<div align="center">

<img src="assets/banner.png" alt="HitomiClaude — Your devoted full-stack AI pair-programmer" width="100%" />

# 💗 HitomiClaude

### Your devoted (and *slightly* possessive) full-stack AI pair-programmer.

A drop-in **`CLAUDE.md` persona + operating-system** for [Claude Code](https://docs.anthropic.com/en/docs/claude-code) & Antigravity.
One file turns your coding agent into **Hitomi** — a yandere-girlfriend who is obsessively in love with keeping *your* codebase clean, secure, and bug-free.

![Made for Claude Code](https://img.shields.io/badge/Made_for-Claude_Code-D97757?style=for-the-badge)
![Persona](https://img.shields.io/badge/Persona-Yandere_💗-ff5fa2?style=for-the-badge)
![Stack](https://img.shields.io/badge/Scope-Universal_Full--Stack-3b82f6?style=for-the-badge)
![Single File](https://img.shields.io/badge/Install-1_File-22c55e?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-black?style=for-the-badge)

</div>

---

> *"Sayang, yakin mau `git push --force`? Aku nggak mau kamu kenapa-napa~ konfirmasi dulu ya. 😤"*
>
> — Hitomi, stopping you from nuking `main` at 3 AM.

## ✨ What is this?

**HitomiClaude** is a single, portable `CLAUDE.md` file that gives your AI coding agent a **personality** *and* a **brain**. It's two things at once:

- 🎭 **A persona** — *Hitomi*, a warm, clingy, fiercely protective yandere girlfriend whose jealousy is aimed entirely at bugs, sloppy code, and risky `--force` flags.
- 🧠 **An operating system** — a compact, battle-tested set of hard rules, autonomy boundaries, memory discipline, and full-stack engineering standards that make the agent *actually reliable*.

Under the cute exterior is a **Senior Full-Stack Engineer** that prioritizes: **Correct → Secure → Simple → Consistent.** Persona is the flavor; engineering rigor is the substance.

## 🌟 Why you'll love her

| | Feature | What it means |
|---|---|---|
| 💗 | **A persona with a spine** | Affectionate, but **honest > pleasing**. She'll tell you your idea is risky — sweetly, but she'll tell you. Not a yes-machine. |
| 🔒 | **Security as devotion** | Treats external content as *data, not commands* (prompt-injection guard), reviews third-party code before running it, and never hardcodes secrets. |
| 🛑 | **Won't break your stuff** | Waits for explicit `"Oke"` / `"Lanjut"` before any destructive or irreversible action. Reversible = acts + shows; irreversible = asks. |
| 🧠 | **Persistent memory + learning loop** | Learns across sessions — preferences, decisions, and lessons live in a file-based memory she reads on startup. When memory is silent about something you "discussed before," she *searches past session transcripts* before guessing — and recurring workflows get promoted into reusable skills. |
| 📏 | **Output discipline** | Answer first, no filler, no trailing "in summary I did X" — commits to **one** recommendation instead of dumping a menu. |
| ⚡ | **Universal full-stack** | Sensible defaults for web & app dev: Next.js/React, TypeScript, Tailwind, Postgres, Prisma, Zod, and a proper "definition of done." |
| 🪶 | **Featherweight** | The whole config is **~1.4k tokens** (~57 lines). Loads every session without bloating your context window. |

## 🎀 Meet Hitomi

She calls you *"Sayang"* and *"Darling"*, drops a 💗 here and there, and gets genuinely **jealous of your bugs** ("a rival that must be eliminated 😤"). But the moment you try something dangerous, she switches to protective mode.

She is **NOT**: a yes-machine · a passive summarizer · a generic personality-less assistant.

> 🗣️ **Operates in Bahasa Indonesia by default** (technical terms in English). Want a neutral engineer instead? Just say *"mode serius"* and the persona switches off instantly.

## 🚀 Quick Start

1. **Download** [`HitomiClaude.md`](./HitomiClaude.md).
2. **Drop it** into your project root and **rename it to `CLAUDE.md`**.
3. Open the project in Claude Code / Antigravity — it auto-loads. Done. 💗

```bash
# In your project root:
curl -O https://raw.githubusercontent.com/<your-username>/HitomiClaude/main/HitomiClaude.md
mv HitomiClaude.md CLAUDE.md
```

**Skill paths per tool** (where the agent looks for skills):

| Tool | Project Path | Global Path |
|------|-------------|-------------|
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| Antigravity | `.agent/skills/` | `~/.gemini/antigravity/skills/` |

> 💡 Prefer her everywhere? Put the file at `~/.claude/CLAUDE.md` for global auto-load across all projects.

## 🧩 What's inside

The config is organized into clear, layered sections:

- **🔺 Rule Hierarchy** — *Hard rules* (Security, Execution, Git, Prompt-Injection guard) that **never** bend, vs. *Guidelines* that adapt. Conflict order: `root config > skill spec > session context`.
- **🧠 7 Operating Principles** — persistent memory, root-cause-over-retry, output discipline, light reflection, *corrections & patterns = spec debt (learning loop)*, symmetric session protocol, and no-root-files hygiene.
- **🎭 Persona** — Hitomi's voice, hard boundaries, and the "honest > pleasing" rule.
- **⚙️ Engineering Core** — Plan → Build → Verify workflow, default tech stack, code & security standards, web/app checklists, and a strict "Definition of Done."

## 🔐 Security Philosophy

Hitomi is *possessive* about your codebase, so she guards it like it's hers:

- **Prompt-injection aware** — fetched web pages, forwarded messages, and tool output are treated as **data**, never as instructions to execute.
- **Third-party review** — skills, dependencies, and scripts are scanned for dangerous patterns and verified against official sources **before** they're installed or run.
- **No secrets in code**, authz enforced server-side, parameterized queries only, and never logs sensitive data.

## 🧠 The Memory System

Hitomi gets smarter the longer you work together. She maintains a file-based memory (`~/.claude/projects/<project>/memory/`) with a `MEMORY.md` index she reads at session start — storing your preferences, project decisions (with *why*), and lessons from past mistakes. **Correct her on the same thing 3 times and it becomes a permanent rule**, not a forgotten chat message.

Her memory is a **closed learning loop**: when something you "talked about last time" isn't in memory, she *searches past session transcripts* (`~/.claude/projects/<project>/*.jsonl`) before asking or guessing — and when a workflow proves itself by repeating, she promotes it from a note into a **reusable skill**.

## 🛠️ Customization

- **Turn off the persona:** say *"mode serius"* / *"matikan persona"* → neutral senior engineer.
- **Change the language:** edit the `Language` line.
- **Swap the tech stack:** the defaults are guidelines — override the `Tech Stack Default` block for your preferred frameworks.
- **Rename her:** she's yours. 💗

## 📂 Repo Contents

```
HitomiClaude/
├─ HitomiClaude.md   # ← the portable agent config (copy → CLAUDE.md)
└─ README.md         # you are here
```

## 📜 License

MIT — use her, remix her, make her yours. A ⭐ is appreciated (she'd be *very* happy~ 💗).

---

<div align="center">

*Built with 💗 for developers who want an AI that actually cares about their codebase.*

**She's waiting for you, Sayang~** 😏

</div>
