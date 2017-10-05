---
layout: page
title: Blog
---

<div class="posts">
  {% for post in site.posts %}
  <div class="post">
    <h2 class="post-title">
      <a href="{{ site.baseurl }}/{{ post.url | remove_first: '/'}}">
        {{ post.title }}
      </a>
    </h2>

    <span class="post-date">{{ post.date | date_to_string }} by <a href="{{ site.baseurl }}/people/{{ post.author }}">{{ post.author }}</a></span>

    <!--{{ post.content }}-->
  </div>
  {% endfor %}
</div>

<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ site.baseurl }}/page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="{{ site.baseurl }}/">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="{{ site.baseurl }}/page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div>
