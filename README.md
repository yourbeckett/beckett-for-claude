# beckett

[beckett](https://www.yourbeckett.com/) is one place for everything you're keeping track of: notes, tasks and reminders, calendars, projects, habits and goals, recipes and meal plans, lists, and the people who matter to you. This plugin connects Claude to your beckett account, so you can ask about any of it or make changes in plain language.

Ask about your week, a project, or a person, and Claude answers from what you've saved. New tasks, notes, and plans land in the right place in beckett, ready for you to open, change, or delete. The same beckett works on iPhone, iPad, Mac, and the web, and with ChatGPT and the other agents you connect.

The plugin also adds skills for everyday jobs, which you can pick from the `/` menu: `beckett:start`, `beckett:today`, `beckett:notes`, `beckett:people`, `beckett:birthdays`, `beckett:reminders`, `beckett:calendar`, `beckett:projects`, `beckett:check-ins`, `beckett:habits`, `beckett:recipes`, `beckett:meal-plan`, `beckett:grocery-list`, `beckett:watchlist`, and `beckett:bookmarks`. Another skill helps Claude choose the right beckett tool for each request.

## Try asking

- Set up a project for two weeks in Portugal in May: a day-by-day itinerary, a packing checklist, and what to book first.
- Get me ready for tomorrow's meetings: what I've saved about each person and anything I still owe them.
- Plan next week's dinners, using my saved recipes where you can, and add everything I need to my grocery list.
- I'm making salmon bowls Tuesday and lemon chicken orzo Thursday. Put them on my meal plan and what I need on my grocery list.
- Look at the books I've loved and suggest three I'd probably like next, then add them to my reading list.

## Set it up

1. Add the beckett plugin from the Claude directory.
2. On the plugin's **Connectors** tab, connect beckett. In Claude Code, run `/mcp` and choose beckett.
3. Sign in to beckett, or create an account. A new account starts with a free week, no card needed.
4. Approve the connection on the beckett consent screen.

To stop sharing, disconnect beckett in Claude's connector settings.

## Use it

From a conversation with Claude, you can:

- Keep track of people: who someone is, how you know them, and what you've noted about them
- Plan your days with reminders, calendar events, and a focus list for today
- Run projects with checklists, notes, and linked tasks
- Track habits and goals, and look back at how things are going
- Plan meals from your saved recipes and build the grocery list
- Save links, books, movies, and shows for later

Deleting takes two steps. Claude first prepares the deletion of one exact record, then deletes it with a short-lived confirmation.

## Data

The plugin itself stores nothing and runs no code on your computer. It points Claude at beckett's server, `https://api.yourbeckett.com/mcp`, which you authorize with OAuth.

When Claude calls a beckett tool, it sends that request's details to beckett, such as a note to save or a search query. beckett returns the matching data from your account. beckett doesn't receive your full Claude conversation. What beckett stores, and for how long, is covered in the [beckett privacy policy](https://yourbeckett.com/privacy).

## Support

Visit [yourbeckett.com/support](https://yourbeckett.com/support). Terms of service: [yourbeckett.com/terms](https://yourbeckett.com/terms).
