---
layout: page
title: blog
permalink: /blog/
---

Here are all of the blog posts I've written. Not all dates are reflective of when the material itself was composed. All thoughts my own. There is not intended to be any thematic coherence or material consistency between posts. 

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>