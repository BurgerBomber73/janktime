---
title: Welcome to the Jank Time Blog
---

{% for post in site.posts limit:1 %}
  <article>
    <header>
      <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%B %d, %Y" }}
      </time>
    </header>
    <div class="post-excerpt">
      {{ post.excerpt }}
    </div>
  </article>
{% endfor %}

