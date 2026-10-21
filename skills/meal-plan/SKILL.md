---
name: meal-plan
description: "Plan meals for the week in beckett and add the ingredients from saved recipes to the grocery list."
---

# Meal plan

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Start from saved recipes: search them with `beckett_recipe_read`, and use what's saved, such as prep and cook times, tags, and loved recipes, to fit the week the user describes. Fill any gaps with meal ideas.
- Create the plan with `beckett_meal_plan_write` and `create`, one entry per date and meal: a `recipe_ref` for a saved recipe, or a `name` for anything else.
- Add what's needed to the active grocery list with `beckett_grocery_list_write`: `add_recipe_items` for saved recipes and `add_items` for the rest. Add to the existing active list even when it already has items; if several are active, use the first one listed. Use `build_grocery_list` on the plan only when no list is active.
- Confirm the plan by day in a few short lines.
