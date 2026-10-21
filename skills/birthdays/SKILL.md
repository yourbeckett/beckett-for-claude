---
name: birthdays
description: "Save birthdays in beckett as yearly events linked to the person, with a reminder before each one."
---

# Birthdays

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Find the person with `beckett_entity_read`. If they aren't saved yet, add them with `beckett_entity_write`.
- Create an all-day event with `beckett_event_write`: `all_day` true, `recurrence` `yearly`, and the person in `person_refs`. Set `reminder_minutes_before` to the lead time they want, such as a week before.
- If they ask to keep other details about the person, such as gift ideas, save them with `beckett_store_notes`.
