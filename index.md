---
layout: default
title: Home
---

# Chinese Stories

Add a new file in `_stories/` and it will appear here automatically.

<ul class="story-list">
  {% assign sorted = site.stories | sort: "date" | reverse %}
  {% for story in sorted %}
    <li class="story-list-item">
      <a href="{{ story.url | relative_url }}">{{ story.title }}</a>
      <div class="meta">
        {{ story.date | date: "%Y-%m-%d" }}
        {% if story.level %} · {{ story.level }}{% endif %}
        {% if story.tags %} · {{ story.tags | join: ", " }}{% endif %}
      </div>
    </li>
  {% endfor %}
</ul>
