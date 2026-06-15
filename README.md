# Skill Bloat Detector · 技能膨胀检测器

[![Version](https://img.shields.io/badge/version-1.2.0-blue)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Hermes](https://img.shields.io/badge/Hermes-Agent-7C3AED)](https://github.com/NousResearch/hermes-agent)

[English](#english) | [中文](#中文)

---

## English

**Detect and fix "the more skills, the dumber the agent" syndrome.**

Your Hermes agent has 200+ skills. Half are zombies (never used). Academic writing has 22 overlapping skills competing for every request. The available_skills block eats ~16K tokens before you even start reasoning.

### Proven results

```
203 → 132 skills (-35%)
1.7 MB → 1.0 MB text (-38%)
~6,000 tokens freed (+20% reasoning budget)
Benchmark: 6/10 → 9/10
🔴 critical → 🟢 healthy
```

### Quick start

In your Hermes session:

| Say this | What happens |
|----------|-------------|
| `检测 skill bloat` | Full diagnosis + report |
| `一键优化` | Auto-fix (P0→P1→P2) + verify |
| `只做静态分析` | Inventory + overlap only, no changes |

Or run the 30-second health check manually — see [SKILL.md](SKILL.md) §健康快检.

### Install

```bash
hermes skills install https://raw.githubusercontent.com/SpencerRaw/hermes-skill-bloat-detector/main/SKILL.md
```

### How it works

```
30s Health Check → Phase 0 (Inventory) → Phase 1 (Overlap) → Phase 2 (Diagnose + Fix)
```

Detects 7 degradation mechanisms: context pollution, skill selection errors, content bloat, inter-skill conflicts, zombie skills, duplicate skills, and prompt cache invalidation.

---

## 中文

**检测和修复「技能越多、智能体越蠢」的 skill bloat 现象。**

当 200+ 技能吃掉了 16K tokens 的 context 预算，一半技能从未被使用——这个工具给你数据驱动的诊断和修复。

### 实战验证

```
203 → 132 技能 (-35%)
1.7 MB → 1.0 MB 文本 (-38%)
释放 ~6,000 tokens (+20% 推理空间)
Benchmark: 6/10 → 9/10
🔴 临界 → 🟢 健康
```

### 快速使用

| 说这个 | 发生什么 |
|--------|---------|
| `检测 skill bloat` | 完整诊断 + 报告 |
| `一键优化` | 自动修复 (P0→P1→P2) + 验证 |
| `只做静态分析` | 仅盘点 + 重叠分析, 不修改 |

或手动跑 30 秒健康快检 — 见 [SKILL.md](SKILL.md) §健康快检.

### 安装

```bash
hermes skills install https://raw.githubusercontent.com/SpencerRaw/hermes-skill-bloat-detector/main/SKILL.md
```

### 工作流

```
30秒快检 → Phase 0 (静态盘点) → Phase 1 (重叠分析) → Phase 2 (诊断 + 修复)
```

检测 7 种退化机制：上下文污染、技能选择错误、内容膨胀、技能间冲突、僵尸技能、重复技能、prompt 缓存失效。

---

**[Changelog](CHANGELOG.md)** · MIT License · [SpencerRaw](https://github.com/SpencerRaw)
