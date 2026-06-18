---
layout: default
title: "Portfolio | Myreen Repizo"
description: "Work samples and deliverables from Myreen Repizo: ISO 27001, SOC 2, GRC, and information security consulting."
permalink: /portfolio/
---

<style>
  .portfolio-wrapper {
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    color: #1a1a2e;
    max-width: 860px;
    margin: 0 auto;
    padding: 0 1.5rem;
  }
  .portfolio-hero {
    padding: 3.5rem 0 2.5rem;
    border-bottom: 2px solid #e8ecf0;
  }
  .portfolio-eyebrow {
    font-size: 0.75rem;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: #2563eb;
    margin-bottom: 0.75rem;
  }
  .portfolio-hero h1 {
    font-size: clamp(1.75rem, 4vw, 2.5rem);
    font-weight: 800;
    color: #0f172a;
    letter-spacing: -0.02em;
    margin: 0 0 1rem;
    line-height: 1.2;
  }
  .portfolio-hero p {
    font-size: 1.05rem;
    line-height: 1.75;
    color: #475569;
    max-width: 600px;
    margin: 0;
  }

  .portfolio-grid {
    padding: 2.5rem 0;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1.25rem;
  }
  .portfolio-card {
    display: flex;
    flex-direction: column;
    padding: 1.5rem;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    text-decoration: none;
    color: inherit;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .portfolio-card:hover {
    border-color: #2563eb;
    box-shadow: 0 4px 16px rgba(37,99,235,0.08);
    text-decoration: none;
  }
  .card-tag {
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #2563eb;
    margin-bottom: 0.6rem;
  }
  .portfolio-card h2 {
    font-size: 1rem;
    font-weight: 700;
    color: #0f172a;
    margin: 0 0 0.6rem;
    line-height: 1.35;
  }
  .portfolio-card p {
    font-size: 0.875rem;
    color: #64748b;
    line-height: 1.65;
    margin: 0 0 1.25rem;
    flex: 1;
  }
  .card-arrow {
    font-size: 0.85rem;
    font-weight: 700;
    color: #2563eb;
  }

  .empty-state {
    padding: 3rem 0;
    color: #94a3b8;
    font-size: 0.95rem;
  }
</style>

<div class="portfolio-wrapper">

  <div class="portfolio-hero">
    <p class="portfolio-eyebrow">Portfolio</p>
    <h1>Work samples &amp; deliverables</h1>
    <p>
      Reference materials, frameworks, and deliverables from client engagements and independent research
      across ISO 27001, SOC 2, GRC, and information security.
    </p>
  </div>

  <div class="portfolio-grid">
    {% for item in site.portfolio_items %}
    <a href="{{ item.url | relative_url }}" class="portfolio-card">
      {% if item.categories %}
      <div class="card-tag">{{ item.categories | join: " · " }}</div>
      {% endif %}
      <h2>{{ item.title }}</h2>
      {% if item.description %}
      <p>{{ item.description }}</p>
      {% endif %}
      <span class="card-arrow">View &rarr;</span>
    </a>
    {% else %}
    <p class="empty-state">No portfolio items yet.</p>
    {% endfor %}
  </div>

</div>
