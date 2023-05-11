{%- for sponsor in currentSponsors -%}
  {%- if sponsor_level != sponsor.Level -%}
    {%- assign sponsor_level = sponsor.Level -%}
      <div class="sponsor-class text-center">
        <h3>{{ sponsor_level }}</h3>
      </div>
  {%- endif -%}      

  <div class="sponsor sponsor-{{ sponsor.Level | downcase }}"><a href="{{ sponsor.Link }}"><img src="{{ site.homepage_sponsors_year }}/sponsors/{{ sponsor.Image }}" alt="{{ sponsor.Name }}" /></a></div>

{%- endfor -%}