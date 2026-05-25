# Response Template

Use this template to keep every run consistent. Adapt detail level to the user request, but preserve the section order unless the user asks for a shorter response.

## Core Brief Gate Response

If any core field is missing, incomplete, vague, or only implied, stop and use this exact response pattern:

```markdown
**目前還缺少以下核心欄位，補齊後我才能開始產出分鏡提案：**

| 缺少欄位 | 請提供內容 |
|---|---|
| [Missing Core Field 1] | [Short instruction] |
| [Missing Core Field 2] | [Short instruction] |

請直接補上以上欄位即可。  
我收到後會依序完成：
1. 補齊創意策略
2. 生成 Key Idea
3. 設計 exactly 10 格分鏡
4. 生成 final English image prompt
5. 如你有要求，產出 one single 16:9 storyboard image
```

Do not provide partial creative strategy, storyboard panels, final image prompts, negative prompts, or images while core fields are missing.

## Default Full Response Structure

```markdown
**1. Brief Understanding**

| Field | Content | Source |
|---|---|---|
| Brand |  | user-provided |
| Product |  | user-provided |
| Product Category |  | user-provided / reasonable assumption |
| Target Audience |  | user-provided |
| Consumer Problem |  | user-provided |
| Desired Transformation |  | user-provided |
| Tone |  | user-provided |
| Text Language |  | user-provided |
| Board Title / Main Headline |  | user-provided |
| Key Benefit |  | user-provided / reasonable assumption |
| Usage Occasion |  | user-provided / reasonable assumption |

**2. Creative Strategy**

- Board Title / Main Headline:
- Key Idea:
- Story Structure:
- Brand Role:
- Product Role:
- Core Flow: problem -> trigger -> transformation -> payoff -> ending

**3. Performance Arc**

| Stage | Character State | Emotion | Body Language | Visual Language |
|---|---|---|---|---|
| Before |  |  |  |  |
| Trigger |  |  |  |  |
| After |  |  |  |  |

**4. Storyboard Design: Exactly 10 Panels**

| Panel | Story Beat | Shot Type | Visual Description | Product Role | Caption |
|---|---|---|---|---|---|
| 1 | Problem situation | Wide shot |  |  |  |
| 2 | Pain point detail | Extreme close-up |  |  |  |
| 3 | POV confusion or frustration | POV shot |  |  |  |
| 4 | Product discovery | Low angle or over-shoulder |  |  |  |
| 5 | Product interaction | Macro close-up |  |  |  |
| 6 | Usage moment | Slow-motion close-up |  |  |  |
| 7 | Transformation explosion | Dynamic angle |  |  |  |
| 8 | Environment change | Wide environmental shot |  |  |  |
| 9 | Character reaction | Medium close-up |  |  |  |
| 10 | Confident payoff | Hero action shot |  |  |  |

**5. Layout Architecture**

| Section | Ratio | Function | Content |
|---|---:|---|---|
| TOP | 40% | Key Visual + headline |  |
| MIDDLE | 35% | 10-panel storyboard |  |
| BOTTOM | 25% | Product + Branding |  |

**6. Color System**

| Stage | Color | Emotion | Purpose |
|---|---|---|---|
| Before |  |  |  |
| Trigger |  |  |  |
| After |  |  |  |

**7. Final English Image Prompt**

```text
[final prompt]
```

**8. Negative Prompt**

```text
[negative prompt]
```

**9. Final Check**

| Check | Status | Note |
|---|---|---|
| All 8 core fields present | pass/fail |  |
| Product is the trigger | pass/fail |  |
| Board title / headline visible | pass/fail |  |
| Exactly 10 panels | pass/fail |  |
| TOP / MIDDLE / BOTTOM structure | pass/fail |  |
| Packshot + branding included | pass/fail |  |
| Clear Before / After contrast | pass/fail |  |
| Varied shot types | pass/fail |  |
```

## Image Mode Response

When image generation is explicitly requested, do not stop after the prompt. Generate the one single 16:9 storyboard image after preparing the prompt.

After image generation, give only a short note if needed:

```markdown
**Generated output note**
The image follows the 16:9 storyboard board structure. Brand text and logos may still need post-production correction for client-facing use.
```
