# Changelogs

本文件记录 `miniapp-bootstrap` skill 的重要架构、行为、依赖和文档变更。

记录规则：

- 仅记录有意义的架构、行为、依赖或文档变化。
- 按日期倒序维护，每次变更使用 `Added`、`Changed`、`Fixed` 或 `Removed` 分类。
- 变更描述应说明影响范围，避免记录纯格式化或无行为变化的调整。
- 每次更新 `SKILL.md` 或项目级文档基线时，同步更新本文件。

## 2026-09-15

### Changed

- 将前端默认架构从 `uni-app + Vue 3 + TypeScript + Pinia` 调整为微信小程序原生实现。
- 前端统一使用 WXML、WXSS、JavaScript、JSON 和原生 `wx.*` API。
- 将客户端目录示例调整为原生小程序的 `pages/`、`components/`、`app.js`、`app.json` 和 `app.wxss` 结构。
- 明确禁止引入 uni-app、Vue、React、Taro、Pinia 等跨平台或状态管理框架。
- 将 API 请求约束调整为基于原生 `wx.request` 的请求客户端。
- 将跨页面状态约束调整为 `App` 实例状态、独立 store 模块或明确作用域的共享工具。
- 明确小程序前端属于原生 `miniprogram` 运行时，使用原生 JavaScript，不把 Node.js 专属模块作为前端依赖。
- 明确 Node.js 仅用于本地工具链或后端运行时，前端不得引入 `fs`、`path`、`http`、`process` 等 Node.js-only API。
- 将 `changelogs.md` 纳入项目文档基线，并规定重要变更需要同步记录。

### Added

- 新增仓库级变更记录文档 `changelogs.md`。
