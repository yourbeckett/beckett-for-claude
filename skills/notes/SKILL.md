---
name: notes
description: "Save a note to beckett, filed by topic and linked to the people and places it mentions, or find a note you saved."
---

# Notes

- If no beckett tools are available, beckett isn't connected yet. Tell the user once, and if you can suggest connectors, suggest beckett so they get a Connect button. Give the steps, keep what they asked for, and offer to finish it once beckett is connected. Don't say anything was saved to or found in beckett.
  - In Claude chat or Cowork: open **Customize > Plugins**, choose **beckett**, and select **Connect** on the **Connectors** tab.
  - In Claude Code: run `/mcp`, choose **beckett**, and sign in.
  - Signing in creates a beckett account for anyone who doesn't have one, with a free week and no card.
- When beckett is connected, follow the shared rules in the use-beckett skill.
- To save something the user wants kept, use `beckett_store_notes`. beckett files the note by topic and links the people and places it mentions.
- To find notes, search with `beckett_note_read`. For notes about a person, look them up with `beckett_entity_read` first, then read the notes linked to them.
