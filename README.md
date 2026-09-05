<div align="center">

<img src="https://caravel-site.pages.dev/assets/icon.png" width="64" height="64" alt="Caravel">

# Caravel

### 你掌舵，Agent 并行。

本地优先的多 AI 编码 Agent 工作台，把项目、任务、会话和代码验收放在一起。

**Claude Code · Codex · OpenCode · pi · Grok**

<p>
  <a href="https://caravel-site.pages.dev/"><strong>访问官网 ↗</strong></a>
  &nbsp; · &nbsp;
  <a href="https://caravel-site.pages.dev/demo/"><strong>在线体验</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/yy36295238/caravel-releases/releases/latest"><strong>下载 macOS 版</strong></a>
</p>

[![Latest Release](https://img.shields.io/github/v/release/yy36295238/caravel-releases?display_name=tag&style=flat-square&label=release&color=416fae)](https://github.com/yy36295238/caravel-releases/releases/latest)

Apple Silicon / Intel · 使用你自己的 Agent 和模型账号

[![Caravel 工作台：全部任务、Agent 会话与代码验收](https://caravel-site.pages.dev/assets/workbench.png)](https://caravel-site.pages.dev/)

**点击截图，访问官网并体验完整工作台。**<br>
<sub>演示使用产品原版界面与示例数据，无需安装。</sub>

</div>

## 从目标，到交付

- **并行派发**：给不同项目创建任务，选择 Agent，让多项工作同时推进。
- **集中跟进**：查看执行状态，接续会话，在需要时确认权限或调整方向。
- **审查交付**：查看代码 Diff，继续修改，或在验收后合并。

我的应用、定时器、工作流和更多功能，前往 [官网查看](https://caravel-site.pages.dev/#possibilities) 或 [在线操作体验](https://caravel-site.pages.dev/demo/)。

## 开始使用

1. [下载最新 macOS 安装包](https://github.com/yy36295238/caravel-releases/releases/latest)，打开 DMG，将 **Caravel** 拖入「应用程序」。
2. 准备 Git 和至少一个已安装、完成登录或配置的受支持 Agent CLI。
3. 添加本地项目，创建任务，选择 Agent 并开始运行。

安装后支持应用内更新。任务与会话保存在本机；Agent 调用在线模型或使用外部集成时仍会联网。

<details>
<summary><strong>首次打开被 macOS 阻止？</strong></summary>

当前公开版本尚未使用 Apple Developer ID 签名和公证。先尝试右键「打开」，或在「系统设置 → 隐私与安全性」中放行 Caravel。

如果仍因下载隔离被阻止，确认安装包来自本仓库 Releases，且应用已放入「应用程序」，再在终端执行：

```sh
xattr -dr com.apple.quarantine /Applications/Caravel.app
```

此命令仅移除 Caravel 的下载隔离属性。其他安装问题见 [官网安装帮助](https://caravel-site.pages.dev/#install-help)。

</details>

---

本仓库提供 **macOS 安装包与版本记录**。产品介绍、交互演示与常见问题请以 [官网](https://caravel-site.pages.dev/) 为主。

[版本记录](https://github.com/yy36295238/caravel-releases/releases) · [完整功能说明](docs/product-overview.md) · [常见问题](https://caravel-site.pages.dev/#faq)
