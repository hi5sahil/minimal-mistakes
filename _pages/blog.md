---
permalink: /blog/
title: "All Posts"
header:
  overlay_image: "https://media.giphy.com/media/26tPcVAWvlzRQtsLS/source.gif"
---

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.posts %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
   <!-- <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2> -->
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
