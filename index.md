---
layout: default
---

<div class="home">

  Welcome to this collection of bits and pieces by some (not so
  random) Passau Graduate Students. They are technically built from a
  github-repository using Jekyll. And they are philosophically founded
  as
  a <a href="https://communitywiki.org/wiki/DoOcracy">do-ocracy</a>:
  if you think something should be on these pages, put it here. If you
  see something that could be improved, do it. (Don't be afraid to
  break anything -- everything's version-controlled.)

  The content comes in roughly two flavors. On the one hand, there are
  (very) rough notes on scientific topics (think: "What is ...?", see
  "Posts" below). On the other hand, there's general information that
  we refer to (and are asked for) regularly (think: "How to ...?", see
  "Pages" below).

  For more details, see the
  <a href="_pages/brown-bag-orga">organizational page</a> of the seminar or a get a first
  impression of the latest topics in the following list or [here](./_pages/brown-bag-orga).

<h2 class="page-heading">Last Three Sessions</h2>

<ul class="post-list">
    {% for post in site.posts offset:0 limit:3 %}
      <li>
        <h3>
          <span class="post-meta">{{
    post.date | date: "%-d %b %Y" }}</span> <a class="post-link" href="{{ post.url | prepend:
    site.baseurl }}">{{ post.title }}</a>
        </h3>
      </li>
    {% endfor %}
  </ul>

<h2 class="page-heading">Pages</h2>

  <ul class="pages-list">
    {% for page in site.pages %}
    <li>
        <h2>
          <a class="pages-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a>
        </h2>
    </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>
