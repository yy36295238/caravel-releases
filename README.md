<div align="center">

# Caravel ⛵

### 本地优先的多 AI 编程 Agent 指挥台

把散落在终端里的 **Claude Code、Codex 和 OpenCode** 变成可派发、可追踪、可对话、可验收的任务工作流。

Local-first macOS control center for AI coding agents.

<p>
  <a href="https://github.com/yy36295238/caravel-releases/releases/latest"><strong>下载 macOS 最新版</strong></a>
  ·
  <a href="https://github.com/yy36295238/caravel-releases/releases">查看版本记录</a>
</p>

![Latest Release](https://img.shields.io/github/v/release/yy36295238/caravel-releases?display_name=tag&style=flat-square&label=release&color=1677ff)
![macOS](https://img.shields.io/badge/macOS-Apple%20Silicon%20%7C%20Intel-111111?style=flat-square&logo=apple)
![Local First](https://img.shields.io/badge/data-local--first-22a06b?style=flat-square)
![Agents](https://img.shields.io/badge/agents-Claude%20Code%20%7C%20Codex%20%7C%20OpenCode-7c3aed?style=flat-square)

</div>

---

## Caravel 是做什么的？

同时运行多个 AI 编程 Agent 时，真正麻烦的往往不是生成代码，而是管理过程：哪个 Agent
正在做什么、卡在权限还是等待输入、改了哪些文件、应该继续对话还是开始验收。

Caravel 在现有 Agent CLI 和代码编辑器之上增加一个桌面任务层：一个任务关联一个工作区和
一个 Agent，从目标派发、运行监控、多轮对话到代码 diff 验收，都在同一个工作台中完成。

> **Caravel 不替代你的 Agent、模型或 IDE。** 你仍然使用自己的 Claude Code、Codex、
> OpenCode 与编辑器；Caravel 负责把多个 Agent 和多个项目组织成清晰、可控的工作流。

## 一条完整的 AI 编程工作流

**连接工作区 → 创建任务 → 选择 Agent → 监控执行 → 继续对话 → 查看 Diff → 完成验收**

你不必再在多个终端窗口之间寻找会话，也不必靠记忆判断每个任务进行到了哪里。

## 核心能力

| 能力 | 你能得到什么 |
|---|---|
| **多 Agent 统一管理** | 在一个工作台中使用 Claude Code、Codex 和 OpenCode，按任务选择最合适的 Agent。 |
| **任务状态实时追踪** | 集中查看运行中、待确认、待验收、已完成和失败任务，快速发现卡点。 |
| **多轮对话与会话续接** | 保留任务上下文，继续向同一个 Agent 补充要求、纠正方向或追问结果。 |
| **工作区与隔离运行** | 任务绑定 Git 仓库或文件夹，可直接运行，也可使用隔离副本或独立分支。 |
| **代码 Diff 与验收** | 在应用内查看 Agent 的代码改动，让“完成任务”真正落到可审查的结果上。 |
| **定时与无人值守** | 安排稍后执行或周期任务，减少必须守在电脑前等待的时间。 |
| **飞书远程操作（可选）** | 在手机上查看任务、继续对话或处理待确认事项，无需开放公网端口。 |
| **本地优先** | Caravel 的任务、工作区和配置保存在本机，不要求注册 Caravel 云账号。 |

## 适合谁？

- 同时维护多个项目，希望并行安排 AI 编程任务的开发者。
- 经常在 Claude Code、Codex、OpenCode 之间切换，希望统一管理会话的人。
- 希望把 AI 编程从“开终端聊天”升级为可追踪、可审查任务流程的团队或个人。
- 需要定时执行、远程查看进度，或让 Agent 在无人值守时继续工作的用户。

## 支持的 Agent

| Agent | 使用方式 |
|---|---|
| **Claude Code** | 连接本机已安装并登录的 `claude` CLI |
| **OpenAI Codex** | 连接本机已安装并登录的 `codex` CLI |
| **OpenCode** | 连接本机已安装并登录的 `opencode` CLI |

Agent 的账号登录、模型选择和 API 凭据仍由各自 CLI 管理，Caravel 不接管这些敏感信息。

## 下载与安装

### 运行前准备

- 一台 Apple Silicon 或 Intel Mac。
- 已安装 Git。
- 已安装并登录 Claude Code、Codex 或 OpenCode 中的至少一个。

### 安装 Caravel

1. 打开 [最新版本下载页](https://github.com/yy36295238/caravel-releases/releases/latest)。
2. 下载 `Caravel_x.y.z_universal.dmg`。
3. 打开 DMG，将 **Caravel** 拖入「应用程序」。
4. 首次启动时，右键点击 `Caravel.app`，选择「打开」。

当前版本尚未使用 Apple Developer ID 签名或公证。如果 macOS 仍阻止打开，请确认安装包来自本仓库，
然后在「系统设置 → 隐私与安全性」中仅放行 Caravel。不建议使用命令批量清除应用的安全属性。

安装一次后，后续版本可以直接通过 Caravel 应用内更新。

## 安全使用建议

Caravel 可以启动本机 Agent、读写工作区并执行经过授权的命令，应将它视为具有本地代码执行能力的
开发工具。为了保护代码、账号和本机数据，请遵循以下原则：

- **只从官方仓库下载和更新**：仅使用本仓库 Releases 页面或 Caravel 应用内更新，不安装他人重新打包的版本。
- **只连接可信工作区**：陌生仓库可能通过项目说明、脚本或依赖影响 Agent 行为；运行前先检查来源和关键脚本。
- **谨慎开启全自动模式**：默认保留 Agent 的审批与沙箱保护；只有在任务和工作区均可信时，才允许无人值守执行。
- **谨慎授权 mini-app**：只安装来源可信的 mini-app；网络、浏览器、文件、剪贴板和 Caravel 数据权限仅在确有必要时授予。
- **保护敏感凭据**：按需配置飞书和自定义模型密钥，不要把 Token、密码或私钥写进任务提示、日志或可提交文件；备份应用数据时同样按敏感数据处理。
- **执行外部操作前复核**：合并、提交、推送、部署或运行生成的脚本前，先检查 Diff、目标分支和实际命令。
- **及时更新**：优先使用最新版本，并同步更新 macOS、Agent CLI 和项目依赖，及时获得安全修复。

如果工作区、mini-app 或安装包来源无法确认，建议停止运行并先完成核验。

## 3 分钟快速开始

1. 打开 Caravel，在设置中确认已识别到你使用的 Agent CLI。
2. 注册一个本地 Git 仓库或项目文件夹作为工作区。
3. 新建任务，写清目标并选择 Agent，然后开始运行。
4. 在任务详情中查看状态与输出；需要调整时直接继续对话。
5. Agent 完成后查看代码 Diff，确认结果并完成验收。

## 常见问题

<details>
<summary><strong>Caravel 是新的 AI 模型或代码编辑器吗？</strong></summary>

不是。Caravel 是 AI coding agent manager / desktop control center，负责组织本机已有的
Claude Code、Codex 和 OpenCode。你可以继续使用熟悉的 IDE、终端和模型账号。

</details>

<details>
<summary><strong>数据会上传到 Caravel 服务器吗？</strong></summary>

Caravel 的任务、工作区配置和运行记录保存在本机，不要求 Caravel 云服务。Agent CLI
本身是否访问云端，取决于你选择的 Agent、模型和它自己的配置。

</details>

<details>
<summary><strong>为什么 macOS 首次打开会提示无法验证开发者？</strong></summary>

当前公开版本尚未使用 Apple Developer ID 签名和公证。请确认安装包来自本仓库的
Releases 页面，然后按上方安装步骤右键打开或清除隔离属性。

</details>

<details>
<summary><strong>支持 Windows 或 Linux 吗？</strong></summary>

当前公开安装包只提供 macOS 通用版，同时支持 Apple Silicon 与 Intel。

</details>

<details>
<summary><strong>如何获得新版本？</strong></summary>

可以在 Releases 页面手动下载，也可以在安装后使用 Caravel 应用内自动更新。

</details>

---

如果 Caravel 让你的多 Agent 工作流更清晰，欢迎收藏本仓库，方便及时获取新版本。

<!--
产品截图加入建议：
1. assets/screenshots/workbench.png：工作台总览，建议 1600×1000，作为首屏主图。
2. assets/screenshots/task-detail.png：任务详情、多轮对话和状态，建议 1600×1000。
3. assets/screenshots/diff-review.png：代码 Diff 与验收，建议 1600×1000。
4. assets/screenshots/remote-control.png：飞书远程操作，可选，建议 1200×900。
图片就绪后，在首屏 badges 下加入 workbench 大图，在“核心能力”后用两列展示另外两张。
截图前请隐藏真实项目名、路径、用户名、对话内容、密钥和公司数据。
-->
