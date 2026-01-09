---
layout: archive
title: "The Forensic Tennis Lab"
permalink: /lab/
author_profile: true
header:
  overlay_image: /assets/images/header-bg.jpg
  overlay_filter: 0.5
---

<div class="lab-container">

  <div class="lab-manifesto">
    <h2>The Gap Between "Feel" and Physics</h2>
    <p>I am a Materials Science student and competitive tennis player obsessed with one question: <em>What is actually happening when ball meets string?</em></p>

    <p>In engineering school, we are taught to approximate. In tennis, players claim to feel the nuance of a micron. My goal is to bridge this gap. I treat the tennis racket not just as a piece of equipment, but as a complex system of viscoelastic polymers and composite laminates that must manage energy transfer (hysteresis) and vibration damping (entropy).</p>

    <h3>My Core Mission</h3>
    <p>I seek the <strong>physical explanations for phenomenological experiences.</strong> Do the intangible sensations players describe (such as"pocketing," "crispness," and "plushness") hold up to scientific scrutiny? Are these experiences <strong>epistemologically true</strong>, rooted in material reality, or are they just cognitive biases born from marketing and hearsay?</p>
  </div>

  <div class="lab-sidebar">
    <h3>🔬 Recent Autopsies</h3>
    <ul>
      {% for post in site.posts limit:5 %}
        <li>
          <strong><a href="{{ post.url }}">{{ post.title }}</a></strong><br>
          <small style="color: #666;">{{ post.date | date: "%B %d, %Y" }}</small><br>
          <span style="font-size: 0.85em;">{{ post.excerpt | strip_html | truncatewords: 10 }}</span>
        </li>
      {% endfor %}
    </ul>
    <p style="text-align: center; margin-top: 20px;">
      <a href="/year-archive/" class="btn btn--inverse btn--small">View Full Archive</a>
    </p>
  </div>

</div>