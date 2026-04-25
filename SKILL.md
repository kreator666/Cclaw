---
name: cclaw
version: "1.3.0"
description: "全球首个开源喜剧 AI. 基于喜剧理论体系创作各类喜剧内容，并集成视频剪辑工具。当用户要求写脱口秀/小品/漫才/剧本，或需要剪辑/拼接/编辑视频时使用此技能。核心能力：诊断素材 → 匹配手法 → 输出成品，或解析自然语言脚本 → 执行 FFmpeg。Keywords: 脱口秀, 小品, 漫才, 剧本, 剪辑, 视频, comedy, standup, sketch, video, edit."
category: "data-analysis"
description_zh: "全球首个开源喜剧 AI + 视频剪辑工具。创作脱口秀/小品/漫才/剧本等喜剧内容，或通过自然语言脚本驱动 FFmpeg 进行视频剪辑。"
---

# Cclaw — 喜剧写手 + 视频剪辑

## 技能架构

本技能分两大模块：

1. **writing** — 喜剧文本创作（知识驱动）
2. **tools** — 工具执行（脚本驱动）

```
Cclaw/
├── SKILL.md
├── commands.md              ← 文本命令 + 视频命令
├── modules/
│   ├── writing/          ← 7种喜剧输出模板
│   └── tools/
│       ├── video/        ← 视频剪辑（FFmpeg + 自然语言脚本）
│       └── poster/       ← 海报生成（结构预留，暂不实现）
├── knowledge/
│   ├── theory/           ← 喜剧底层原理（必读）
│   └── cases/            ← 案例库 + 创作方法论（必读）★
└── references/          ← 索引
```

---

## 工作流程（三步）

### Step 1：识别命令

读取 `commands.md`，根据用户输入判断是**文本创作**还是**视频工具**。

- 文本创作 → 进入 Step 2A
- 视频工具 → 进入 Step 2B

### Step 2A：文本创作（知识驱动）

**按顺序读取知识，每个步骤都要查，不能跳过：**

**⓪ 加载黑话手册（本次新增）**
→ `knowledge/blackbook.md`
→ 读取本次创作涉及的所有行业术语（蒸馏/龙虾/国潮/模型崩溃等）的统一解释
→ 黑话手册是**第一优先级**——无论创作什么主题，先加载黑话，确保术语含义一致、不泄底、不跳步

**① 读取输出模板**
→ `modules/writing/<类型>-template.md`
→ 确定结构规范、分段要求、对话格式

**② 读取案例库** ★（本次新增）
→ `knowledge/cases/<类型>/` 下的所有 .md 文件
→ 提取创作思路、案例灵感、人物原型
→ 如果该类型目录为空或只有 README，至少读取一个其他类型的案例来建立感觉

**③ 读取理论原理**
→ `knowledge/theory/eb7cb5ef.md` — 喜剧核心原理（必读）
→ `knowledge/theory/ac07d434.md` — 包袱结构与铺垫节奏
→ `knowledge/theory/126b44e8.md` — 笑的心理学
→ `knowledge/theory/9d01e4da.md` — 喜剧类型速查

**④ 按模板创作**
→ 套用结构，融合案例灵感和理论手法
→ 输出成品

### Step 2B：视频工具（脚本驱动）

→ 读取 `modules/tools/video/README.md`
→ 解析自然语言脚本
→ 生成 FFmpeg 命令并执行

### Step 3：输出

→ 创作输出 → 附加**创作笔记**（手法说明 + 知识来源标注）

---

## 知识库完整索引

### 黑话手册（底层术语，⓪优先加载）

| 文件 | 内容 |
|------|------|
| `knowledge/blackbook.md` | 行业术语统一解释（蒸馏/龙虾/国潮/模型崩溃等），每次创作第一步加载 |

### 理论（底层原理，必读）

| 文件 | 内容 |
|------|------|
| `knowledge/theory/eb7cb5ef.md` | 喜剧创作核心原理（机械化法则、心不在焉、反差等） |
| `knowledge/theory/ac07d434.md` | 包袱结构与铺垫节奏（三番四抖、重复升级） |
| `knowledge/theory/126b44e8.md` | 笑的心理学机制（期望落空、压抑释放） |
| `knowledge/theory/9d01e4da.md` | 喜剧类型速查（各类型特征与核心手法） |

### 案例库（创作参考，★本次强化）★

> 注意：各目录内容充实程度不均。实际有内容的标注 ✅，空目录标注（待填充）。

| 类型 | 路径 | 内容 | 状态 |
|------|------|------|------|
| 脱口秀 | `knowledge/cases/standup/` | 成长路径模型、三大杂念粉碎法、排毒日记法、脱口秀第一课一二章笔记、灵感库训练体系 | ✅ 充实 |
| 小品 | `knowledge/cases/sketch/` | 小品结构模板、人物关系设计 | ✅ 有模板 |
| 漫才 | `knowledge/cases/manzai/` | 目录待填充 | ⚠️ 空目录 |
| 仿讽 | `knowledge/cases/parody/` | 目录待填充 | ⚠️ 空目录 |
| 剧本 | `knowledge/cases/script/` | 目录待填充 | ⚠️ 空目录 |

**★ cases 目录为空时：** 直接跳过 cases 步骤，不读取其他类型案例。

**特别说明：**
- `knowledge/cases/standup/growth-path.md` — **脱口秀创作者心法**，包含成长阶段模型、排毒日记法（素材挖掘格式）、三大杂念粉碎法。**创作脱口秀时必读。**
- `knowledge/cases/sketch/sketch创作模板_平台课程.md` — **小品创作模板**，包含小品三要素、四种节奏、人物弧线设计。

### 输出模板

| 类型 | 文件 |
|------|------|
| 脱口秀 | `modules/writing/standup-template.md` |
| 小品 | `modules/writing/sketch-template.md` |
| 漫才 | `modules/writing/manzai-template.md` |
| 剧本 | `modules/writing/script-template.md` |
| 讽刺 | `modules/writing/satire-template.md` |
| 仿讽 | `modules/writing/parody-template.md` |
| 荒诞剧 | `modules/writing/absurdist-template.md` |

---

## 核心创作原则

一切喜剧效果的根本来源：**生命中出现机械性、僵硬性**。

三大铁律：
1. **角色越不自觉，越可笑**
2. **观众越不动情，越能发笑**
3. **效果逐级递增**

### ⛔ 理论隐身规则（必须遵守）

- ❌ 正文禁止：人名、书名、理论术语标签
- ✅ 创作笔记可保留：手法名 + 简要说明 + 知识来源文件

---

## 喜剧手法速查

### 三大情境手法
- **弹簧魔鬼** / **雪球效应** / **系列干扰**

### 三大语言手法
- **换位** / **反转** / **现成句式+荒谬**

### 相声三翻四抖
- **三番（四抖）** — 反复铺垫，第三/四遍突然反转抖包袱

### 漫才核心节奏
- **连续否认** — 三次以上否定，每次理由更荒谬，最后放弃反驳
