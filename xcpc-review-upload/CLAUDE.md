# XCPC Review Skill 项目

本项目包含一个 XCPC（ICPC/CCPC）赛后复盘 skill。

## 项目结构

```
xcpc-skill/
├── CLAUDE.md                           # 本文件
└── .claude/
    └── skills/
        └── xcpc-review.md              # XCPC 复盘 skill 定义
```

## Skill 说明

### xcpc-review

对 XCPC 比赛进行详细的赛后复盘分析。

**触发方式**：用户提到"复盘"、"XCPC 复盘"、"比赛总结"、"赛后分析"、"WA 分析"等关键词，或上传题目/题解/代码文件。

**输入**：
- 题目描述文件（PDF/MD/TXT）
- 题解文件（PDF/MD/TXT）
- 用户各题的比赛代码（.cpp/.py/.java 等）

**输出**：一份结构化的 Markdown 复盘报告，包含：
- 逐题分析（正确性、错因、经验教训）
- 共性问题诊断（错误分布、知识短板、代码习惯）
- 改进计划（短期/中期/长期）
- 亮点与进步
