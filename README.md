# fashion-web-scraper · 时尚官网/秀场素材自动采集

> 给一个品牌官网 / 秀场链接，变成一批归档可用的参考素材：自动定位最新季秀场、提取设计理念、下载高清图、按素材库规范落盘登记。可独立使用，也可作为 [fashion-studio](https://github.com/hexiaoyu0525-design/fashion-studio) 的可选旁挂。

License: **CC BY 4.0**（使用须署名）· 版本 0.1.0 · 作者：hexiaoyu0525-design

---

## 这是什么

一个 **Agent Skill**：`SKILL.md` + `assets/setup.ps1`（可选本地批量通道的初始化脚本）。核心是「通道选择 + 落盘规范 + 版权分级」方法论——零代码也能用（通道③手动放图，人人可用、永远可用）。

## 三条通道（按环境选，不强制）

| 通道 | 场景 | 代价 |
|---|---|---|
| ① 本地 playwright-cli | 批量 / 定时 / 无人值守 | 需本地 Node.js ≥ 18 + 浏览器内核 |
| ② Agent 内置浏览器 | 临时少量、零部署 | 慢；出口网络受限时国际站可能被拦 |
| ③ 手动放图 / 直接发参考图 | **零门槛，人人可用** | 慢，但永远可用 |

## 安装

- **独立使用**：把 `fashion-web-scraper` 文件夹放入 Agent 的 skills 目录（Claude Code `~/.claude/skills/`、WorkBuddy `~/.workbuddy/skills/`、豆包 `.user_skills/` 等）。
- **配合 fashion-studio**：[fashion-studio](https://github.com/hexiaoyu0525-design/fashion-studio) 的路由表指向本技能；不装也完全可用（fs 自带手动放图通道）。
- **换新电脑**：需要通道①时运行 `pwsh -NoProfile -File assets/setup.ps1 -InstallBrowser`；不装内核不影响使用。

## 与 fashion-studio 的关系

- 独立仓库、独立方法论；`fashion-studio` 负责设计生产，本技能只负责「官网/秀场素材采集」这一件事。
- 采集素材的命名、落盘、版权分级沿用 fashion-studio 的 `asset-library-schema.md` 口径；未装 fs 时按 SKILL.md 内「落盘规范」执行。

## 使用边界

本仓库公开，欢迎学习与借鉴方法论（通道设计、降级思路、版权分级思路均可参考）。但不得在未署名或改名换名后作为自己作品发布；引用本作品内容请注明出处。

## 许可证

[CC BY 4.0](LICENSE) · 完整法律文本见 LICENSE。© 2026 hexiaoyu0525-design · 仓库：<https://github.com/hexiaoyu0525-design/fashion-web-scraper>
