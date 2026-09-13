# Halide

A dark, quiet [Masthead](https://github.com/JoeriDijkstra/masthead) theme for
photographers. Named after the silver halide crystals that make film work.

The point of the theme is the **Gallery** page: a photography category you fill
in from the page editor — a kicker, an intro, and a repeatable list of photos.
It renders as a masonry grid with a click-to-enlarge lightbox that is pure CSS
(`:target`), so there is no JavaScript in the theme at all.

## Adding a gallery

In the admin: **New page → Theme page → Gallery**. Then fill in:

| Field | What it does |
|---|---|
| Kicker | Small label above the title — `Portraits`, `Iceland, 2024` |
| Intro | A short paragraph under the title. Empty = skipped |
| Columns | Columns on desktop. Drops to 2 on tablet, 1 on phone |
| Show photo count | The `6 PHOTOGRAPHS` line |
| Image corners | Rounding for every photo on the page: off / small / medium / large |
| Photos | Add / remove / drag-reorder rows: image, caption, alt text |

Each photo row takes an uploaded image, an optional caption (shown under the
thumbnail and in the enlarged view), and alt text (falls back to the caption).
Rows with no image are skipped, so a half-filled row won't break the grid.

Make one page per category — `Portraits`, `Landscapes`, `Weddings` — and they
show up in the site nav automatically.

## The home page

**New page → Theme page → Home**, then set it as the site homepage. Four
sections, each with its own on/off switch, so you can run the whole thing or
just a hero:

| Section | Contains |
|---|---|
| Hero | Wide image, title, tagline, and an optional button |
| Featured galleries | A repeatable list of cover image + title + kicker + link |
| Statement | A short about paragraph with an optional portrait beside it |
| Journal | The latest N posts, with N up to you |

Sections you switch off render nothing at all — no empty headings, no gaps. The
same **Image corners** dropdown applies here.

## Posts

Every post gets two options in the post editor:

| Field | What it does |
|---|---|
| Cover photo | A wide image above the post, and the thumbnail beside it in every post list |
| Cover alt text | Describes the cover for screen readers |

Leave the cover empty and the post renders as plain text — the list row falls
back to its old full-width layout, so a mixed list is fine.

## Tokens

`bg`, `fg`, `accent` and `max` (content width) drive the whole palette; the
muted, rule and sunken tones are derived from them with `color-mix`, so
changing the background keeps the theme coherent. `favicon` and the two post
toggles (`show_search`, `show_tags`) work as in any Masthead theme.

## Render version

The theme pins `"render_version": "v1"`, so page settings reach templates as
`page.page_options.<key>` and post settings as `post.post_options.<key>`.
