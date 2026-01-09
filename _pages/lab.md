---
layout: archive
title: "The Forensic Tennis Lab"
permalink: /lab/
author_profile: true
header:
  overlay_image: /assets/images/header-bg.jpg
  overlay_filter: 0.5
classes: wide
---

<style>
  /* Force the container to use maximum available space */
  .page__inner-wrap {
    max-width: 100% !important; /* Overrides the theme's narrow limit */
  }
  
  .lab-container {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
    margin-top: 20px;
  }

  .lab-manifesto {
    flex: 3; /* CHANGED: Now takes 75% of the width */
    min-width: 300px; /* Prevents it from getting too skinny on phones */
  }

  .lab-sidebar {
    flex: 1; /* Takes 25% of the width */
    min-width: 250px;
    background-color: #f8f9fa;
    padding: 25px;
    border-radius: 8px;
    border-left: 5px solid #24292e; /* Darker accent line */
    height: fit-content;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05); /* Subtle shadow for depth */
  }

  .lab-sidebar h3 {
    margin-top: 0;
    font-size: 1.1em;
    border-bottom: 2px solid #e1e4e8;
    padding-bottom: 15px;
    margin-bottom: 15px;
  }

  .lab-sidebar ul {
    list-style: none; /* Removes bullet points for a cleaner look */
    padding: 0;
    margin: 0;
  }

  .lab-sidebar li {
    margin-bottom: 15px;
    border-bottom: 1px solid #eee; /* Light separator lines */
    padding-bottom: 10px;
  }
  
  .lab-sidebar li:last-child {
    border-bottom: none;
  }

  .lab-sidebar a {
    text-decoration: none;
    font-weight: 600;
    color: #0366d6;
  }
  
  .lab-sidebar a:hover {
    text-decoration: underline;
  }
</style>

<div class="lab-container">

  <div class="lab-manifesto">
    <h2>The Gap Between "Feel" and Physics</h2>
    <p style="font-size: 1.1em; line-height: 1.6;">
      I am a Materials Science student and competitive tennis player obsessed with one question: <em>What is actually happening when ball meets string?</em>
    </p>

    <p>In engineering school, we are taught to find heuristic solutions, maximizing for safe functionality. In tennis, players claim to feel the nuance of a micron (though sometimes they are just looking for excuses). My goal is to bridge this gap. I treat the tennis racket not just as a piece of equipment, but as a complex system of viscoelastic polymers and composite laminates that must manage energy transfer (hysteresis) and vibration damping (entropy).</p>

    <div style="background: #eef6fc; padding: 20px; border-left: 5px solid #207de5; margin: 30px 0;">
      <h3 style="margin-top: 0;">My Core Mission</h3>
      <p style="margin-bottom: 0;">I seek the <strong>physical explanations for phenomenological experiences.</strong> Do the intangible sensations players describe (such as "pocketing," "crispness," and "plushness") actually hold up to scientific scrutiny? Are these experiences <strong>epistemologically true</strong>, rooted in material reality, or are they cognitive biases born from marketing and hearsay?</p>
    </div>
  </div>

  <div class="lab-sidebar">
    <h3>🔬 Recent Autopsies</h3>
    <ul>
      {% for post in site.posts limit:5 %}
        <li>
          <a href="{{ post.url }}">{{ post.title }}</a><br>
          <small style="color: #6a737d;">{{ post.date | date: "%B %d, %Y" }}</small>
        </li>
      {% endfor %}
    </ul>
    
    {% if site.posts.size == 0 %}
      <p style="color: red; font-size: 0.8em;">*No posts found.*</p>
    {% endif %}

    <div style="margin-top: 20px; text-align: center;">
      <a href="/year-archive/" class="btn btn--inverse btn--small" style="width: 100%;">View Full Archive</a>
    </div>
  </div>

</div>