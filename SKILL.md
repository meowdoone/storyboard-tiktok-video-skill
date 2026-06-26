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

Important: this skill is about realism and storyboard logic, not memorizing one fixed scene. Pick the scene, person, action, and pacing from the current product and target platform. Once a storyboard image exists, that storyboard becomes the visual source of truth for that project only.

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

Hard language rule: the third section's script text must be in English. In the script table, all `屏幕字幕` and `旁白 / 口播` values must be natural English, even when surrounding instructions or section labels are Chinese.

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

The goal of the storyboard is to make a product video feel filmable:

- real person or real hand behavior,
- believable room/location for this product,
- clear camera distance and angle,
- visible product action,
- one useful visual idea per frame,
- low AI feel and low ad-polish.

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

For every product, derive the visual chain from what the product actually does. Do not reuse a previous kitchen/person/story from memory unless the current product naturally needs it.

Keep continuity locked inside the current storyboard:

- same product,
- same person only if the storyboard uses a person,
- same room or environment only within this generated sequence,
- same lighting family,
- same drink/food/mess/object state where relevant,
- no scene carried over from previous projects unless the user asks for it.

The storyboard image should feel like real phone footage, not a polished ad board.

Product correctness is more important than image beauty. If the generated storyboard changes the product shape, color, spout, vessel, buttons, or key structure, regenerate the storyboard before writing the final script.

## Storyboard Realism And Continuity

When a storyboard image already exists, treat these as locked for that project:

- the product shape and key parts,
- the product color and scale,
- the visible product-use action,
- the selected creator or hands, if present,
- the selected location, if present,
- the lighting and phone-shot style,
- the object/result continuity.

Do not rewrite prompts as if starting from a blank canvas, and do not reuse the previous storyboard's person or room as a default.

Bad keyword style:

```text
A casual female creator in a kitchen uses the product...
```

Good keyword style:

```text
Use the attached storyboard as the visual reference. Preserve the current product shape, product action, chosen creator/hands, chosen location, lighting, and phone-shot framing from this storyboard. Animate only the small action in this shot...
```

The model should continue the current storyboard, not重新生一个人物/场景, and not copy a remembered scene from a different product.

## 15- or 30-Second Script Rules

The third section should include a concise script table. Use 15 seconds by default; use 30 seconds when the user asks for it.

Language rule: keep the table headers if desired, but write every screen subtitle and voiceover line in English. The `画面` column can be concise Chinese or English, but the actual script text that would appear on screen or be spoken must be English.

For 15 seconds:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-2s | ... | No cold drinks? | "I just wanted something icy." |
| 2-5s | ... | Pour it in | "Add your favorite drink mix." |
| 5-8s | ... | Watch it turn slushy | "It gets thick and frosty right in the tank." |
| 8-11s | ... | Pull and serve | "Now just dispense it into a glass." |
| 11-15s | ... | Summer drinks at home | "This is the easiest little party drink." |
```

For 30 seconds:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-3s | ... | No cold drinks? | "I just wanted something icy." |
| 3-7s | ... | Pour it in | "Add your favorite drink mix." |
| 7-12s | ... | Watch it turn slushy | "It gets thick and frosty right in the tank." |
| 12-17s | ... | Pull and serve | "Now just dispense it into a glass." |
| 17-23s | ... | Looks like a real slush | "The texture is the whole point." |
| 23-30s | ... | Summer drinks at home | "This is the easiest little party drink." |
```

The script must match the storyboard exactly. Do not introduce new people, rooms, claims, or product actions that are not in the storyboard. Use natural English creator language, not brand-deck language.

## If The User Later Asks For FYPro Keywords

FYPro keywords must be written as image-to-video continuation prompts based on the storyboard, not as fresh text-to-image prompts.

Use this structure:

```text
Use the provided storyboard/reference frame as the visual source. Preserve the current storyboard's product shape, product action, chosen creator/hands, chosen location, lighting, object continuity, and framing. Only animate: {small action}. Camera: handheld phone, slight natural movement. Do not change the product, action logic, or chosen visual setup.
```

For each frame, mention the locked visual details from the current storyboard and one small motion only.

Do not use prompts that invite the model to create a new person or a new generic location when a storyboard reference already exists.

## TikTok Style Defaults

Default settings:

- 9:16 vertical
- 15 seconds
- realistic UGC
- handheld iPhone look
- natural daylight
- believable real location chosen for the current product
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
- Are all screen subtitles and voiceover lines in English?
- Did you avoid extra sections unless requested?
- Is the video idea visually doable in TikTok/FYPro?
- Are product claims safe and grounded?
