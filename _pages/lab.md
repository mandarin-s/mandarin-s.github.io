---
layout: archive
title: "The Forensic Tennis Lab"
permalink: /lab/
author_profile: true
header:
  overlay_image: /assets/images/header-bg.jpg
  overlay_filter: 0.5
---

<style>
  .lab-container {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
  }
  .lab-manifesto {
    flex: 2; /* Takes 66% width */
    min-width: 300px;
  }
  .lab-sidebar {
    flex: 1; /* Takes 33% width */
    min-width: 250px;
    background-color: #f4f4f4;
    padding: 20px;
    border-radius: 8px;
    border-left: 5px solid #333;
    height: fit-content;
  }
  .lab-sidebar h3 {
    margin-top: 0;
    border-bottom: 1px solid #ccc;
    padding-bottom: 10px;
  }
  .lab-sidebar ul {
    padding-left: 20px;
  }
  .lab-sidebar li {
    margin-bottom: 10px;
  }
</style>

<div class="lab-container">

  <div class="lab-manifesto">
    <h2>The Gap Between "Feel" and Physics</h2>
    <p>I am a Materials Science student and competitive tennis player obsessed with one question: <em>What is actually happening when ball meets string?</em></p>

    <p>In engineering school, we are taught to approximate. In tennis, players claim to feel the nuance of a micron. My goal is to bridge this gap. I treat the tennis racket not just as a piece of equipment, but as a complex system of viscoelastic polymers and composite laminates that must manage energy transfer (hysteresis) and vibration damping (entropy).</p>

    <h3>My Core Mission</h3>
    <p>I seek the <strong>physical explanations for phenomenological experiences.</strong> Do the intangible sensations players describe—"pocketing," "crispness," "plushness"—hold up to scientific scrutiny? Are these experiences <strong>epistemologically true</strong>, rooted in material reality, or are they cognitive biases born from marketing?</p>
  </div>

  <div class="lab-sidebar">
    <h3>🔬 Recent Autopsies</h3>
    
    <ul>
      {% for post in site.posts limit:5 %}
        <li>
          <a href="{{ post.url }}"><strong>{{ post.title }}</strong></a>
          <br>
          <small>{{ post.date | date: "%B %d, %Y" }}</small>
        </li>
      {% endfor %}
    </ul>

    {% if site.posts.size == 0 %}
      <p style="color: red; font-size: 0.8em;">*No posts found. Check _config.yml for future: true*</p>
    {% endif %}

    <br>
    <a href="/year-archive/" class="btn btn--inverse btn--small" style="width: 100%; text-align: center;">View Full Archive</a>
  </div>

</div>