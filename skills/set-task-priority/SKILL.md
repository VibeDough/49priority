---
name: set-task-priority
description: Add a colored priority dot directly before Codex task titles in the sidebar and track status for projects and subtasks. Use when the user asks to mark, color, rank, rename, or change the priority of a Codex task or child task; mentions urgency, P0-P6, red/orange/yellow/green/blue/purple/gray dots; or wants task-list priority visible at a glance.
---

# Set Task Priority

Make priority visible in the Codex sidebar by prefixing task titles with a colored circle.

## Start a task

1. Detect an explicit label in the request. Accept a color, `P0`-`P6`, or a priority name.
2. If the request is actionable and has no label, ask only:

   `先标一下优先级：🔴 紧急 / 🟠 高 / 🟡 中 / 🟢 普通 / 🔵 低 / 🟣 有空再做 / ⚪ 暂停？`

3. Accept one-click-style short replies such as `红`, `橙色`, `P2`, or `普通`.
4. Rename the current Codex task with the available task/thread title tool. Preserve the existing title and add the selected marker at the beginning.
5. Default the initial status to `待开始` unless the user supplied another status.
6. Confirm in one compact line, then continue the task:

   `🔴 P0 紧急 · 🟠 进行中 — 修复登录崩溃`

Example sidebar title: `🔴 创建任务优先级标记插件`.

Do not ask for a priority again after it has been set in the current task.

## Rename sidebar tasks

- Use the Codex task-title/thread-title tool immediately after the user selects a marker.
- Target the calling task when no task ID is specified.
- When a child task ID is available and the user explicitly targets that child, rename that child task.
- Preserve the title text. P0-P5 add or replace one leading priority marker.
- Recognize `🔴`, `🟠`, `🟡`, `🟢`, `🔵`, and `🟣` as priorities; recognize `⚪` as a pause marker.
- Allow one priority plus one pause marker in the canonical order `<priority> ⚪ <title>`. Pause may also stand alone as `⚪ <title>`.
- Never duplicate markers. Changing `🔴 ⚪ 修复登录` to blue must produce `🔵 ⚪ 修复登录`.
- Do not add status markers to the sidebar title; the leading circle is priority only.
- If the title tool is unavailable, say that the current Codex surface cannot rename the task. Do not pretend the sidebar changed.

## Priority scale

| Marker | Code | Meaning | Use when |
|---|---:|---|---|
| 🔴 | P0 | 紧急 | Act now; blocking, outage, or hard deadline |
| 🟠 | P1 | 高 | Next item; important and time-sensitive |
| 🟡 | P2 | 中 | Planned soon; meaningful but not blocking |
| 🟢 | P3 | 普通 | Normal queue |
| 🔵 | P4 | 低 | Useful improvement with little urgency |
| 🟣 | P5 | 有空再做 | Someday or exploratory work |
| ⚪ | P6 | 暂停 | Parked, deferred, or intentionally inactive; may be added after P0-P5 |

Treat the color as a label, not a claim about task status.

## Status scale

Use a separate status marker:

- ⚪ `待开始`
- 🟠 `进行中`
- 🟣 `等待/阻塞`
- 🟢 `已完成`
- ⚫ `已取消`

Update the compact label when the user says `开始`, `阻塞`, `完成`, `取消`, or an equivalent phrase.

## Projects, files, and subtasks

When ranking multiple items, preserve their hierarchy and output a compact table with `对象`, `优先级`, `状态`, and `下一步`. Sort siblings by priority from P0 to P6; do not reorder a parent beneath its children. Rename only the Codex tasks whose IDs are known and whose priority the user selected.

The Codex project/folder header is not a task title. Do not rename a filesystem folder or claim to style the project header. Apply the visible marker to task and child-task rows.

Only create or update a project tracking file when the user explicitly asks to save or persist the labels. Use `.codex/task-priorities.md` unless the project already has a task-tracking convention. Touch no unrelated files.

## Interaction rules

- Infer priority only when the user clearly states urgency; otherwise ask.
- Allow `跳过` and continue without a label.
- Do not interrupt a trivial greeting or a purely conversational message.
- Do not block emergency remediation merely to collect a label; infer P0, state the inference, and proceed.
- Keep the prompt and confirmation in the user's language.
