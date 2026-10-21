---
name: projects
description: "Set up and run projects in beckett, such as a trip or a renovation, with checklists, an itinerary or budget, tasks, and linked notes."
---

# Projects

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Create the project with `beckett_project_write`: its name and details, plus the saved people and notes that belong to it.
- Build it out with `beckett_project_content_write`, using text, checklist, table, tasks, and calendar blocks. Shape it to the job, such as a day-by-day itinerary, a packing checklist, and tasks for what to book on a trip, or a budget table and a contractor checklist for a renovation.
- To change an existing project, find it with `beckett_project_read`, list its blocks with `beckett_project_content_read`, then update the block you need.
- Confirm what you set up in a few short lines.
