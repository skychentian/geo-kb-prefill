# GEO 品牌知识库预填

给 Claude Code / Codex / Cursor / Grok 用的 Skill。输入品牌名，全网检索官网、工商、媒体和公开讨论，交叉校对后按 11 模块预填一份品牌知识库。客户只需补公开搜不到的内部数据。

## 装哪个环境

把本仓库克隆到对应 skills 目录，目录名保持 `geo-kb-prefill`：

```bash
# Claude Code
git clone https://github.com/skychentian/geo-kb-prefill.git ~/.claude/skills/geo-kb-prefill

# Codex
git clone https://github.com/skychentian/geo-kb-prefill.git ~/.codex/skills/geo-kb-prefill

# Grok
git clone https://github.com/skychentian/geo-kb-prefill.git ~/.grok/skills/geo-kb-prefill

# Cursor
git clone https://github.com/skychentian/geo-kb-prefill.git ~/.cursor/skills/geo-kb-prefill
```

已有目录要更新：

```bash
git -C ~/.claude/skills/geo-kb-prefill pull
```

## 怎么用

在对话里直接说：

```text
帮我预填酷嗨米的品牌知识库。官网是 https://example.com。本地介绍在 ./公司介绍.md。搜完先回访我确认，再落到当前目录。
```

或只给品牌名：「帮 XX 预填知识库」。

Agent 会先问缺的关键项（官网、本地资料、不能对外写的内容），再检索，再给你一页简报，确认后落库。

## 输出

`[预填] {品牌名}-品牌知识库.md`

每条信息带来源标注：双源确认 / 待确认 / 需客户补充 / 冲突待裁定。

## 需要什么

- 能上网的 Agent（Claude Code、Codex、Grok、Cursor 均可）
- 不依赖飞书、不依赖特定付费搜索 API
- 有 Tavily / 社媒 CLI 会更深，没有也能跑

## 不做什么

- 不写售前方案、不写出问题库、不写 EEAT 文章
- 不把 UGC 当工商/参数/荣誉的唯一依据
- 不编造搜不到的数据
