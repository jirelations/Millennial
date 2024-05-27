---
layout: default
title: Podcast
permalink: /podcast/
---
<div class="post-content">
<h1>{{ page.title }}</h1>

To subscribe to this podcast, go to your podcast player and choose "Subscribe with URL" (or similar). Then paste this URL there: {{ site.url }}{{ site.baseurl }}/podcast.xml

To create your podcast episode for the course, <a href="#podcast-checklist">jump to the Podcast Checklist below</a>.

{% for entry in site.podcasts %}
  <article>
    <h2><a href="{{ entry.url }}">{{ entry.title }}</a></h2>
    <p>{{ entry.short_description }}</p>
      {% if entry.image %}
        {% include featured-image.html image=entry.image %}
      {% endif %}
      {% include audio.html mp3=entry.mp3 %}
  </article>
{% endfor %}
</div>

To subscribe to this podcast, go to your podcast player and choose "Subscribe with URL" (or similar). Then paste this URL there: {{ site.url }}{{ site.baseurl }}/podcast.xml

{% for entry in site.podcasts %}
  <article>
    <h2><a href="{{ entry.url }}">{{ entry.title }}</a></h2>
    <p>{{ entry.short_description }}</p>
      {% if entry.image %}
        {% include featured-image.html image=entry.image %}
      {% endif %}
      {% include audio.html mp3=entry.mp3 %}
  </article>
{% endfor %}
</div>