# Caravel ⛵

Caravel 是一款本地优先的 macOS AI 编程 Agent 指挥台。它把 Claude Code、Codex、
OpenCode 等编码 Agent 集中到一个桌面工作台中，让你可以统一派发任务、查看执行状态、
继续对话并验收代码改动。

## 主要功能

- 按工作区组织 AI 编程任务，同时管理多个 Agent。
- 实时查看任务状态，在同一个界面继续对话或停止运行。
- 查看代码 diff，集中完成改动审查和验收。
- 支持定时任务、提示词管理和可选的飞书远程操作。
- 任务与配置保存在本机，日常使用不依赖 Caravel 云服务。

## 下载与安装

1. 前往 [Releases](https://github.com/yy36295238/caravel-releases/releases/latest) 下载最新的
   `Caravel_x.y.z_universal.dmg`，Apple Silicon 与 Intel Mac 均可使用。
2. 打开 DMG，将 Caravel 拖入「应用程序」。
3. 首次启动时，右键点击 `Caravel.app`，选择「打开」。如果仍被 macOS 阻止，可执行：

```bash
sudo xattr -cr "/Applications/Caravel.app"
```

运行任务前，请先安装并登录至少一个编码 Agent CLI：Claude Code、Codex 或 OpenCode。
安装完成后，后续版本可以直接通过 Caravel 应用内更新。
