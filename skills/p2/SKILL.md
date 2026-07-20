---
name: p2
description: Mark the current or explicitly referenced Codex task P2 medium priority with a yellow dot in its sidebar title. Use when the user invokes $p2.
---

# P2 Yellow

Use explicitly referenced Codex tasks as targets when the user includes task/thread references; otherwise target the current task. Support multiple explicit references. Resolve each existing title, replace any leading P0-P5 circle with `🟡`, and preserve a following `⚪` pause marker when present. Produce `🟡 ⚪ <title>` for a paused task and `🟡 <title>` otherwise. Never duplicate either marker. Use the Codex task-title/thread-title tool, confirm briefly, and continue the user's task. If the tool is unavailable, state that the sidebar was not changed.
