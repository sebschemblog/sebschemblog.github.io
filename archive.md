---
layout: page
title: Blog Archive
---
## Labs
{% for post in site.categories.Labs %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%b %Y" }})
{% endfor %}

## Lectures
{% for post in site.categories.Lectures %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%b %Y" }})
{% endfor %}

## Travel
{% for post in site.categories.Travel %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%b %Y" }})
{% endfor %}

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
