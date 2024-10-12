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

## Podcast Checklist

- [ ] Fragen vorbereiten, die zur Person und zum Thema relevant sind
- [ ] [Einverständniserklärung](../assets/pdf/media-release.pdf) von allen, deren Stimme in der Aufzeichnung gehört werden kann (einschließlich Ihnen)
- [ ] Audio an einem ruhigen, ungestörten Ort im Innenraum aufzeichnen, entweder
  - [ ] in Präsenz auf dem Handy (Testen Sie, dass alle Stimmen gehört werden können), oder
  - [ ] per Video-Anruf (wenn notwendig) mit der Aufzeichnungsfunktion. (Gutes Backup: beide Seiten zeichnen auch mit dem Handy auf.)
- [ ] Audio bearbeiten (z.B. in der [Audacity](https://www.audacityteam.org/)-App), bis die Aufzeichnung ca. 10 Minuten ist
- [ ] Audio [in OLAT hochladen](https://olat-ce.server.uni-frankfurt.de/olat/auth/RepositoryEntry/20609269764/CourseNode/1714358581837189007)
