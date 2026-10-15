# Reader-skill Report Structure

Use this structure when generating literature report documents from academic papers.

## Bilingual Report

Title page:
- Paper title / 論文標題
- Authors / 作者
- Venue and year / 期刊會議與年份
- DOI, arXiv, URL, or source file / 文獻來源
- Report generation date / 匯報生成日期

1. Executive Summary / 快速總覽
- Research question / 研究問題
- Core method / 核心方法
- Main finding / 主要發現
- Why it matters / 學術或工程意義
- Evidence label for each key point

2. Reading Map / 閱讀導圖
- Suggested reading order
- Important sections, figures, tables, and equations
- What to focus on when preparing a group meeting or presentation

3. Background and Motivation / 背景與動機
- Field context
- Unsolved problem or limitation in prior work
- Paper's stated objective

4. Method / 方法
- Overall framework
- Core model, algorithm, experiment workflow, or theoretical derivation
- Formula list with variable definitions, units, and assumptions
- Implementation details if present

5. Experiments or Evidence / 實驗、模擬或論證證據
- Dataset/sample/device/software/environment
- Parameter settings
- Baselines or controls
- Evaluation metrics

6. Results / 結果分析
- Key quantitative results
- Figure/table-by-figure/table interpretation
- What each result supports
- Any contradictory or weak evidence

7. Contributions and Novelty / 創新點
- Contribution claimed by the authors
- Evidence from the paper
- Whether the novelty is methodological, experimental, theoretical, application-oriented, or system-level

8. Limitations / 侷限性
- Limitations stated by the authors
- Limitations inferred from scope, assumptions, dataset, sample size, metrics, or missing ablation
- Label inferred points clearly

9. Reproducibility / 可覆現要點
- Required data, code, instruments, software, versions, parameters, and steps
- Missing details that prevent reproduction

10. Relationship to User Topic / 與使用者課題關系
- Directly reusable ideas
- Cautions before reuse
- Possible extension experiments or simulations

11. Presentation Notes / 匯報講稿要點
- 5-minute version
- 10-minute version
- likely questions from supervisor or audience

12. Reference Trace Table / 原文依據索引表
- Claim
- Source location
- Evidence type: text, equation, figure, table, experiment
- Confidence: high, medium, low

## Chinese-Only Report

Use the same intellectual structure, but make all explanatory prose Chinese. Preserve English titles, model names, software names, formulas, variable symbols, datasets, and cited reference names.

Recommended Chinese headings:
- 文獻資訊
- 一頁式摘要
- 閱讀路線
- 研究背景與問題
- 方法與模型
- 實驗/模擬/資料設定
- 結果與圖表解讀
- 創新點與貢獻
- 侷限性與邊界條件
- 可覆現要點
- 與使用者課題的關系
- 匯報講稿要點
- 原文依據索引表

## Evidence Label Format

Preferred:
- `來源: Section 2.1, p. 3`
- `來源: Methods, pp. 4-5, Eq. (3)`
- `來源: Results, Fig. 5 and Table 2`
- `來源: 原文 Discussion, p. 9`

If exact location is unavailable:
- `來源: 原文未提供頁碼；見 Results 小節關於 Fig. 4 的段落`
- `來源: PDF 文字提取未識別章節號；見第 6 頁表格下方段落`

Inference labels:
- `推斷: 基於作者實驗設定和缺失消融項`
- `建議: 可作為後續模擬實驗方向，非原文結論`

## Quality Checklist

Before final delivery:
- Both reports exist and open.
- Chinese text is readable, not garbled.
- Each key conclusion has a source label.
- Quantitative values match the paper.
- Figures, tables, and equations are not misnumbered.
- Inferred comments are not mixed with original claims.
- The report notes missing information honestly.
- The final answer lists exact output paths and verification.
