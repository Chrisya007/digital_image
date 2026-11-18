# AGENTS.md — LLM Wiki & Single-Page Scrapbook Journal Presentation Constitution

## 1. Project Objective & Grounding Rules
- **Topic:** How Digital Images Work: Pixels, Color Spaces & Quantization
- **Target Audience:** Beginners with no prior background in computer graphics or signal processing.
- **Strict Grounding Rule:** Every definition, formula, comparison, and numerical value in `wiki/` and `index.html` must come strictly from `raw/` (via `wiki/`). Do not introduce outside facts or unverified claims.
- **Language:** Write all prose, headings, and journal text in clear English while preserving exact technical terms (`RGB`, `HSV`, `CIELAB`, `K-Means`, `Floyd-Steinberg`, `DEFLATE`, `DCT`).
- **Clean Style:** Do not use emojis anywhere in `wiki/`, `outline.md`, `verification_log.md`, or `index.html`.

## 2. Directory Structure & Permissions
```text
digital-images-wiki/
├── AGENTS.md              # Read-only project constitution
├── raw/                   # Immutable original source articles (NEVER modify or delete)
├── wiki/                  # AI-compiled Markdown knowledge base
│   ├── index.md           # Master catalog of all source pages and concept pages
│   ├── log.md             # Chronological append-only log of all ingests and updates
│   ├── sources/           # One structured summary per file in raw/
│   └── concepts/          # Synthesized atomic concept notes with [[wiki-links]]
├── outline.md             # Page-by-page journal plan reviewed at Node 2 checkpoint
├── verification_log.md    # Audit log of loop checks, errors found, and fixes applied
└── index.html             # Self-contained single-page scrapbook journal presentation