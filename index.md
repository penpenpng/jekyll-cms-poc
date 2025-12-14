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

# Relays from toml

<ul>
{% for _, relay in site.awesomes.Relays %}
  <li>
    <code>{{ relay.address }}</code> - {{ relay.description_ja }} by
  </li>
{% endfor %}
</ul>
