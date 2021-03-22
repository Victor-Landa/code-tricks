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
