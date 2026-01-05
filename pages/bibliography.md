---
layout: base
title: Publications
permalink: /publications/
background: https://images.unsplash.com/photo-1470549638415-0a0755be0619?auto=format&w=2000
---

<!-- Bibliography with tabbed interface -->

<style>
/* Tab container */
.tabs { width: 100%; }

/* Buttons row */
.tab-buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 18px;
}

/* Buttons */
.tab-link {
  background-color: #f1f1f1;
  border: none;
  padding: 8px 14px;
  cursor: pointer;
  font-weight: 600;
  border-radius: 6px;
  transition: background 0.18s;
}
.tab-link:hover { background-color: #e6e6e6; }

/* Active button */
.tab-link.active {
  background-color: #2563eb; /* blue */
  color: #fff;
}

/* Content panels */
.tab-content {
  display: none;
  padding-top: 6px;
}
</style>

<div class="tabs">

  <!-- Tab buttons -->
  <div class="tab-buttons" role="tablist" aria-label="Publications categories">
    <button class="tab-link active" onclick="openTab(event,'book')" role="tab" aria-selected="true">Book</button>
    <button class="tab-link" onclick="openTab(event,'book-chapter')" role="tab">Book Chapter</button>
    <button class="tab-link" onclick="openTab(event,'journals')" role="tab">Journals</button>
    <button class="tab-link" onclick="openTab(event,'conferences')" role="tab">Conferences and Announcements</button>
    <button class="tab-link" onclick="openTab(event,'other')" role="tab">Other (Slides/Datasets/Short articles/Preprints)</button>
  </div>

  <!-- Tab content: use markdown="1" so kramdown will process the Markdown and Liquid tags inside -->
  <div id="book" class="tab-content" markdown="1" style="display:block;" role="tabpanel" aria-hidden="false">
## Book

<p style="margin-bottom:15px"></p>

### 2018

{% bibliography --query @book[year=2018] %}
  </div>

  <div id="book-chapter" class="tab-content" markdown="1" role="tabpanel" aria-hidden="true">
## Book Chapter

<p style="margin-bottom:15px"></p>

### 2023

{% bibliography --query @inbook[year=2023] %}

### 2022

{% bibliography --query @inbook[year=2022] %}

### 2019

{% bibliography --query @inbook[year=2019] %}
  </div>

  <div id="journals" class="tab-content" markdown="1" role="tabpanel" aria-hidden="true">
## Journals

<p style="margin-bottom:15px"></p>

### 2025
{% bibliography --query @article[year=2025] %}

### 2024 
{% bibliography --query @article[year=2024] --template bib %}

### 2023
{% bibliography --query @article[year=2023] %}

### 2022
{% bibliography --query @article[year=2022] %}

### 2021
{% bibliography --query @article[year=2021] %}

### 2020
{% bibliography --query @article[year=2020] %}

### 2019
{% bibliography --query @article[year=2019] %}
  </div>

  <div id="conferences" class="tab-content" markdown="1" role="tabpanel" aria-hidden="true">
## Conferences and Announcements

<p style="margin-bottom:15px"></p>

### 2025
{% bibliography --query @inproceedings[year=2025] %}
{% bibliography --query @conference[year=2025] %}

### 2024
{% bibliography --query @inproceedings[year=2024] %}
{% bibliography --query @conference[year=2024] %}

### 2023
{% bibliography --query @inproceedings[year=2023] %}
{% bibliography --query @conference[year=2023] %}

### 2022
{% bibliography --query @inproceedings[year=2022] %}
{% bibliography --query @conference[year=2022] %}

### 2021
{% bibliography --query @inproceedings[year=2021] %}
{% bibliography --query @conference[year=2021] %}

### 2020
{% bibliography --query @inproceedings[year=2020] %}
{% bibliography --query @conference[year=2020] %}

### 2019
{% bibliography --query @inproceedings[year=2019] %}
{% bibliography --query @conference[year=2019] %}
  </div>

  <div id="other" class="tab-content" markdown="1" role="tabpanel" aria-hidden="true">
## Other (Slides/Datasets/Short articles/Preprints)

<p style="margin-bottom:15px"></p>

### 2025
{% bibliography --query @misc[year=2025] %}

### 2024
{% bibliography --query @misc[year=2024] %}

### 2023
{% bibliography --query @misc[year=2023] %}

### 2022
{% bibliography --query @misc[year=2022] %}

### 2021
{% bibliography --query @misc[year=2021] %}

### 2020
{% bibliography --query @misc[year=2020] %}

### 2019
{% bibliography --query @misc[year=2019] %}

### 2016
{% bibliography --query @*[year=2016] %}

### 2015
{% bibliography --query @inproceedings[year=2015] %}
{% bibliography --query @article[year=2015] %}
  </div>

</div>

<script>
/* Tab switching function */
function openTab(evt, tabId) {
  // hide all tab-contents
  var contents = document.querySelectorAll('.tab-content');
  contents.forEach(function(c) {
    c.style.display = 'none';
    c.setAttribute('aria-hidden','true');
  });

  // remove active from all buttons
  var buttons = document.querySelectorAll('.tab-link');
  buttons.forEach(function(b) {
    b.classList.remove('active');
    b.setAttribute('aria-selected','false');
  });

  // show selected
  var selected = document.getElementById(tabId);
  if (selected) {
    selected.style.display = 'block';
    selected.setAttribute('aria-hidden','false');
  }

  // mark clicked button active
  evt.currentTarget.classList.add('active');
  evt.currentTarget.setAttribute('aria-selected','true');

  // optionally, update URL hash without jumping (so back/refresh works)
  if (history && history.replaceState) {
    history.replaceState(null, null, '#' + tabId);
  }
}

/* Optional: open tab from hash on page load */
document.addEventListener('DOMContentLoaded', function() {
  var hash = location.hash.replace('#','');
  if (hash) {
    var btn = Array.from(document.querySelectorAll('.tab-link')).find(b => b.getAttribute('onclick') && b.getAttribute('onclick').includes("'" + hash + "'"));
    if (btn) { btn.click(); return; }
  }
  // default is already Book open (first button marked active and first panel style=block)
});
</script>



