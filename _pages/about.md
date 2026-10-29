---
layout: academic
permalink: /
title: "About"
description: "Minseok Joo is an M.S.-Ph.D. Integrated student at Korea University, interested in generative AI, video world models, video generation, and 3D vision."
redirect_from:
  - /about/
  - /about.html
---

<section id="about" class="about" aria-labelledby="about-heading">
  <h2 id="about-heading">About Me</h2>
  <p>I am an M.S.-Ph.D. Integrated student at Korea University, advised by <a href="https://scholar.google.com/citations?hl=en&amp;user=LfBoJt8AAAAJ&amp;view_op=list_works&amp;sortby=pubdate">Prof. Hyunwoo J. Kim</a> in the <a href="https://mlvlab.github.io/#/home">Machine Learning and Vision (MLV) Lab</a>.</p>
  <p>I'm interested in <strong>generative AI</strong> for modeling the structure and dynamics of the real world, with a particular focus on <strong>video world models</strong>, <strong>video generation</strong>, and <strong>3D vision</strong>.</p>
  <p>Please feel free to <a href="mailto:{{ site.author.email }}">get in touch</a> about potential collaborations or research opportunities. You can also find my <a href="{{ site.author.cv_url | relative_url }}" target="_blank" rel="noopener" aria-label="CV (PDF, opens in a new tab)">CV</a> here.</p>
</section>

<section id="news" class="news" aria-labelledby="news-heading">
  <h2 id="news-heading">News</h2>
  {% assign news_visible = 6 %}
  <ul class="news-list">
    {% for item in site.data.news limit: news_visible %}
    <li><span class="news-date">{% if item.date_label %}{{ item.date_label }}{% else %}{{ item.date | date: "%b %Y" }}{% endif %}</span><span class="news-text">{{ item.text }}</span></li>
    {% endfor %}
  </ul>
  {% if site.data.news.size > news_visible %}
  <details class="news-more">
    <summary><span class="news-more-closed">Show older news ({{ site.data.news.size | minus: news_visible }})</span><span class="news-more-open">Hide older news</span></summary>
    <ul class="news-list">
      {% for item in site.data.news offset: news_visible %}
      <li><span class="news-date">{% if item.date_label %}{{ item.date_label }}{% else %}{{ item.date | date: "%b %Y" }}{% endif %}</span><span class="news-text">{{ item.text }}</span></li>
      {% endfor %}
    </ul>
  </details>
  {% endif %}
</section>

<section id="publications" aria-labelledby="publications-heading">
  <div class="section-heading">
    <h2 id="publications-heading">Publications</h2>
    <a href="{{ site.author.googlescholar | escape }}">Google Scholar ↗</a>
  </div>
  {% include publication-list.html %}
</section>

<section id="service" class="service" aria-labelledby="service-heading">
  <h2 id="service-heading">Academic Service</h2>
  <dl class="service-list">
    <dt>Conference Reviewer</dt>
    <dd>CVPR 2026, ICML 2026, ECCV 2026, NeurIPS 2026, ICLR 2027</dd>
  </dl>
</section>
