# 🗂️ Project Organizer Skill

[中文](README_zh.md) | [日本語](README_ja.md) | [한국어](README_ko.md)

> An AI skill that enforces structured file organization across all your projects — automatically.

## What It Does

When installed, this skill makes your AI assistant **proactively organize files** during every project. No more messy folders after long working sessions.

| Trigger | Behavior |
|---------|----------|
| Starting a new project | Proposes and creates a standardized folder structure |
| Creating files during tasks | Places each file in the correct folder automatically |
| Saying "organize" or "clean up" | Scans and reorganizes the entire project folder |
| Every 3–5 file operations | Runs a cleanup checkpoint |

## Core Rules

### 📁 Standard Project Structure

```
project-name/
├── README.md        — Project description, status, conventions
├── drafts/          — Working drafts, iterative versions
├── figures/         — Images, charts, diagrams
├── scripts/        — Code that generates outputs
├── references/      — Source materials, templates
├── output/          — Final deliverables only
└── archive/         — Superseded versions (moved, not deleted)
```

### 📝 Naming Convention

| ✅ Do | ❌ Don't |
|-------|---------|
| `report_v1.docx` | `report_final.docx` |
| `report_v2.docx` | `report_new.docx` |
| `submission_20260226.docx` | `report_final_FINAL.docx` |

### 🏗️ Domain Templates

The skill includes ready-made templates for:
- **Academic Papers** — drafts / figures / scripts / references / output / archive
- **Web Applications** — src / public / scripts / docs / dist
- **Data Analysis** — data / notebooks / scripts / figures / output

## Installation

### For Antigravity / Claude Users

Drop the `project-organizer/` folder into your skills directory:

```
~/.gemini/antigravity/skills/project-organizer/
```

The skill activates automatically in all new conversations.

### Manual Use

You can also reference `SKILL.md` as a system prompt or custom instruction for any AI assistant.

## Why This Exists

After a multi-week AI-assisted paper writing project, we ended up with 70+ files dumped flat in a single folder — scripts mixed with drafts, temp files next to final submissions. This skill was born from that pain, encoding the organization principles we wish we had from the start.

## License

MIT
