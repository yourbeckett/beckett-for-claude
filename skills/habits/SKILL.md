---
name: habits
description: "Log runs, sleep, mood, or any habit in beckett by saying what you did, then ask how the week went."
---

# Habits and trackers

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Log something the user did or measured, such as "I ran 3 miles" or "slept badly," as an entry on the matching habit or tracker with `beckett_tracker_write`. If none matches, offer to create one, such as a goal of three runs a week.
- For questions like "how has my sleep been?", read that tracker's entries with `beckett_tracker_read` and `action: history`, then summarize what the entries show, without medical advice.
