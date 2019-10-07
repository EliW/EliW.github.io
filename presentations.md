---
---

## Presentations

I've given a lot of presentations about programming and technology at conferences and user groups around the world.  I have them all listed below, with links to the slide decks.

{% for item in site.data.presentations %}
### {{ item.year }}
  {% for event in item.events %}
* __{{ event.name }}__{% if event.date %} - {{ event.date }}{% endif -%}{% if event.loc %} (_{{ event.loc }}_){% endif -%}
    {% for talk in event.talks %}
      {%- if talk.file %}
  * [{{ talk.title }} \[{{talk.type | default: "PDF"}}\]](/assets/presentations/{{ item.year }}/{{ talk.file }})
      {%- else %}
  * {{ talk.title }}
      {%- endif %}
    {%- endfor %}
  {% endfor %}
{% endfor %}
