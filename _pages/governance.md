---
layout: default
title: Governance
permalink: /governance/
custom_css: governance.css
---

<body>

  
  <!-- Main Content -->
  <div class="content">
    <h1>Governance</h1>
    <div class="info-box">
      <a href="{{ '/BOP-ESG/' | relative_url }}">BOP’s ESG Vision, Mission Statement, Policy Statement, Green Banking Principles/Objectives</a>
      <a href="{{ '/BOD/' | relative_url }}">Profile of the Board of Directors</a>

      <div class="info-dropdown" onclick="toggleDropdown(this)">Auditor's Name</div>
      <div class="expand-content">A.F. Ferguson & Co., Chartered Accountants</div>

      <div class="info-dropdown" onclick="toggleDropdown(this)">Legal Advisors</div>
      <div class="expand-content">Salim Baig & Associates, 16, 3rd Floor, Imtiaz Plaza, The Mall, Lahore</div>

      <a href="Management.html">Management</a>
      <a href="#">Code of Conduct for Directors</a>
      <a href="#">Key Highlights of Board Remuneration Policy 2020</a>
    </div>
  </div>

  <!-- Theme + Dropdown Script -->
  <script>
    function toggleTheme() {
      const current = document.documentElement.getAttribute('data-theme');
      const next = current === 'dark' ? 'light' : 'dark';
      document.documentElement.setAttribute('data-theme', next);
    }

    function toggleDropdown(el) {
      el.classList.toggle("open");
    }
  </script>

</body>
