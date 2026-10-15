# Academic Skills for Claude Code & Codex

> 三個面向中國科研工作者的學術技能包，覆蓋論文寫作、學術 Office 文件生成與科研計算三大場景。
> 所有 skill 均可在 **Claude Code** 和 **Codex** 兩個平台上直接使用。

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Claude%20Code-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Platform-Codex%20CLI-brightgreen?style=flat-square" />
  <img src="https://img.shields.io/badge/Language-Chinese--first-red?style=flat-square" />
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Skills-3-purple?style=flat-square" />
</p>

---

## 技能概覽

| 技能 | 核心用途 | 典型場景 |
|------|----------|----------|
| [`research-writing-skill`](#1-research-writing-skill--論文寫作) | 論文章節撰寫、修改、潤色 | 論文正文、摘要、引言、方法、實驗、回覆審稿人 |
| [`office-academic-skill`](#2-office-academic-skill--學術-office-文件) | 學術 Word/PPT 生成與編輯 | 文獻閱讀報告、組會 PPT、開題/中期/答辯 PPT |
| [`scientific-toolkit-skill`](#3-scientific-toolkit-skill--科研計算工具箱) | 科研計算與資料分析 | MATLAB/Python 模擬、訊號處理、統計、機器學習、論文配圖 |

三個 skill 設計為**互補協作**關係，可在同一任務中聯動呼叫：

```
論文寫作場景：
  scientific-toolkit-skill（資料分析、出圖）
  → research-writing-skill（撰寫論文正文）
  → office-academic-skill（生成答辯 PPT）

文獻閱讀場景：
  office-academic-skill（PDF → Word 閱讀報告）
  → office-academic-skill（組會 PPT）

模擬研究場景：
  scientific-toolkit-skill（MATLAB/Python 模擬 + 論文配圖）
  → research-writing-skill（方法 + 實驗章節）
```

---

## 1. research-writing-skill — 論文寫作

**中文優先**的學術寫作技能，適用於論文正文、LaTeX/Overleaf 文稿、學位論文等。

### 功能

- 論文各章節撰寫：摘要、引言、相關工作、方法、實驗、討論、結論
- 論文修改與潤色：邏輯性、術語一致性、引用準確性
- 審稿意見回覆（Rebuttal / Peer-review response）
- 論證規劃：從模糊想法到論文大綱

### 寫作原則

- 預設中文表達，保留英文標題、公式、變數、方法名、軟體命令、參考文獻
- 不編造資料、DOI、期刊資訊、實驗結果
- 區分「原文/已有資料」「使用者確認內容」「推斷」「建議性擴充套件」四類資訊
- 避免「顯著」「先進」「有效」等模糊用詞，代之以可測量的條件和對比基準

### 內建參考資源

| 路徑 | 內容 |
|------|------|
| `paper-writing/section_rhetorical_moves/` | 各章節修辭結構指南 |
| `paper-writing/writing_checklists/` | 寫作自查清單 |
| `paper-writing/figure_templates/` | 圖表規劃模板 |
| `paper-writing/brainstorming_guide.md` | 從想法到論文藍圖 |

---

## 2. office-academic-skill — 學術 Office 文件

**中文優先**的學術 Word 和 PowerPoint 工作流，生成可編輯的 `.docx` 和 `.pptx` 檔案。

### 功能

**Word 文件**

- PDF/論文 → 文獻閱讀報告（雙語或中文）
- 結構化 DOCX 生成：標題、表格、圖表佔位符、來源標註
- 對已有 Word 文件進行版本化編輯

**PowerPoint 簡報**

- 文獻報告 PPT、組會 PPT、課程報告 PPT
- 開題/中期/答辯 PPT（模板匹配、母版克隆）
- 科研展示 PPT、科普 PPT

### PPT 質量規則

- 每頁一個核心觀點，使用「行動標題」（陳述結論而非話題標籤）
- 圖表、公式承載技術論證，避免大段文字
- 保持座標軸、單位、圖例、公式、資料來源的科學準確性
- 白色或剋制的學術背景，用顏色引導注意力

### 內建參考資源與工具

| 路徑 | 內容 |
|------|------|
| `office-docx/` | OOXML 級別 DOCX 檢查與編輯，含 XSD 模式庫 |
| `office-pptx/` | OOXML 級別 PPTX 檢查與編輯 |
| `thesis-defense-pptx/scripts/` | 論文上下文提取、模板克隆、幻燈片匯出、溢位檢查等工具指令碼 |
| `report-structure.md` | 預設文獻報告結構與證據標註格式 |

---

## 3. scientific-toolkit-skill — 科研計算工具箱

面向**光電資訊科學與工程**領域的科研計算技能。

### 功能

**MATLAB/Octave**

- 訊號/影象處理、FFT、濾波、矩陣計算、模擬、論文配圖匯出
- 保留原始程式碼結構，集中管理關鍵引數，新增物理意義註釋

**Python 科學計算**

| 庫 | 用途 |
|----|------|
| NumPy, SciPy, pandas | 資料處理與數值計算 |
| matplotlib, seaborn | 論文級資料視覺化 |
| scikit-learn | 機器學習（分類、迴歸、聚類、降維）|
| statsmodels | 統計建模（線性模型、時間序列、GLM）|
| SymPy | 符號數學與公式推導 |
| pymoo | 多目標最佳化 |
| simpy | 離散事件模擬 |
| QuTiP | 量子光學/開放量子系統 |
| pymatgen | 材料科學計算（晶體結構、能帶、態密度）|
| TimesFM | 時間序列預測 |
| NetworkX | 圖與網路分析 |
| Astropy | 天文/光學成像資料處理 |

**文獻與引用**

- 論文查詢：arXiv, PubMed, CrossRef, Semantic Scholar, OpenAlex
- 引文管理：DOI → BibTeX，文獻後設資料提取，引文驗證

### 領域關注

- 光學、光電子、光通訊、光纖感測
- BOTDR/BOTDA、BGS、SPM、色散、噪聲、去卷積
- 光譜學、探測器資料、感測器時間序列、標定與不確定度

### 內建參考資源

20+ 子模組的詳細參考文件、指令碼模板和示例，包括 matplotlib 出圖模板、統計檢驗選擇指南、scikit-learn 分類管線等。

---

## 跨平台安裝

三個 skill 採用相同的目錄結構和 SKILL.md 格式，在 Claude Code 和 Codex 中均可直接載入。

### Claude Code

```bash
# 克隆倉庫
git clone https://github.com/你的使用者名稱/claude-academic-skills.git

# 安裝到全域性 skills 目錄
cp -r claude-academic-skills/research-writing-skill ~/.claude/skills/
cp -r claude-academic-skills/office-academic-skill ~/.claude/skills/
cp -r claude-academic-skills/scientific-toolkit-skill ~/.claude/skills/
```

也可透過 Plugin 方式一鍵安裝：

```bash
/plugin install 你的使用者名稱/claude-academic-skills
```

### Codex

```bash
# 安裝到全域性 skills 目錄
cp -r claude-academic-skills/research-writing-skill ~/.codex/skills/
cp -r claude-academic-skills/office-academic-skill ~/.codex/skills/
cp -r claude-academic-skills/scientific-toolkit-skill ~/.codex/skills/
```

也可透過 `--plugin-url` 引數在當前會話中直接載入：

```bash
codex --plugin-url https://github.com/你的使用者名稱/claude-academic-skills
```

> 如需**專案級安裝**，將 skill 目錄放入專案根目錄下的 `.claude/skills/` 或 `.codex/skills/` 即可，僅對該專案生效。

---

## 目錄結構

每個 skill 統一採用以下結構：

```
skill-name/
├── SKILL.md          # 技能定義與使用說明
├── agents/           # 子代理配置
└── references/       # 參考文件、指令碼、模板等資源
```

---

## 語言與證據規範

三個 skill 共同遵循以下規範：

| 規範 | 說明 |
|------|------|
| **預設中文** | 解釋、正文撰寫、幻燈片製作均使用中文 |
| **保留英文** | 論文標題、公式、變數名、模型名、軟體命令、參考文獻條目 |
| **不編造資料** | 不虛構 DOI、作者、期刊、實驗值、圖表編號、頁碼、結論 |
| **標註來源** | 對宣告、引數、定量結果、資料集、圖表等附加來源標籤 |

---

## 致謝

本專案在設計過程中參考了以下優秀的開源 Skill 專案，感謝這些作者的公開貢獻：

| 專案 | 簡介 |
|------|------|
| [zouchenzhen/thesis-defense-pptx-skill](https://github.com/zouchenzhen/thesis-defense-pptx-skill) | 從論文 PDF/LaTeX 生成可編輯答辯 PPTX，支援模板風格保留、逐頁 PNG 匯出與文字溢位檢查，專為 Windows + PowerPoint 環境最佳化 |
| [K-Dense-AI/scientific-agent-skills](https://github.com/K-Dense-AI/scientific-agent-skills) | 134+ 科研 Agent Skill 集合，涵蓋 MATLAB/Octave、Matplotlib、訊號處理、科學視覺化等模組 |
| [tfriedel/claude-office-skills](https://github.com/tfriedel/claude-office-skills) | 系統化的 Office 文件處理 Skill 集，包含 docx/、pptx/、pdf/、xlsx/ 四個子模組，結構清晰 |
| [Gabberflast/academic-pptx-skill](https://github.com/Gabberflast/academic-pptx-skill) | 專注學術 PPT 規範：結論式標題、每頁一個核心觀點、圖表引用標準與參考文獻頁 |
| [SNL-UCSB/paper-writing-skill](https://github.com/SNL-UCSB/paper-writing-skill) | 編碼了經過驗證的論文寫作原則，涵蓋論證邏輯、圖表支撐、初稿重構與壓縮 |

---

## 許可

本倉庫採用 [MIT License](LICENSE) 開源許可。

- 你可以自由使用、複製、修改、合併、釋出、分發、再許可和/或銷售軟體的副本
- 需在軟體所有副本或實質性部分中保留版權宣告和本許可宣告
- 軟體按「原樣」提供，不提供任何形式的明示或暗示保證

其中引用的部分外部資源（如 `scientific-toolkit-skill/references/scientific-skills/` 中的指令碼）遵循其原始許可協議。
