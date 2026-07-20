---
name: px
description: Remove a colored priority dot from the current or explicitly referenced Codex task sidebar title. Use when the user invokes $px.
---

# PX Clear Priority

Use explicitly referenced Codex tasks as targets when the user includes task/thread references; otherwise target the current task. Support multiple explicit references. Resolve each title, then use the Codex task-title/thread-title tool to remove the complete leading marker sequence. Recognize one P0-P5 marker, one optional `⚪` pause marker, and the spaces immediately following them. Preserve every other character in the title.

If no leading marker exists, leave the title unchanged and confirm briefly. If the title tool is unavailable, state that the sidebar was not changed. Continue any task included in the user's request.
