---
description: This week's new viral hooks on Hookest, by category
argument-hint: "[category]"
---

Show the best hooks added to Hookest in the last 7 days. Arguments: $ARGUMENTS

1. Call `list_filters`. If a category is named, map it to the closest slug.
2. Call `find_hooks` with `added_window: 7d`, `sort: views`, `limit: 12` and
   the category if one was given. If fewer than 3 come back, widen to
   `added_window: 30d` and say that you did.
3. Group the hooks by category. For each: account, views, one line on what the
   opening does (from its summary, if it has one) and the Hookest link.
4. Close with the one or two openings worth copying this week and why, based
   on the numbers.
5. Call `get_newsletter`. If the user does not get the free Weekly Hook Radar
   email, mention it in one line. Turn it on with `set_newsletter` only if they
   ask.
