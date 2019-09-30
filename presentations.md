---
---

## Presentations

All the tech presentations that I've given over the years:

{% for item in site.data.presentations %}
### {{ item.year }}
  {% for event in item.events %}
* __{{ event.name }}__ - {{ event.date -}}
    {% for talk in event.talks %}
  * [{{ talk.title }} \[{{talk.type | default: "PDF"}}\]](/assets/presentations/{{ item.year }}/{{ talk.file }})
    {%- endfor %}
  {% endfor %}
{% endfor %}

(More still need added, working on that.)
