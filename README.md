# Guofeng Scrapbook Xiaohongshu Skill

[中文文档](README.zh-CN.md)

`guofeng-scrapbook-xiaohongshu` is a Codex skill for creating Guofeng scrapbook-style visual content for Xiaohongshu. It turns Chinese literature, history, poetry, character studies, and reflective knowledge topics into a consistent visual content system.

It is designed for more than one-off image prompts. The goal is to help build a reusable account-level visual language: Guofeng aesthetics, vintage paper, collage layouts, handwritten annotations, knowledge cards, character covers, relationship maps, quote cards, and publishing copy.

## What It Creates

- Guofeng scrapbook covers for Xiaohongshu
- Visual content for classic Chinese literature
- Historical or literary character covers
- Relationship maps, faction maps, and family trees
- Poetry cards, quote cards, and healing reflection cards
- Account avatars, profile visuals, and series covers
- Full book content packages: covers, character visuals, relationship maps, quote cards, titles, captions, and hashtags

## Core Style

This skill keeps a stable visual DNA:

- warm off-white vintage paper background
- old book page texture
- torn paper edges and layered paper
- washi tape, translucent tape, sticky notes, and labels
- handwritten notes, arrows, circles, and underlines
- red and blue pen annotations, seal stamps, and small gold stamps
- watercolor illustration, colored pencil texture, and Chinese ink accents
- information-rich layouts with comfortable spacing
- an educational, collectible, and emotionally healing atmosphere

## Repository Structure

```text
.
├── SKILL.md
├── examples/
│   ├── avatar.md
│   ├── liu-bei.md
│   ├── sanguo-cover.md
│   └── sun-quan.md
└── references/
    ├── book-series-workflow.md
    ├── negative-rules.md
    ├── publishing.md
    ├── style-reference.md
    └── templates.md
```

## Installation

Clone this repository into your Codex skills directory:

```powershell
cd "$env:USERPROFILE\.codex\skills"
git clone git@github.com:Amroll/xhs-shouzhang-codex-skill.git guofeng-scrapbook-xiaohongshu
```

If the skill already exists locally, update it with:

```powershell
cd "$env:USERPROFILE\.codex\skills\guofeng-scrapbook-xiaohongshu"
git pull
```

## Example Prompts

```text
Use the guofeng-scrapbook-xiaohongshu skill to create a full Xiaohongshu Guofeng scrapbook content package for Romance of the Three Kingdoms.
```

```text
Create a Liu Bei character cover in Guofeng scrapbook collage style for Xiaohongshu.
```

```text
Make a Dream of the Red Chamber character relationship map as a high-save Xiaohongshu knowledge graphic.
```

```text
Create a healing quote card for Su Shi, including Xiaohongshu title, caption, and hashtags.
```

## Workflow

When the user provides only a book title or topic, this skill identifies the content type and uses the relevant reference files:

- `book-series-workflow.md`: full book-to-Xiaohongshu content package
- `style-reference.md`: consistent visual style
- `templates.md`: cover, character, relationship map, quote card, and account visual templates
- `negative-rules.md`: rules that prevent visual drift
- `publishing.md`: Xiaohongshu title, caption, hashtag, and interaction hooks

When the user explicitly asks to generate images, the skill prefers available image generation tools and selects GPT Image 2 when the environment exposes a model choice.

## Maintenance Notes

- Add new style rules to `references/style-reference.md`
- Add new layout structures to `references/templates.md`
- Add new few-shot examples to `examples/`
- Do not commit API keys, tokens, `.env` files, or private personal data
