# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AI Jumpstart is a hands-on, self-paced educational course teaching effective use of AI assistants (Claude, ChatGPT, Gemini). It is a static website built with Quarto.

## Build Commands

```bash
quarto preview          # Live-reload dev server
quarto render           # Build static site to _site/
quarto render file.qmd  # Render a single page
```

There are no package managers, test frameworks, or linters — just Quarto.

## Architecture

- **`_quarto.yml`** — Project config: site structure, navigation (navbar + docked sidebar), theme (cosmo/darkly), output to `_site/`
- **`index.qmd`** — Homepage with module cards linking to each lesson
- **`modules/`** — Seven `.qmd` files (00–06), each a self-contained lesson following a consistent pattern: intro → exercise → notice boxes → follow-up prompts → evaluation
- **`reference.qmd`** — Platform comparison table, prompting cheat sheet, strengths/weaknesses
- **`about.qmd`** — Course background
- **`styles.css`** — Custom CSS classes for the course UI (see below)

## Content Conventions

- **Platform parity**: Instructions are given side-by-side for Claude, ChatGPT, and Gemini using callout divs (`.platform-claude`, `.platform-chatgpt`, `.platform-gemini`)
- **Prompt boxes**: User-facing prompts use `.prompt-box` (dark-themed, copyable)
- **Other custom classes**: `.followup-box`, `.notice-box`, `.try-it`, `.module-card` — all defined in `styles.css`
- **Tone**: Conversational, encouraging, non-technical. Written for people with zero AI experience.
- **Module length**: Each exercise targets 10–20 minutes of hands-on work

## When Editing Content

- Maintain platform-agnostic framing; if adding platform-specific instructions, include all three platforms
- Use existing CSS classes rather than inline styles
- Keep the consistent module structure (intro → exercise → notice → follow-up → evaluation)
- The GitHub repo link in the navbar points to `github.com/pem725/ai-jumpstart`
