---
name: px
description: Remove a colored priority dot from the current or explicitly referenced Codex task sidebar title. Use when the user invokes $px.
---

# PX Clear Priority

Use explicitly referenced Codex tasks as targets when the user includes task/thread references; otherwise target the current task. Support multiple explicit references. Resolve each title, then use the Codex task-title/thread-title tool to remove exactly one leading priority marker. Recognize `🔴`, `🟠`, `🟡`, `🟢`, `🔵`, `🟣`, and `⚪`, plus the single space immediately following the marker. Preserve every other character in the title.

If no leading marker exists, leave the title unchanged and confirm briefly. If the title tool is unavailable, state that the sidebar was not changed. Continue any task included in the user's request.
