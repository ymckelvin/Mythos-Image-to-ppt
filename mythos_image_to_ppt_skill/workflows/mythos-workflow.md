# Mythos Workflow

```text
1. Input source image
2. VisionParseAgent parses sections, groups, elements, relationships
3. LayoutAgent builds layout tree
4. TypographyAgent reconstructs editable text
5. AssetExtractAgent extracts high-resolution visual assets
6. PPTCompilerAgent compiles layout tree into PPTX
7. Render PPTX into screenshot
8. VisualDiffAgent compares source image and rendered screenshot
9. QAAgent validates editability and quality
10. RepairAgent routes issues and triggers rebuild
11. Export final design reconstruction package
```
