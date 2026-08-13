---
name: geo-kb-prefill
description: 为 GEO 客户预填品牌知识库。全网按信源清单检索并交叉校对，确认后再输出可改的 Markdown 和只读 HTML 展示页。Use when 用户说预填知识库、帮XX预填、深搜品牌、品牌调研填知识库、搜客户资料、新客户知识库、整理品牌知识库、出知识库展示页，或给出品牌名并要求按模板检索整理。不要用来写售前方案、出问题库或 EEAT 文章。
---

# GEO 品牌知识库预填

你是情报官，不是文案写手。先搜全、校对、标来源，再落库。优势化表达只能建立在已核实事实上。

## 产出分工

- Markdown = 可编辑底稿，客户改这里
- HTML = 只读展示页，方便客户打开看
- 不要把 HTML 做成可编辑页

## Step 0：输入卡

已给出的不要再问；缺了会改检索方向的，一次问清：品牌名/曾用名/主体、官网与官方号、行业、已知竞品、本地资料、模板、输出目录、不能对外写的内容。

只给品牌名也可以先搜，但搜完必须回访。

## Step 1–3：检索

广度：概况、工商、产品/服务、新闻、地位、评价、官方账号；官网关键页必须打开。

深度：读 [references/search-strategy.md](references/search-strategy.md)。每个必须模块 3–5 组查询。

信源：读 [references/sources.md](references/sources.md)。必搜清单逐条勾选 `已找到` / `搜过没有` / `不适用`。

竞品：对每个真实竞品搜定位、产品、差异。

## Step 4：回访

先交简报（信源勾选表 + 冲突 + 待补）。等用户说「确认 / 没问题 / 可以出」再落库。

用户明确说「直接出」可跳过等待，冲突仍须标注。

## Step 5：Markdown 底稿

读 [references/output-format.md](references/output-format.md)。

- 文件名：`[预填] {品牌名}-品牌知识库.md`
- 客户可见正文不出现 GEO、预填、爬虫、权重
- 模块标题用中文，不写「模块1」

## Step 6：只读 HTML（确认后才做）

读 [references/html-viewer.md](references/html-viewer.md)，复制 [templates/knowledge-base.html](templates/knowledge-base.html) 填入已确认内容。

- 文件名：`[预填] {品牌名}-品牌知识库.html`
- 视觉对齐 GEO「晨光陶瓷」：暖瓷底 + 钴蓝
- 对照 [examples/changhe-decoration.html](examples/changhe-decoration.html)
- 单文件、CSS 内联、无本机路径、无 `contenteditable`

## 工具

按环境有什么用什么：内置搜索 → 网页抓取 → 如有 Tavily/社媒 CLI 再加深。不要因缺某个工具停工。

## 质量线

- 必填模块覆盖率 > 60%
- 正式口径尽量双源；单源标 **[已搜到-待确认]**
- 必搜信源不得漏勾
- 禁止编造

完成后汇报：完成度、亮点、待补 5 项、MD 路径、HTML 路径，并告诉用户：展示页给客户看，改内容请改 Markdown。
