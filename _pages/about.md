---
title: "About"
layout: page
permalink: /about/
---

# About

<div class="section-card">
<div class="pi-card">
<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ site.name }}" width="220" height="270">
<div>
<h2 class="pi-name">{{ site.name }}</h2>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.title }}, {{ site.institution }}</p>
<div class="pi-links">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.links.cv | prepend: '/' | relative_url }}" class="icon-link" title="CV" aria-label="CV">{% include icon.html name="cv" %}</a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate" aria-label="ResearchGate">{% include icon.html name="researchgate" %}</a>{% endif %}
{% if site.links.afrobarometer and site.links.afrobarometer != ""%}<a href="{{ site.links.afrobarometer }}" class="fas fa-globe icon-pad-right" title="Afrobarometer" aria-label="Afrobarometer">{% include icon.html name="afrobarometer" %}</a>{% endif %}

</div>
{% if site.data.pi[0].education %}
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","&#8211;" }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>

{% for project in site.data.research %}
<div class="section-card" markdown="0">
<h2>{{ project.name }}</h2>
{% if project.website or project.repo or project.docs or project.paper %}
<div class="pub-actions" style="margin-bottom: var(--space-3);">
{% if project.website %}<a href="{{ project.website }}" target="_blank" class="btn-pill btn-website">Website</a>{% endif %}
{% if project.repo %}<a href="{{ project.repo }}" target="_blank" class="btn-pill btn-git">Code</a>{% endif %}
{% if project.docs %}<a href="{{ project.docs }}" target="_blank" class="btn-pill btn-link">Docs</a>{% endif %}
{% if project.paper %}<a href="{{ project.paper }}" target="_blank" class="btn-pill btn-link">Paper</a>{% endif %}
</div>
{% endif %}
{% if project.authors %}<p><strong>Authors:</strong> <em>{{ project.authors }}</em></p>{% endif %}
<p>{{ project.description }}</p>
</div>
{% endfor %}

<div class="section-card">
  <h2>CV</h2>
  <p>
    <a href="/papers/Resume_Sunderland.pdf" target="_blank">
      Download my CV (PDF)
    </a>
  </p>
  <iframe
    src="/papers/Resume_Sunderland.pdf"
    width="100%"
    height="700px"
    style="border: none;">
  </iframe>
</div>



