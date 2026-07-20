---
name: plist
description: List visible Codex tasks that have colored priority dots and sort them from P0 to P6. Use when the user invokes $plist or asks to see marked or prioritized Codex tasks.
---

# Priority List

Use the Codex task/thread listing tool to read recent visible tasks. Select titles whose leading marker sequence contains `🔴`, `🟠`, `🟡`, `🟢`, `🔵`, `🟣`, or `⚪`. Recognize both standalone pause titles such as `⚪ Task` and additive pause titles such as `🔴 ⚪ Task`.

Sort by P0-P5 marker while preserving recency within the same priority. Place standalone `⚪` tasks after P5. Prefer tasks from the current project when project or workspace metadata is available; otherwise clearly label the result as recent visible Codex tasks.

Return a compact table with `优先级`, `任务`, and `状态`. Report `暂停` whenever the leading marker sequence contains `⚪`, including when it is combined with P0-P5. Do not rename, open, archive, or otherwise modify tasks. If listing tools are unavailable, state that this Codex surface cannot read the task list.
