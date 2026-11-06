---
layout: default
title: Home
date: 2026-11-06
tags: [Craft, Crochet, Yarn, Stationary, 3D Printing]
description: "Home page."
---

# Welcome to The Clarke Space

Bookmark this page to keep an eye on project updates, documentation, and personal craft patterns.

---

## Quick Navigation
- [Check out my Crochet Main Page](_crochet/crochetmain.html)
- [View Chunky Pig Project](_crochet/chunkypig.html)
- [View All Crochet Projects](#recent-crochet-projects)

---

### Recent Updates
Write your latest updates here in plain Markdown text!

<h2 id="recent-crochet-projects">Recent Crochet Projects</h2>

<div class="card-grid">
  {% assign sorted_projects = site.crochet | sort: "date" | reverse %}
  {% for project in sorted_projects %}
    <a href="{{ site.baseurl }}{{ project.url }}" class="card">
      {% if project.thumbnail %}
        <div class="card-image" style="background-image: url('{{ project.thumbnail }}');"></div>
      {% else %}
        <div class="card-image placeholder">No Image</div>
      {% endif %}
      <div class="card-content">
        <h3>{{ project.title }}</h3>
        <span class="card-date">{{ project.date | date: "%B %d, %Y" }}</span>
      </div>
    </a>
  {% endfor %}
</div>



