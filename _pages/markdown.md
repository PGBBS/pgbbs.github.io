---
title: "How to Markdown"
layout: page
---

We use Markdown as markup-language (with file-extension .md). Here's a
[cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
More specifically, we use markdown's
[kramdown](http://kramdown.gettalong.org/syntax.html)-flavor. Sometimes,
the Liquid processing might interpret some markdown incorrectly (e.g.
the links to posts in the code block above). Then you have to enclose
them with "raw"-tags (see the source if this file).

You can also use emojis -- at least the ones supported by Github's
Jekyll-plugin. Here's a [list](http://www.webpagefx.com/tools/emoji-cheat-sheet/).

Kramdown offers a
[table of contents](http://kramdown.gettalong.org/converter/html.html#toc)
derived from the headlines. Just decorate an (unordered) list with the
Inline Attribute List (IAL) `{:toc}` (see source code of this
file). Jekyll will then replace it with a Table of Contents based on
the headings of the file; you can exclude headings by attaching the
IAL `{:.no_toc}`.

## Code Snippets with Markdown

You can have a basic code block as an (4-space) indented text
surrounded by blank lines, where the preceding paragraph ends with a
colon :

    like this
	and that

More specifically, you can specify the language for proper
highlighting as you can see in the source of this example (taken from
the default installation's `welcome-to-jekyll`)

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}


## Software: Editor for Markdown

- Windows: [MarkdownPad](http://markdownpad.com/) has a free and paid version
- and then, of course, the usual suspects: Vim, Emacs, Atom
