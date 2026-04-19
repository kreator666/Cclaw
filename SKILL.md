---
name: comedy-writer
description: 喜剧写手 — 基于喜剧理论体系创作各类喜剧内容。当用户要求写脱口秀、小品、漫才、剧本、讽刺文章、仿讽、荒诞剧、段子，或将任何文本/素材改编为喜剧版本时使用此技能。核心能力：诊断素材 → 匹配手法 → 输出成品。Keywords: 脱口秀, 小品, 漫才, 剧本, 讽刺, 仿讽, 荒诞剧, 段子, 改编, comedy, standup, sketch, satire, parody.
---

# 喜剧写手

## 技能架构

本技能分三大模块：

1. **命令模块** (`commands.md`) — 识别用户命令，决定输出类型
2. **知识库** (`knowledge/`) — 喜剧理论与案例，支撑分析与创作
3. **输出模块** (`outputs/`) — 各喜剧类型的成品模板与规格

## 核心创作原则

**喜剧 = 镶嵌在活物上的机械装置**（柏格森）

一切喜剧效果的根本来源：生命中出现机械性、僵硬性。

三大铁律：
1. **角色越不自觉，越可笑** — 心不在焉是喜剧之源
2. **观众越不动情，越能发笑** — 保持情感距离
3. **效果逐级递增** — 每次重复都比上次更荒谬

---

## 工作流程

### Step 1：识别命令（必须）

读取 `commands.md`，根据用户输入匹配命令类型。

无明确命令时 → 根据素材判断最适合的类型。

### Step 2：分析素材（必须）

从 `knowledge/theory/comedy-types.md` 了解素材适合哪种喜剧类型，
再读取对应理论文件深入理解手法。

### Step 3：创作（必须）

读取 `outputs/` 下对应的输出模板，
按模板规格创作，并应用知识库中的理论手法。

### Step 4：输出创作笔记

每次输出末尾附加创作笔记，注明：
- 使用的喜剧手法 + 对应理论
- 可进一步强化的方向

---

## 知识库速查

| 知识文件 | 内容 |
|---------|------|
| `knowledge/theory/bergson.md` | 柏格森核心理论（必读） |
| `knowledge/theory/xiangsheng.md` | 中国相声包袱结构 |
| `knowledge/theory/freud.md` | 弗洛伊德：笑的释放机制 |
| `knowledge/theory/comedy-types.md` | 喜剧类型速查 + 推荐手法 |
| `knowledge/cases/standup/` | 脱口秀案例库 |
| `knowledge/cases/sketch/` | 小品案例库 |
| `knowledge/cases/manzai/` | 漫才案例库 |
| `knowledge/cases/script/` | 剧本案例库 |
| `knowledge/cases/parody/` | 讽刺/仿讽案例库 |

---

## 输出模板速查

| 输出类型 | 模板文件 |
|---------|---------|
| 脱口秀 | `outputs/standup-template.md` |
| 小品 | `outputs/sketch-template.md` |
| 漫才 | `outputs/manzai-template.md` |
| 剧本 | `outputs/script-template.md` |
| 讽刺文 | `outputs/satire-template.md` |
| 仿讽 | `outputs/parody-template.md` |
| 荒诞剧 | `outputs/absurdist-template.md` |

---

## 喜剧手法速查（核心）

### 三大情境手法
- **弹簧魔鬼** — 被压制的力量反复弹起，每次更猛烈
- **雪球效应** — 小因→大果，效应自我增强
- **系列干扰** — 两条独立事件线索交叉碰撞

### 三大语言手法
- **换位** — 庄→俗（滑稽模仿）或 俗→庄（幽默）
- **反转** — 主宾对调，让对方自食其果
- **现成句式+荒谬** — 刻板语言表达荒谬内容

### 相声三翻四抖
- **三番（四抖）** — 反复铺垫，第三/四遍突然反转抖包袱

### 角色设计核心
- **单一执念型** — 人格被一个缺点主宰（阿巴贡式）
- **系统性心不在焉** — 围绕中心思想的持续脱离现实（堂吉诃德式）
- **无意识暴露** — 角色最可笑的话/动作，恰是TA最不自觉的瞬间
