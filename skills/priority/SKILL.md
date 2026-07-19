---
name: priority
description: Show the Codex task priority picker and add the selected colored dot to the current task title. Use when the user invokes $priority or asks to choose a task priority.
---

# Priority Picker

Ask once: `选择优先级：$p0 🔴 / $p1 🟠 / $p2 🟡 / $p3 🟢 / $p4 🔵 / $p5 🟣 / $p6 ⚪`.

Accept a code, color, or Chinese priority name. Then use the Codex task-title/thread-title tool to prefix the current title with the matching circle. Replace any existing leading priority circle instead of stacking markers. Preserve the rest of the title and continue the user's task.

Map P0-P6 to: 🔴 紧急, 🟠 高, 🟡 中, 🟢 普通, 🔵 低, 🟣 有空再做, ⚪ 暂停.

If the title tool is unavailable, state that the sidebar was not changed.
