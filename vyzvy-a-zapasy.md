---
layout: page
title: Výzvy a zápasy
order: 3
---

Poslední aktualizace 22.11.2021.

{% assign challenges = site.challenges | reverse %}
| Vyzyvatel | Vyzvaný | Datum výzvy | Výsledek | Vítěz | Detaily zápasu |
| --------- | ------- | ----------- | -------- | ----- | -------------- |
{% for challenge in challenges %}| {{ challenge.challenger }} | {{ challenge.challengee }} | {{ challenge.date | date: "%Y-%m-%d" }} | {% if challenge.match %}{{ challenge.match.challenger_score }}:{{ challenge.match.challengee_score }} | {% if challenge.match.challenger_score > challenge.match.challengee_score %}{{ challenge.challenger }}{% else %}{{ challenge.challengee }}{% endif %} | [otevřít]({{challenge.url}}){% else %}- | - | - {% endif %}|
{% endfor %}
