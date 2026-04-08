# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 架构说明

单文件 HTML 应用（`index.html`），无构建步骤，无外部依赖。所有 HTML、CSS、JavaScript 均内联在同一文件中。

- **状态**：内存中的 `todos` 数组，通过 `localStorage`（键名 `todos`）持久化
- **数据结构**：每条待办 `{ id: number (Date.now()), text: string, done: boolean }`
- **渲染**：每次状态变更都调用 `render()` 重绘列表，无虚拟 DOM 或框架
- **筛选状态**：模块级变量 `filter`，取值为 `'all'` | `'active'` | `'done'`

## 运行方式

直接用浏览器打开 `index.html` 即可，无需服务器。

<!-- 测试修改 -->

## 测试部分
这是push技能的测试修改。

### 再次测试
测试push技能的功能。
