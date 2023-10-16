---
---

## Presentations

Following is a non-comprehensive list of presentations about programming and technology I've given at conferences and user groups around the world.

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
