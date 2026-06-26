# XCPC Review Skill

一个基于 Claude Code 的 **XCPC（ICPC/CCPC）赛后复盘分析工具**，帮助竞赛选手系统性地回顾比赛表现、定位错误根因、制定改进计划。

## 功能概览

- 📊 **逐题深度分析** — 对每道题进行正确性检查、算法对比、代码质量评估
- 🐛 **错因自动归类** — 将错误分为算法选择、边界遗漏、实现 Bug、审题错误等 10 个类别
- 🔍 **共性问题诊断** — 跨题目发现知识短板和不良代码习惯
- 📋 **结构化报告输出** — 生成包含比赛概况、逐题分析、改进计划的 Markdown 复盘报告
- 🌐 **Codeforces API 集成** — 支持自动拉取比赛提交、排名、题目和题解

## 两种使用方式

### 方式一：手动上传文件

直接提供题目描述（PDF/MD/TXT）、题解、以及你的比赛代码（.cpp/.py/.java），Skill 会逐题分析。

### 方式二：接入 Codeforces API（推荐）

提供你的 **CF handle** 和 **Contest ID**，Skill 自动拉取：

| 数据 | 来源 |
|------|------|
| 所有提交记录 | `codeforces.com/api/contest.status` |
| 比赛排名 & 罚时 | `codeforces.com/api/contest.standings` |
| 题目描述 | CF 题目页面 |
| 官方题解 | CF Editorial 博客 |

## 触发关键词

在 Claude Code 中提到以下任意关键词即可触发复盘：

> 复盘、XCPC 复盘、比赛总结、赛后分析、WA 分析、竞赛回顾、CF 复盘、Codeforces VP 复盘

## 复盘报告结构

每份报告包含五个章节：

1. **比赛概况** — 总题数、AC 数、WA 数、排名/成绩
2. **逐题分析** — 考点、解法、结果、错因、经验教训
3. **共性问题诊断** — 错误分布、知识短板、代码习惯、比赛策略
4. **改进计划** — 短期/中期/长期可执行措施
5. **亮点与进步** — 肯定做得好的地方

## 项目结构

```
xcpc-review/
├── README.md
├── CLAUDE.md
├── .gitignore
├── .claude/
│   └── skills/
│       └── xcpc-review.md       # Skill 定义文件
└── problems/
    ├── README.md                # 题目目录使用说明
    └── CF_2237D/                # 示例题目
        ├── fetch_problem.py     # 题目抓取脚本
        └── statement.txt        # 题目描述
```

## 安装与使用

### 前置条件

- 安装 [Claude Code](https://docs.anthropic.com/en/docs/claude-code/overview)
- （可选）GitHub 账号用于查看/复刻本项目

### 安装 Skill

将 `.claude/skills/xcpc-review.md` 放入你项目的 `.claude/skills/` 目录，或者在 Claude Code 中直接引用本仓库。

### 使用示例

```
# CF API 模式
帮我复盘 Codeforces Round #2060，我的 handle 是 your_handle

# 手动上传模式
帮我复盘今天的比赛（上传题目 PDF 和代码）
```

## 许可证

MIT License
