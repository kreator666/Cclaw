---
name: cclaw
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
├── commands.md              ← 扩展：文本命令 + 视频命令
├── modules/
│   ├── writing/          ← outputs/ 迁入：7种喜剧模板
│   └── tools/
│       ├── video/        ← 视频剪辑（FFmpeg + 自然语言脚本）
│       └── poster/       ← 海报生成（结构预留，暂不实现）
├── knowledge/            ← 喜剧理论 + 案例库
└── references/          ← 索引
```

---

## 工作流程

### Step 1：识别命令（必须）

读取 `commands.md`，根据用户输入匹配命令类型。

**两个入口：**
- 文本创作 → 路由到 writing 模块
- 视频工具 → 路由到 tools/video 模块

### Step 2：执行

**writing 模块：**
- 分析素材（`knowledge/theory/`）
- 匹配手法
- 按模板创作

**tools/video 模块：**
- 解析自然语言脚本 → FFmpeg 命令
- 执行并返回结果

### Step 3：输出

创作输出 → 附加创作笔记（含手法说明）

---

## 核心创作原则

一切喜剧效果的根本来源：生命中出现机械性、僵硬性。

三大铁律：
1. **角色越不自觉，越可笑**
2. **观众越不动情，越能发笑**
3. **效果逐级递增**

### ⛔ 理论隐身规则（必须遵守）

- ❌ 正文禁止：人名、书名、理论术语标签
- ✅ 创作笔记可保留：手法名+简要说明

---

## 知识库速查

| 文件 | 内容 |
|------|------|
| `knowledge/theory/eb7cb5ef.md` | 喜剧创作核心原理 |
| `knowledge/theory/ac07d434.md` | 包袱结构与铺垫节奏 |
| `knowledge/theory/126b44e8.md` | 笑的心理学机制 |
| `knowledge/theory/9d01e4da.md` | 喜剧类型速查 |
| `knowledge/cases/standup/` | 脱口秀案例库 |

---

## 输出模板速查

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

## 喜剧手法速查

### 三大情境手法
- **弹簧魔鬼** / **雪球效应** / **系列干扰**

### 三大语言手法
- **换位** / **反转** / **现成句式+荒谬**

### 相声三翻四抖
- **三番（四抖）** — 反复铺垫，第三/四遍突然反转抖包袱