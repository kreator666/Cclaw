# comedy-writer

基于亨利·柏格森《喜剧的本质》及其他喜剧理论的模块化喜剧创作技能。

## 架构

```
├── SKILL.md                  # 技能入口
├── commands.md               # 用户命令配置
├── knowledge/                # 知识库
│   ├── theory/              # 喜剧理论
│   │   ├── bergson.md      # 柏格森核心
│   │   ├── xiangsheng.md   # 中国相声包袱
│   │   ├── freud.md        # 弗洛伊德笑论
│   │   └── comedy-types.md # 喜剧类型速查
│   └── cases/              # 案例库（可扩展）
│       ├── standup/
│       ├── sketch/
│       ├── manzai/
│       ├── script/
│       └── parody/
└── outputs/                  # 输出模板
    ├── standup-template.md   # 脱口秀
    ├── sketch-template.md    # 小品
    ├── manzai-template.md    # 漫才
    ├── script-template.md   # 剧本
    ├── satire-template.md    # 讽刺文
    ├── parody-template.md    # 仿讽
    └── absurdist-template.md # 荒诞剧
```

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

## 核心原理

> 喜剧 = 镶嵌在活物上的机械装置
> — 亨利·柏格森《喜剧的本质》

三大铁律：
1. **角色越不自觉，越可笑**
2. **观众越不动情，越能发笑**
3. **效果逐级递增**

## 安装

放入 OpenClaw 的 skills 目录即可：
```
~/.qclaw/skills/comedy-writer/
```
