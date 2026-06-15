# Skill Bloat Detector · 技能膨胀检测器

[English](#english) | [中文](#中文)

---

## English

**Detect and fix "skills get dumber as they multiply" syndrome.**

Your Hermes agent has 200+ skills. Half are zombies (never used). Academic writing has 22 overlapping skills competing for every request. Your available_skills block eats 16K tokens before you even start reasoning.

This skill runs data-driven diagnostics, benchmarks your agent, and cleans up the mess — with backups.

### What it does

| Phase | Action | Output |
|-------|--------|--------|
| **0** — Inventory | Count skills, measure size, track growth, find zombies | Data portrait |
| **1** — Overlap | Cluster by function, detect duplicates, cross with usage | Overlap clusters |
| **2** — Diagnose + Fix | Root cause analysis, tiered remediation (P0→P3) | Clean agent |

### Real-world results (203 → 132 skills)

```
Before:  203 skills, 1.7 MB, 56 zombies (45%), 11 duplicates, 🔴 critical
After:   132 skills, 1.0 MB, 0 zombies, 0 duplicates, 🟢 healthy
Token savings: ~6,000 tokens (+20% reasoning budget)
Benchmark score: 6-7 → 9.0/10
```

### Quick start

```
# In your Hermes session:
"检测 skill bloat"     → Full diagnosis + report
"一键优化"              → Auto-fix (P0→P1→P2) + verify
"只做静态分析"          → Phase 0+1 only, no changes
```

### Install

```bash
hermes skills install https://raw.githubusercontent.com/SpencerRaw/hermes-skill-bloat-detector/main/SKILL.md
```

---

## 中文

**检测和修复「技能越多、智能体越蠢」的 skill bloat 现象。**

当你的 Hermes agent 有 200+ 个技能，一半是僵尸，学术写作 22 个技能竞争同一个请求，available_skills 吃掉 16K tokens——你需要这个工具。

### 核心流程

| 阶段 | 做什么 | 产出 |
|------|--------|------|
| **0** — 静态盘点 | 统计技能数/体积/增长速率/僵尸比例 | 数据画像 |
| **1** — 重叠分析 | 功能聚类 + 重复副本检测 + 使用频率交叉 | 重叠簇清单 |
| **2** — 诊断修复 | 根因定位 + P0→P3 分级修复 + 验证 | 健康 agent |

### 实战验证（203 → 132）

```
优化前: 203 技能, 1.7 MB, 56 僵尸 (45%), 11 重复, 🔴 临界
优化后: 132 技能, 1.0 MB, 0 僵尸, 0 重复, 🟢 健康
Token 节省: ~6,000 (+20% 推理空间)
Benchmark: 6-7 → 9.0/10
```

### 快速使用

```
检测 skill bloat         → 完整诊断报告
一键优化                  → 自动修复 + 验证
只做静态分析              → Phase 0+1, 不修改
```

### 安装

```bash
hermes skills install https://raw.githubusercontent.com/SpencerRaw/hermes-skill-bloat-detector/main/SKILL.md
```

---

MIT License · [SpencerRaw](https://github.com/SpencerRaw)
