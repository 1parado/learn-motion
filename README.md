# Learn Motion

复刻与拆解优秀界面动效的实验场。每个 demo 都是可交互的纯前端页面。

## 在线预览

**GitHub Pages：** https://1parado.github.io/learn-motion/

## 已有动效

| 名称 | 说明 | 入口 |
|------|------|------|
| 果冻下拉菜单 | 阻尼弹簧 + 前后缘双弹簧高亮跟随 | [demos/果冻下拉菜单.html](demos/果冻下拉菜单.html) |

## 本地打开

```bash
# 直接打开首页
open index.html

# 或起一个静态服务
npx serve .
```

## 目录结构

```
learn-motion/
├── index.html              # 聚合首页（卡片列表）
├── demos/
│   └── 果冻下拉菜单.html    # 单个动效 demo
└── README.md
```

## 添加新动效

1. 在 `demos/` 下新建 HTML 文件  
2. 在 `index.html` 的 `.grid` 里加一张卡片，`href` 指向新文件  
3. 推送到 `main`，Pages 会自动更新  

## 技术说明

- 无构建、无依赖，单文件 HTML 即可运行  
- 弹簧曲线参考 DS Bot 的 `motion.js`：二阶阻尼弹簧采样为 CSS `linear()`  
- 高亮条用「前缘硬弹簧 + 后缘软弹簧」制造果冻拉伸感  
