{% assign past_year = 0 %}
{% for class in site.data.teaching %}
{% assign current_year = class.year %}
{% if class.display == 'y' %}
{% if past_year != current_year %}
## {{ class.year }}
{% endif %}

### {{ class.titre }}
<!-- class.shortname -->
<!-- class.hours -->
  _{{ class.track }}_ 

{{ class.details }}


{% endif %}
{% assign past_year = current_year %}

{% endfor %}


