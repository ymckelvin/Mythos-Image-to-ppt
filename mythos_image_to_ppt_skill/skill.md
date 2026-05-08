# Mythos: Image to PPT
## skill.md v1

---

# Overview

Mythos: Image to PPT 是一个 AI Native 的设计重建系统。

它的目标不是生成一个“像 PPT 的图片”，而是高保真地重建一个真正可编辑的设计工程文件。

```text
Image
↓
Design Understanding
↓
Layout Tree
↓
Multi-Agent QA
↓
Repair Loop
↓
Editable PPT
```

---

# Core Philosophy

## 1. Structure First

页面必须被理解为：

```text
Slide
→ Section
→ Group
→ Element
```

而不是随机元素。

## 2. Fidelity First

目标：

```text
70% Fidelity
30% Engineering
```

优先：

- 原图视觉一致
- 信息层级一致
- 主视觉一致
- 页面气质一致

## 3. Editable Engineering

最终输出必须：

- text editable
- group preserved
- shape native
- layout stable

禁止：

```text
full slide screenshot
```

---

# Editable Boundary

## 必须结构化

以下必须 editable：

- 标题
- 正文
- KPI
- Button
- Card
- Workflow Node
- Layout Structure
- Table Text
- Comparison Block

## 允许 Raster

以下允许图片化：

- 人物
- 产品图
- 光效
- 插画
- 背景
- mesh gradient

前提：不影响文字编辑。

---

# Core Agents

## VisionParseAgent

负责：

- section parsing
- group detection
- semantic parsing
- reading order
- relationship understanding

目标：理解设计结构，而不是仅 OCR。

## LayoutAgent

负责：

- alignment
- spacing
- hierarchy
- layout graph
- group preservation

目标：页面必须“稳”。

## TypographyAgent

负责：

- OCR fidelity
- text reconstruction
- typography hierarchy
- overflow prevention

禁止 AI rewrite text。

## AssetExtractAgent

负责：

- logo extraction
- icon extraction
- high-resolution asset export
- background separation

默认 2K+。

## PPTCompilerAgent

负责：

```text
Layout Tree
↓
Editable PPT
```

输出：

- textbox
- shape
- image
- group
- z-index
- section hierarchy

## QAAgent

负责：

- editable validation
- layout validation
- OCR validation
- hierarchy validation
- density validation

## VisualDiffAgent

负责：

```text
Source Image
VS
Rendered PPT Screenshot
```

检查：

- text similarity
- layout similarity
- hierarchy similarity
- density similarity
- asset fidelity

## RepairAgent

负责：

```text
Generate
↓
Inspect
↓
Repair
↓
Rebuild
```

---

# Multi-Agent Flywheel

```text
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
```

默认最多 3 iterations。

---

# Quality Priorities

## Priority 1 — Editable Fidelity

最重要：

- 真正可编辑
- 不 flatten
- 不整页截图
- text editable
- group preserved
- shape native

## Priority 2 — Text Fidelity

必须：

- 不错字
- 不漏字
- 不乱码
- 不 AI 改写

标题和 KPI 必须 100% accurate。

## Priority 3 — Visual Fidelity

必须：

- 主视觉一致
- layout 一致
- hierarchy 一致
- density 一致

## Priority 4 — Layout Stability

必须：

- alignment stable
- spacing stable
- reading flow stable

---

# Layout Schema Philosophy

Layout 不是坐标系统，而是关系系统。

核心关系：

- belongs_to
- layer_above
- aligned_with
- same_spacing_as
- reading_order

---

# Vision Failure Taxonomy

Mythos 特别警惕：

## Structural Failures

- card boundary failure
- merged table failure
- flow arrow failure

## Hierarchy Failures

- annotation loss
- reading order collapse

## Semantic Failures

- icon semantic failure
- workflow logic failure
- color semantic failure

## Visual Failures

- layout drift
- density collapse
- low-resolution assets

---

# Final Outputs

Mythos 输出：

```text
output/
├── final_ppt/
├── layout_json/
├── assets/
├── rendered_slides/
├── qa_reports/
├── visual_diff/
├── repair_logs/
└── metadata/
```

---

# Final Goal

Mythos 最终目标不是 Image → PPT，而是 Design Understanding Engine。

未来支持：

- PPT
- Figma
- HTML
- React
- Design Systems

---

# Final Principle

Mythos 的核心目标：

> 高保真地重建一个真正还能继续工作的设计工程文件。
