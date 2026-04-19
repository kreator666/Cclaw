# Cclaw

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

全球首个开源喜剧创作 AI。

## 支持的创作类型

| 类型 | 命令关键词 |
|------|-----------|
| 脱口秀 | 脱口秀 / standup |
| 小品 | 小品 / sketch |
| 漫才 | 漫才 / manzai |
| 剧本 | 剧本 / 独幕剧 |
| 讽刺文 | 讽刺 / satire |
| 仿讽 | 仿讽 / parody |
| 荒诞剧 | 荒诞 / absurdist |
| 改编 | 改编 / 改成喜剧 |


## 安装

```bash
# 方式一：SkillHub CLI（推荐）
skillhub install comedy-writer

# 方式二：从 GitHub Release 安装
skillhub install https://github.com/kreator666/comedy-writer/releases/latest/download/comedy-writer.skill

# 方式三：手动安装
# 将本仓库内容放入 OpenClaw 的 skills 目录：
# ~/.qclaw/skills/comedy-writer/
```

## 使用示例

```
用户：根据这条新闻写个脱口秀
用户：帮我把这篇文章改编成漫才
用户：写个讽刺文，主题是内卷
用户：用荒诞剧的形式表达沟通的不可能
```

## 许可证

本技能采用 **CC BY-NC 4.0**（知识共享署名-非商业性）许可证。

**允许：**
- ✅ 个人使用和研究
- ✅ 非商业目的的分享和改编（需署名）

**禁止：**
- ❌ 任何商业使用（包括嵌入产品/服务收费）
- ❌ 商业授权请联系：kreator666

详见 [LICENSE](./LICENSE) 文件。

## 架构

```
├── SKILL.md                     # 技能入口 + 工作流程
├── commands.md                  # 用户命令配置
├── knowledge/                   # 知识库
│   ├── theory/                 # 喜剧理论（哈希索引）
│   │   ├── eb7cb5ef.md        # 喜剧创作核心原理（必读）
│   │   ├── ac07d434.md        # 包袱结构与铺垫节奏
│   │   ├── 126b44e8.md        # 笑的心理学机制
│   │   └── 9d01e4da.md        # 喜剧类型速查 + 推荐手法
│   └── cases/                  # 案例库（可扩展）
│       ├── standup/
│       ├── sketch/
│       ├── manzai/
│       ├── script/
│       └── parody/
├── outputs/                     # 输出模板
│   ├── standup-template.md      # 脱口秀
│   ├── sketch-template.md       # 小品
│   ├── manzai-template.md       # 漫才
│   ├── script-template.md       # 剧本
│   ├── satire-template.md       # 讽刺文
│   ├── parody-template.md       # 仿讽
│   └── absurdist-template.md    # 荒诞剧
└── references/                  # 重定向索引
    ├── comedy-theory.md         # 理论文件索引
    └── comedy-templates.md      # 模板文件索引
```