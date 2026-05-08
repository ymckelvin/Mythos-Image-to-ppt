# Mythos: Image to PPT

Mythos: Image to PPT is an agentic skill for reconstructing static images, generated posters, design screenshots, or PPT screenshots into editable PowerPoint engineering files.

It focuses on:

- high visual fidelity
- editable text and shapes
- layout structure preservation
- multi-agent QA
- screenshot-based visual diff
- repair loop

## Core Pipeline

```text
Source Image
→ VisionParseAgent
→ LayoutAgent
→ TypographyAgent
→ AssetExtractAgent
→ PPTCompilerAgent
→ QAAgent
→ VisualDiffAgent
→ RepairAgent
→ Final Editable PPT
```

## Repository Structure

```text
mythos-image-to-ppt-skill/
├── skill.md
├── README.md
├── agents/
│   ├── VisionParseAgent.md
│   ├── LayoutAgent.md
│   ├── TypographyAgent.md
│   ├── AssetExtractAgent.md
│   ├── PPTCompilerAgent.md
│   ├── QAAgent.md
│   ├── VisualDiffAgent.md
│   └── RepairAgent.md
├── schemas/
│   └── layout-schema.json
├── qa/
│   └── quality-rubric.md
├── repair/
│   └── repair-rules.json
├── workflows/
│   └── mythos-workflow.md
├── docs/
│   ├── github-upload-guide.md
│   └── vision-failure-taxonomy.md
└── examples/
```

## Philosophy

Mythos does not aim to generate a PPT-looking image.

It aims to reconstruct a design into an editable working file.

```text
70% Fidelity
30% Engineering
```
