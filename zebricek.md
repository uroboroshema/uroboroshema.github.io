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
| ------ | ----------------- | --------- | ---------------- | ----------------- | ----------------- |
| 1.     | PSA               | Pardubice | Ano              |                   |                   |
| 2.     | Krkavci           | Praha     | Ne               | Duelanti          |                   |
| 3.     | Duelanti          | Praha     | Ne               |                   | Krkavci           |
| 4.     | Digladior         | Praha     | Ano              |                   |                   |
| 5.     | Poslední Argument | Praha     | Ano              |                   |                   |
| 6.     | Helops            | Přepeře   | Ano              |                   |                   |
