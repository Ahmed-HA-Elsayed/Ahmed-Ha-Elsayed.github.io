---
layout: page
permalink: /teaching/
title: teaching
description: Teaching experience in electromagnetics, quantum computing, photonics, semiconductors, and MEMS.
nav: true
nav_order: 6
---

I support undergraduate engineering and physics education through tutorials, laboratory sessions, and guided problem solving.

<style>
  .teaching-history {
    margin-top: 2rem;
  }

  .teaching-role {
    padding: 1.75rem 0;
    border-top: 1px solid var(--global-divider-color);
  }

  .teaching-role:last-child {
    border-bottom: 1px solid var(--global-divider-color);
  }

  .teaching-role-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    gap: 1.5rem;
  }

  .teaching-institution {
    margin: 0 0 0.25rem;
    color: var(--global-theme-color);
    font-size: 0.95rem;
    font-weight: 500;
  }

  .teaching-role-title {
    margin: 0;
    font-size: 1.35rem;
    line-height: 1.35;
  }

  .teaching-period {
    margin: 0.2rem 0 0;
    color: var(--global-text-color-light);
    font-size: 0.9rem;
    white-space: nowrap;
  }

  .teaching-summary {
    max-width: 760px;
    margin: 0.85rem 0 1.25rem;
    line-height: 1.65;
  }

  .teaching-courses-title {
    margin: 0 0 0.55rem;
    font-size: 1rem;
    font-weight: 500;
  }

  .teaching-course-list {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    margin: 0;
    padding: 0;
    border-top: 1px solid var(--global-divider-color);
    list-style: none;
  }

  .teaching-course-list li {
    min-width: 0;
    padding: 0.65rem 0.75rem;
    border-bottom: 1px solid var(--global-divider-color);
    border-left: 2px solid var(--global-theme-color);
    font-size: 0.92rem;
    line-height: 1.4;
  }

  @media (max-width: 767px) {
    .teaching-role-header {
      display: block;
    }

    .teaching-period {
      margin-top: 0.4rem;
      white-space: normal;
    }

    .teaching-course-list {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }
  }

  @media (max-width: 480px) {
    .teaching-course-list {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="teaching-history">
  <section class="teaching-role">
    <header class="teaching-role-header">
      <div>
        <p class="teaching-institution">Nile University</p>
        <h2 class="teaching-role-title">Teaching Assistant</h2>
      </div>
      <p class="teaching-period">July 2025 - Present</p>
    </header>
    <p class="teaching-summary">
      Deliver tutorials and laboratory sessions across electromagnetics, quantum technologies, electronics, and core engineering subjects.
    </p>
    <h3 class="teaching-courses-title">Courses and laboratories</h3>
    <ul class="teaching-course-list">
      <li>Electromagnetics</li>
      <li>Applied Electromagnetics</li>
      <li>Quantum Computing</li>
      <li>Antenna Theory</li>
      <li>Semiconductors</li>
      <li>Optics</li>
      <li>Logic Design</li>
      <li>Signals and Systems</li>
      <li>Analog Integrated Circuits</li>
    </ul>
  </section>

  <section class="teaching-role">
    <header class="teaching-role-header">
      <div>
        <p class="teaching-institution">Zewail City University of Science and Technology</p>
        <h2 class="teaching-role-title">Teaching Assistant</h2>
      </div>
      <p class="teaching-period">July 2024 - May 2025</p>
    </header>
    <p class="teaching-summary">
      Assisted with tutorials and laboratory sessions in photonics, semiconductor devices, and microsystems design.
    </p>
    <h3 class="teaching-courses-title">Courses and laboratories</h3>
    <ul class="teaching-course-list">
      <li>Photonics</li>
      <li>Semiconductors</li>
      <li>MEMS Design</li>
    </ul>
  </section>
</div>
