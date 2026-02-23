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
  /* --- LAYOUT OVERRIDES --- */
  /* Force the container to use maximum available space */
  .page__inner-wrap {
    max-width: 100% !important;
  }
  
  .lab-container {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
    margin-top: 20px;
  }

  /* --- LEFT COLUMN (MANIFESTO) --- */
  .lab-manifesto {
    flex: 3; 
    min-width: 300px;
  }

  /* --- RIGHT COLUMN (SIDEBAR CONTAINER) --- */
  .sidebar-column {
    flex: 1;
    min-width: 250px;
    display: flex;
    flex-direction: column;
    gap: 20px; /* Space between the two tabs */
  }

  /* --- WIDGET STYLING (THE TABS) --- */
  .case-widget {
    background-color: #f8f9fa;
    padding: 20px;
    border-radius: 8px;
    border: 1px solid #e9ecef;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
  }

  /* Widget 1: Active Cases (Yellow Warning Border) */
  .active-cases {
    border-left: 5px solid #f1c40f; 
  }

  /* Widget 2: Archive (Navy Folder Border) */
  .closed-cases {
    border-left: 5px solid #2c3e50; 
  }

  /* --- TEXT & LIST STYLES --- */
  .widget-title {
    margin-top: 0;
    font-size: 1.1em;
    font-weight: 700;
    border-bottom: 2px solid #e1e4e8;
    padding-bottom: 10px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .widget-subtitle {
    font-size: 0.85em;
    color: #6a737d;
    margin-bottom: 15px;
    font-style: italic;
    margin-top: -5px;
  }

  .case-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }

  .case-list li {
    margin-bottom: 12px;
    border-bottom: 1px solid #eee;
    padding-bottom: 8px;
  }
  
  .case-list li:last-child {
    border-bottom: none;
  }

  .case-list a {
    text-decoration: none;
    display: block;
  }

  /* Metadata Styling */
  .case-id {
    display: block;
    font-size: 0.7em;
    font-weight: 800;
    color: #adb5bd;
    letter-spacing: 1px;
    text-transform: uppercase;
  }

  .case-name {
    display: block;
    font-weight: 600;
    font-size: 0.95em;
    color: #0366d6;
    margin-top: 2px;
  }
  
  .case-name:hover {
    text-decoration: underline;
  }

  .case-date {
    font-size: 0.75em;
    color: #586069;
  }

  .archive-btn {
    width: 100%;
    padding: 8px;
    background: #fff;
    border: 1px solid #d1d5da;
    border-radius: 4px;
    color: #24292e;
    font-size: 0.85em;
    font-weight: 600;
    cursor: pointer;
    text-align: center;
  }
  
  .archive-btn:hover {
    background-color: #f3f4f6;
  }

  /* Mobile Responsive */
  @media (max-width: 768px) {
    .lab-container {
      flex-direction: column;
    }
  }
</style>

<div class="lab-container">

  <div class="lab-manifesto">
    <h2>Bridging the Gap Between "Feel" and Physics</h2>
    <p style="font-size: 1.1em; line-height: 1.6;">
      I am a Materials Science student and competitive tennis player obsessed with one simple question: <em>What is actually happening when ball meets string?</em>
    </p>

    <p>In engineering school, we are taught to solve problems using strict methodologies, maximizing for function and safety. On the tennis court, however, players evaluate equipment based on intangible sensations—claiming to feel the nuance of a micron in their strings or a slight shift in composite layup. I wanted to see if I could connect these two worlds.</p>
    
    <p>I built this site to take my biggest passion and subject it to the rigor of my classroom education. By treating the tennis racket as a complex system of viscoelastic polymers and composite laminates, I am learning how to translate subjective "feel" into quantifiable data like energy transfer (hysteresis) and vibration damping (entropy).</p>

    <div style="background: #eef6fc; padding: 20px; border-left: 5px solid #207de5; margin: 30px 0;">
      <h3 style="margin-top: 0;">My Core Mission</h3>
      <p style="margin-bottom: 0;">This lab is my open notebook. My goal is to formalize my curiosity into structured, research-driven investigations. I want to find the physical explanations for phenomenological experiences—testing whether the sensations players describe (like "pocketing" or "crispness") are rooted in measurable material reality. It is a space to learn, experiment, and document the physics behind the game I love.</p>
    </div>
  </div>

  <div class="sidebar-column">

    <div class="case-widget active-cases">
      <h3 class="widget-title"><span></span> Open Case Files</h3>
      <p class="widget-subtitle">Live dev logs & active investigations.</p>
      
      <ul class="case-list">
        {% assign open_cases = site.posts | where: "status", "open" %}
        
        {% for post in open_cases limit:3 %}
        <li>
          <a href="{{ post.url }}">
            <span class="case-id">CASE {{ post.case_id | default: "???" }}:</span>
            <span class="case-name">{{ post.title }}</span>
            <span class="case-date">{{ post.date | date: "%b %d, %Y" }}</span>
          </a>
        </li>
        {% else %}
        <li><span class="case-name" style="opacity:0.5;">No active investigations.</span></li>
        {% endfor %}
      </ul>
    </div>

    <div class="case-widget closed-cases">
      <h3 class="widget-title"><span></span> Case Archive</h3>
      <p class="widget-subtitle">Final forensic reports.</p>
      
      <ul class="case-list">
        {% assign closed_cases = site.posts | where: "status", "closed" %}
        
        {% for post in closed_cases limit:5 %}
        <li>
          <a href="{{ post.url }}">
            <span class="case-id">CASE {{ post.case_id | default: "000" }}:</span>
            <span class="case-name">{{ post.title }}</span>
            <span class="case-date">{{ post.date | date: "%b %d, %Y" }}</span>
          </a>
        </li>
        {% endfor %}
        
        <li style="border: none; margin-top: 10px;">
          <a href="/autopsies/archive"><button class="archive-btn">View Full Evidence Locker</button></a>
        </li>
      </ul>
    </div>

  </div>