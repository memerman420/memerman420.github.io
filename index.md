--- 
layout: default
title: Home
---

<div class="posts">{% for post in paginator.posts %}

<div class="post">

# [{{ post.title }}]({{ post.url }})

<span class="post-date">{{ post.date | date_to_string }}</span> {{ post.content }}</div>

{% endfor %}</div>

<div class="pagination">{% if paginator.next_page %} [Older]({{ site.baseurl }}page{{paginator.next_page}}) {% else %} <span class="pagination-item older">Older</span> {% endif %} {% if paginator.previous_page %} {% if paginator.page == 2 %} [Newer]({{ site.baseurl }}) {% else %} [Newer]({{ site.baseurl }}page{{paginator.previous_page}}) {% endif %} {% else %} <span class="pagination-item newer">Newer</span> {% endif %}</div>
