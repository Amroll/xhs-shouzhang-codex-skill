---
name: guofeng-scrapbook-xiaohongshu
description: Create or generate consistent Xiaohongshu-ready guofeng scrapbook collage images, preferably with GPT Image 2 when an image model can be selected, plus visual prompts, book content packages, cover concepts, relationship maps, representative character visuals, quote cards, account visuals, and publishing copy for Chinese literature, history, poetry, character studies, and healing knowledge posts. Use when the user inputs a book title and wants an automatic package with actual images or prompts for book cover, character relationship map, representative character images, golden quote image, Xiaohongshu topic and content, or asks for 国风手账拼贴, 小红书封面, 爆款知识图, 四大名著视觉转化, 人物封面, 关系图, 金句图, 账号头像简介, prompt 统一风格, 生成图片, GPT Image 2, or building a repeatable visual brand system.
---

# Guofeng Scrapbook Xiaohongshu

Use this skill to turn Chinese literature, history, poetry, character studies, and reflective knowledge topics into a stable Xiaohongshu visual brand:

- 治愈系国风手账拼贴
- 知识可视化
- 小红书高收藏封面
- 轻复古纸张质感
- 温暖奶油色、文艺少女感、国风高级审美

The goal is not only to generate one image prompt. The goal is to keep every output looking like it belongs to the same recognizable visual account.

## Core Workflow

For every request:

1. Identify the content type:
   - book content package from a book title
   - overview cover
   - character cover
   - batch character series
   - relationship map
   - quote or emotional reflection card
   - account avatar or profile visual
   - publishing copy
   - full content series
2. If the user inputs only a book title, or asks for a full book-to-Xiaohongshu workflow, read `references/book-series-workflow.md` first and generate the full package.
3. If the user asks for a named group of characters, a complete character set, or a multi-character series, follow the Batch Character Series rules before generating images.
4. Read `references/style-reference.md` when visual consistency matters.
5. Read `references/templates.md` and choose one layout template.
6. Add topic-specific cultural elements, characters, scenes, and emotional keywords.
7. Add Xiaohongshu-style annotations that create curiosity, collectability, and shareability.
8. Read `references/negative-rules.md` and apply the negative rules.
9. If the user says generate, make, create, 做, 出图, 生成封面, 生成图片, or asks for an automatic book package, treat the visual prompt as internal input and call the available image generation tool for each requested image. Prefer GPT Image 2 when the tool allows model selection. Do not show prompt text as the final deliverable unless the user specifically asks for prompt, 提示词, or 文案 only.
10. If the user is preparing to publish, read `references/publishing.md` and add title, caption, hashtags, and interaction hooks.

Use examples from `examples/` as few-shot references when the user asks for a similar output.

## Batch Character Series

Use this mode when the user asks for a named character group, full roster, complete set, 多个角色, 人物系列, 群像系列, 全员封面, 金陵十二钗, 水浒 108 将, 三十六计人物, 唐宋诗人系列, or similar multi-character requests.

Default behavior:

1. Treat each character as one separate `Template B: Character Cover` image.
2. Keep the same aspect ratio, layout skeleton, border style, paper texture, color palette, title placement, seal placement, and annotation density across the whole series.
3. Give each character distinct visual cues: clothing color, symbolic object, flower or plant, posture, facial temperament, iconic scene, and 2-4 character-specific annotations.
4. Start by listing the character roster and planned visual differentiators. If the roster is famous and stable, proceed without asking the user to confirm. If the roster is ambiguous, ask one concise clarification.
5. For 12 or fewer characters, generate the full set in one batch when the image tool can handle it. For more than 12 characters, split into numbered batches and keep a consistent series plan.
6. Name outputs consistently with the series and character name, such as `honglou-jinling-01-lin-daiyu`, `honglou-jinling-02-xue-baochai`.
7. Do not collapse a requested full character set into 2-3 representative characters. Representative selection only applies when the user asks for a general book package and does not request a complete group.
8. Do not turn the full character set into one collage grid by default. Default output is separate character images, suitable for a Xiaohongshu carousel.

Optional collection collage:

- If the user explicitly asks for 拼图, 九宫格, 合集图, 总览拼图, 一张图放下全部角色, or collection poster, generate an additional overview collage after the individual character images.
- For 12 characters, prefer a clean 3x4 collection layout with equal card sizes, shared title, tiny name labels, and enough spacing so faces and names remain readable.
- The collection collage is a supplement, not a replacement, unless the user asks for only one collage image.

