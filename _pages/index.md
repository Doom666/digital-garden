---
layout: page
title: Home
id: home
permalink: /
---

# Welcome!

You take the <a href="https://www.youtube.com/watch?v=jvDRfb60nwI" style="color: white; font-weight: bold; background:#0043ff; border-radius:100%; box-shadow: 5px 5px 5px #0e0b3c, inset 5px 5px 5px #ffffff70, inset 2px 2px 3px #ffffff90, inset 7px 7px 7px #ffffff50; padding: 12px;">blue pill -</a> the story ends, you wake up in your bed and believe whatever you want to believe. 




You take the <a href="/the-core" style="color: white; font-weight: bold; background:#fe2b2b; border-radius:100%; box-shadow: 5px 5px 5px #3c0b0b, inset 5px 5px 5px #ffffff70, inset 2px 2px 3px #ffffff90, inset 7px 7px 7px #ffffff50; padding: 12px;">red pill -</a> - you stay in Wonderland and I show you how deep the rabbit-hole goes.



<div class="backlink-box">
<h2>Changelog:</h2>
<p>There are a total of {{ site.notes.size }} notes, from which, the latest are:</p>
  {% assign notes = site.notes | where_exp: "item", "item.path contains 'notes'" | sort: "last_modified_at" | reverse %}
  {% for entry in notes limit: 5 %}
  {% unless entry.path contains "index.md" or entry.path contains "index.html" %}
  <div class="list-entry">
    <div><a class="internal-link" href="{{ entry.url }}">{{ entry.title }}</a> <span
        class="faded">{{ entry.last_modified_at | date: '%a, %b %e, of %Y; %R.'}}</span></div>
    <div>{{ entry.excerpt | strip_html | truncatewords: 10 }}</div>

  </div>
  {% endunless %}
  {% endfor %}

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
