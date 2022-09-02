---
layout: page
title: Výzvy a zápasy
order: 3
---

{% assign challenges = site.challenges | reverse %}
{% if challenges[0].match %}
Poslední změna {{ challenges[0].match.date | date: "%e.%-m.%Y" }}.
{% else %}
Poslední změna {{ challenges[0].date | date: "%e.%-m.%Y" }}.
{% endif %}

| Číslo | Vyzyvatel | Vyzvaný | Datum výzvy | Výsledek | Vítěz | Detaily zápasu |
| ----- | --------- | ------- | ----------- | -------- | ----- | -------------- |
{% for challenge in challenges %}| U{{ challenge.id | split: "U" | last | plus: 0 }} | {{ challenge.challenger }} | {{ challenge.challengee }} | {{ challenge.date | date: "%Y-%m-%d" }} | {% if challenge.match %}{{ challenge.match.challenger_score }}:{{ challenge.match.challengee_score }} | {% if challenge.match.challenger_score > challenge.match.challengee_score %}{{ challenge.challenger }}{% else %}{{ challenge.challengee }}{% endif %} | [otevřít]({{challenge.url}}){% else %}- | - | - {% endif %}|
{% endfor %}