For 金陵十二钗, use the canonical main twelve by default:

- 林黛玉
- 薛宝钗
- 贾元春
- 贾探春
- 史湘云
- 妙玉
- 贾迎春
- 贾惜春
- 王熙凤
- 贾巧姐
- 李纨
- 秦可卿

Keep all twelve visually connected as one collectible Xiaohongshu carousel series, while making each card immediately recognizable.

## Fixed Visual DNA

Every visual prompt should preserve these anchors:

- scrapbook collage, hand-made layout, layered paper
- warm cream old paper background
- vintage book page texture
- torn paper edges
- soft pink washi tape and translucent tape
- peach sticky notes, labels, small flower stickers
- handwritten annotations, arrows, circles, underlines
- red and blue pen notes
- soft watercolor illustration
- delicate colored pencil texture
- Chinese ink accents
- red seal stamp or gold stamp
- gentle shadows between paper layers
- warm honey-like soft light
- high information density but comfortable spacing
- educational, healing, warm, and softly girlish atmosphere

Preferred color system:

- warm cream
- milky ivory
- peach pink
- apricot blush
- dusty rose
- milk tea brown
- soft champagne gold
- tiny accents of bamboo green
- tiny accents of misty blue
- ink black

Avoid making the palette too dark, too saturated, too neon, too candy-like, or too theatrical. Keep the girlish feeling warm, literary, and refined rather than cute in a childish way.

## Layout Templates

### Template A: Overview Cover

Use for works, dynasties, schools of thought, large topics, or "one image to understand X".

Structure:

- top: large brush-calligraphy title
- near title: red seal and 2-4 Xiaohongshu collection tags
- center: main visual cluster of key people, events, or symbolic objects
- sides: sticky notes, arrows, handwritten explanations
- bottom: timeline, map, chapter tags, or core relationship summary

Good for:

- 三国演义
- 红楼梦
- 水浒传
- 唐诗宋词
- 魏晋风骨

### Template B: Character Cover

Use for a single person, literary character, poet, historical figure, or protagonist.

Structure:

- top: large brush-calligraphy name
- below title: 1-2 short identity subtitles
- center: half-body or three-quarter character sticker illustration
- sides: classic events, personality keywords, symbolic objects
- bottom: one concise Xiaohongshu-friendly insight note, such as "拆开来看，才懂她为什么这么选"

Good for:

- 曹操
- 刘备
- 孙权
- 诸葛亮
- 林黛玉
- 苏轼
- 李白

### Template C: Relationship Map

Use for complex groups, factions, family trees, emotional relationships, political alliances, or plot networks.

Structure:

- center: relationship network or faction map
- around center: character stickers or profile cards
- arrows: alliances, conflicts, kinship, emotional ties
- bottom: simplified legend or "一张图理清" explanation

Good for:

- 三国阵营
- 红楼梦人物关系
- 水浒 108 将
- 朝代人物关系

### Template D: Quote Or Reflection Card

Use for poetry, emotional posts, philosophical lines, healing reflections, and literary insights.

Structure:

- center: large quote or short sentence
- background: spacious old paper and subtle collage
- decoration: one symbolic object, plant, book, lamp, moon, window, or landscape
- annotation: 1-3 small handwritten reflections

Good for:

- 古诗词
- 孤独感
- 女性成长
- 人生后劲
- 文学金句

### Template E: Account Visual

Use for avatar, banner, profile identity, or visual branding.

Structure:

- clear central subject, suitable for circular crop if avatar
- simple but recognizable scrapbook environment
- strong face or symbol visibility
- fewer text elements than content covers
- keep the same color system and paper texture

Good for:

- 小红书头像
- 账号主页视觉
- 博主 IP 形象
- 系列封面统一视觉

## Prompt Output Structure

When generating an image prompt, use this structure:

```text
主题：
画幅：
核心风格：
标题文字：
副标题/标签：
主体画面：
人物/对象：
经典元素：
手账拼贴元素：
小红书批注：
颜色：
光线与质感：
情绪氛围：
构图要求：
负面规则：
```

If the image generation system prefers prose prompts, combine these sections into one polished paragraph after the structured version.

## Image Generation Model Preference

When generating images, prefer GPT Image 2.

Apply this rule as follows:

1. If the image generation tool exposes a model selector, choose GPT Image 2.
2. If the tool does not expose a model selector, still generate the image with the available image generation tool and mention only if necessary that this environment did not allow explicit GPT Image 2 selection.
3. Do not fall back to prompt-only output merely because GPT Image 2 cannot be explicitly selected.
4. Use prompt-only output only when the user explicitly asks for prompts or when no image generation tool is available.

