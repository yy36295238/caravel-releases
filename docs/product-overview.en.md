# Caravel product and feature guide

**English** · [简体中文](product-overview.md)

## Product positioning

**Caravel is a local-first workspace for multiple AI coding agents, built for developers working across projects and tasks. It supports macOS (Apple Silicon / Intel) and Windows x64.**

Both platforms provide the complete app with all feature modules and retain existing application data. macOS supports in-app updates; Windows updates use the latest installer. Choose your platform on the [download page](https://github.com/yy36295238/caravel-releases/releases/latest). See the [installation help](https://caravel-site.pages.dev/?lang=en#install-help) for first-launch instructions.

Caravel brings Claude Code, Codex, OpenCode, pi, Grok, TRAE, and other coding agents into one desktop workbench. Delegate tasks, track progress, handle permissions, review code, and deliver changes in one place. Install or upgrade agents from Settings.

Keep using your own agent CLIs, model accounts, and IDE. Caravel organizes agents, projects, conversations, and code changes into a clear task workflow.

## Why Caravel exists

A CLI is straightforward for one or two tasks. With several projects and agents running at once, it becomes harder to know which task is running, waiting for input, or ready for review—and which conversation belongs to which project.

Developers end up maintaining a mental table of terminals, projects, agents, goals, permissions, and changes. Managing the agents becomes a bottleneck of its own.

Caravel turns these separate execution sessions into traceable tasks. Each task has a goal, workspace, agent, ongoing conversation, status, and final code changes. Delegate, monitor, intervene, and review from one workbench.

## Core value

- **Unified management**: multiple agents, projects, and parallel tasks in one workspace.
- **Visible progress**: follow execution, agent actions, pending decisions, and results.
- **Controlled delivery**: permissions, code review, and acceptance determine how changes reach your project.
- **Reusable methods**: save prompts, skills, lessons, and successful workflows.
- **Continuous improvement**: use cost insights and AI reviews to improve collaboration.
- **Tools close at hand**: schedules, databases, and small apps support everyday work.

## Feature map

| Area | Capabilities | Purpose |
|---|---|---|
| Core workflow | Agent coordination, tasks, safe delivery, mobile collaboration | Manage delegation, intervention, and code review |
| Automation | Schedules and workflows | Run recurring tasks and structured processes |
| Knowledge and effectiveness | Prompts, skills, lessons, insights, reviews | Reuse methods and assess results, cost, and runtime health |
| Development tools | Editor, databases, to-dos, inbox, clipboard, apps | Handle everyday development and personal productivity |
| Settings and environment | Agents, plugins, models, permissions, maintenance | Manage tools, capabilities, and preferences |

## Features

### 1. Workbench

Create and manage AI agent tasks with list, board, and split views.

- Manage Claude Code, Codex, OpenCode, pi, Grok, and TRAE together.
- Conversations, permissions, plans, subagent progress, code diffs, and delivery share one page.
- Display live assistant replies smoothly as chunks arrive. History, synchronized records, and web polling snapshots appear in full; returning to the window skips queued background animation. Follow reasoning and tool activity exposed by the agent.
- Choose a model and reasoning effort for a new task, a continuation, or a conversation fork. Defaults follow model settings. Manage models in Agent settings; historical tasks retain their existing model selection. Task headers show the latest known reasoning effort; continuations retain it without overwriting manual choices.
- Scrolling toward the top loads earlier messages while preserving your reading position, including task quick previews and mobile task details.
- Task turn counts and active time cover the full conversation, independently of message pagination. Active time excludes idle waits for input between turns.
- Long task descriptions can be summarized into short titles asynchronously by the selected agent and model. Execution continues; the original name remains while generation runs. Desktop, web, and mobile details show generation status. Full goals and manual names are preserved, and failure keeps the original name.
- Link several workspaces to a task and view directly or indirectly related tasks.
- Separate-branch tasks can create an isolated copy for each Git project, with per-project remote main/master baselines and development branches. Add projects, inspect connection status, browse files, and use Git from the task’s project panel.
- Projects added during a run join the next run, or you can pause, attach, and continue. Multi-project execution requires agent or adapter support for additional working directories.
- Copy conversation messages as text or images.
- Startup and periodic checks reconcile running tasks and pending confirmations whose processes have exited. Explicitly interrupted tasks await continuation without restarting automatically. Codex/TRAE runs without current-turn records or a clear final state are marked as failed.
- Stop a task at any time or take over in a terminal.

### 2. Task library

Keep and find historical tasks in one place.

- Filter by status, agent, workspace, date, and related tasks.
- Search, favorite, archive, and group tasks.
- Search sidebar workspaces by name or path. Matching groups expand temporarily; clearing the search restores their previous state.
- Import and synchronize existing agent sessions, including native and officially migrated TRAE CLI 2.0 sessions. Codex supports both older and newer session formats. Rebuilding preserves image attachments and reply ratings; incomplete parsing or failed writes retain the original conversation while reconciling run status separately. Manual sync reports incomplete conversation updates; historical runs do not overwrite the current task status.
- Open workspaces and manage Git branches, commits, pushes, and conflicts. Remove separate-branch entries even when their local copy is missing. Cleaned projects with missing directories are hidden while tasks and recovery information remain available.
- Commit only selected files while preserving unselected staged changes and tracked-file deletions. Task headers show the branch and changed-file count.
- Choose a model and generate a commit message directly in the commit dialog, edit the draft, then commit or commit and push. Generated summaries use a type prefix by default and prioritize explicit formatting instructions. Additional instructions stay available when collapsed; search and reuse the latest 20 entries shared across repositories on this machine.

### 3. Schedules

Automate work that runs daily, weekly, at intervals, or just once.

- Describe the time and task in natural language; review the parsed form before creating the schedule.
- Alternatively, enter the name, instructions, and recurrence manually.
- Run daily, weekly, every few minutes or hours, or once.
- Set multiple times for daily or weekly schedules, such as 09:30 and 20:30.
- Restrict interval schedules to selected weekdays and working hours.
- Choose local reminders, local scripts, or agent execution. Reminders do not call an agent. Agents can generate and trial a script once, then run it on schedule without repeated model calls; shell and PowerShell are supported.
- Optionally catch up on runs missed while the computer was unavailable.
- Run a schedule immediately to inspect its behavior.
- Review run history and output, with optional notification cards.
- Pause, edit, or delete schedules; use list or card views and see the next run time.

### 4. Editor

Browse, search, and edit project files.

- Multiple tabs, syntax highlighting, and autosave.
- Markdown, Mermaid, and image previews; open pasted file or directory paths.
- Inspect, locate, and revert changes relative to the last commit, including image comparisons in diffs.
- Copy full paths, open complete diffs, and use common Git actions from file previews. Collapse directories in the diff file tree.
- Open the current directory in an installed external editor and remember that preference. Supported locations include the main workspace, linked directories, and isolated copies.

### 5. Databases

Connect to MySQL, PostgreSQL, SQLite, MongoDB, or Redis to query and edit data.

- Browse objects, filter and page through data, open local SQLite files, query MongoDB documents, and manage Redis keys.
- Write SQL or document queries, inspect and edit results, and export complete results, including SQL output. For editable results, cell and row-detail value dialogs let you edit raw text, set NULL, and stage changes for confirmation and submission in the results panel.
- Resize result columns by dragging or keyboard; hidden columns and horizontal scrolling retain correct field positions.
- Generate, explain, optimize, and repair queries with a conversational SQL Copilot.
- Save queries, use parameters, and inspect execution history and object definitions.
- Let agents access authorized database capabilities through MCP.
- Confirm dangerous production operations and inspect target-table size before changes.
- Refuse to save connection passwords when encryption fails; key errors do not silently replace the existing key.
- Collapse connection lists. Look up exact Redis keys directly or continue wildcard searches by cursor, with a clear distinction between an unfinished scan and no matches. Type filtering also works with Redis versions before 6.

### 6. To-dos, inbox, and clipboard

Keep personal tasks and reference material nearby.

- **To-dos**: to-do, in-progress, and done states; tags, date ranges, subtasks, images, and attachments. Convert a to-do into an AI task and follow its completion automatically.
- **Inbox**: collect ideas, questions, and material with tags, images, and files.
- **Clipboard**: retain text, code, JSON, and image history with search, categories, favorites, and reusable snippets. On macOS, capture runs only after clipboard changes and skips file references; explicit image pasting and attachments remain available.

### 7. Prompts, skills, and lessons

Reuse effective instructions, tools, and knowledge.

- Group prompts, use variables, pin entries, and preselect skills and MCP tools. Insert prompts from buttons or `/` commands while creating a task or continuing a conversation.
- Search prompt titles, bodies, aliases, and groups alongside group navigation. Click a title to edit; creating within a group retains that group.
- Combine skills and MCP tools for each task. MCP dependencies of selected skills follow into tasks and workflows.
- Reviews can still save solutions, usage scenarios, and lessons. There is no separate knowledge-library entry in the sidebar or feature settings; existing knowledge data remains intact.

### 8. Workflows

Combine agent steps, commands, and human approval into repeatable processes.

- Assign roles, models, skills, and requirements to individual steps.
- Use variables, automatic advancement, approval gates, retries, jumps, and cancellation.
- Attach existing tasks to a workflow.
- Extract a reusable workflow from a successful agent conversation.
- Keep execution history for later review.
- Search text within embedded workflow conversations, see match counts, and navigate between matches.

### 9. Insights and reviews

Assess effectiveness, cost, and opportunities to improve.

- **Insights**: task efficiency, agent and model performance, tool usage, cost, permissions, and runtime health.
- Compare spending or tokens with the previous period; drill down by agent, model, workspace, or tag. The high-usage ranking aggregates runs by task within the current filters, with run details and a link to the original task.
- View supported account quotas and reset times. TRAE weekly quota depends on its enterprise service; unavailable data shows an error or an older snapshot.
- Inspect installation size, stored data, memory, and CPU usage per agent. TRAE storage covers CLI data and excludes other IDE data.
- **Reviews**: use time, workspace, and tag filters to generate AI summaries with evidence, achievements, issues, and next steps.
- Export reports or turn their conclusions into prompts, lessons, workflows, or skills.
- Rate individual replies and compare approval rates by model.

### 10. My apps

Keep personal tools inside the workbench.

- Describe a small tool and have AI build it, such as a daily report helper or dashboard.
- Add a website or local webpage as a linked app and open it in a window.
- Apps can fetch data, access selected files, send notifications, or view tasks after requesting the corresponding permissions.
- Private storage and database access require authorization. Cross-database file access, query duration, concurrency, and result size are limited. Network redirects across origins require a new authorized request; oversized responses are truncated.
- Improve apps, save versions, and export them to share.

### 11. Separate branches and controlled delivery

Agents can execute independently while you retain control over key permissions and final changes.

- Work in isolated copies to avoid directly changing the original project.
- Inspect branch changes, browse copy files, and safely remove local copies from the workspace.
- Clean up completed, safe copies from Settings while keeping tasks and remote branches available for continuation.
- Review changes across repositories in multi-project tasks, then commit and push individually or together. Partial push failures retain successful results; uncommitted or unpushed work still needs review.
- Unlinking a project stops its participation in future runs but preserves its copy and results. Deleting a separate-branch task also keeps its copies; newer copies can start a new task and conversation through Continue Development.
- Before cleaning up a project copy, check uncommitted files and remote commit state and keep recovery information. Resume at the original path. If the remote result branch was deleted, show that explicitly; after cleanup, a new branch can be created from the mainline.
- Legacy separate-branch tasks retain their directories and linking behavior. Create a new task for multi-project isolation. New separate-project tasks cannot fork into a shared writable copy.
- Confirm sensitive actions with one-time or persistent permissions.
- Review changes before merging; request further work or discard the result when necessary.

### 12. Settings

Manage preferences and the execution environment.

- **Agents**: choose agents, models, permissions, and defaults. CLI model discovery marks existing models it did not find, allowing bulk removal and saving.
- **Codex transport**: App Server is the default; saved CLI/ACP choices remain. Changes affect subsequent runs. App Server supports resume, fork, approval cards, input forms, and mid-run instructions; standard mode allows workspace writes with on-request approval, while plan mode is read-only. CLI has no live approvals or mid-run instructions, uses read-only standard/plan modes, and offers forks when supported by the installed version. Fast applies only to ACP.
- **TRAE**: requires CLI 2.0 and an Enterprise Flagship account. Discover account models and reasoning efforts; use tasks, workflows, schedules, and AI assistance. Images, additional directories, forks, and mid-run instructions depend on CLI capabilities.
- **Installation and tools**: install or upgrade agents and supporting tools such as Git, Node, and cc-switch. Upgrades retain the detected installation source and verify runnable versions. Progress, queues, and installer guidance remain visible across menu changes. Graphical installers require completion and a refresh; batch upgrades distinguish completed, manual, and failed results.
- **Plugins**: manage Claude, Codex, OpenCode, and TRAE plugins and select them for tasks.
- **Terminal**: choose the default terminal for opening shells or taking over agent sessions.
- **Appearance and language**: themes, task animations, and zoom. Choose Simplified Chinese, English, or system language. Desktop windows synchronize; browser and mobile clients store their own preference. The desktop app retains Chinese when unset. User content, code, and history stay in their original language.
- **Language coverage**: workbench, Git, editor, databases, workflows, schedules, personal tools, insights, reviews, tray, fixed tool-window titles, notifications, and Feishu remote-control text. Built-in AI assistance defaults to the interface language and respects an explicitly requested language.
- **Error recovery**: page, rendering, and startup failures show available reasons and stack traces for copying and feedback, with a reload option. The main window can return home; tool windows recover their current page. Action errors keep the interface visible with a dismissible notice. Rust panics save a local report and show its location and reason on the next launch; forced termination and native WebView crashes are outside this coverage. Save unsaved input before reloading.
- **Feature management**: show, hide, and reorder sidebar entries.
- **Skills**: inspect skills and MCP tools for different agents. TRAE supports global skills and native stdio/HTTP MCP configuration; task-level SSE uses a proxy.
- **Remote control**: configure Feishu, intelligent conversations, and message history.
- **Browser access**: independently enable the full web client and read-only mobile client. Disabling one leaves the other available; enabled access modes are restored after restart.
- **Updates**: macOS update checks and downloads support system proxies and show download and installation progress. Manual and startup updates share progress across navigation. Failed checks offer a browser download link; Windows uses the latest installer in the browser.
- **Maintenance**: updates, runtime environment, isolated copies, and service logs. Copy lists show directories still on disk, support grouping by task or project, search, rescanning, and task links. Recovery metadata stays in tasks; directories without recovery metadata are not cleaned up automatically.

### 13. Feishu remote collaboration

Follow tasks and handle key decisions away from your computer, without configuring a public server address.

- View task status and agent progress.
- Create tasks and continue conversations.
- Handle permission requests and code acceptance.
- Receive key status notifications.

## Typical workflow

1. Install the agents you need in Settings, select a project, describe a goal, and choose an agent.
2. Follow multiple runs from the workbench.
3. Respond when permissions or decisions need your attention.
4. Review completed changes and choose to merge, continue, or discard them.
5. Save useful prompts, lessons, and workflows.
6. Schedule recurring work by describing the time and action, then confirming the form.
7. Improve future collaboration through reviews and cost insights.
8. Generate a personal tool or add a useful website in My apps.

## Who it is for

Developers using several coding agents, engineers working across projects, users who want autonomous execution with code control, people running recurring checks and fixes, heavy users building reusable AI methods, and technical leads tracking efficiency, cost, and delivery quality. It also brings reminders, scripts, databases, and small personal tools into the same workspace.

## Product principles

**Local-first**: the app manages tasks, conversations, workspaces, and personal knowledge on your machine. You choose whether to enable remote capabilities such as Feishu.

**Agent choice**: choose tools according to model strengths, task type, and personal preference. Install and upgrade them in Settings and manage them through one product interface.

**You decide; agents execute**: retain goal-setting, permission decisions, code review, and final acceptance while agents handle repetitive execution.

[Download Caravel](https://github.com/yy36295238/caravel-releases/releases/latest) · [Website](https://caravel-site.pages.dev/?lang=en) · [Try the demo](https://caravel-site.pages.dev/demo/?lang=en)
