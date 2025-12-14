Hello Jekyll


# Relays

<ul>
{% for relay in site.data.relays %}
  <li>
    <code>{{ relay.address }}</code> - {{ relay.description_ja }} by
    {% for author in relay.authors %}
      <a href="{{ author.url }}">{{ author.name }}</a>{% unless forloop.last %}, {% endunless %}
    {% endfor %}
  </li>
{% endfor %}
</ul>

# Relays by markdown

{% for relay in site.data.relays %}
- `{{ relay.address }}` - {{ relay.description_ja }} by {% for author in relay.authors %}
      [{{ author.name }}]({{ author.url }}){% unless forloop.last %}, {% endunless %}
   {% endfor %}
{% endfor %}
