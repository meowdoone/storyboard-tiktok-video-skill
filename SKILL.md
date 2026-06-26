---
name: storyboard-tiktok-video
description: Use when a user wants a TikTok/TK product-video storyboard from a product link, product image, product screenshot, ecommerce page, or short product description. The required output format is product image first, then storyboard image, then 15-second video script text. Especially useful for FYPro, StoreClaw, or image-to-video workflows where the user wants clear product truth before video generation.
---

# 故事版的 TikTok 视频 Skill

## Purpose

Turn a product into a TikTok-ready video storyboard package with exactly three default sections:

1. 产品图
2. 故事版
3. 15 秒视频脚本文字

This skill is intentionally narrow. It is for product-facing TikTok/TK demo work where the user wants a clean handoff before video generation.

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
## 3. 15 秒视频脚本文字
```

Do not include FYPro keywords, negative prompts, correction prompts, product-truth cards, long platform analysis, source notes, or extra recommendations by default.

If the user asks for FYPro keywords later, provide them as a separate follow-up output.

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

The storyboard should be a 5-frame visual sequence for a 15-second TikTok video:

1. Hook: everyday pain point or scroll-stopping moment.
2. Context: person and environment make the need believable.
3. Product entry: product appears naturally and is used.
4. Usage/detail: close-up proof of what the product does.
5. Payoff: realistic result or emotional close.

Keep continuity locked:

- same product,
- same person,
- same room or environment,
- same lighting family,
- same drink/food/mess/object state where relevant.

The storyboard image should feel like real phone footage, not a polished ad board.

## 15-Second Script Rules

The third section should include a concise script table:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-2s | ... | ... | "..." |
| 2-5s | ... | ... | "..." |
| 5-8s | ... | ... | "..." |
| 8-11s | ... | ... | "..." |
| 11-15s | ... | ... | "..." |
```

The script should match the storyboard exactly. Use natural creator language, not brand-deck language.

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

## Multi-Product Output

For multiple products from the same brand, repeat the three sections per product:

```markdown
## Product A

### 1. 产品图
...

### 2. 故事版
...

### 3. 15 秒视频脚本文字
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
- Is there a 15-second script after the storyboard?
- Did you avoid extra sections unless requested?
- Is the video idea visually doable in TikTok/FYPro?
- Are product claims safe and grounded?

