<div align="center">

**Claude Code · Codex · OpenCode · pi · Grok**

<p>
  <a href="https://caravel-site.pages.dev/?lang=zh-CN"><strong>访问官网 ↗</strong></a>
  &nbsp; · &nbsp;
  <a href="https://caravel-site.pages.dev/demo/?lang=zh-CN"><strong>在线体验</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/yy36295238/caravel-releases/releases/latest"><strong>下载 Caravel</strong></a>
</p>

[![Latest Release](https://img.shields.io/github/v/release/yy36295238/caravel-releases?display_name=tag&style=flat-square&label=release&color=416fae)](https://github.com/yy36295238/caravel-releases/releases/latest)

macOS（Apple Silicon / Intel）与 Windows x64 · 使用你自己的 Agent 和模型账号

[English](README.md) · **简体中文**

<img src="https://caravel-site.pages.dev/assets/icon.png" width="64" height="64" alt="Caravel">

# Caravel

### 少一点工具切换，多一点真正的创造。

本地优先的多 AI 编码 Agent 工作台。你定目标，Agent 并行推进，结果由你验收。

![Caravel 工作旅程：从 Agent 接入、任务并行到结果交付与经验沉淀](https://raw.githubusercontent.com/yy36295238/caravel-releases/main/docs/assets/caravel-story-zh-CN.png)

</div>

## 当你手上不止一件事

一个项目有 Bug 要修，另一个项目的文档还没补齐，新的想法又冒了出来。你已经在用 AI，却仍要来回切换终端、找回上下文，再逐一确认改动。

在 Caravel 里，这些工作可以同时往前走。每个任务都有自己的目标、项目、对话和代码改动，你随时知道它做到哪一步。

### 写下目标，让几件事一起往前走

给 Codex 派发修复任务，让 Claude Code 补另一个项目的文档，然后继续处理你的需求。工作台集中呈现哪些任务在运行、哪些需要确认、哪些等你验收；想到下一件事，先用快捷浮窗记进待办，准备好后再转成任务。

### 看清改动，再决定交付

打开任务，就能沿着原来的对话继续沟通，查看文件和代码 Diff。你可以要求补一个边界处理，也可以在审查后交付：隔离副本合并回项目，独立分支提交并推送成果。采用这两种模式时，Agent 在副本中工作，原项目的修改由你决定。

### 把这次做成的方法，留给下一次

一次排查结束后，把有效的指令保存为提示词，或从成功对话中提炼工作流，检查并确认后复用。下次遇到类似问题，带上已经验证过的方法开始，让每次完成都为下一次省一点力。

## 工作继续，注意力由你安排

- **查资料时，工具就在旁边**：浏览文件、预览 Markdown、操作 Git，或连接数据库查数，减少搬运上下文的来回切换。
- **离开电脑时，仍能接上进度**：配置飞书并保持本机 Caravel 与飞书桥运行，就能接收任务通知、继续对话、处理授权与验收。
- **遇到重复事项时，安排它按时做**：用定时器运行提醒、本地脚本或 Agent 任务；按计划执行需要 Caravel 保持运行。

你继续使用自己的 Agent、模型账号、Git 和 IDE。任务与会话保存在本机；在线模型和外部集成按各自配置联网。

## 先体验一次从目标到交付

[![Caravel 工作台：全部任务、Agent 会话与代码验收](https://caravel-site.pages.dev/assets/workbench-zh-CN.png)](https://caravel-site.pages.dev/demo/?lang=zh-CN)

**[打开在线体验](https://caravel-site.pages.dev/demo/?lang=zh-CN)**，先看看任务如何推进，再打开 Diff 感受审查过程。演示使用产品原版界面与示例数据，无需安装。

想了解更多场景，查看 [产品亮点](docs/product-highlights.md) 或 [完整功能说明](docs/product-overview.md)。

## 开始使用

1. [下载安装包](https://github.com/yy36295238/caravel-releases/releases/latest)：macOS 打开 `.dmg`，将 **Caravel** 拖入「应用程序」；Windows x64 下载并运行 `Caravel_*_x64-setup.exe`。
2. 准备 Git 和至少一个已安装、完成登录或配置的受支持 Agent CLI。
3. 添加本地项目，创建任务，选择 Agent 并开始运行。

macOS 与 Windows 均提供包含全部功能模块的 Caravel 通用版。macOS 支持应用内自动更新；Windows 更新时下载并运行新版安装包，安装前准备 Git for Windows、Node.js 和 Agent CLI。Windows 安装包尚未签名，如遇 SmartScreen 提示，确认来自本仓库 Releases 后，点击「更多信息 → 仍要运行」。任务与会话保存在本机；Agent 调用在线模型或使用外部集成时仍会联网。

<details>
<summary><strong>首次打开被 macOS 阻止？查看「仍要打开」和终端放行命令</strong></summary>

当前公开版本尚未使用 Apple Developer ID 签名和公证。确认安装包来自本仓库 Releases，并将 Caravel 放入「应用程序」后，可选择以下任一方式打开。

**方式一：在系统设置中允许打开**

1. 先尝试打开一次 Caravel，让 macOS 显示阻止提示。
2. 打开「系统设置 → 隐私与安全性」，向下找到 Caravel 被阻止的说明，点击「仍要打开」。
3. 按提示输入 Mac 登录密码或使用 Touch ID，再点击「打开」。部分系统版本的按钮文案为「仍然打开」。

**方式二：终端放行命令**

打开 Mac 的「终端」，执行以下命令，再重新打开 Caravel：

```sh
xattr -dr com.apple.quarantine /Applications/Caravel.app
```

此命令仅移除 Caravel 的下载隔离属性。其他安装问题见 [官网安装帮助](https://caravel-site.pages.dev/?lang=zh-CN#install-help)。

</details>

---

本仓库提供 **macOS / Windows 安装包与版本记录**。产品介绍、交互演示与常见问题请以 [官网](https://caravel-site.pages.dev/?lang=zh-CN) 为主。

[版本记录](https://github.com/yy36295238/caravel-releases/releases) · [完整功能说明](docs/product-overview.md) · [常见问题](https://caravel-site.pages.dev/?lang=zh-CN#faq)
