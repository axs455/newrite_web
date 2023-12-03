---
layout: page
title: News
list_title: List
paginate: true
entries_layout: grid
aside:
  toc: true
permalink: /news/
---

### News
{% for post in site.posts %}
* [{{ post.title }}]({{ post.url}})
<p>(Posted: {{ post.date | date: "%B %d, %Y" }})</p>
{% endfor %}

---
