# Beckett

Beckett keeps your notes, people, tasks, calendars, habits, projects, recipes, meal plans, grocery lists, books, movies, shows, and saved links in one place that you and Claude both work in. Anything Claude adds shows up in the Beckett app on iPhone, web, and Mac, and anything you change there is available to Claude.

This plugin connects Claude to your Beckett account and adds a skill that teaches Claude which Beckett tool to use and when to check or save memory.

## Requirements

A Beckett account with an active subscription or free trial. Sign up at [yourbeckett.com](https://yourbeckett.com).

## Set it up

1. Add the Beckett plugin from the Claude directory.
2. On the plugin's **Connectors** tab, connect Beckett and sign in with your Beckett account.
3. On the Beckett consent screen, choose a memory mode and approve the connection:
   - **Manual**: Claude uses Beckett memory only when you ask.
   - **Automatic context**: Claude checks Beckett before each substantive request and saves notes only when you ask.
   - **Automatic memory**: Claude checks Beckett before each substantive request and saves durable facts you state automatically.

To change the memory mode, disconnect Beckett in Claude's connector settings and connect again. To stop sharing, disconnect Beckett there.

## Use it

Ask Claude in plain language. For example:

- "Add oat milk and eggs to my grocery list."
- "What do I have on my calendar Thursday?"
- "Put Dune on my reading list."
- "Plan dinners for next week from my saved recipes."
- "Remember that my sister's birthday is March 4."

Deleting takes two steps. Claude first prepares the deletion of one exact record, then deletes it with a short-lived confirmation.

## Data

The plugin itself stores nothing and runs no code on your computer. It points Claude at Beckett's server, `https://api.yourbeckett.com/mcp`, which you authorize with OAuth.

When Claude calls a Beckett tool, it sends that request's details to Beckett, such as a note to save or a search query. Beckett returns the matching data from your account. Beckett doesn't receive your full Claude conversation. What Beckett stores and how long it keeps it is covered in the [Beckett privacy policy](https://yourbeckett.com/privacy).

## Support

Visit [yourbeckett.com/support](https://yourbeckett.com/support). Terms of service: [yourbeckett.com/terms](https://yourbeckett.com/terms).
