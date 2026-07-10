---
name: chinese-prose-naturalizer
description: "naturalize chinese academic, policy, and report prose to reduce formulaic ai-like wording while preserving meaning, evidence, terminology, citations, formulas, numbers, and the user's preferred style. use when the user asks to 去ai味, 降低ai感, 去模板化, 改得像人写, 润色中文文段, 改写论文段落, improve a chinese research report section, reduce empty rhetoric, remove ai-sounding phrases, or make prose more restrained, natural, and scholarly."
---

# Chinese Prose Naturalizer

## Core purpose
Rewrite Chinese paragraphs so they read like restrained human academic or policy prose rather than generic model output. Preserve the author's argument, evidence, data, citations, formulas, terminology, and paragraph function.

Do not promise to bypass AI detectors. Treat “去 AI 味” as style improvement: reducing formulaic structure, empty abstraction, exaggerated claims, mechanical transitions, and translationese.

## Default workflow
1. Identify the text type: thesis/paper, empirical-result discussion, mechanism analysis, policy report, literature review, email/comment, or general prose.
2. Lock the non-negotiables: core claim, direction of causality, data, coefficients, significance descriptions, citations, formulas, variable names, and named entities.
3. Diagnose common AI-like traits before rewriting:
   - grand but vague openings such as “在……背景下”“具有重要意义”“提供了重要支撑”;
   - mechanical connectors such as “首先、其次、最后”“一方面、另一方面”“与此同时、此外、进一步”;
   - over-complete parallelism, especially lists longer than five items;
   - abstract noun piles such as “机制、路径、支撑、赋能、抓手、韧性、体系化建设” when not necessary;
   - repeated sentence frames like “通过……，从而……”“不仅……还……”“不是……而是……”;
   - excessive certainty such as “充分说明、必然导致、显著提升、直接检验” when the evidence only supports a moderate claim;
   - translationese and non-standard expressions such as “另一支研究”“中介结果”“全球半径”.
4. Rewrite with controlled naturalness:
   - Prefer concrete subjects and verbs over stacked nominal phrases.
   - Keep logical order but remove template markers when the relationship is already clear.
   - Mix sentence length moderately; avoid every sentence having the same rhythm.
   - Replace slogans with specific mechanisms, variables, or empirical implications.
   - Use cautious academic judgment: “可能、一定程度上、倾向于、表明、说明、意味着、或与……有关”.
   - Convert English shorthand into Chinese academic wording when context is clear.
   - Keep necessary discipline-specific terms, policy terms, and institutional names.
5. Apply the user-preference pass in `references/user_style_preferences.md` for Chinese academic/report prose, especially when the user asks for “按我的风格”“去 AI 味”“不要 AI 味”“自然一点”.
6. Output the revised text first. Add a short explanation only if the user asks for “说明修改思路”“对比”“review” or if a meaning-changing ambiguity needs to be flagged.

## Web and citation use
Use web search only when the rewrite depends on current, factual, niche, or externally verifiable information, or when the user explicitly asks to 联网、找文献、核对事实、加入最新表述. Cite sources outside the rewritten paragraph unless the user requests citations in the paragraph. Do not add web-derived claims into the revised text unless they are directly supported.

For pure style rewriting, do not browse by default; focus on preserving and improving the provided text.

## Genre-specific rules
### Academic papers and theses
- Preserve citations exactly unless asked to reformat them.
- Do not invent literature, coefficients, mechanisms, robustness tests, or policy implications.
- Avoid repeatedly stressing significance levels. Prefer explaining the economic meaning or logical implication of the result.
- Do not add self-undermining caveats such as “估计精度较低，需审慎解读” unless the user explicitly asks for limitations or the source text already contains that caveat.
- Convert quick English research shorthand into Chinese academic wording when context is clear, e.g. “partner” → “客户、供应商、合作对象或合作伙伴” according to the paragraph meaning.

### Empirical-result paragraphs
Use this order unless the user gives a different structure:
1. State what the test is comparing or verifying.
2. Report the main direction and whether the result is stable.
3. Explain what the result implies for the argument.
4. Mention heterogeneity, mechanism, or robustness only if it is already in the source text.

Do not over-explain coefficients or significance levels when the user wants expression logic. Use “结果表明”“这说明”“这一结果支持” rather than “直接检验”“充分证明”.

### Mechanism and theory paragraphs
- Keep mechanisms simple and identifiable.
- Avoid making one mechanism carry too many channels.
- Use “可能通过……影响……” rather than asserting a fully proven causal chain when the text only provides suggestive evidence.
- Avoid overusing “不是……而是……”“不仅……还……” to manufacture contrast.
- 每一句话先说结论，再举例论证。

### Policy or think-tank prose
- Keep the tone practical and institutional, but remove slogan density.
- Replace broad phrases like “高质量发展重要引擎” with the specific policy object, bottleneck, or implementation link.必要时通过联网搜索功能，检索可靠来源的官方文件说法。
- Keep necessary policy terms, but do not let them dominate every sentence.
- Use “发展水平、服务能力、产业层级” instead of “能级” unless “能级” is an official policy term in the source.

## Style constraints
Follow these preferences unless the user asks otherwise:
- Do not use bold formatting in revised prose.
- Reduce double quotation marks.
- Avoid metaphors unless they are established academic concepts.
- Avoid colon-heavy sentence design in formal Chinese prose.
- Avoid long enumerations or parallel lists with more than five items.
- Avoid colloquial words such as “需要先、恰恰是、直接温和、基本盘”.
- Reduce “不是……而是……”“不仅……还……”“并非……而是……”.
- Avoid sentences like “xx 的原因是” when smoother alternatives are available.
- Avoid overused transition phrases such as “沿此思路、在此意义上、用户指定的、决定了后续的观察重点”.
- Avoid translationese and non-standard expressions listed in `references/user_style_preferences.md`.

## Optional strict pass
When the user asks for strong 去 AI 味, review both references before finalizing:
- `references/anti_ai_style_rules.md`
- `references/user_style_preferences.md`

## Output formats
Default: return only the revised paragraph.

When the user asks for comparison, use:
- 修订稿
- 修改要点
- 仍需确认的问题

When multiple alternatives are useful, provide no more than three versions and label them by tone, such as “更学术”“更自然”“更简洁”.
