# Anti-AI Style Rules for Chinese Prose

Use this reference for strict Chinese prose naturalization, especially academic manuscripts, research reports, and policy writing. Use it together with `user_style_preferences.md` when the user asks for strong 去 AI 味 or says the text should follow their usual writing preferences.

## High-priority edits
1. Remove fake completeness. If the source paragraph has three parallel clauses only for rhythm, keep the strongest two or merge them.
2. Replace empty importance claims with the actual analytical object.
   - Before: “这一问题具有重要理论和现实意义。”
   - After: “这一问题关系到变量设定能否准确刻画企业的供应链调整。”
3. Replace template openings.
   - Before: “在全球价值链重构和外部不确定性上升的背景下……”
   - After: “全球价值链重构提高了企业调整供应链布局的压力……”
4. Convert abstract nouns into actions when possible.
   - Before: “为企业供应链韧性提升提供支撑。”
   - After: “降低企业寻找国内替代供应商的成本。”
5. Reduce chained causality.
   - Before: “通过降低交易成本，从而促进企业……”
   - After: “交易成本下降后，企业更容易……”
6. Remove unnecessary contrast templates.
   - Before: “这一结果并非说明企业完全放弃海外供应商，而是表明国内市场规模扩大后，企业可能更多转向本土采购。”
   - After: “这一结果表明，国内市场规模扩大后，企业可能更多转向本土采购。”

## Words and phrases to question
Do not automatically delete these words, but check whether each one adds meaning:
“显著、持续、不断、有效、充分、重要、关键、核心、深刻、全面、赋能、抓手、路径、机制、支撑、推动、优化、协同、韧性、体系、格局、释放、激发、夯实、助力、能级”.

## Safer academic replacements
- “充分说明” → “表明 / 说明 / 在一定程度上支持”
- “必然导致” → “可能导致 / 倾向于带来 / 有助于解释”
- “产生重要影响” → “影响 / 改变 / 提高 / 降低”
- “具有重要意义” → state the concrete implication
- “赋能” → “支持 / 改善 / 降低成本 / 提高效率”
- “打造……格局” → “形成……关系 / 改善……结构”
- “直接检验” → “检验 / 考察 / 用于识别 / 提供经验证据”
- “中介结果” → “机制检验结果 / 机制分析结果”
- “另一支研究” → “另一类研究 / 另一条研究脉络 / 相关研究”

## Sentence-level rhythm
- Prefer one clear claim per sentence.
- Keep long sentences only when the logical relationship is genuinely complex.
- Use short transition words sparingly: “因此、同时、相应地、由此”.
- Avoid making every sentence end with “提供支撑、奠定基础、具有意义”.
- Avoid colon-heavy structures unless they improve readability.
- Avoid long parallel lists; compress or split lists longer than five items.

## Preservation rules
Always preserve:
- citations, source names, years, formulas, coefficients, p-values, sample sizes, table/column references;
- variable names, model names, and institutional terms;
- the original direction of the argument and the strength of the evidence.

Never add:
- new empirical results;
- invented literature;
- stronger causal language than the source supports;
- policy prescriptions that are not implied by the text;
- self-undermining caveats that were not present in the source or requested by the user.

## Quick final checklist
Before returning the rewrite, check:
1. Does the paragraph still say the same thing?
2. Are claims more concrete and less slogan-like?
3. Are transitions necessary rather than decorative?
4. Are citations and data unchanged?
5. Does the text follow the user's avoid-list and formatting preferences?
6. Does the text sound like a researcher revising their own paragraph, not a generic polishing model?
