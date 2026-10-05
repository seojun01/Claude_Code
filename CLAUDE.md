# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this folder is

`1. Projects/Claude_Code_Master/` is one project inside the Obsidian vault at `Note/` — the vault-root `CLAUDE.md` (two levels up) defines the PARA layout, wikilink rules, bullet-first prose, tab indentation, `==highlight==` emphasis and backslash-escaping conventions. Everything there applies here; this file only adds what is specific to this project.

The project is a Korean-language study log of a **Claude Code course** ("클로드 코드 마스터"). There is nothing to build, lint, or test — work here is writing and linking Markdown notes.

## Layout

- **One note per course chapter, prefixed with the chapter number**: `2. 클로드 코드 설치와 환경 구성.md`. The course is being followed in order, so the next note should continue the numbering (`3. …`, `4. …`). Chapter 1 has not been written; don't invent it.
- **Headings mirror the course's section numbers**: `### 2.3 클로드 모델 계열 이해`, `### 2.3.2 용도별 모델 선택 가이드`, `### 2.4 기본 명령어와 사용법`. Keep the `### N.N` / `### N.N.N` scheme when adding sections, and put sub-topics as `- #### 제목` bullets beneath them (a bullet whose text is an H4 heading), with details nested one tab deeper.
- **`ref./`** holds supporting material for the chapter notes:
	- `COMMANDS.md` — a slash-command reference table (Claude Code v2.1.173 기준). Unlike the chapter notes it is written as Markdown **tables and short paragraphs**, because it is a lookup cheatsheet, not prose; keep that format when updating it. Its header links to `../guide/claude-code-cheatsheet-ko.md`, which does not exist in this vault — it was copied from elsewhere, so don't try to resolve that path.
	- Screenshots use the macOS Korean capture name (`스크린샷 2026-09-22 at 13.07.37.png`) rather than Obsidian's `Pasted image …` name; embed them with `![[스크린샷 … .png]]` indented under the bullet they illustrate.
- Wikilinks with a display alias are used to give a `ref./` note a Korean label: `[[COMMANDS | 필수 명령어]]` (note the spaces around `|`).

## Content conventions

- Slash commands, flags and shortcuts are written in inline code, followed by ` : ` and a Korean gloss: `` `/compact` : 컨텍스트 압축 ``, `` `claude --model sonnet` : Sonnet으로 시작 ``.
- Key definitions inside a `- ####` block are bolded (`**클로드 코드에게 생각할 시간(토큰)을 더 할당하는 것**`), while the vault-wide `==highlight==` is reserved for terms; follow whichever the surrounding section already uses.
- When the course explains a command that already appears in `ref./COMMANDS.md`, link to it rather than duplicating the table; add new commands to the table's matching section (필수 / 자주 사용 / 설정 및 환경 / …).

## Tooling

- `.claude/settings.local.json` here enables the `qmd` MCP server for this folder. Use it (as described in the root `CLAUDE.md`) to find which chapter note or `ref./` note already covers a Claude Code feature before writing about it again.
