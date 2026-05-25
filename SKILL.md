---
name: commercial-storyboard-generator
description: generate professional commercial advertising storyboard boards, campaign boards, product ad concepts, and final image-generation prompts from a brand/product brief. use when the user asks for a 16:9 ad storyboard, commercial storyboard sheet, campaign board, product visual proposal, social video storyboard, key visual plus 10-panel layout, or final storyboard image based on brand, product, target audience, consumer problem, desired transformation, tone, text language, and board title/headline.
---

Use this skill to turn a product brief into a professional commercial storyboard board workflow.

## Non-negotiable Core Brief Gate

Before doing any creative strategy, storyboard design, final prompt writing, negative prompt writing, or image generation, run the Core Brief Gate.

The Core Brief Gate must verify these 8 fields:
1. Brand
2. Product
3. Target Audience
4. Consumer Problem
5. Desired Transformation
6. Tone
7. Text Language
8. Board Title / Main Headline

If any core field is missing, incomplete, vague, or only implied, stop immediately and ask the user to provide only the missing fields using [references/response-template.md](references/response-template.md).

Do not proceed to strategy, storyboard, final prompt, or image generation until all 8 core fields are present.

Never infer or invent core fields. Only infer non-core fields.

## Primary workflow

1. Detect whether the user wants strategy only, prompt only, storyboard only, or a final image.
2. Run the Core Brief Gate.
3. If any core field is missing, ask only for the missing fields and stop.
4. If all core fields are present, continue automatically.
5. Infer missing non-core fields and label them as reasonable assumptions.
6. Build the creative strategy.
7. Design exactly 10 storyboard panels.
8. Generate the final English image prompt.
9. If the user explicitly wants an image, generate one single 16:9 storyboard image.
10. Validate the output with the quality checklist.

For full field definitions, aliases, and missing-field behavior, consult [references/input-schema.md](references/input-schema.md).

## Output modes

Use Mode C.

- If the user asks for a prompt, strategy, or storyboard only, stop before image generation.
- If the user asks for a final image, complete the strategy, storyboard, prompt, and then generate the image.
- If the user's request is ambiguous, generate the strategy, storyboard, and prompt first, then ask whether they want the image generated.
- If image generation is requested but any core field is missing, ask for the missing fields first.

## Trigger interpretation

Treat these requests as in scope:
- a 16:9 commercial storyboard board
- campaign board
- product ad storyboard
- social video storyboard
- product visual proposal
- key visual plus 10 panels
- advertising storyboard prompt
- image prompt for a commercial storyboard sheet
- final storyboard image for a brand, product, audience, and pain point

Treat these as out of scope unless the user explicitly asks for storyboard-board output:
- logo-only design
- generic copywriting
- single product packshot only
- ordinary moodboard without story structure
- long-form article writing

## Required output logic

Always ensure all of the following are true:
- The product is the trigger of transformation, not a passive prop.
- The layout is one single 16:9 board.
- The board uses TOP / MIDDLE / BOTTOM sections.
- TOP contains the key visual.
- MIDDLE contains exactly 10 storyboard panels.
- BOTTOM contains a product packshot, branding, and tagline.
- The board title / main headline appears clearly in the TOP or BOTTOM section.
- The story arc clearly moves from problem to trigger to transformation to payoff to ending.
- The visual language shows a clear Before / After contrast.
- Shot types vary and do not repeat mechanically.
- The final image prompt is written in English.
- Text that appears inside the generated image uses the user's selected text language.

## Creative strategy procedure

Only start this procedure after the Core Brief Gate passes.

1. Summarize the brief in a compact table.
2. Identify or infer the product category.
3. Generate one Key Idea using this formula:
   - {problem state} -> {product usage} -> {desired transformation}
4. Select the best story structure. For structure definitions, consult [references/story-structures.md](references/story-structures.md).
5. Build a Before / Trigger / After performance arc.
6. Pick the visual language based on category. Consult [references/product-visual-language.md](references/product-visual-language.md).
7. Design the 10 storyboard panels using [references/storyboard-panel-template.md](references/storyboard-panel-template.md).
8. Assemble the final image prompt using [references/final-prompt-template.md](references/final-prompt-template.md).
9. Format the response using [references/response-template.md](references/response-template.md).
10. Validate the plan against [references/quality-checklist.md](references/quality-checklist.md).

## Response formatting

Use [references/response-template.md](references/response-template.md) as the default response contract. Keep the response concise when the user asks for speed, but do not omit:
- Core Brief Gate when fields are incomplete
- creative strategy
- board title / main headline
- exactly 10 storyboard panels
- final English image prompt when requested
- final image generation when explicitly requested

## Image generation rules

When generating the final image:
- Create one single 16:9 storyboard board.
- Require exactly 10 storyboard panels.
- Require a clear editorial commercial layout.
- Include the board title / main headline visibly in the TOP or BOTTOM section.
- Use the user's requested text language for visible captions, headline, and taglines.
- Keep logos, label design, and packaging as accurate as possible, but note that text and logos may still need post-production correction.

## Reference image safety

If the user provides reference images or asks to match a moodboard:
- Use reference images only for mood, energy, styling, outfit direction, and color palette.
- Do not replicate any real person's face.
- Create a completely new fictional character.
- Preserve product shape, packaging, label design, and branding as much as possible.

## Tone and quality bar

Keep the output commercially useful.
- Be precise.
- Be execution-focused.
- Avoid vague praise.
- Avoid weak storytelling.
- Avoid letting the board become only a collage of pretty shots.
- Challenge weak briefs by identifying missing consumer problem, weak transformation, or unclear product role.
- Be assertive about collecting the 8 core fields.

## Example

For a worked example, consult [references/example-pocari-sweat.md](references/example-pocari-sweat.md).
