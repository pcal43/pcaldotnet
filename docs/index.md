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
    display: flex;
    flex-direction: column;
    height: 100%;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 16px rgba(0,0,0,0.1);
    transition: transform 0.2s ease;
    text-align: center;
    text-decoration: none;
    color: inherit;
    background: white;
    padding: 0;  /* Remove padding around the card */
  }

  .card img {
    width: 100%;
    height: 100%;  /* Make the image fill the entire height of the card */
    object-fit: cover;  /* Ensure the image covers the area without distortion */
    margin: 0;  /* No space between image and the tile */
  }

  .card .content {
    padding: 0.75rem 1rem;  /* Smaller padding to reduce spacing */
    display: flex;
    flex-direction: column;
    align-items: center;
    flex-grow: 1;
    justify-content: space-between;  /* Push title and description towards top */
  }

  .card .title {
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }

  .card .description {
    font-size: 0.9rem;
    font-style: italic;
    color: #555;
    margin: 0;
  }

  .card:hover {
    transform: translateY(-5px);
  }
</style>

<div class="grid">
  {% for project in site.data.projects %}
    <a href="{{ project.url }}" class="card">
      <img src="{{ project.image }}" alt="{{ project.title }}">
      <div class="content">
        <div class="title">{{ project.title }}</div>
        <div class="description">{{ project.description }}</div>
      </div>
    </a>
  {% endfor %}
</div>
