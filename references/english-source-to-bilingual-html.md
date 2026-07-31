# English Source → Bilingual Editorial HTML Workflow

Use this workflow only with `editorial-bilingual-longform`.

## Outcome and boundary

The layout skill accepts an article-ready English source and turns it into a faithful bilingual article-style HTML document. Its主体是排版，不是转写或内容创作。

- 英文文章直接进入排版：保留原文结构与表达，不改写原文。
- 音频、视频或逐字稿必须先由上游流程重新构建为结构完整的文章，再进入本流程。
- 逐字稿只是上游素材，不把逐字稿作为最终展示内容。

Keep useful 时间戳（timestamps）as source metadata when available. 默认不嵌入播放器；只有用户明确要求时才启用播放器、逐段跳转或字幕同步等媒体扩展。不制作同步播放器 as part of the default editorial output.

The work is source-led: 不自动补充事实, arguments, examples, or external research. If source text is unclear, mark uncertainty or ask the user instead of silently inventing content.

## Stage 0: Confirm article readiness

If the input is already an English article, continue without substantive rewriting. If the input is raw audio, video, or a transcript, stop the layout phase and hand it to an upstream editorial workflow. That workflow should remove spoken repetition and fragmented delivery, recover the argument, and produce a faithful article without adding outside facts. Resume this design workflow only after the article has been approved or is otherwise ready for presentation.

## Stage 1: Capture the article

### Article

1. Preserve title, author, date, source link, headings, paragraph order, lists, quotations, images, captions, and meaningful inline emphasis.
2. Remove site chrome, comments, advertisements, and unrelated recommendations.
3. Download or copy permissible 图片（images）into a local relative asset folder. Keep every retained image in its 原始顺序（original order）.

### Article reconstructed from audio

1. Use the approved reconstructed article, not the complete transcript, as the layout source.
2. Preserve speaker attribution, quotations, section transitions, and useful timestamps only when they remain meaningful in article form.
3. Do not restore removed filler or repetition merely because it appeared in the transcript.

### Article reconstructed from video

1. Use the approved reconstructed article, not the complete transcript, as the layout source.
2. Identify visual moments that carry information not contained in the finished article text.
3. Extract only those explanatory frames or supplied images, keep their original order, and record the source timestamp for traceability.

## Stage 2: Establish editorial structure

1. Recover the source heading hierarchy; do not invent more sections merely to shorten the page.
2. Identify ordinary paragraphs, Key Statements, Action Text Cards, lists, tables, images, and captions by meaning.
3. Keep actionable prompts, commands, queries, or executable examples distinct from ordinary quotations.
4. Treat a lead as semantic metadata only; it does not receive a separate font-size tier.

## Stage 3: 忠实翻译（Translate faithfully）

1. Translate into natural Chinese without changing claims, certainty, tone, names, technical terms, or causal relationships.
2. Preserve code, URLs, identifiers, product names, and quoted interface labels unless an established Chinese form exists.
3. When a phrase is ambiguous, prefer a transparent translation and retain the English nearby; do not resolve uncertainty by invention.
4. Translate image captions and component labels so they can switch with the reading mode.

## Stage 4: 语义配对（Semantic pairing）

Create one `.bi` wrapper per independently readable semantic unit. Each wrapper contains the complete corresponding `.en` and `.zh` content.

- Pair by meaning, not by sentence count.
- Do not split a list away from the sentence that introduces it.
- Do not merge separate source paragraphs when doing so weakens scanability.
- Verify that neither language contains an unmatched claim.

## Stage 5: Apply the design system

1. Copy `../assets/editorial-bilingual-longform-template.html`.
2. Replace placeholder content without changing the three-mode structure.
3. Put English first in bilingual DOM pairs only where the template rules expect it; the visual modes control what is shown.
4. Insert images and bilingual captions in the source's original order near the relevant semantic group.
5. Use the base Editorial Longform components and the bilingual system's overrides.

## Stage 6: Verify

Check all three modes separately:

- Chinese: Chinese primary, English rail on hover/focus/click.
- Bilingual: English above Chinese, 10px pair gap, 30px group gap, no interaction decoration.
- English: English primary, Chinese rail on hover/focus/click.

Then verify heading order, font assignments, special components, image order, caption switching, keyboard behavior, mobile layout, print output, relative assets, and source attribution. Spot-check translations against the source at the beginning, middle, and end before delivery.
