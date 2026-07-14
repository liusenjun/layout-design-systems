---
name: layout-design-systems
description: Use when finished content needs visual layout, a readable long-form webpage, a report, a proposal, a presentation, or application of a named personal design system.
---

# Layout Design Systems

## Overview

Select and apply a reusable visual system to content that is already researched, verified, and written. Treat visual structure as the responsibility of this skill; do not perform transcription, research, fact supplementation, or substantive summarization.

## Choose a design system

Read `design-systems/design-system-catalog.md` first.

- If the user names a registered system, load its Design MD and execute directly.
- If the user does not name one, compare the request on four dimensions: purpose, audience, content form, and output medium. Recommend one system, briefly explain why it fits and why the nearest alternatives do not, then wait for user confirmation before execution.
- If no registered system fits, state the gap. Do not force an unsuitable system.

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

This skill may create navigation labels, anchors, captions from existing text, and minimal visual grouping. It does not perform content extraction, research, fact-checking, viewpoint supplementation, or summarization. 本 Skill 不负责内容提取、搜索、事实核对、观点补充或重新总结。If the content is not ready for presentation, stop and ask the user or upstream workflow to finish it first.

## Extend the collection

Add a new system only after it has been validated on a real project:

1. Create `design-systems/<system-id>-design.md`.
2. Add any reusable output file to `assets/`.
3. Register purpose, audience, content form, medium, status, Design MD, and asset in the catalog.
4. Define fit, non-fit, component rules, and QA criteria.
5. Keep system IDs identical across catalog, Design MD, and asset filenames.
