{% assign past_year = 0 %}
{% for class in site.data.teachings %}
{% assign current_year = class.year %}
{% if class.display == 'y' %}
{% if past_year != current_year %}
## {{ class.year }}
{% endif %}

### {{ class.titre }}
<!-- class.shortname -->
<!-- class.hours -->
  _{{ class.track }}_ - [Course page]({{ class.link }})

{{ class.details }}


{% endif %}
{% assign past_year = current_year %}

{% endfor %}


