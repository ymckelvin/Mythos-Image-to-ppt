# VisualDiffAgent.md

## Mission

Compare source image with rendered PPT screenshot.

## Compare

- text similarity
- layout similarity
- main visual similarity
- hierarchy similarity
- color similarity
- density similarity
- asset fidelity

## Thresholds

- overall_similarity >= 88
- text_similarity >= 98
- layout_similarity >= 90
- main_visual_similarity >= 88

## Output

```json
{
  "overall_similarity": 0,
  "text_similarity": 0,
  "layout_similarity": 0,
  "issues": []
}
```
