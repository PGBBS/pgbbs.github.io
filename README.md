# PGBBS: Passau Graduate Student Brown Bag Seminar

Manu & Konstantin decided to accompany our graduate student seminar
with a blog at [https://pgbbs.github.io/](https://pgbbs.github.io). It
is built as github-page with Jekyll from the sources in
[this repository](https://github.com/PGBBS/pgbbs.github.io).

Disclaimer: This is a purely private endeavor and not an official
publication of our employer or the university. The views and advice
presented here are therefore completely nonbinding -- in any
direction. Use at your own risk. :-)

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
