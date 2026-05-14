# Negative Rules

Apply these rules to prevent style drift.

## Permanent Bans

Never use:

- cyberpunk
- futuristic UI
- modern app interface
- high-saturation neon
- dark horror style
- game splash art
- fantasy armor unless the user explicitly asks
- 3D render
- CGI
- hyper-realistic skin
- realistic photography
- heavy influencer makeup
- modern celebrity styling
- glossy plastic face
- movie poster composition
- overly dramatic battlefield poster
- messy composition
- unreadable text
- text overload
- generic stock image feeling

## Chinese Negative Prompt

Add or apply:

```text
不要写实摄影，不要3D渲染，不要CGI，不要赛博朋克，不要现代UI，不要现代网红妆，不要影视海报感，不要游戏立绘感，不要暗黑恐怖风，不要高饱和霓虹色，不要杂乱排版，不要低质量文字，不要AI塑料脸
```

## English Negative Prompt

Use when the image model benefits from English negative terms:

```text
no realistic photo, no 3D render, no CGI, no cyberpunk, no modern UI, no modern clothing, no heavy makeup, no hyper realistic skin, no dark horror style, no movie poster, no game splash art, no plastic AI face, no messy composition, no unreadable text, no excessive saturation
```

## Correction Rules

If output starts to look too decorative:

- increase knowledge labels
- add a map, timeline, or annotation layer
- reduce flowers and generic ornaments

If output starts to look too academic:

- add tape, stickers, handwritten notes, and soft watercolor texture
- add emotional Xiaohongshu annotations

If output starts to look too fantasy:

- reduce armor, weapons, dramatic lighting, and heroic poses
- add book pages, ink wash, paper texture, and study-note elements

If output starts to look too crowded:

- reduce annotations to 4-6 short phrases
- make the main title larger
- group details into sticky notes
- keep a clear central visual subject

