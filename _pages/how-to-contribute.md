---
title:  "How to contribute"
layout: page
---

Great! You're most welcome to contribute. Don't be shy, anything that
you consider even remotely relevant already has 1 (potential) reader.
:smile: Just get a quick 'n' dirty draft out quickly. Or edit somebody else's
quick 'n' dirty draft. And along the way, you can learn some awesome
stuff about Git and Jekyll. These pages are built from a Git-repository,
living at

[https://github.com/PGBBS/pgbbs.github.io](https://github.com/PGBBS/pgbbs.github.io).

# Posts vs. Pages

Posts and pages live as mardown-files (.md) in the directories `_posts` and
`_pages` (surprise). They need a header, where the minimal example (of
this very page) is:

    ---
    title: "How to contribute"
    layout: page
    ---

Alternatively, `post` instead of `page` (duh!). There's also one other
point, where posts and pages differ: the filename. For posts it is
always in the format: `_posts/YYYY-MM-DD-<title>.md` (where title may differ
from the title in the frontmatter). For pages it is either
`_pages/<title>.md` or `_pages/<title-as-directory>/index.md`.

Optional header information: `category`.

Expert note: Further possible information for the header is `date` and
`permalink`. We don't use any of these (at least not as defaults),
because the date (for posts) is derived from the filename and the
permalink as well (as set in `_config.yml`). If you ever want to set a
permalink, remember forward-slashes on both ends, like `permalink:
"/about/"`.

## Background: Difference between Posts and Pages

Jekyll differentiates between *posts* and *pages*. While the former
serve the role of blog posts (usually with timestamps), the latter can
be thought of as static (for example the "About"-page).

# Markup: Markdown

We use Markdown as markup-language (with file-extension .md). Here's a
[cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
More specifically, we use markdown's
[kramdown](http://kramdown.gettalong.org/syntax.html)-flavor.

You can also use emojis -- at least the ones supported by Github's
Jekyll-plugin. Here's a list [TODO].

## Software: Editor for Markdown

- Windows: [MarkdownPad](http://markdownpad.com/) has a free and paid version
- and then, of course, the usual suspects: Vim, Emacs, Atom

