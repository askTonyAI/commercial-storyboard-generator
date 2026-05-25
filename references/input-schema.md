# Input Schema

## Core Brief Gate

These 8 fields are required. If any core field is missing, incomplete, vague, or only implied, stop and ask only for the missing fields.

Do not proceed to creative strategy, storyboard panels, final prompt, negative prompt, or image generation until all 8 core fields are present.

| Core Field | Purpose | Example |
|---|---|---|
| Brand | Define the advertiser and branding context | Pocari Sweat |
| Product | Define the product hero and usage | Pocari Sweat bottle |
| Target Audience | Define the character, scene, and emotional tone | Women athletes aged 18-25 |
| Consumer Problem | Define the story starting point | Exhausted, thirsty, unfocused after training in hot weather |
| Desired Transformation | Define the story ending | Regain energy and clarity after one refreshing drink |
| Tone | Define the emotional and visual direction | BRIGHT + SPORTY |
| Text Language | Define the language used inside the image | Korean |
| Board Title / Main Headline | Define the main communication line shown on the board | One Sip Reset |

## Field Alias Map

Recognize these aliases as equivalent fields.

| Core Field | Acceptable Aliases |
|---|---|
| Brand | 品牌, 品牌名稱, 客戶, 廣告主, Brand |
| Product | 產品, 商品, 服務, 主打品項, Product |
| Target Audience | 目標對象, TA, 受眾, 族群, 消費者, Target |
| Consumer Problem | 痛點, 問題, 情境問題, 想解決的問題, 困擾 |
| Desired Transformation | 產品轉變, 使用後改變, Before After, 希望產生的轉變, 效果 |
| Tone | 調性, 風格, 視覺語氣, 氛圍, Tone |
| Text Language | 圖中文字語言, 畫面文字語言, 字幕語言, Caption language |
| Board Title / Main Headline | 標題, 主標, 主視覺標題, 分鏡圖標題, Headline, Main headline |

## Core Field Assumption Rule

Never infer or invent these core fields:
- Brand
- Product
- Target Audience
- Consumer Problem
- Desired Transformation
- Tone
- Text Language
- Board Title / Main Headline

If the user explicitly asks the assistant to assume missing information, only infer non-core fields. Still ask for any missing core fields.

## Non-core fields

These fields are optional. Infer them when helpful and label them as reasonable assumptions.

| Field | Purpose |
|---|---|
| Product Category | Food, beverage, beauty, fashion, travel, technology, service, or other |
| Key Benefit | Most important benefit or promise |
| Reason to Believe | Why the audience should believe the promise |
| Usage Occasion | When and where the product is used |
| Required Elements | Mandatory brand or scene elements |
| Avoid | Visual or brand constraints to avoid |
| Reference Images | Mood, styling, color, or packaging guidance |
| Tagline | Closing brand line if different from the board title |

## Missing-field policy

- Missing core fields: ask for them and stop.
- Vague core fields: ask for clarification and stop.
- Missing non-core fields: infer them and mark them as reasonable assumptions.
- Missing product category: infer from the product.
- Missing usage occasion: infer from audience + problem.
- Missing key benefit: infer from the product + desired transformation.

## Preflight Check

Before producing creative strategy, run this check internally:

| Core Field | Status |
|---|---|
| Brand | present / missing / vague |
| Product | present / missing / vague |
| Target Audience | present / missing / vague |
| Consumer Problem | present / missing / vague |
| Desired Transformation | present / missing / vague |
| Tone | present / missing / vague |
| Text Language | present / missing / vague |
| Board Title / Main Headline | present / missing / vague |

If any status is missing or vague, ask only for those fields and stop.

## Preferred user input format

Encourage this format when the user needs a template:

- Brand:
- Product:
- Target Audience:
- Consumer Problem:
- Desired Transformation:
- Tone:
- Text Language:
- Board Title / Main Headline:
- Product Category:
- Key Benefit:
- Usage Occasion:
- Required Elements:
- Avoid:
