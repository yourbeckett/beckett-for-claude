---
name: recipes
description: "Save a recipe to beckett from a link, a photo, or an idea, ready to add to the grocery list."
---

# Recipes

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Save recipes with `beckett_recipe_write` and `create`. For a link, pass it as `source_url`. For a photo or an idea, write out the name, ingredients, and steps, plus prep and cook minutes when you know them.
- Find saved recipes with `beckett_recipe_read` and `search`, by name, ingredient, cuisine, tag, or `loved`.
- After saving, offer to add the ingredients to the grocery list, as the grocery-list skill describes.
