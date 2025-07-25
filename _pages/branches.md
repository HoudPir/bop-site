---
layout: default
title: Branches
permalink: /branches/
custom_css: branches.css
---

# Our Branches

<table class="branches-table">
  <thead>
    <tr>
      <th>S#</th>
      <th>Branch Name</th>
      <th>Address</th>
      <th>Phone</th>
      <th>Email</th>
    </tr>
  </thead>
  <tbody>
    {% for branch in site.data.branches %}
    <tr>
      <td data-label="S#">{{ forloop.index }}</td>
      <td data-label="Branch Name">{{ branch.name }}</td>
      <td data-label="Address">{{ branch.address }}</td>
      <td data-label="Phone">{{ branch.phone }}</td>
      <td data-label="Email"><a href="mailto:{{ branch.email }}">{{ branch.email }}</a></td>
    </tr>
    {% endfor %}
  </tbody>
</table>
<script>
    function toggleTheme() {
      const current = document.documentElement.getAttribute('data-theme');
      const next = current === 'dark' ? 'light' : 'dark';
      document.documentElement.setAttribute('data-theme', next);
    }
  </script>
