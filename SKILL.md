---
name: storyboard-tiktok-video
description: Use when a user wants a TikTok/TK product-video storyboard from a product link, product image, product screenshot, ecommerce page, or short product description. The required output format is product image first, then storyboard image, then 15-second or 30-second video script text. Especially useful for FYPro, StoreClaw, or image-to-video workflows where the user wants clear product truth before video generation.
---

# 故事版的 TikTok 视频 Skill

## Purpose

Turn a product into a TikTok-ready video storyboard package with exactly three default sections:

1. 产品图
2. 故事版
3. 15 秒或者 30 秒视频脚本文字

This skill is intentionally narrow. It is for product-facing TikTok/TK demo work where the user wants a clean handoff before video generation.

Important: once a storyboard image exists, that storyboard becomes the visual source of truth. Do not invent a new person, outfit, room, product angle, or scene style in later script or keyword work.

## When To Use

Use this skill when the user asks for:

- TikTok/TK product video storyboards.
- FYPro, StoreClaw, or image-to-video preparation.
- "先产品图，再故事版，再脚本".
- More products from one brand, each with a product image and storyboard.
- A clearer product demo format for creators, social media, affiliates, or UGC ads.

Do not use this skill for generic marketing copy, long ad strategy, product listing copy, or full campaign reports unless the user explicitly asks to expand beyond the three-section output.

## Core Rule

Default output must contain only these three sections for each product:

```text
## 1. 产品图
## 2. 故事版
## 3. 15 秒或者 30 秒视频脚本文字
```

Do not include FYPro keywords, negative prompts, correction prompts, product-truth cards, long platform analysis, source notes, or extra recommendations by default.

If the user asks for FYPro keywords later, provide them as a separate follow-up output.

## No Autonomous Regeneration

Do not generate new images just because the user asks for keywords, scripts, or video prompts.

Only generate or regenerate images when the user explicitly asks for:

- 故事版
- 生图
- 换一个图
- 重画
- 重新生成
- 多给几张图

If a storyboard already exists and the user asks for keywords or video text, write from the existing storyboard. Do not create a new visual direction.

## Product Intake

Accept any of these inputs:

- Product URL
- Product image
- Product screenshot
- Product name and brand
- Ecommerce page
- Chat context that contains a product link or product direction

If the user gives a brand and asks for more products, find 2-3 suitable products from that brand. Choose products that are visually demonstrable in TikTok:

- obvious before/use/payoff sequence,
- simple household or lifestyle action,
- strong visual texture or movement,
- low compliance risk,
- easy for image/video generation tools to understand.

## Product Image Rules

The first section must show or link the product image before any storyboard.

Prefer official product images from the brand site or ecommerce page. If the image cannot be fetched, use the best available product screenshot or generated reference image, and label it clearly.

Never make the user infer the product from the storyboard alone.

## Storyboard Rules

The storyboard is the most important part of this skill. It must not be a random lifestyle image or a generic ad mood board.

Default storyboard format:

- one contact-sheet style image,
- 5 numbered vertical panels,
- each panel is a 9:16 TikTok-style keyframe,
- panels must form one continuous product-use sequence,
- product appearance must be copied from the product image.

The 5-frame visual sequence should follow this logic:

1. Hook: everyday pain point or scroll-stopping moment.
2. Product entry: product appears naturally and is used.
3. Product process/detail: close-up proof of what the product does.
4. Output/use result: the product delivers the visible result.
5. Payoff: creator/friend/family reaction or social-use ending.

For a SLUSHi-style product, the correct visual chain is:

1. no ice / empty freezer hook,
2. pour pink drink into the correct machine,
3. red or pink slush forming inside the transparent horizontal vessel,
4. slush dispensing from the front vertical spout into a glass,
5. creator and friend drinking together with the same machine visible.

Keep continuity locked:

- same product,
- same person,
- same room or environment,
- same lighting family,
- same drink/food/mess/object state where relevant.

The storyboard image should feel like real phone footage, not a polished ad board.

