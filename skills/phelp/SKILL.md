---
name: phelp
description: List every 49priority shortcut with its marker and purpose. Use when the user invokes $phelp or asks for all 49priority commands.
---

# Priority Help

Return this compact command list without renaming, opening, or otherwise modifying any task:

| Command | Meaning |
|---|---|
| `$p0` | 🔴 Urgent |
| `$p1` | 🟠 High |
| `$p2` | 🟡 Medium |
| `$p3` | 🟢 Normal |
| `$p4` | 🔵 Low |
| `$p5` | 🟣 Someday |
| `$p6` | ⚪ Pause; standalone or additive |
| `$px` / `$pclear` | Clear all leading priority and pause markers |
| `$priority` | Show the priority picker |
| `$plist` | List marked tasks in priority order |
| `$pnext` | Open the highest-priority non-paused task |
| `$phelp` | Show this command list |

Use the user's language for the meanings and one-line explanation. Mention that `$p6` can produce either `⚪ Task` or `🔴 ⚪ Task`, and that repeated markers are deduplicated.
