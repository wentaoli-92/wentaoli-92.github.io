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
  scroll-snap-type: x mandatory;
  scrollbar-color: #d66b64 #f8e2e0;
  scrollbar-width: thin;
  overscroll-behavior-inline: contain;
}

.publication-card {
  flex: 0 0 min(86%, 430px);
  scroll-snap-align: start;
  padding: 20px;
  border: 1px solid #efc4c0;
  border-radius: 10px;
  background: #fff9f8;
  box-shadow: 0 3px 12px rgba(110, 16, 10, 0.07);
}

.publication-card p {
  margin: 0.55rem 0 0;
}

.publication-number {
  display: inline-block;
  margin-right: 8px;
  color: #8b2821;
  font-weight: 700;
}

.publication-venue {
  display: inline-block;
  padding: 2px 8px;
  border-radius: 999px;
  background: #f4b6b1;
  color: #4b1410;
  font-size: 0.86rem;
  font-weight: 700;
}

.publication-title {
  color: #5f1712;
  font-size: 1.05rem;
  line-height: 1.35;
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
  margin: 0.35rem 0 0;
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

<div class="publication-slider" role="region" aria-label="Five latest publications" tabindex="0">
  <article class="publication-card">
    <span class="publication-number">01</span><span class="publication-venue">ICDE 2027</span>
    <p class="publication-title"><strong>Maintaining Ego-Betweenness Centrality at Billion Scale</strong></p>
    <p>Kaiyu Chen, Dong Wen, <strong>Wentao Li</strong>, Wenjie Zhang, Xuemin Lin.</p>
  </article>

  <article class="publication-card">
    <span class="publication-number">02</span><span class="publication-venue">TKDE 2026</span>
    <p class="publication-title"><strong>Structural Clustering for Bipartite Graphs</strong></p>
    <p>Mingyu Yang, <strong>Wentao Li*</strong>, Wei Wang, Dong Wen, Min Gao, Lu Qin.</p>
  </article>

  <article class="publication-card">
    <span class="publication-number">03</span><span class="publication-venue">SIGKDD 2026</span>
    <p class="publication-title"><strong>E2E: Efficient Filtered AKNN Search via Adaptive Termination</strong></p>
    <p>Wenxuan Xia, Mingyu Yang, <strong>Wentao Li</strong>, Wei Wang.</p>
  </article>

  <article class="publication-card">
    <span class="publication-number">04</span><span class="publication-venue">ICDE 2026</span>
    <p class="publication-title"><strong>Efficient Top-k Nearest Neighbors Search in Dynamic Road Networks</strong></p>
    <p>Junhua Zhang, Yamei Song, <strong>Wentao Li*</strong>, Lu Qin.</p>
  </article>

  <article class="publication-card">
    <span class="publication-number">05</span><span class="publication-venue">ICDE 2026</span>
    <p class="publication-title"><strong>An Efficient and Scalable Approach for Path Queries on Public Transportation Networks</strong></p>
    <p>Junhua Zhang, <strong>Wentao Li</strong>, Wenjie Zhang, Lu Qin, Xiaochun Yang.</p>
  </article>
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
  <strong>Numeric-Constrained Shortest Path Query Processing on Road Networks</strong>
  <p>National Natural Science Foundation of China, Young Scientists Fund (Category C), Grant No. 62302417 · January 2024–December 2026 · RMB 300,000 · Principal Investigator · Ongoing.</p>
</div>

<div class="funding-item">
  <strong>Key Technologies for Heterogeneous Data Management Based on Foundation Models</strong>
  <p>Guangzhou Municipal Science and Technology Bureau, University–Institution–Enterprise Joint Funding Project, Grant No. 2024A03J0621 · January 2024–December 2026 · RMB 300,000 · Participant · Ongoing.</p>
</div>

## Awards

- [2021 Global Top 100 Chinese Rising Stars in Artificial Intelligence](https://xueshu.baidu.com/usercenter/index/aischolar), 2021.
- SIGMOD Travel Award, 2019.
- Outstanding Graduate of Chongqing City, 2016.
- Outstanding Graduate of Chongqing University, 2016.

</main>
</div>
