---
---

## Presentations

Details & links to all the tech presentations that I've given over the years:

{% for item in site.data.presentations %}
- {{ item.year }}
  {% for event in item.events %}
  - {{ event.name }} - {{ event.date }}
    {% for talk in event.talks %}
    - [{{ talk.title }}]({{ talk.file }})
    {% endfor %}
  {% endfor %}
{% endfor %}

<ul>
   {% for item in site.data.navigation %}
      <li><a href="{{ item.url }}">{{ item.title }}</a></li>
   {% endfor %}
</ul>
