---
name: check-ins
description: "Set up check-ins that beckett sends on a schedule, such as a weekday nudge to log a run or a Sunday prompt to plan the week, and change or pause them."
---

# Check-ins

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- A check-in is a recurring prompt beckett sends to ask the user for an update. Create one with `beckett_check_in_write`: its type (`recurring_check_in`, `habit_nudge`, `task_reminder`, or `event_reminder`), the time, a short label, the frequency (`daily`, `weekday`, `weekly`, `custom`, or `interval_days`), and the prompt to ask.
- To change a check-in, find it with `beckett_check_in_read`, then update its time, frequency, or prompt. To pause one, set `active` to false; to resume it, set `active` to true.
- A one-time reminder is a task, not a check-in; see the reminders skill.
