---
layout: post
title: "Y Combinator Startup School Notes"
date: 2019-11-01 23:59:59 -0000
categories: incubators
author: "Sagun Garg"
tags: ycombinator notes startups 
---


## MVP Basics for a StartUp

[SeriesMVP: Episode 1](https://www.youtube.com/watch?v=1hHMwLxN6EM)

**QUESTIONS ?**

- Are you solving for a Problem of a User ?
- Are you your own User? 
- Is your MVP Embarrassing enough (optimise for speed) Does some value stick with a user ?
- Are you optimising for a Niche early on non-scalable with your MVP?
- Are you solving Non-scaling but manually ?

**DON’T**

- Don’t build product before defining the problem of a user 
- Don’t build for a mysterious set of users
- Don’t iterate problem and market(fall in love with problem statement on the solution) but iterate only on the solution
- Don’t build heavy MVP (keep it lean landing page + spreadsheet)
- Don’t solve for everyone 

[SERIESMVP: Episode2](https://www.youtube.com/watch?v=UiB0GFOuWwM)

1. Iterations of MVP: Be prepared to throw away your solutions during iterations. Hold the problem and market hard and close to your chest, be very flexible with the solution

2. Stages of Iteration
 - 1st MVP: Use Problem Statement(Solve for a User) + Gut feel Solution(Don’t Listen Users for Solution)
 - 2nd MVP: Problem Statement +. Market (Hold on to This) + Solution (Listen to Early users Feedback)
 - 3rd MVP: MVSP Vs MVLP: Minimum Viable (Shitty vs Lovable) Product

3. Product + Early Users for an established industry is a better way to lead the MVP without caring much for business model (because it is an established industry hence optimise for growth. Business model is much easier to discover. But if it is a new playbook then market sizing, goto market and business model need to be emphasised before the product early on)

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}