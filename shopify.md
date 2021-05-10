Get the sizes on the variants with an associated URL.
```liquid
{% assign product_sizes = '' %}
{% assign product_variants_shareable_url = '' %}

{% for variant in product.variants %}
	{% if variant.title contains ' / ' %}
		{% assign variant_splitted = variant.title | split: ' / ' %}
    {% assign variant_size = variant_splitted | first %}
    {% assign variant_url = variant.url %}
		{% unless product_sizes contains variant_size %}
			{% assign product_sizes = product_sizes | append: variant_size | append: ',' %}
	    {% assign product_variants_shareable_url = product_variants_shareable_url | append: variant_url | append: ',' %}
    {% endunless %}
	{% endif %}
{% endfor %}

{% assign product_sizes_array = product_sizes | split: ',' %}
{% assign product_variants_shareable_url_array = product_variants_shareable_url | split: ',' %}

{% for size in product_sizes_array %}
	{{ size }}
{% endfor%}
```
Filter products by tag groups.
```liquid
{% assign tag_groups = '' %}
{% for tag in collection.all_tags %}
	{% if tag contains '_' %}
  	{% assign group = tag | split: '_' | first %}
  	{% assign tag_groups = tag_groups | append: group | append: ',' %}
	{% endif %}
{% endfor %}

{% assign tag_groups = tag_groups | split: ',' | uniq | sort %}


{% for group in tag_groups %}
	{% for tag in collection.all_tags %}
  	{% assign tag_parts = tag | split: '_' %}
  	{% assign tag_group = tag_parts | first %}
  	{% if tag_group == group %}
			<a {% if current_tags contains tag %}class="active"{% endif %} href="{{ routes.collections_url }}/{% if collection.handle != blank %}{{ collection.handle }}{% else %}all{% endif %}/{{ tag | handleize }}">{{ tag }}</a>
  	{% endif %}
	{% endfor %}
{% endfor %}
```
