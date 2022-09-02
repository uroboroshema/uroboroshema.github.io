**Datum výzvy**: {{ include.data.date | date: "%Y-%m-%d" }}  
{% if include.data.match %}**Datum zápasu**: {{ include.data.match.date }}  
**Místo zápasu**: {{ include.data.match.place }}  
**Vyzyvatel**: {{ include.data.challenger }}
  * {{ include.data.match.challenger_lineup[0] }}
  * {{ include.data.match.challenger_lineup[1] }}
  * {{ include.data.match.challenger_lineup[2] }}{% if include.data.match.challenger_lineup.size == 4 %}
  * {{ include.data.match.challenger_lineup[3] }} (N){% endif %}

**Vyzvaný**: {{ include.data.challengee }}
  * {{ include.data.match.challengee_lineup[0] }}
  * {{ include.data.match.challengee_lineup[1] }}
  * {{ include.data.match.challengee_lineup[2] }}{% if include.data.match.challengee_lineup.size == 4 %}
  * {{ include.data.match.challengee_lineup[3] }} (N){% endif %}  


**Výsledek**: {{ include.data.match.challenger_score }}:{{ include.data.match.challengee_score}}
{% if include.data.match.video_code %}
Záznam zápasu:
{{ include.data.match.video_code }}
{% endif %}
{% else %}**Vyzyvatel**: {{ include.data.challenger }}  
**Vyzvaný**: {{ include.data.challengee }}

## Zápas ještě neproběhl.
{% endif %}
