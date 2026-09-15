# miniapp-bootstrap

用于从 0 初始化小程序项目的 Codex/Agent Skill，默认采用微信 `miniprogram` 原生前端（`WXML + WXSS + Native JavaScript + JSON + wx.* API`）、`NestJS + Prisma + MySQL` 后端、`pnpm workspace` monorepo。

它融合了两个参考 skill 的核心思想：一方面保留小程序项目生命周期、文档事实源、变更治理和验证流程；另一方面补充集中配置、统一响应、鉴权、SSE/长连接方案等全栈工程约束。前端不使用 `uni-app`、Vue、React、Taro、Pinia 等跨平台或状态管理框架，直接使用微信小程序原生能力。Node.js 只用于本地工具链或后端，不作为小程序前端运行时。

主文件见 [SKILL.md](SKILL.md)，变更记录见 [changelogs.md](changelogs.md)。
