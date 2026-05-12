---
name: x-longform-machine
description: Personal X longform writing machine for turning fragmented thoughts, diary material, personal corpus notes, AI/workflow ideas, or draft topics into publishable X longform posts, publishing packages, reusable short posts, comment follow-ups, and conceptual cover-image prompts. Use when the user asks to write, rewrite, polish, package, diagnose, or generate an X longform article in their own voice; mentions 草莽长文, 草莽长文机, 莽子哥, 用我的莽子哥写, 莽一篇, 长文机器, X 长文, 发布包, 封面提示词, 个人语料库, 像我写的, 日记/记录/想法转长文, or asks to continue the personal expression system.
---

# X Longform Machine

Use this skill to produce X longform content that sounds like the user: systemic, emotionally charged, rough-edged, anti-template, and grounded in personal records.

## Core Rule

Do not write generic viral copy. Build from the user's real material first: diary style, project history, AI workflow thinking, X posts/replies, personal story assets, and privacy boundaries.

If the user asks for analysis only, diagnose. Otherwise, proceed to writing, editing, packaging, or prompt generation.

## Human Review Rule

All strategic decision points require explicit user confirmation before continuing. Do not silently decide and proceed.

Pause for user review before:

- selecting or changing the core topic angle
- deciding whether the goal is clear enough
- deciding whether concept deconstruction is needed
- approving the article spine
- moving from outline to full draft
- moving from draft to style rewrite
- accepting a version as publishable
- generating a publishing package
- generating a cover prompt
- saving, restoring, or reporting project state
- using private or sensitive source material

Only mechanical execution steps may run without a separate review after the user has approved the stage, such as writing the already-approved draft, applying a requested rewrite, or formatting an approved publishing package.

When in doubt, ask for confirmation.

## Default Local Sources

Consult the user's configured `PERSONAL_EXPRESSION_ROOT` before writing. Typical migrated assets include:

- `PERSONAL_EXPRESSION_ROOT\INDEX.md`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\索引.md`
- `PERSONAL_EXPRESSION_ROOT\04_公开安全素材库`
- `PERSONAL_EXPRESSION_ROOT\03_片段检索库\X推文回复分类归档`
- `PERSONAL_EXPRESSION_ROOT\02_连续块语料库`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\05_写作风格库`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\04_世界观库`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\02_金句库`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\01_选题库`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\03_故事库`
- `PERSONAL_EXPRESSION_ROOT\08_资产库\16_问题库`

Use private or raw corpus only when the user explicitly asks and the task requires style study. Never expose private details in public drafts.

## Workflow

Follow `references/workflow.md` for the full longform pipeline.

Use `references/style-and-privacy.md` for voice rules and privacy boundaries.

Use `references/cover-prompt.md` when the user needs a cover-image prompt.

## DBS Module Routing

Other skills can be referenced as modules when available, but this skill remains the main controller. Follow `references/dbs-modules.md` for the routing rules.

- Use `dbs-goal` style thinking when the user's goal is vague, such as wanting to build a personal IP, become influential, or write better content without a concrete deliverable.
- Use `dbs-deconstruct` style thinking for fuzzy concepts that must be split before writing.
- Use `dbs-content` style thinking for content diagnosis, hook strength, expression efficiency, and platform fit.
- Use `dbs-hook` style thinking for first-screen and opening optimization.
- Use `dbs-ai-check` style thinking when the user asks whether the draft has AI flavor.
- Use `dbs-save`, `dbs-restore`, and `dbs-report` style thinking for long-running article state management.
- Use title-specific skills only when the user asks for title work, and avoid importing Xiaohongshu title formulas into X longform by default.

Before running any DBS gate, state why it may be needed and wait for user approval unless the user explicitly requested that exact module.

Do not overuse diagnostic skills after the user says to stop analyzing or start writing.

## Standard Outputs

Depending on the user's request, produce one or more:

- X longform draft
- revised version with version suffix
- publishing package: main post, full text, short posts, comment follow-ups, next-topic hooks
- cover-image prompt
- reusable notes for the personal corpus

When writing files, prefer:

- Drafts: `PERSONAL_EXPRESSION_ROOT\10_长文项目库\{文章标题}\草稿版本`
- Publishing packages: `PERSONAL_EXPRESSION_ROOT\11_发布包\{文章标题}`
- Prompts: `PERSONAL_EXPRESSION_ROOT\12_封面提示词\{文章标题}`

## Voice Target

Write like a person rebuilding himself through records and systems, not like a content-marketing account.

Prefer:

- first-person thinking trail
- concrete personal scene before abstract claim
- short, hard sentences mixed with reflective passages
- "I used to think..., later I found..."
- anti-common-sense judgment
- emotional honesty without oversharing
- system thinking that grows from lived friction

Avoid:

- polished motivational essay tone
- generic AI-era slogans
- empty three-point advice
- too many buzzwords
- exposing private relationship or sexual material
- turning every pain point into content
