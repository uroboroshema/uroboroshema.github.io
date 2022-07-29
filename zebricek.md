---
layout: page
title: Žebříček
order: 2
---

{% assign challenges = site.challenges | reverse %}
{% if challenges[0].match %}
Poslední změna {{ challenges[0].match.date | date: "%d.%-m.%Y" }}.
{% else %}
Poslední změna {{ challenges[0].date | date: "%d.%-m.%Y" }}.
{% endif %}

| Pořadí | Klub              | Město     | Dostupný k výzvě | Vyzvaný týmem     | Vyzývá tým        |
| ------ | ----------------- | --------- | ---------------- | -------------     | ----------------- |
| 1.     | Krkavci           | Praha     | Ne               | PSA               |                   |
| 2.     | PSA               | Pardubice | Ne               |                   | Krkavci           |
| 3.     | Duelanti          | Praha     | Ano              |                   |                   |
| 4.     | Digladior         | Praha     | Ano              |                   |                   |
| 5.     | Poslední Argument | Praha     | Ano              |                   |                   |
| 6.     | Helops            | Přepeře   | Ano              |                   |                   |
