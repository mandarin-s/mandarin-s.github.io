---
layout: default
title: The Lab
permalink: /lab/
---

<style>
  /* MAIN CONTAINER: Puts Content and Sidebar side-by-side */
  .lab-container {
    display: flex;
    flex-direction: row;
    gap: 40px; /* Space between columns */
    margin-top: 20px;
  }

  /* LEFT COLUMN: Your Bio & Intro */
  .main-content {
    flex: 2; /* Takes up 66% of width */
  }

  /* RIGHT COLUMN: The Sidebar */
  .sidebar-column {
    flex: 1; /* Takes up 33% of width */
    display: flex;
    flex-direction: column;
    gap: 20px; /* Space between widgets */
  }

  /* WIDGET BOX STYLING */
  .case-widget {
    background: #f8f9fa;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
  }

  /* "ACTIVE" WIDGET (Yellow Warning Look) */
  .active-cases {
    border-left: 5px solid #f1c40f; 
  }

  /* "CLOSED" WIDGET (Navy Archive Look) */
  .closed-cases {
    border-left: 5px solid #2c3e50;
  }

  /* TEXT STYLES */
  .widget-title {
    margin-top: 0;
    font-size: 1.1rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    display: flex;
    align-items: center;
    gap: 8px;
    color: #333;
  }

  .widget-subtitle {
    font-size: 0.85rem;
    color: #6c757d;
    margin-bottom: 15px;
    margin-top: 5px;
    font-style: italic;
  }

  /* LIST STYLES */
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
    border: none;
  }

  .case-list a {
    text-decoration: none;
    display: block;
    transition: all 0.2s ease;
  }

  .case-list a:hover {
    transform: translateX(3px); /* Subtle slide effect */
  }

  .case-id {
    display: block;
    font-size: 0.7rem;
    font-weight: 800;
    color: #adb5bd;
    letter-spacing: 1px;
  }

  .case-name {
    display: block;
    font-weight: 600;
    font-size: 0.95rem;
    color: #2c3e50;
    line-height: 1.3;
  }

  .case-name:hover {
    color: #007bff;
  }

  .case-date {
    font-size: 0.75rem;
    color: #999;
  }

  /* ARCHIVE BUTTON */
  .archive-btn {
    width: 100%;
    padding: 8px;
    background: #fff;
    border: 1px solid #ced4da;
    border-radius: 4px;
    color: #495057;
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
    text-align: center;
    transition: background 0.2s;
  }

  .archive-btn:hover {
    background: #e9ecef;
  }

  /* MOBILE RESPONSIVENESS */
  @media (max-width: 768px) {
    .lab-container {
      flex-direction: column; /* Stack vertically on phones */
    }
    .sidebar-column {
      order: 2; /* Put sidebar below content on mobile */
      margin-top: 30px;
    }
  }
</style>

<div class="lab-container">

  <div class="main-content">
    <h1>The Gap Between "Feel" and Physics</h1>
    
    <p>I am a Materials Science student and competitive tennis player obsessed with one question: <em>What is actually happening when ball meets string?</em></p>

    <p>In engineering school, we are taught to find heuristic solutions, maximizing for safe functionality. In tennis, players claim to feel the nuance of a micron. My goal is to bridge this gap.</p>

    <p>I treat the tennis racket not just as a piece of equipment, but as a complex system of viscoelastic polymers and composite laminates that must manage energy transfer (hysteresis) and vibration damping (entropy).</p>
    
    <p>This lab is my open notebook for forensic engineering investigations into sports technology.</p>
  </div>


  <div class="sidebar-column">

    <div class="case-widget active-cases">
      <h3 class="widget-title">
        <span>⚠️</span> Open Case Files
      </h3>
      <p class="widget-subtitle">Live dev logs & active investigations.</p>
      
      <ul class="case-list">
        
        <li>
          <a href="/projects/cor-part-1">
            <span class="case-id">CASE 002:</span>
            <span class="case-name">Project COR (Part 1): Building the Vision Pipeline</span>
            <span class="case-date">Jan 16, 2026</span>
          </a>
        </li>

        <li>
          <div style="opacity: 0.5; cursor: default;">
            <span class="case-id">CASE 002:</span>
            <span class="case-name">Part 2: Drop Tower Calibration (Pending)</span>
          </div>
        </li>

      </ul>
    </div>

    <div class="case-widget closed-cases">
      <h3 class="widget-title">
        <span>📁</span> Case Archive
      </h3>
      <p class="widget-subtitle">Final forensic reports.</p>
      
      <ul class="case-list">
        
        <li>
          <a href="/autopsies/head-auxetic">
            <span class="case-id">CASE 001:</span>
            <span class="case-name">Decoded: The Physics of HEAD's Auxetic Tech</span>
            <span class="case-date">Dec 12, 2025</span>
          </a>
        </li>
        
        <li style="margin-top: 15px; border: none;">
          <a href="/autopsies/archive" style="text-decoration: none;">
            <button class="archive-btn">View Full Evidence Locker</button>
          </a>
        </li>

      </ul>
    </div>

  </div> </div> ```