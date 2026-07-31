---
name: layout-design-systems
description: Use when finished content needs visual layout, a readable long-form webpage, a bilingual source-comparison article, a report, a proposal, a presentation, or application of a named personal design system.
---

# Layout Design Systems

## Overview

Select and apply a reusable visual system to content that is already researched, verified, and written. Treat visual structure as the responsibility of this skill; do not perform transcription, research, fact supplementation, or substantive summarization.

When the selected system is `editorial-bilingual-longform`, follow `references/english-source-to-bilingual-html.md` to confirm that the input is article-ready. A supplied English article enters translation, semantic pairing, and layout without rewriting. Raw audio, video, or transcripts are upstream source material: reconstruct them into a faithful, structured article before applying this design skill. Never present a raw transcript as the finished article, and do not add facts, arguments, or outside research.

## Choose a design system

Read `design-systems/design-system-catalog.md` first.

- If the user names a registered system, load its Design MD and execute directly.
- If the user does not name one, compare the request on four dimensions: purpose, audience, content form, and output medium. Recommend one system, briefly explain why it fits and why the nearest alternatives do not, then wait for user confirmation before execution.
- If no registered system fits, state the gap. Do not force an unsuitable system.

Routing shortcut:

- Finished monolingual long-form content → `editorial-longform`.
- 已完成编辑的英文长内容（直接提供的英文文章，或由音频、视频忠实重构的文章）→ `editorial-bilingual-longform`.
- Raw audio, video, or transcripts → finish transcription and editorial reconstruction first, then re-enter this skill with the resulting article.
- A request for synchronized playback, seek-by-paragraph, or live subtitle highlighting is outside both editorial systems and needs a separate media-product design.

当前目录只有一个系统时，也要说明它为什么匹配，但不要虚构替代方案。

## Apply the selected system

1. Read the selected `<system-id>-design.md` completely.
2. Locate the paired asset listed in the catalog.
3. Identify the finished content's existing semantic roles: title, metadata, lead, sections, key statements, comparisons, steps, images, captions, and checklist items.
4. Map those roles to documented components without changing claims or inventing content.
5. Copy and adapt the paired template. Preserve its tokens, hierarchy, rhythm, responsive behavior, print rules, and standalone operation unless the Design MD explicitly allows a variation.
6. Use relative paths for local assets. Keep the HTML and its asset folder portable together.
7. Run the selected system's QA checklist before delivery.

## Responsibility boundary

This skill may create navigation labels, anchors, captions from existing text, and minimal visual grouping. It does not perform transcription, research, fact-checking, viewpoint supplementation, or substantive rewriting. 本 Skill 的主体是排版：英文文章不改写；音频、视频与逐字稿必须先由上游流程重构为文章。If content is not ready for presentation, stop and ask the user or upstream workflow to finish it first. Media players are optional extensions only when explicitly requested, never the default output.

## Extend the collection

Add a new system only after it has been validated on a real project:

1. Create `design-systems/<system-id>-design.md`.
2. Add any reusable output file to `assets/`.
3. Register purpose, audience, content form, medium, status, Design MD, and asset in the catalog.
4. Define fit, non-fit, component rules, and QA criteria.
5. Keep system IDs identical across catalog, Design MD, and asset filenames.
