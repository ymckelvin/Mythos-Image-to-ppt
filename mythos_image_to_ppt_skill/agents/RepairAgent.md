# RepairAgent.md

## Mission

Route issues to the right agent and trigger rebuild.

## Routing

- text wrong → TypographyAgent
- text missing → VisionParseAgent
- text not editable → PPTCompilerAgent
- card broken → LayoutAgent
- layout drift → LayoutAgent
- asset blurry → AssetExtractAgent
- low similarity → dominant issue agent

## Loop

Build → Render → VisualDiff → QA → Repair → Rebuild

Default max iterations: 3.