For multi-image book packages, use the same model choice consistently across all generated images in the package whenever possible.

## Xiaohongshu Language

Use short, emotionally sticky annotations. Prefer lines that feel collectible, curious, and conversational.

Common annotation patterns:

- 一张图读懂 XXX
- 建议收藏
- 拆开来看，才懂 XXX
- XXX 真的后劲太大了
- 原来真正的道理藏在这里
- 这里封神
- 终于理清了
- 原来 XXX 才是关键
- 最容易被低估的人
- 这段关系太复杂了
- 看完突然懂了

Do not overfill the image with text. Use 4-8 short annotations for a cover, 2-4 for an avatar or simple card.

## Topic Expansion Rules

When the user gives only a topic, infer appropriate cultural details.

For literature:

- include major characters
- include iconic scenes
- include symbolic objects
- include emotional interpretation
- include a clear collection value

For historical figures:

- include identity, era, symbolic object, major events
- avoid turning the figure into a generic fantasy game character
- keep the interpretation accessible and emotionally resonant

For poetry or quotes:

- foreground mood, season, object, and atmosphere
- use more empty space than character covers
- reduce noisy stickers

For relationship maps:

- prioritize clarity over decoration
- use arrows, color grouping, and labels
- keep faction or relationship logic readable

## Negative Rules

Always include or apply these restrictions:

- no realistic photo
- no 3D render
- no CGI
- no cyberpunk
- no modern UI
- no modern clothing unless the user explicitly asks for modern fusion
- no heavy influencer makeup
- no hyper-realistic skin
- no dark horror style
- no movie poster style
- no game character splash art
- no plastic AI face
- no messy composition
- no unreadable text
- no excessive saturation
- no generic stock-photo feeling
- visible Chinese text must not contain "小时候", "长大后", "长大以后", "长大后才读懂", "长大后才能看懂", or "长大后才看懂"
- do not use childhood-versus-adulthood framing; use analysis-based insight framing instead

When writing Chinese prompts, include concise English negative prompt terms at the end if useful for the target image model.

## Publishing Add-On

If the user asks whether a post is ready for Xiaohongshu, or asks for publishing help, include:

- cover title
- post title options
- short caption
- hashtags
- comment prompt
- collection hook

Title patterns:

- 剖析之后，才懂 XXX
- 一张图理清 XXX
- XXX 真的后劲太大了
- 原来 XXX 才是隐藏主角
- 拆开来看，才懂她为什么这么选
- 读懂这一层，才算真的看懂 XXX
- 不是 XXX 变了，是我们终于看懂了

Interaction hooks:

- 你最喜欢谁？
- 哪句话后劲最大？
- 剖析之后，你重新理解了谁？
- 你想看下一期谁？
- 这张关系图你看懂了吗？

## Quality Checklist

Before finalizing, check:

- The visual style matches guofeng scrapbook collage.
- The output is suitable for Xiaohongshu 3:4 vertical cover unless another format is requested.
- The title is visually strong.
- The subject is clear at first glance.
- The image has collection value, not just decoration.
- The text density is rich but not chaotic.
- The prompt includes paper, tape, handwritten notes, and soft material texture.
- The color palette stays warm, restrained, and recognizable.
- Negative rules prevent style drift.
- Visible text avoids all childhood-versus-adulthood phrases and uses analysis-based insight titles.

## Default Response Style

If the user asks for a prompt, 提示词, or 文案 only, output the prompt directly.

If the user asks to generate, make, create, 做, 出图, 生成封面, or 生成图片, use the available image generation tool to create images directly. Prefer GPT Image 2 when model selection is available. Build the prompts internally, call the image generation tool, and do not stop at prompts.

If no image generation tool is available in the current environment, say that image generation is unavailable here and provide the prompt package as a fallback.

If the user asks for a system, series, or account strategy, output:

1. visual positioning
2. template choice
3. prompt
4. publishing copy
5. next-series suggestions

If the user inputs a book title and asks for the automatic package, output:

1. book overview cover image
2. character relationship map image
3. representative character cover images
4. golden quote or theme sentence image
5. Xiaohongshu topic, title options, caption, hashtags, interaction hook
6. next-post sequence

When image generation is unavailable, fall back to the same package as prompts and clearly say that the images were not generated.

Keep the answer practical and ready to use.
