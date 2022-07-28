---
layout: base
title: Publications
permalink: /publications/
background: https://images.unsplash.com/photo-1470549638415-0a0755be0619?auto=format&w=2000
---

<!-- # Bibliography -->

[**Book**](#book) &nbsp; [**Book Chapter**](#book-chapter) &nbsp; [**Journals**](#journals) &nbsp; [**Conferences and Announcements**](#conferences-and-announcements) &nbsp; [**Other**](#other)

<br/>

## Book

<p style="margin-bottom:15px"></p>

### 2018

{% bibliography --query @book[year=2018] %}
<br/>

## Book Chapter
<p style="margin-bottom:15px"></p>

### 2022

{% bibliography --query @inbook[year=2022] %}

### 2019

{% bibliography --query @inbook[year=2019] %}


<br/>

## Journals

<p style="margin-bottom:15px"></p>

### 2022

{% bibliography --query @article[year=2022] %}

### 2021

{% bibliography --query @article[year=2021] %}

### 2020

{% bibliography --query @article[year=2020] %}

### 2019

{% bibliography --query @article[year=2019] %}

<br/>

## Conferences and Announcements

<p style="margin-bottom:15px"></p>

<!-- ### 2020

{% bibliography --query @inproceedings[year=2020] %} -->

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


<br/>

## Other

<p style="margin-bottom:15px"></p>

### Short articles
<p style="margin-bottom:15px"></p>

### 2022

{% bibliography --query @misc[year=2022] %}

### 2021

{% bibliography --query @misc[year=2021] %}

### 2020

{% bibliography --query @misc[year=2020] %}

### 2019

{% bibliography --query @misc[year=2019] %}

<br/>



### Thesis

{% bibliography --query @phdthesis %}


[//]: # {% bibliography --query @ \* [year=2017] %}
[//]: # (pandoc --filter=pandoc-citeproc --standalone publications.md -o publications.html)
