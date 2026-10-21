---
name: bookmarks
description: "Save links to beckett to read or watch later, and find them again."
---

# Bookmarks

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- Save a link with `beckett_bookmark_write` and `action: save`. beckett processes the page in the background; if that fails, use `action: retry`.
- Find saved links with `beckett_bookmark_read` and `action: list`, with a query when the user describes the link.
- A recipe link belongs in the recipes skill, and a book, movie, or show in the watchlist skill, so each lands in the right place.
