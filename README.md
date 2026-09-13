# meshcode-ai/skills-docs

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-3-blue)](#)
[![Standard](https://img.shields.io/badge/agent--skills-spec-brightgreen)](https://agentskills.io/specification)

**Document generation skills for Claude Code, Codex, Cursor, and meshcode — PowerPoint decks (pptx), Word documents (docx), and print/screen PDFs.** The 3 document skills (`docs-*`) are distilled editions containing **judgment knowledge only**, with no scripts: conclusion-first deck storylines and chart-by-question rules, report/proposal/memo structures with real Word-style discipline, print-vs-screen route selection, and the three silent PDF failures (unembedded fonts, rasterized text, image bloat) — each skill ending in a mandatory QA contract that verifies the generated file itself. They follow the Agent Skills standard (agentskills.io) — unzip into your project's `.meshcode/skills/` (flat layout) and Claude Code, Codex, Cursor, and meshcode desktop pick them up from the next session.

## Who this is for

- **Founders and sales teams** — investor decks and proposals where one slide = one claim, not a wall of bullets
- **Operators and analysts** — reports whose numbers trace back to a source, delivered as verified files
- **Anyone shipping print** — route selection (HTML→PDF vs LaTeX vs docx export) decided before the first page is built
- **AI agent operators** — knowledge-first document skills ready for stores and registries

## Skill list

| Skill | Role | Core judgment criteria |
|---|---|---|
| `docs-pptx` | Presentation generation | Conclusion first, ≤ 1 message/slide, chart-by-question, type floor 28/18pt |
| `docs-docx` | Document/report generation | Type decides structure, BLUF, ≤ 3 heading levels, reopen-and-verify QA |
| `docs-pdf` | PDF production | Route first, font embedding / OCR layer / bloat — the 3 silent failures |

## Install

1. Download the zip → extract into your project's `.meshcode/skills/` (flat: `.meshcode/skills/docs-pptx/SKILL.md`)
2. Start a new Claude Code · Codex · Cursor · meshcode session → skills are exposed automatically
3. Full catalog at the hub: [github.com/meshcode-ai/skills](https://github.com/meshcode-ai/skills)

## Skill details

### docs-pptx
> Presentation generation — deck storyline, slide-by-slide outline, chart choice, and generating/editing .pptx files with overflow and font QA. Use when the user says "make a presentation", "build a deck", "PowerPoint", "investor deck slides"…

### docs-docx
> Document generation — report/proposal structure, heading hierarchy, styles, and producing verified .docx files via pandoc or docx libraries. Use when the user says "write a report", "make a document", "Word file", "proposal document"…

### docs-pdf
> PDF production — print vs screen route selection, page layout, font embedding, and export verification for reports, ebooks, and one-pagers. Use when the user says "make a PDF", "print-ready", "ebook", "PDF report"…

## Hub & related repos

- Hub catalog: **[github.com/meshcode-ai/skills](https://github.com/meshcode-ai/skills)** (llms.txt · index.json · robots.txt)
- [skills-exec](https://github.com/meshcode-ai/skills-exec) — the board memo and investor update these documents carry · [skills-design](https://github.com/meshcode-ai/skills-design) — visual identity behind them

## Use with meshcode

Built for [meshcode](https://meshcode.ai?utm_source=github&utm_medium=org_readme&utm_campaign=gh_skills-docs) (free download — macOS/Windows):

1. Open your project in meshcode
2. In chat, ask **"show available skills"**, then **"install the document skills"** — meshcode fetches from this repo automatically
3. They appear in the next session and load only when a task matches

Manual alternative: repo zip → `.meshcode/skills/`. Also works in Claude Code (`~/.claude/skills/`), Codex, and Cursor.

## Distillation log (2026-09-13)

- Sources: independent distillation — pptxgenjs / python-pptx / pandoc official docs plus deck and document typography craft. The anthropics/skills docx · pdf · pptx skills are source-available (not open source), so they were **not used** — written independently, nothing ported
- Excluded: tool installation steps, runtime-only fields, scripts
- Kept: artifact verification rules (pptx text overflow and font fallback / docx reopen-and-verify with CJK fonts / pdf font embedding, OCR layer, file size) and the output contract (outline approval → file → QA report)
