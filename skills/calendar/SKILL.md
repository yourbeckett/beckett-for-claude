---
name: calendar
description: "Add appointments and events to the beckett calendar, including ones the user mentions in passing, like a school play on Friday at 6. Also move events and show the schedule for a day or week."
---

# Calendar

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- When the user shares an upcoming appointment or event with a day or time, such as "Henry's school play is Friday at 6," add it to the calendar and confirm in one line. Ask only when the day or time is unclear.
- Appointments, meetings, and other scheduled occurrences are events in `beckett_event_write`. Set the start and end times or `all_day`, `recurrence` for repeats, the location, the people involved in `person_refs`, and `reminder_minutes_before` when they want an alert.
- To see a day or week, use `beckett_event_read` with `action: list` and `from_at` and `to_at` for that range.
- To-dos with a due date are tasks, not events; see the reminders skill. Calendars themselves are containers in `beckett_calendar_write`.
- Times use the account's time zone in beckett. Don't ask for a time zone; write times without a UTC offset unless the user names a zone.
