---
layout: page
title: Výzvy a zápasy
order: 3
---

Poslední změna 31.3.2022.

{% assign challenges = site.challenges | reverse %}
| Číslo | Vyzyvatel | Vyzvaný | Datum výzvy | Výsledek | Vítěz | Detaily zápasu |
| ----- | --------- | ------- | ----------- | -------- | ----- | -------------- |
{% for challenge in challenges %}| U{{ challenge.id | split: "U" | last | plus: 0 }} | {{ challenge.challenger }} | {{ challenge.challengee }} | {{ challenge.date | date: "%Y-%m-%d" }} | {% if challenge.match %}{{ challenge.match.challenger_score }}:{{ challenge.match.challengee_score }} | {% if challenge.match.challenger_score > challenge.match.challengee_score %}{{ challenge.challenger }}{% else %}{{ challenge.challengee }}{% endif %} | [otevřít]({{challenge.url}}){% else %}- | - | - {% endif %}|
{% endfor %}
