---
name: geo-kb-prefill
description: 为 GEO 客户预填品牌知识库。全网按信源清单检索并交叉校对，用品牌方口吻写成可供 AI 抓取的详细正文，确认后再输出 Markdown 和只读 HTML。Use when 用户说预填知识库、帮XX预填、深搜品牌、品牌调研填知识库、搜客户资料、新客户知识库、整理品牌知识库、出知识库展示页，或给出品牌名并要求按模板检索整理。不要用来写售前方案、出问题库或 EEAT 文章。
---

# GEO 品牌知识库预填

检索时你是情报官。写正文时你是品牌自己在对外介绍。禁止调研腔。

## 产出分工

- `{品牌名} · 品牌知识库.md`：客户可见底稿，品牌口吻，给 AI 抓取
- `{品牌名} · 品牌知识库.html`：只读展示页
- `[内部] {品牌名}-信源勾选.md`：勾选表和检索备注，不进客户正文
- 不要把 HTML 做成可编辑页

## Step 0：输入卡

已给出的不要再问；缺了会改检索方向的，一次问清：品牌名/曾用名/主体、官网与官方号、行业、已知竞品、本地资料、模板、输出目录、不能对外写的内容。

只给品牌名也可以先搜，但搜完必须回访。

## Step 1–3：检索

广度：概况、工商、产品/服务、新闻、地位、评价、官方账号；官网关键页必须打开。

深度：读 [references/search-strategy.md](references/search-strategy.md)。每个必须模块 3–5 组查询，细节尽量留全。

信源：读 [references/sources.md](references/sources.md)。必搜清单逐条勾选 `已找到` / `搜过没有` / `不适用`。

竞品：对每个真实竞品搜定位、产品、差异。

## Step 4：回访

先交简报（信源勾选表 + 冲突 + 待补）。等用户说「确认 / 没问题 / 可以出」再落库。

用户明确说「直接出」可跳过等待，不笃定处仍标「待确认」。

## Step 5：品牌正文

读 [references/voice-and-labels.md](references/voice-and-labels.md) 和 [references/output-format.md](references/output-format.md)。

- 文件名：`[预填] {品牌名}-品牌知识库.md`（文件名可留预填；**标题和正文禁止出现预填/调研词**）
- 口吻：用公司名做主语（「君阳电力以……」），不要「我们」，不要「官网显示」
- 密度：给 AI 抓取，宁可冗余，不要摘要
- 标注：笃定不标；不笃定写「待确认」；没有写「待补充」
- 信源表只写内部附件

## Step 6：只读 HTML（确认后才做）

读 [references/html-viewer.md](references/html-viewer.md)，复制 [templates/knowledge-base.html](templates/knowledge-base.html)。

- 文件名：`[预填] {品牌名}-品牌知识库.html`
- 正文同样是品牌口吻，标签只用「待确认 / 待补充」
- 对照 [examples/changhe-decoration.html](examples/changhe-decoration.html)

## 工具

按环境有什么用什么：内置搜索 → 网页抓取 → 如有 Tavily/社媒 CLI 再加深。不要因缺某个工具停工。

## 质量线

- 必填模块覆盖率 > 60%，且产品/案例有完整细节不是三行摘要
- 正文零调研腔
- 标注只有「待确认 / 待补充」两档例外
- 禁止编造

完成后汇报：完成度、亮点、待补 5 项、MD / HTML / 内部信源文件路径。
