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

## Site Navigation

* [Check out my Crochet Main Page](_crochet/crochetmain.html)
* [View Chunky Pig Project](_crochet/chunkypig.html)

---

### Recent Updates
Write your latest updates here in plain Markdown text!

# Recent Crochet Projects

{% assign sorted_projects = site.crochet | sort: "date" | reverse %}
<ul>
  {% for project in sorted_projects %}
    <li>
      <a href="{{ site.baseurl }}{{ project.url }}">{{ project.title }}</a>
      <span style="color: var(--text-muted); font-size: 0.85rem;">— {{ project.date | date: "%B %d, %Y" }}</span>
    </li>
  {% endfor %}
</ul>
