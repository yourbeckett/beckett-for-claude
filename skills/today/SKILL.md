---
name: today
description: "See your day in beckett: today's events, what's due, and what changed recently."
---

# Today

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Read today's events with `beckett_event_read`, from midnight today to midnight tomorrow in the user's time zone.
- Read open tasks due today or overdue with `beckett_task_read`, with `due_before` set to the end of today.
- Read recent changes with `beckett_get_activity`.
- Summarize in a few short lines, most time-sensitive first, and point out what needs attention rather than listing everything.
