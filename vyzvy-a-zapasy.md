---
layout: page
title: Výzvy a zápasy
order: 3
---

Aktuální k 22.11.2021.

## Proběhlé zápasy

{% assign matches = site.data.matches | sort: "date" %}
{% for match in matches %}
#### {{ site.data.challenges[match.challenge].challenger }} vs {{ site.data.challenges[match.challenge].challengee }} - {{ match.date }}
**Datum výzvy**: {{ site.data.challenges[match.challenge].date }}  
**Vyzyvatel**: {{ site.data.challenges[match.challenge].challenger }} - 
{{ match.challenger_lineup[0] }},
{{ match.challenger_lineup[1] }},
{{ match.challenger_lineup[2] }}{% if match.challenger_lineup.size == 4 %},
({{ match.challenger_lineup[3] }}){% endif %}  
**Vyzvaný**: {{ site.data.challenges[match.challenge].challengee }} - 
{{ match.challengee_lineup[0] }},
{{ match.challengee_lineup[1] }},
{{ match.challengee_lineup[2] }}{% if match.challengee_lineup.size == 4 %},
({{ match.challengee_lineup[3] }}){% endif %}  
**Výsledek**: {{ match.challenger_score }}:{{ match.challengee_score}}
{% endfor %}

## Podané výzvy
{% assign challenges = site.data.challenges | sort: "date" %}

| Vyzyvatel | Vyzvaný | Datum výzvy | Proběhl zápas |
| --------- | ------- | ----------- | ------------- |
{% for challenge in challenges %}| {{ challenge.challenger }} | {{ challenge.challengee }} | {{ challenge.date }} | {% if challenge.finished %}Ano{% else %}Ne{% endif %}
{% endfor %}