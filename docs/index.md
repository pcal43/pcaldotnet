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
  }

  .card img {
    width: 100%;
    height: auto; /* preserve aspect ratio */
    aspect-ratio: 1 / 1; /* enforces square if browser supports it */
    object-fit: contain; /* don’t crop square images */
    background: #f8f8f8;
  }

  .card .content {
    padding: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .card .title {
    font-size: 1.2rem;
    font-weight: bold;
