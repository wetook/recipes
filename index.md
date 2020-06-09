---
title: Recipes organized in arbitrary categories
---

{% for category in site.data.categories -%}
## {{ category.last }}

{% for recipe in site.recipes -%}
{% if recipe.tags contains category.first -%}
- [{{ recipe.title }}]({{ recipe.url }})
{% endif -%}
{% endfor %}

{% endfor %}
