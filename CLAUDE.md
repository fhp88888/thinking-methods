# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository purpose

This repository is a curated knowledge base with two top-level collections:

- `通用思维方式/`: existing general-purpose thinking methods, grouped by reasoning or thinking style.
- `软件工程定律/`: Chinese-localized translations and summaries of major laws from *Laws of Software Engineering*, grouped by software-engineering topic.

The root `README.md` is the main navigation surface. Any structural change should keep the homepage readable as an overview first, then as an index.

## Common commands

This repository has no build, lint, or test toolchain.

Useful commands are structural/content checks:

- List top-level content:
  - `find . -maxdepth 2 -type d | sort`
- List Markdown files:
  - `find . -name "*.md" | sort`
- Search for a term across entries:
  - `grep -R "关键词" 通用思维方式 软件工程定律 README.md`
- Check git status:
  - `git status`

There is no single-test command because there is no automated test suite in this repository.

## Content architecture

### 1. General thinking methods

`通用思维方式/` preserves the original content with minimal change. Its subdirectories are the primary taxonomy:

- `演绎推理`
- `归纳推理`
- `溯因推理`
- `批判性思维`
- `系统思维`
- `横向思维`
- `模型思维`

These entries are standalone Markdown notes with frontmatter (`title`, `category`, `description`) followed by explanatory sections.

### 2. Software engineering laws

`软件工程定律/` is organized by software-engineering topic rather than by generic reasoning style. Current category structure:

- `团队`
- `规划`
- `架构`
- `质量`
- `规模`
- `设计`
- `决策`

Each law should remain a short, readable Markdown note with:
- frontmatter (`title`, `category`, `description`)
- `## 什么是...`
- `## 适用场景`
- `## 局限性与注意事项`

The tone should stay faithful to the original idea while being naturally rewritten for Chinese readers, not a literal line-by-line translation.

## Editing guidance specific to this repo

- Prefer preserving existing entry bodies in `通用思维方式/`; structural reorganization is favored over content rewrites there.
- When adding or revising `软件工程定律/` content, keep terminology consistent across related entries and with the root `README.md` index.
- If you rename, add, or remove entries, update `README.md` in the same change so links stay valid.
- This repo is documentation-first; navigation clarity and category consistency matter more than introducing new documentation layers.
