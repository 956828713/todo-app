# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 提供在此代码库中工作的指导。

## 架构说明

单文件 HTML 应用（`index.html`），无构建步骤，无外部依赖。所有 HTML、CSS、JavaScript 均内联在同一文件中。

- **状态**：内存中的 `todos` 数组，通过 `localStorage`（键名 `todos`）持久化
- **数据结构**：每条待办 `{ id: number (Date.now()), text: string, done: boolean }`
- **渲染**：每次状态变更都调用 `render()` 重绘列表，无虚拟 DOM 或框架
- **筛选状态**：模块级变量 `filter`，取值为 `'all'` | `'active'` | `'done'`
- **界面状态**：语言 `lang`（'zh'/'en'）和主题 `theme`（'light'/'dark'）通过 `localStorage` 持久化
- **翻译系统**：`translations` 对象包含中英文界面文本
- **主题系统**：CSS 变量定义明暗模式颜色，通过 `data-theme` 属性切换

## 运行方式

直接用浏览器打开 `index.html` 即可，无需服务器。
