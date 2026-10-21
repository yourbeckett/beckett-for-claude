---
name: people
description: "Keep track of the people in your life in beckett, and pull together what you've saved about someone before you see them."
---

# People

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Look someone up with `beckett_entity_read`, which returns who they are, how they're connected, and the notes saved about them. Add someone new with `beckett_entity_write`, and record how people are connected with `beckett_relationship_write`.
- To get ready to see someone, gather their record and notes, open tasks that involve them with `beckett_task_read`, and upcoming events with them with `beckett_event_read`. For a day's meetings, list that day's events and do this for each person on them.
- Lead with what matters for the meeting: anything the user owes them or promised, then the details worth remembering.
