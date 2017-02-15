---
title: How to write your thesis (in LaTeX)
layout: page
---


Disclaimer: This is a purely private page of myself and not an official
publication of my employer. The views and advice presented here are
therefore completely nonbinding -- in any direction. Use at your own
risk. :-)

# Install LaTeX

You will need LaTeX-distribution and an editor.

## LaTeX-distributions

For the former, the most popular is

- [TeX Live](https://www.tug.org/texlive/) (Linux, Windows) by
  the TeX User Group
- [MacTeX](http://www.tug.org/mactex/) (Mac OS) by the TeX User Group
- MiKTeX (Windows only)

## LaTeX-editors

For the latter, any text editor will do, but you might also want some
IDE-functionality

- [TeXStudio](http://www.texstudio.org) (Linux, Mac OS X, Windows)
- [Texmaker](http://www.xm1math.net/texmaker/) (Linux, Mac OS X,
  Windows)
- [TeXPad](http://www.texpadapp.com) (Mac OS X)
- ... and of course: Emacs with AucTeX

# Write LaTeX

Armin Gerl has provided a template for the (German) master thesis
(based on the standard `report`-class):

- [pdf-preview][1]
- [directory as zip][2]

[1]:{{ site.url }}/docs/thesis-de-report/master-thesis-de.pdf
[2]:https://github.com/PGBBS/pgbbs.github.io/tree/master/docs/thesis-de-report

Alternatively, Florian Stegmaier built template (based on the
KomaScript `scrreprt`-class):

- [pdf-preview][3]
- [directory as zip][4]

[3]:{{ site.url }}/docs/thesis-de-scrreprt/rootFile.pdf
[4]:{{ site.repo }}/docs/thesis-de-scrreprt

## Maintain your bibliography with BibTeX

- [german introduction](http://www.juergenfenn.de/tex/dtk/bibonline.pdf)
- [english
  introduction](http://www.tug.org/pracjourn/2006-4/fenn/fenn.pdf)

A text editor is sufficient to maintain one's .bib-file, but if you
prefer some GUI (which might for example also link to the corresponding
pdf's), there's [JabRef](http://jabref.sourceforge.net/).

## Help

- [LaTeX
  Basics](https://www.youtube.com/playlist?list=PLuyjaM3Uz-oOS7zcMFaROwrg83KBR1Sui)
  (introduction videos, in German)
- [Begin LaTeX in minutes](https://github.com/VoLuong/Begin-Latex-in-minutes)
  (short introduction text, in English)
