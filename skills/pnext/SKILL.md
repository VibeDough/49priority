---
name: pnext
description: Find and open the highest-priority visible Codex task by its colored title dot. Use when the user invokes $pnext or asks to jump to the next prioritized Codex task.
---

# Next Priority

Use the Codex task/thread listing tool to read recent visible tasks. Consider titles beginning with `🔴`, `🟠`, `🟡`, `🟢`, `🔵`, or `🟣` and rank them in that order. Exclude any task whose leading marker sequence contains `⚪`, because it is paused even when it also has a priority marker.

Exclude the calling task when another marked task is available. Prefer tasks from the current project when project or workspace metadata is available. Within the same priority, choose the most recently active task.

Use the Codex navigation tool to open the selected task because invoking `$pnext` is explicit permission to navigate. Confirm the selected title briefly. If no marked task exists, say so without opening an unmarked task. If listing or navigation tools are unavailable, state that this Codex surface cannot jump between tasks.
