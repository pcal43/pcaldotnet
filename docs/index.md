---
layout: default
title: Projects
---

<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 1.5rem;
    padding: 2rem 0;
  }
  .card {
    display: block;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 16px rgba(0,0,0,0.1);
    transition: transform 0.2s ease;
    text-align: center;
    text-decoration: none;
    color: inherit;
  }
  .card img {
    width: 100%;
    height: auto;
    display: block;
  }
  .card .title {
    padding: 1rem;
    font-size: 1.2rem;
  }
  .card .description {
    text-style: italic;
    padding: 1rem;
    font-size: 1rem;
  }
  .card:hover {
    transform: translateY(-5px);
  }
</style>

<div class="grid">
  {% for project in site.data.projects %}
    <a href="{{ project.url }}" class="card">
      <img src="{{ project.image }}" alt="{{ project.title }}">
      <div class="title">{{ project.title }} </div>
      <div class="description">{{ project.description }} </div>
            

    </a>
  {% endfor %}
</div>
