# 海报生成模块

> **暂不实现**，结构预留。

## 目录结构

```
poster/
├── README.md             ← 本文件
└── templates/          ← 海报模板规格
    ├── standup-poster.md
    ├── comedy-show.md
    └── social-card.md
```

## 实现方式（待定）

三种方案：

| 方案 | 说明 | 依赖 |
|--------|------|------|
| A. 自包含 | Python + PIL/Pillow 生成 | Python 环境 |
| B. 委托 canvas-design skill | 调用 canvas-design 能力 | canvas-design skill |
| C. 混合 | 布局用 canvas-design，数据用 PIL | 两者 |

## 海报类型

| 类型 | 尺寸 | 用途 |
|------|------|------|
| standup-poster | 1080×1920 | 抖音/B站封面 |
| comedy-show | 1920×1080 | 演出宣传海报 |
| social-card | 1200×630 | 社交媒体分享卡 |

## 未来实现时参考

- 脱口秀海报要素：演员名、日期、场地、主题词、视觉锚点（大笑/惊讶表情）
- 设计风格：强对比、喜剧感字体、一句话文案
- 参考 canvas-design skill 生成 PNG/PDF