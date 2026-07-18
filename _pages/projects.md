---
layout: page
title: projects
permalink: /projects/
description: Research and technical projects.
nav: true
nav_order: 3
display_categories: [research]
horizontal: true
---

Selected research and engineering projects in quantum devices, MEMS sensing, cosmological inference, and digital IC implementation.

<style>
  .projects .projects-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin: 1.5rem 0 0;
  }

  .projects .projects-list > .col {
    width: 100%;
    max-width: 100%;
    padding: 0;
  }

  .projects .projects-list .card {
    overflow: hidden;
  }

  .projects .projects-list .card > .row {
    display: grid;
    grid-template-columns: minmax(180px, 30%) minmax(0, 1fr);
    margin: 0;
  }

  .projects .projects-list .card > .row > [class*="col-md-"] {
    width: auto;
    max-width: none;
    padding: 0;
  }

  .projects .projects-list .card > .row > .col-md-12 {
    grid-column: 1 / -1;
  }

  .projects .projects-list figure,
  .projects .projects-list picture {
    display: block;
    height: 100%;
    margin: 0;
  }

  .projects .projects-list .card-img {
    width: 100%;
    height: 100%;
    min-height: 190px;
    max-height: 230px;
    object-fit: contain;
    padding: 0.75rem;
    background: var(--global-card-bg-color);
  }

  .projects .projects-list .card-body {
    display: flex;
    flex-direction: column;
    height: 100%;
    padding: 1.1rem 1.25rem;
  }

  .projects .projects-list .project-card-link {
    color: inherit;
  }

  .projects .projects-list .project-card-link:hover {
    text-decoration: none;
  }

  .projects .projects-list .project-media {
    display: block;
    height: 100%;
  }

  .projects .projects-list .card-title {
    margin-bottom: 0.55rem;
    font-size: 1.2rem;
    line-height: 1.35;
  }

  .projects .projects-list .card-text {
    margin-bottom: 0;
    font-size: 0.95rem;
    line-height: 1.6;
  }

  .projects .projects-list .project-tools {
    margin: 0.75rem 0 0;
    color: var(--global-text-color-light);
    font-size: 0.84rem;
    line-height: 1.5;
  }

  .projects .projects-list .project-tools strong {
    color: var(--global-text-color);
    font-weight: 500;
  }

  .projects .projects-list .project-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: auto;
    padding-top: 0.85rem;
  }

  .projects .projects-list .project-actions .btn {
    display: inline-flex;
    align-items: center;
    gap: 0.4rem;
    width: auto;
  }

  @media (max-width: 767px) {
    .projects .projects-list .card > .row {
      grid-template-columns: 1fr;
    }

    .projects .projects-list .card-img {
      height: 170px;
      min-height: 0;
      max-height: 170px;
    }

    .projects .projects-list .card-body {
      padding: 1rem;
    }
  }
</style>

<div class="projects">
  {% if site.enable_project_categories and page.display_categories %}
    {% for category in page.display_categories %}
      <a id="{{ category }}" href=".#{{ category }}">
        <h2 class="category">{{ category }}</h2>
      </a>
      {% assign categorized_projects = site.projects | where: "category", category %}
      {% assign sorted_projects = categorized_projects | sort: "importance" %}
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-1 projects-list">
            {% for project in sorted_projects %}
              {% include project_list_item.liquid %}
            {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="grid">
          {% for project in sorted_projects %}
            {% include projects.liquid %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}
  {% else %}
    {% assign sorted_projects = site.projects | sort: "importance" %}
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 projects-list">
          {% for project in sorted_projects %}
            {% include project_list_item.liquid %}
          {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="grid">
        {% for project in sorted_projects %}
          {% include projects.liquid %}
        {% endfor %}
      </div>
    {% endif %}
  {% endif %}
</div>
