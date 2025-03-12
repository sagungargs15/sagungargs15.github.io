---
layout: default
---

## Sagun's Speaker: Panels, KeyNotes, Ideas and Notes

<ul>
  {% for talk in site.talks %}
    <li>
      <a href="{{ talk.url }}">{{ talk.title }}</a>
    </li>
  {% endfor %}
</ul>
