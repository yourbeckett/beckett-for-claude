---
name: grocery-list
description: "Add items to the beckett grocery list, check them off, or read the list back."
---

# Grocery list

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Find the active list with `beckett_grocery_list_read` and status `active`. Add to it even when it already has items. If several lists are active, use the first one listed, which is the most recently updated. Create a list only when the user asks for a new one or none is active.
- Add items with `beckett_grocery_list_write` and `add_items`. For a saved recipe, use `add_recipe_items` with the recipe's ref so its ingredients come in with quantities.
- For a meal that isn't saved as a recipe, work out the ingredients it needs, then add them with `add_items`.
- Check items off with `set_checked`, and read the list back with `beckett_grocery_list_read`.