Product correctness is more important than image beauty. If the generated storyboard changes the product shape, color, spout, vessel, buttons, or key structure, regenerate the storyboard before writing the final script.

## Storyboard Character Lock

When a storyboard image already exists, treat these as locked:

- same person,
- same face / age range / creator type,
- same hairstyle,
- same outfit,
- same room,
- same lighting,
- same product,
- same product position and color,
- same drink/food/mess/result continuity.

Do not rewrite prompts as if starting from a blank canvas.

Bad keyword style:

```text
A casual female creator in a white shirt makes a drink in a kitchen...
```

Good keyword style:

```text
Use the attached storyboard as the visual reference. Keep the exact same creator, hairstyle, white t-shirt, blue jeans, kitchen counter, blue-gray slushie machine, pink lemonade color, and phone-shot framing from the storyboard. Animate only the small action in this shot...
```

The model should continue the storyboard人物, not重新生一个人.

## 15- or 30-Second Script Rules

The third section should include a concise script table. Use 15 seconds by default; use 30 seconds when the user asks for it.

For 15 seconds:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-2s | ... | ... | "..." |
| 2-5s | ... | ... | "..." |
| 5-8s | ... | ... | "..." |
| 8-11s | ... | ... | "..." |
| 11-15s | ... | ... | "..." |
```

For 30 seconds:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-3s | ... | ... | "..." |
| 3-7s | ... | ... | "..." |
| 7-12s | ... | ... | "..." |
| 12-17s | ... | ... | "..." |
| 17-23s | ... | ... | "..." |
| 23-30s | ... | ... | "..." |
```

The script must match the storyboard exactly. Do not introduce new people, rooms, claims, or product actions that are not in the storyboard. Use natural creator language, not brand-deck language.

## If The User Later Asks For FYPro Keywords

FYPro keywords must be written as image-to-video continuation prompts based on the storyboard, not as fresh text-to-image prompts.

Use this structure:

```text
Use the provided storyboard/reference frame as the visual source. Preserve the same creator, outfit, kitchen, product, lighting, drink color, and framing. Only animate: {small action}. Camera: handheld iPhone, slight natural movement. Do not change the person, product, room, outfit, or product shape.
```

For each frame, mention the locked visual details from the storyboard and one small motion only.

Do not use prompts that invite the model to create a new person, such as "a casual creator" or "a female model" when a storyboard person already exists.

## TikTok Style Defaults

Default settings:

- 9:16 vertical
- 15 seconds
- realistic UGC
- handheld iPhone look
- natural daylight
- lived-in room
- low AI feel
- one simple creator action per shot

Prefer:

- ordinary kitchens, living rooms, bathrooms, bedrooms, entryways, yards,
- imperfect framing,
- real hands and real surfaces,
- small motion,
- believable reaction.

Avoid:

- glossy studio commercial,
- perfect model posing,
- plastic skin,
- fake readable labels,
- floating product,
- magical transformation,
- split-screen before/after unless explicitly requested,
- impossible motion,
- claims beyond product evidence.

## Replacement Image Requests

If the user says "换一个图", regenerate or replace the storyboard image unless they specifically say product image.

Keep the same three-section output structure after replacing the image.

After replacing a storyboard image, update all later scripts or keywords to refer to the new storyboard人物 and scene.

## Multi-Product Output

For multiple products from the same brand, repeat the three sections per product:

```markdown
## Product A

### 1. 产品图
...

### 2. 故事版
...

### 3. 15 秒或者 30 秒视频脚本文字
...
```

Choose product order by TikTok potential:

1. strongest visual hook,
2. clearest usage proof,
3. lowest generation risk.

## Quality Check Before Final

Before responding, check:

- Does every product have a product image first?
- Is there a storyboard image after the product image?
- Is there a 15-second or 30-second script after the storyboard?
- Did you avoid extra sections unless requested?
- Is the video idea visually doable in TikTok/FYPro?
- Are product claims safe and grounded?
