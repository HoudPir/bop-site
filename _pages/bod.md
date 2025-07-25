---
title: Profile of the Board of Directors
permalink: "/bod/"
layout: default
custom_css: bod.css
---

<h1>Profile of the Board of Directors</h1>

<table class="bod-table">
  <thead>
    <tr>
      <th>Name</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    {% for member in site.data.board %}
    <tr>
      <td>{{ member.name }}</td>
      <td>{{ member.position }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<section class="bod-profiles">
  {% for member in site.data.board %}
  <div class="bod-profile">
    <h2>{{ member.name }}</h2>
    <p>{{ member.bio }}</p>
  </div>
  {% endfor %}
</section>
