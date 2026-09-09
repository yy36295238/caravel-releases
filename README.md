<div align="center">

**English** · [简体中文](README.zh-CN.md)

<img src="https://caravel-site.pages.dev/assets/icon.png" width="64" height="64" alt="Caravel">

# Caravel

### Less switching tools. More creating.

A local-first workspace for multiple AI coding agents. You set the goals, agents work in parallel, and you review the results.

**Claude Code · Codex · OpenCode · pi · Grok**

<p>
  <a href="https://caravel-site.pages.dev/?lang=en"><strong>Visit website ↗</strong></a>
  &nbsp; · &nbsp;
  <a href="https://caravel-site.pages.dev/demo/?lang=en"><strong>Try the demo</strong></a>
  &nbsp; · &nbsp;
  <a href="https://github.com/yy36295238/caravel-releases/releases/latest"><strong>Download Caravel</strong></a>
</p>

[![Latest Release](https://img.shields.io/github/v/release/yy36295238/caravel-releases?display_name=tag&style=flat-square&label=release&color=416fae)](https://github.com/yy36295238/caravel-releases/releases/latest)

macOS (Apple Silicon / Intel) and Windows x64 · Use your own agent and model accounts

</div>

## When you have more than one thing to do

One project has a bug to fix. Another needs its documentation updated. A new idea arrives before either is done. You already use AI, but you still switch terminals, recover context, and check each set of changes yourself.

In Caravel, those tasks can move forward together. Each keeps its goal, project, conversation, and code changes in one place, so you can see where the work stands.

### Set the goals and move several tasks forward

Give Codex the bug fix and Claude Code the docs for another project, then get back to your own work. The workbench shows what is running, what needs a decision, and what is ready for review. When another idea comes up, capture it in a to-do from the quick-entry window and turn it into a task when you are ready.

### See the changes before you deliver

Open a task to continue its conversation, browse files, and inspect the code diff. Ask for a missing edge case to be handled, or deliver after review: merge an isolated copy back into the project, or commit and push an independent branch. In these two modes, agents work in separate copies; you decide what reaches the original project.

### Keep what worked for next time

After resolving an issue, save an effective instruction as a prompt, or extract a workflow from the successful conversation, review it, and confirm it for reuse. Start the next similar task with a method you have already checked.

## Keep work moving on your schedule

- **Keep tools close to the task**: browse files, preview Markdown, use Git, or connect a database to query data, with less context to carry between apps.
- **Stay involved away from your desk**: configure Feishu and keep Caravel and its bridge running on your computer to receive task updates, continue conversations, handle permissions, and review results.
- **Schedule the recurring work**: run reminders, local scripts, or agent tasks on a schedule. Scheduled execution requires Caravel to remain running.

Keep using your own agents, model accounts, Git, and IDE. Tasks and conversations stay on your machine; online models and external integrations connect according to their configuration.

## Try the path from goal to delivery

[![Caravel workbench: tasks, agent conversations, and code review](https://caravel-site.pages.dev/assets/workbench-en.png)](https://caravel-site.pages.dev/demo/?lang=en)

**[Open the interactive demo](https://caravel-site.pages.dev/demo/?lang=en)** to see how tasks progress and explore a code diff. The demo uses the actual product interface and sample data. No installation required.

Explore more use cases in the [product highlights](docs/product-highlights.en.md) or the [feature guide](docs/product-overview.en.md).

## Get started

1. [Download the installer](https://github.com/yy36295238/caravel-releases/releases/latest). On macOS, open the `.dmg` and drag **Caravel** into Applications. On Windows x64, download and run `Caravel_*_x64-setup.exe`.
2. Prepare Git and at least one supported agent CLI, installed and signed in or configured.
3. Add a local project, create a task, choose an agent, and start the run.

Both platforms provide the complete Caravel app with all feature modules. macOS supports in-app updates; on Windows, download and run the new installer to update. Windows requires Git for Windows, Node.js, and an agent CLI. The Windows installer is not yet signed: if SmartScreen appears, verify that it came from this repository’s Releases, then choose “More info → Run anyway”. Tasks and conversations stay on your machine; online model calls and external integrations still use the network.

<details>
<summary><strong>First launch blocked on macOS? Use Open Anyway or Terminal</strong></summary>

The public macOS app is not yet signed with an Apple Developer ID or notarized. Verify that the installer came from this repository’s Releases and move Caravel into Applications, then use either option below.

**Option 1: Allow the app in System Settings**

1. Try opening Caravel once to trigger the macOS warning.
2. Open “System Settings → Privacy & Security”, find the notice about Caravel, and click “Open Anyway”.
3. Enter your Mac login password or use Touch ID, then click “Open”. Button wording may vary by macOS version.

**Option 2: Use Terminal**

Open Terminal on your Mac, run this command, and reopen Caravel:

```sh
xattr -dr com.apple.quarantine /Applications/Caravel.app
```

This command only removes Caravel’s download quarantine attribute. See the [installation help](https://caravel-site.pages.dev/?lang=en#install-help) for more details.

</details>

---

This repository provides **macOS / Windows installers and release history**. Visit the [website](https://caravel-site.pages.dev/?lang=en) for product information, the interactive demo, and FAQs.

[Releases](https://github.com/yy36295238/caravel-releases/releases) · [Feature guide](docs/product-overview.en.md) · [FAQ](https://caravel-site.pages.dev/?lang=en#faq)
