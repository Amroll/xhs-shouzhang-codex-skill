# 国风手账小红书 Skill

[English](README.md)

`guofeng-scrapbook-xiaohongshu` 是一个面向 Codex 的国风手账视觉创作技能，用于把中国文学、历史、诗词、人物研究和治愈系知识内容，转化为适合小红书发布的统一视觉体系。

它不只是生成单张图片提示词，而是帮助你建立一套可复用的账号视觉风格：国风、清透手账纸、拼贴、手写批注、知识卡片、人物封面、关系图、金句卡和发布文案。

## 适合做什么

- 小红书国风手账封面
- 文学名著视觉化内容
- 历史人物或文学人物封面
- 批量人物封面系列，比如《红楼梦》金陵十二钗
- 人物关系图、阵营图、家族图
- 古诗词、金句、治愈反思卡
- 账号头像、主页视觉和系列封面
- 书籍内容包：封面、人物图、关系图、金句图、标题、正文、话题标签

批量人物请求默认是“每个角色单独一张封面”。如果你明确说要拼图、九宫格或合集图，skill 也可以额外生成一张总览拼图。

## 核心风格

这个 skill 默认保持一套稳定的视觉 DNA：

- 暖奶油色或浅樱花粉底层纸背景
- 干净手账纸纹理
- 柔和裁纸边缘和多层贴纸感纸张
- 浅粉和纸胶带、透明胶带、桃粉便签、标签
- 手写批注、箭头、圈画、下划线
- 红蓝笔记、浅珊瑚小标签印记、浅香槟贴纸小章
- 水彩插画、彩铅质感、轻墨线条点缀
- 高信息密度，但保持舒服留白
- 更温暖、更精致的少女感，同时保留教育感、收藏感和治愈感

推荐配色包括清透暖奶油色、乳白、浅樱花粉、桃粉、杏粉、豆沙玫瑰、浅米茶色、浅香槟金，并用少量竹青或雾蓝做平衡。最底层的背景纸要保持明亮、轻盈、文艺、小清新，避免深色、脏色、黄褐色或灰米色主背景。

## 目录结构

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

## 安装方式

把这个仓库放到 Codex 的 skills 目录下：

```powershell
cd "$env:USERPROFILE\.codex\skills"
git clone git@github.com:Amroll/xhs-shouzhang-codex-skill.git guofeng-scrapbook-xiaohongshu
```

如果已经在本地有这个 skill，可以直接拉取更新：

```powershell
cd "$env:USERPROFILE\.codex\skills\guofeng-scrapbook-xiaohongshu"
git pull
```

## 使用示例

可以这样向 Codex 提问：

```text
用 guofeng-scrapbook-xiaohongshu 技能，给《三国演义》做一套小红书国风手账内容包。
```

```text
生成一张刘备人物封面，国风手账拼贴风，小红书封面比例。
```

```text
生成《红楼梦》金陵十二钗人物封面，每个人一张，统一国风手账系列风格。
```

```text
帮我做《红楼梦》人物关系图，要求像小红书高收藏知识图。
```

```text
给苏轼做一张治愈系金句卡，带发布标题、正文和话题标签。
```

## 工作流

当用户只给出书名或主题时，这个 skill 会自动判断内容类型，并选择合适的参考文件：

- `book-series-workflow.md`：完整书籍内容包
- `style-reference.md`：统一视觉风格
- `templates.md`：封面、人物、关系图、金句卡、账号视觉模板
- `negative-rules.md`：避免跑偏的负面规则
- `publishing.md`：小红书标题、正文、标签和互动钩子

如果用户明确要求生成图片，skill 会优先使用可用的图像生成工具，并在环境允许时优先选择 GPT Image 2。

## 维护建议

- 新增风格规则时，优先写入 `references/style-reference.md`
- 新增版式时，优先写入 `references/templates.md`
- 新增案例时，放入 `examples/`
- 避免在仓库中提交 API key、token、`.env` 或个人隐私文件
