---
layout: default
title: Wentao Li | Home
---

<link rel="stylesheet" href="{{ '/css/profile-pages.css' | relative_url }}">

<style>
.publication-slider {
  display: flex;
  gap: 16px;
  overflow-x: auto;
  padding: 4px 4px 18px;
  counter-reset: publication-card;
  scroll-snap-type: x mandatory;
  scrollbar-color: #d66b64 #f8e2e0;
  scrollbar-width: thin;
  overscroll-behavior-inline: contain;
}

.publication-card {
  flex: 0 0 min(86%, 430px);
  counter-increment: publication-card;
  scroll-snap-align: start;
  padding: 20px;
  border: 1px solid #efc4c0;
  border-radius: 10px;
  background: #fff9f8;
  box-shadow: 0 3px 12px rgba(110, 16, 10, 0.07);
}

.publication-card p,
.publication-entry p {
  margin: 0.55rem 0 0;
}

.publication-number {
  display: inline-block;
  color: #8b2821;
  font-weight: 700;
}

.publication-number::before {
  content: counter(publication-card, decimal-leading-zero);
}

.publication-venue {
  display: inline-block;
  margin-right: 8px;
  padding: 2px 8px;
  border-radius: 999px;
  background: #f4b6b1;
  color: #4b1410;
  font-size: 0.86rem;
  font-weight: 700;
}

.publication-entry {
  color: #3f2927;
}

.slider-hint {
  margin-top: -0.15rem;
  color: #6d6764;
  font-size: 0.92rem;
}

.funding-item {
  margin: 1rem 0;
  padding: 16px 18px;
  border-left: 4px solid #ff0f00;
  background: #fff9f8;
}

.funding-item p {
  margin: 0.45rem 0 0;
}

.funding-title {
  display: block;
  color: #2f2f2f;
}

.funding-detail {
  color: #5a4542;
}

.funding-summary {
  color: #8b2821;
  font-size: 0.95rem;
}
</style>

<div class="academic-shell">
{% include profile-sidebar.html active="home" %}

<main class="academic-main" markdown="1">

## Overview

I am a Lecturer in the School of Computing and Mathematical Sciences at the University of Leicester. My research focuses on developing efficient and scalable solutions for large-scale data processing and machine learning, with particular interests in graph data processing, graph mining, and vector databases.

I have published more than 30 CORE A*/CCF-A level papers, including work at SIGMOD, VLDB, SIGKDD, ICDE, The Web Conference, TKDE, and VLDBJ. I have also authored one monograph and obtained one patent. More information is available on my [Biography](/biography.html) page.

## News

<p class="slider-hint">Swipe horizontally or use the scrollbar to browse the five latest publications.</p>

{% assign publications_page = site.pages | where: "name", "publications.md" | first %}
{% assign publication_section = publications_page.content | split: "## Selected Publications (* indicates Corresponding Author)" | last %}
{% assign normalized_publications = publication_section | strip | newline_to_br | strip_newlines %}
{% assign publication_items = normalized_publications | split: "<br /><br />1. " %}

<div class="publication-slider" role="region" aria-label="Five latest publications" tabindex="0">
{% for publication in publication_items limit: 5 %}
  {% assign publication_text = publication | remove_first: "1. " | remove: "<br />" | strip %}
  {% assign publication_lines = publication_text | split: "<br>" %}
  {% assign venue_tail = publication_lines[2] | split: "(" | last %}
  {% assign venue = venue_tail | split: ")" | first | strip %}
  <article class="publication-card">
    <span class="publication-venue">{{ venue }}</span>
    <span class="publication-number" aria-label="Publication {{ forloop.index }}"></span>
    <div class="publication-entry">{{ publication_text | markdownify }}</div>
  </article>
{% endfor %}
</div>

[View all selected publications →](/publications.html)

## Prospective Students

I am looking for highly motivated PhD students, including CSC Joint PhD candidates, to join me at the University of Leicester. Our research addresses challenging problems in graph data processing, graph mining, and vector databases.

- **GTA-funded opportunities:** open to qualified UK and international applicants.
- **CSC-funded opportunities:** available to eligible Chinese applicants, including joint PhD candidates.
- **How to apply:** please send your CV and research statement to [wl226@leicester.ac.uk](mailto:wl226@leicester.ac.uk) or [livent@126.com](mailto:livent@126.com).

Please visit the [Prospective Students](/prospective-students.html) page for application details and funding links.

## Funding

<div class="funding-item">
  <strong class="funding-title">Numeric-Constrained Shortest Path Query Processing on Road Networks</strong>
  <p class="funding-detail">National Natural Science Foundation of China · Young Scientists Fund (Category C) · Grant 62302417</p>
  <p class="funding-summary"><strong>Principal Investigator</strong> · Jan 2024–Dec 2026 · RMB 300,000</p>
</div>

<div class="funding-item">
  <strong class="funding-title">Key Technologies for Heterogeneous Data Management Based on Foundation Models</strong>
  <p class="funding-detail">Guangzhou Municipal Science and Technology Bureau · University–Institution–Enterprise Joint Funding Project · Grant 2024A03J0621</p>
  <p class="funding-summary"><strong>Participant</strong> · Jan 2024–Dec 2026 · RMB 300,000</p>
</div>

## Awards

- [2021 Global Top 100 Chinese Rising Stars in Artificial Intelligence](https://xueshu.baidu.com/usercenter/index/aischolar), 2021.
- SIGMOD Travel Award, 2019.
- Outstanding Graduate of Chongqing City, 2016.
- Outstanding Graduate of Chongqing University, 2016.

</main>
</div>
