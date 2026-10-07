---
description: Show which hook categories are gaining or losing momentum on Hookest
argument-hint: "[30d|90d|180d] [category]"
---

Show the user which topic categories are gaining or losing momentum in the
Hookest library.

Arguments: $ARGUMENTS

1. Call `list_filters` to get valid category slugs.
2. Call `discover_trends`. Use the window from the arguments if given
   (`30d`, `90d` or `180d`, default `90d`). If a category is named, map it to
   the closest slug from `list_filters`.
3. Show a short table: category, direction (gaining or losing), and the
   change against the library baseline. Sort by the biggest movers.
4. For the top 2 gaining categories, call `find_hooks` with that category,
   `sort: trending`, `limit: 3`, and list the examples with their links.

Hookest measures category momentum, not hook patterns. If the user asks about
patterns, say that this data does not exist.
