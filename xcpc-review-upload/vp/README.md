# VP（Virtual Participation）比赛

存放模拟参赛/虚拟参赛的比赛记录。

## 目录结构

每场比赛一个文件夹，命名格式：`平台_比赛标识`

```
vp/
├── cf_2060/                    # Codeforces Round #2060
│   ├── editorial.pdf           # 官方题解
│   ├── statements.pdf          # 题目描述
│   ├── review.md               # 赛后复盘报告
│   ├── my_code/                # 比赛时代码
│   │   ├── A.cpp
│   │   ├── B.cpp
│   │   └── ...
│   ├── cf_submissions/         # 从 CF 拉取的提交记录
│   │   ├── A_1_WA.cpp
│   │   ├── A_2_OK.cpp
│   │   └── ...
│   └── solutions/              # 补题后的正确解法
│       ├── A.cpp
│       └── B.cpp
│
├── ncpc_2025/                  # 区域赛
│   ├── editorial.pdf
│   ├── statements.pdf
│   └── ...
│
└── atcoder_abc400/             # AtCoder
    └── ...
```

## 文件说明

| 目录/文件 | 说明 |
|-----------|------|
| `editorial.pdf` | 官方题解 |
| `statements.pdf` | 题目描述 |
| `review.md` | 赛后复盘报告（由 xcpc-review skill 生成） |
| `my_code/` | 比赛时现场写的代码 |
| `cf_submissions/` | 从 Codeforces 拉取的各次提交记录（命名含提交序号和结果） |
| `solutions/` | 赛后补题的正确解法 |
| `submissions.json` | CF API 拉取的原始提交数据（如有） |

## 命名约定

- 代码文件以题号命名：`A.cpp`、`B.cpp`、`C.cpp`
- 多次提交按序号编号：`A_1_WA.cpp`（第1次，WA）、`A_2_AC.cpp`（第2次，AC）
- 结果后缀：`AC`、`WA`、`TLE`、`RE`、`CE`
