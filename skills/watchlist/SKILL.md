---
name: watchlist
description: "Add movies and shows to the beckett watchlist and books to the reading list, or log one you finished with a rating."
---

# Watchlist and reading list

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Add a clear title with `beckett_add_media`. Map "watchlist" to `want_to_watch` and "reading list" to `want_to_read`. Something they just finished is `watched` or `read`, with their rating if they gave one.
- For an ambiguous title, search `beckett_search_media_catalog` first. For titles they've already saved, use `beckett_search_media_library`.
- For suggestions, read what they've loved or rated highest with `beckett_search_media_library` sorted by rating, find candidates with `beckett_search_media_catalog`, and add the ones they ask for.
