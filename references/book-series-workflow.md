# Book Series Workflow

Use this workflow when the user inputs a book title and wants an automatic Xiaohongshu content package.

## Trigger

Use this workflow for requests like:

- 输入一个书名，自动生成一套小红书内容
- 帮我把《红楼梦》做成小红书系列
- 生成《三国演义》的封面、关系图、人物图和文案
- 这本书怎么做成国风手账账号内容

## Default Deliverables

For one book title, produce five parts:

1. book overview cover image
2. character relationship map image
3. representative character cover images
4. golden quote or theme sentence image
5. Xiaohongshu topic and content package

Default image format: 3:4 vertical Xiaohongshu cover.

If the user specifically asks for prompts or 提示词, output prompts instead of images. Otherwise, use the prompts internally and call the image generation tool. Prefer GPT Image 2 when the image tool allows model selection. Do not display the prompt package as the final deliverable unless image generation is unavailable.

## Step 1: Book Overview Cover

Use `Template A: Overview Cover`.

Include:

- large brush-calligraphy book title
- Xiaohongshu tags such as 「一张图读懂」, 「建议收藏」, 「长大后才看懂」
- 4-8 iconic characters, objects, scenes, or motifs
- a map, timeline, chapter strip, or theme cluster when useful
- 4-6 short handwritten annotations

Goal:

Make the viewer understand what the book is about and why the post is worth collecting.

## Step 2: Character Relationship Map

Use `Template C: Relationship Map`.

Include:

- 6-10 core characters only
- clear grouping by family, faction, emotional line, class, or plot function
- arrows with simple relationship labels
- a bottom legend explaining colors or arrow types
- simplified structure over exhaustive accuracy

Goal:

Make the relationship readable at Xiaohongshu cover size. Do not include every character if it makes the graph messy.

## Step 3: Representative Character Selection

Choose 2-3 characters by default for books with many important characters.

If the book has fewer than 5 widely recognized protagonists or core main characters, cover all of them as representative character images.

If the user explicitly asks for a named character group, complete roster, multiple characters, 人物系列, 全员封面, 金陵十二钗, or similar batch character output, do not use this 2-3 character limit. Follow `Batch Character Series` in `SKILL.md` and `Template B2: Batch Character Series` in `references/templates.md`.

Examples:

- 《西游记》 has 4 core protagonists: 唐僧, 孙悟空, 猪八戒, 沙僧. Generate all 4 representative character images.
- 《三国演义》 has many major figures, so choose 2-3 by default unless the user asks for more.
- 《红楼梦》 has many major figures, so choose 2-3 by default unless the user asks for a larger series.

Selection priority:

1. protagonist or emotional center
2. major contrast character
3. most visually recognizable or discussion-worthy character

For each character, infer:

- identity subtitle
- temperament
- symbolic object
- iconic scene or event
- emotional interpretation
- Xiaohongshu annotation hook

Examples:

- 《红楼梦》: 贾宝玉, 林黛玉, 王熙凤 or 薛宝钗
- 《三国演义》: 曹操, 刘备, 诸葛亮
- 《西游记》: 孙悟空, 唐僧, 猪八戒
- 《水浒传》: 宋江, 林冲, 武松

Use `Template B: Character Cover` for each.

## Step 4: Xiaohongshu Topic And Content

## Step 4: Golden Quote Or Theme Sentence Image

Use `Template D: Quote Or Reflection Card`.

Generate one quote-style image for the book. Prefer a famous line from the work when it is well-known and appropriate. If the exact quote is uncertain, use a theme sentence instead of fabricating an exact quotation.

Include:

- one central quote or theme sentence
- a small source label with the book title
- one symbolic object or scene from the book
- generous empty space
- 1-3 handwritten reflection notes
- softer collage density than cover or relationship map images

Goal:

Create a more emotional, saveable image that can work as the final image in a Xiaohongshu carousel.

Good quote-card angles:

- 命运感
- 长大后才懂
- 人心与选择
- 聚散离合
- 理想与现实
- 孤独感

If using a theme sentence, make it clearly interpretive rather than pretending it is a direct quote. For example:

```text
主题句：「小时候看的是热闹，长大后才看见命运。」
```

## Step 5: Xiaohongshu Topic And Content

Use `references/publishing.md`.

Output:

- main post topic
- 3-5 title options
- one short caption
- hashtags
- comment hook
- collection hook
- next 3 post ideas

The topic should be emotionally clickable, not purely academic.

Good topic angles:

- 长大后才读懂
- 人物关系终于理清
- 最容易被误解的人
- 一张图看懂命运线
- 小时候看热闹，长大后看人心

## Output Format

When generating images, follow this working order:

1. Generate the overview cover image.
2. Generate the relationship map image.
3. Generate each representative character image.
4. Generate one golden quote or theme sentence image.
5. Then provide Xiaohongshu publishing content.

Do not replace these image-generation steps with prompt text. Prompt text is only a fallback when the environment cannot generate images or when the user explicitly asks for prompts.

Use GPT Image 2 for all image-generation steps when model selection is available. If the current tool cannot explicitly select GPT Image 2, continue generating with the available image tool rather than stopping at prompts.

When outputting prompts only, use this exact structure:

```text
书名：

一、书名总览封面 Prompt
...

二、人物关系图 Prompt
...

三、代表人物图 Prompt
1. 人物 A
...
2. 人物 B
...
3. 人物 C
...

四、金句图 Prompt
...

五、小红书主题和内容
主题定位：
标题选项：
正文文案：
标签：
互动钩子：
下一期选题：
```

## Accuracy Guardrails

If the book is well-known, infer common characters and scenes.

If the book is obscure or the user asks for strict accuracy, say that exact character selection should be checked against the source text and ask for a character list or edition if needed.

Avoid fabricating obscure plot details. When uncertain, use broader motifs, themes, and visual metaphors.

## Style Guardrails

Keep all four parts visually connected:

- same paper texture
- same warm color palette
- same brush title style
- same handwritten annotation system
- same sticker and collage language

The package should feel like one account series, not four unrelated images.
