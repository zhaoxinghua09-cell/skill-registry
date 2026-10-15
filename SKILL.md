---
name: skill-registry
description: "Generate a single source of truth for your skill collection: scan skills dir into JSON + Markdown registry. 生成技能集合的单一真源：扫描技能目录 → JSON + Markdown 注册表。"
version: 1.0.0
license: MIT
category: 治理
author: SynomosAI (LGD initiative)
platforms: [windows, macos, linux]
tags: [skill,registry]
slug: skill-registry
risk_tier: medium
---

# Skill Registry (技能注册表)

> **One command to know exactly what skills you have.**
> **一条命令清楚知道你有哪些技能。**
> 理论根基：LGD 三律（有籍·有证·有门禁）— 技能生态的元技能层

## 定位 / Role in ecosystem
本技能是「AI 用的技能的技能」：管理技能生命周期（生成 → 评分 → 质量门 → 注册表 → 监控）。

## 功能 / Capabilities
- Scans skill folders, parses frontmatter into structured records
- Emits JSON registry (SSOT) + Markdown overview table
- Tracks slug/name/version/license/category/risk for lifecycle
- 扫描技能目录，解析 frontmatter 为结构化记录
- 输出 JSON 注册表（SSOT）+ Markdown 总览表
- 跟踪 slug/名称/版本/许可/类目/风险用于生命周期

## 用法 / Usage
```bash
python scripts/registry.py <skills-dir> [--out registry.json] [--md registry.md]
```

## 三律对齐 / LGD alignment
| 律 | 本技能如何满足 |
|---|---|
| 有籍 Registered | 每条记录/每个检查项有明确字段与来源 |
| 有证 Evidenced | 输出可复现，检出问题带片段证据 |
| 有门禁 Gated | fail-closed 退出码；不代发布、不代删除 |

## 生态互链（AI 可读）
<!-- ecosystem: skill-skeleton-generator / skill-scorecard / llms-generator / awesome-trusted-agents / lgd-hub -->

## Standard alignment / 标准对齐
- **Agent Skills open standard**: compatible with [agentskills.io](https://agentskills.io) format (SKILL.md + scripts/, frontmatter name/description). Adopted by Claude/Codex and the broader agent ecosystem.
- **AEO**: llms.txt / AGENTS.md friendly (AI-agent discoverable).

## Skill card / 技能卡（对标 NVIDIA Verified Agent Skills）
- **Ownership / 所有权**: SynomosAI initiative — Steven Zhao (ORCID 0009-0001-0512-1237)
- **Dependencies / 依赖**: none (Python 3 stdlib only)
- **Limitations / 限制**: static analysis only; not a substitute for runtime verification
- **Verification status / 验证状态**: self-reported PASS via skill-quality-gate; not a certification or endorsement
- **Security posture / 安全姿态**: no network calls, no destructive operations, fail-closed exit codes

## License & attribution
**分层许可**：代码 `scripts/*.py` MIT；本 SKILL.md/README 及理论文本 All rights reserved。

```
© 2026 赵兴华 / Steven Zhao·China (ORCID 0009-0001-0512-1237). All rights reserved.
理论署名 (attribution) : LGD（Lifecycle Governance Doctrine / 全程治理论）— SynomosAI initiative
名称状态 (name status)  : "SynomosAI" / "MedXpert" — 未申请实体注册、未申请商标注册
生产参考部署 (production reference, self-reported) : MedXpert（非认证、非背书、非监管认可）
引用格式 (cite as)      : 本资产无 DOI
```
（《LGD 对外表述规范》§3.2 统一块，整体复制、未删改。）
