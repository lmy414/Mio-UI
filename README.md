# 澪号前端重构 — 对话区主界面设计

澪号（MIO）Personal Agent 前端 UI 重构原型与交互文档。

## 文件

- [对话区主界面设计.md](./对话区主界面设计.md) — 交互逻辑文档（布局结构、Mini Nav、Sidebar、Chat Panel、Editor Panel、Settings、全局状态）
- [对话区主界面设计.pen](./对话区主界面设计.pen) — Pencil 设计原型文件（用 [Pencil](https://pencil.dev) 打开）

## 设计概要

```
┌──────────┬──────────────┬────────────────────┬─────────────┐
│ Mini Nav │   Sidebar    │    Chat Panel      │   Editor    │
│   52px   │    320px     │      760px          │    340px    │
│          │              │                    │             │
│  通信 ▸   │ 当前会话      │ 标题栏 (纯黑)       │ 标题栏 (纯黑) │
│  識別    │ 搜索          │                    │ Tab 栏      │
│  記録    │ 角色列表      │ 聊天气泡            │ 工具栏       │
│  資源    │ 作戦記録      │ (用户/澪)          │ 代码预览     │
│  設定    │ 資源監視      │                    │             │
│          │              │ 输入区              │             │
└──────────┴──────────────┴────────────────────┴─────────────┘
```

- 底层壁纸 → 暗色覆层(55%) → 玻璃面板(blur 20px)
- 暗色仪表板风格，暖灰配色
- Noto Serif SC（标题） + Inter（正文） + JetBrains Mono（代码）

## 技术栈（目标）

- SolidJS + Tailwind CSS
- 玻璃拟态（Glass Morphism）
- 扩展系统（Slot-based 插件架构）

## 来源

从 [personal-agent](https://github.com/M1rr0r/personal-agent) 主仓库独立出的前端重构专项。
