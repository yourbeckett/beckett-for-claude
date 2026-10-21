---
name: reminders
description: "Add a to-do or reminder to beckett with a due date and alert time, or see what's due."
---

# Reminders and to-dos

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Create to-dos and reminders with `beckett_task_write`. When the user says "remind me," set `due_at` and `reminder_minutes_before`: `[0]` to be reminded at that time, or the lead time they ask for. If they didn't say when, ask.
- Appointments and other scheduled occurrences are events in `beckett_event_write`, not tasks.
- To see what's due, read open tasks with `beckett_task_read`.
- Times use the account's time zone in beckett. Don't ask for a time zone; write times without a UTC offset unless the user names a zone.
