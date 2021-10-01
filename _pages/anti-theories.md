---
layout: pages
---

## Anti-theories

### Anti-Distribution Theory 
> "The product is so good it sells itself"

### Anti-Thesis Investments by VC

> "Use of an antithesis makes the audience better understand the point the speaker is trying to make". Antithesis can be defined as "a figure of speech involving a seeming contradiction of ideas, words, clauses, or sentences within a balanced grammatical structure - Aristotle

### Anti-Portfolio (Missed Startups by VCs)

> "An investor’s anti-portfolio are the deals which they pursed but did not invest, either on their own volition or because they were shut out by other investors"


{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}