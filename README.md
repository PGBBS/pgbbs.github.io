# PGBBS: Passau Grad Students Brown Bag Seminar

Manu & Konstantin decided to accompany our grad student seminar
with a blog. [This
repository](https://github.com/PGBBS/pgbbs.github.io) holds the posts
and pages, i.e. the content, of that blog. It is then built/generated with
Jekyll and dipslayed at [https://pgbbs.github.io/](https://pgbbs.github.io).

So, we have the following architecture:
- In the blog, we have posts ("What is ...") and pages ("How to ...").
  You can browse theme there and edit them here. (There's also some outliers like "about" and "brown-bag".)
- In this repository, we have "the dirty secrets" on how to
  maintain the tech (mainly GitHub Pages, Jekyll, and Markdown) behind
  this blog. The relevant files in `UPPERCASE.md`.
  - README.md :: this overview
  - ISSUES.md :: list of global TODOs (generally: put TODOs as close as
    possible to the point of action.)
  - HOW-TO-CONTRIBUTE.md :: how to write the proper mix of markdown and
    liquid-syntax for this blog
  - LICENSE.md :: ???TODO necessary???
- For programming advice, we frequently move to Jupyter-notebooks in a
  separate repository, since the blog's layout is hardly suitable for
  that. But, we still link from the relevent page, e.g. [How to
  python](https://pgbbs.github.io/_pages/python/)
  links to
  [python-tutorials](https://github.com/zieglerk/python-tutorials).

# Documentation

For reproducibility -- and in case we totally break the system --
let's document the technology and steps to get this site online

## Ruby

- Ruby :: programming language
- Gem and RubyGems :: a Ruby package and Ruby's package manager
- Gemfile :: specifies which packages (but not necessarily which
  version) a Ruby program requires/you want to use. Then install with
  :

      bundle install

- Gemfile.lock :: will be written with the exact package versions (for
  easier distribution/reproducibility). On the next `bundle install`
  these (stricter) requirements will be used (instead of Gemfile's)
- Jekyll :: a static site generator written in Ruby

## Jekyll

## Markdown

## ?Liquid-Syntax?

for everything that Markdown can't do, like toc and
:smile:

## Issues/TODOs

- Do we need a LICENSE file?
- Have 1 disclaimer (possibly as part of about) and link from this
  readme and the footer

# Terminology

For consistency, let's try
- PGBBS: Passau Grad Students Brown Bag Seminar (no dashes, no
  possessive suffix -'s)

# Disclaimer

This is a purely private endeavor and not an official
publication of our employer or the university. The views and advice
presented here are therefore completely nonbinding -- in any
direction. Use at your own risk. :-)
