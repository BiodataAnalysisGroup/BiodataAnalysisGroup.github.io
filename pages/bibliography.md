---
layout: base
title: Publications
permalink: /publications/
background: https://images.unsplash.com/photo-1470549638415-0a0755be0619?auto=format&w=2000
---

<!-- # Bibliography -->


<div class="tabs">
  <!-- Tab buttons -->
  <div class="tab-buttons">
    <button class="tab-link active" onclick="openTab(event, 'book')">Book</button>
    <button class="tab-link" onclick="openTab(event, 'book-chapter')">Book Chapter</button>
    <button class="tab-link" onclick="openTab(event, 'journals')">Journals</button>
    <button class="tab-link" onclick="openTab(event, 'conferences')">Conferences and Announcements</button>
    <button class="tab-link" onclick="openTab(event, 'other')">Other (Posters/Slides/Datasets)</button>
    <button class="tab-link" onclick="openTab(event, 'short-articles')">Short articles and Preprints</button>
  </div>

  <!-- Tab content -->
  <div id="book" class="tab-content" style="display:block;">
    ## Book

    <p style="margin-bottom:15px"></p>

    ### 2018

    {% bibliography --query @book[year=2018] %}
  </div>

  <div id="book-chapter" class="tab-content">
    ## Book Chapter
    <p style="margin-bottom:15px"></p>

    ### 2023

    {% bibliography --query @inbook[year=2023] %}

    ### 2022

    {% bibliography --query @inbook[year=2022] %}

    ### 2019

    {% bibliography --query @inbook[year=2019] %}
  </div>

  <div id="journals" class="tab-content">
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

  <div id="conferences" class="tab-content">
    ## Conferences and Announcements
    <p style="margin-bottom:15px"></p>

    <!-- ### 2020

    {% bibliography --query @inproceedings[year=2020] %} -->



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

  <div id="other" class="tab-content">
    ## Other (Posters/Slides/Datasets)
    <p style="margin-bottom:15px"></p>

    ### 2025

    {% bibliography --query @misc[year=2025] %}

    ### 2024

    {% bibliography --query @misc[year=2024] %}

    ### 2023

    {% bibliography --query @misc[year=2023] %}
  </div>

  <div id="short-articles" class="tab-content">
    ## Short articles and Preprints
    <p style="margin-bottom:15px"></p>

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
