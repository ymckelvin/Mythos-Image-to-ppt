# Mythos: Image to PPT
## skill.md（中文版注释版）

---

# Overview（项目概述）

> 中文说明：
> Mythos 不只是一个 “图片转 PPT” 工具。
> 它的核心目标是：
> “高保真地重建一个真正可编辑的设计工程文件”。

Mythos: Image to PPT 是一个 AI Native 的设计重建系统。

它的目标不是：

- 生成一个“像 PPT 的图片”

而是：

- 高保真地重建一个真正可编辑的设计工程文件

---

# Core Philosophy（核心哲学）

## 1. Structure First（结构优先）

> 中文说明：
> AI 不应该把页面理解成随机元素。
> 而应该理解成：页面 → 模块 → 卡片 → 元素。

页面必须被理解为：

Slide
→ Section
→ Group
→ Element

---

## 2. Fidelity First（高保真优先）

> 中文说明：
> Mythos 不是重新设计。
> 而是尽量还原原图视觉关系。

目标：

70% Fidelity
30% Engineering

优先：

- 原图视觉一致
- 信息层级一致
- 主视觉一致
- 页面气质一致

---

## 3. Editable Engineering（可编辑工程化）

> 中文说明：
> 最终输出必须真的能改。
> 不能只是截图贴回 PPT。

最终输出必须：

- text editable
- group preserved
- shape native
- layout stable

禁止：

- full slide screenshot

---

# Core Agents（核心 Agent）

## VisionParseAgent

> 中文说明：
> 负责“看懂设计结构”。
> 它不是 OCR，而是设计理解。

职责：

- section parsing
- group detection
- semantic parsing
- reading order
- relationship understanding

---

## LayoutAgent

> 中文说明：
> 负责“重建设计关系”。
> 它决定页面稳不稳。

职责：

- alignment
- spacing
- hierarchy
- layout graph
- group preservation

---

## TypographyAgent

> 中文说明：
> 负责 OCR、文字还原、排版与可编辑性。

负责：

- OCR fidelity
- text reconstruction
- typography hierarchy
- overflow prevention

禁止：

- AI rewrite text

---

## AssetExtractAgent

> 中文说明：
> 负责拆解 logo、icon、主视觉、背景等资产。
> 默认输出高清资源。

默认：

2K+

---

## VisualDiffAgent

> 中文说明：
> 核心能力：
> “生成以后自己截图和原图比对”。

负责：

Source Image
VS
Rendered PPT Screenshot

检查：

- text similarity
- layout similarity
- hierarchy similarity
- density similarity
- asset fidelity

---

# Multi-Agent Flywheel（多 Agent 飞轮）

> 中文说明：
> Mythos 不相信第一次生成结果。
> 而是不断检查 → 修复 → 重建。

Generate
↓
Render
↓
Visual Diff
↓
QA
↓
Repair
↓
Rebuild

默认：

3 iterations

---

# Final Outputs（最终输出）

> 中文说明：
> Mythos 输出的不是单个 PPT。
> 而是一整套设计工程文件。

output/
├── final_ppt/
├── layout_json/
├── assets/
├── rendered_slides/
├── qa_reports/
├── visual_diff/
├── repair_logs/
└── metadata/

---

# Final Goal（最终目标）

> 中文说明：
> Mythos 本质上已经不是 “Image to PPT”。
> 而是一个：
> “Design Understanding Engine（设计理解引擎）”。

未来支持：

- PPT
- Figma
- HTML
- React
- Design Systems

---

# Final Principle（最终原则）

> 中文说明：
> Mythos 的最终目标不是生成 PPT。
> 而是：

“高保真地重建一个真正还能继续工作的设计工程文件”
