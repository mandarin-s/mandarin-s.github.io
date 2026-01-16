---
layout: default
title: The Lab
permalink: /lab/
---

<style>
  /* --- SECTION 1: HERO BANNER --- */
  .lab-hero {
    /* REPLACE 'banner.jpg' WITH YOUR ACTUAL IMAGE PATH */
    background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.6)), url('/assets/images/banner.jpg'); 
    background-size: cover;
    background-position: center;
    height: 250px;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    padding-left: 5%;
    border-radius: 8px; /* Optional rounded corners */
    margin-bottom: 30px;
    color: white;
  }

  .lab-hero h1 {
    font-size: 3rem;
    font-weight: 800;
    margin: 0;
    text-shadow: 0 2px 4px rgba(0,0,0,0.5);
  }

  /* --- SECTION 2: PROFILE BAR --- */
  .profile-section {
    display: flex;
    align-items: center;
    gap: 20px;
    margin-bottom: 40px;
    padding-bottom: 30px;
    border-bottom: 1px solid #eee;
  }

  .profile-avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    object-fit: cover;
    border: 1px solid #ddd;
  }

  .profile-info h2 {
    margin: 0 0 5px 0;
    font-size: 1.4rem;
    color: #111;
  }

  .profile-info p {
    margin: 0;
    color: #555;
    font-size: 0.95rem;
  }

  .follow-btn {
    margin-left: auto; /* Pushes button to far right */
    padding: 8px 16px;
    border: 1px solid #ccc;
    background: transparent;
    border-radius: 4px;
    cursor: pointer;
    font-weight: 600;
    color: #333;
  }

  /* --- SECTION 3: MAIN LAYOUT (Content + Sidebars) --- */
  .lab-container {
    display: flex;
    flex-direction: row;
    gap: 40px;
  }

  .main-content {
    flex: 2;
  }

  .sidebar-column {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  /* WIDGET STYLES */
  .case-widget {
    background: #f8f9fa;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    padding: 20px;
  }

  .active-cases { border-left: 5px solid #f1c40f; }
  .closed-cases { border-left: 5px solid #2c3e50; }

  .widget-title {
    margin-top: 0;
    font-size: 1.1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .widget-subtitle {
    font-size: 0.85rem;
    color: #6c757d;
    margin-bottom: 15px;
    font-style: italic;
  }

  .case-list { list-style: none; padding: 0; margin: 0; }
  .case-list li { margin-bottom: 12px; border-bottom: 1px solid #eee; padding-bottom: 8px; }
  .case-list li:last-child { border: none; }
  
  .case-list a { text-decoration: none; display: block; }
  .case-list a:hover { opacity: 0.8; }

  .case-id { display: block; font-size: 0.7rem; font-weight: 800; color: #adb5bd; letter-spacing: 1px; }
  .case-name { display: block; font-weight: 600; font-size: 0.95rem; color: #2c3e50; }
  .case-date { font-size: 0.75rem; color: #999; }

  .archive-btn {
    width: 100%; padding: 8px; background: #fff; border: 1px solid #ced4da;
    border-radius: 4px; color: #495057; font-weight: 600; cursor: pointer;
  }

  /* MOBILE RESPONSIVE */
  @media (max-width: 768px) {
    .lab-container { flex-direction: column; }
    .profile-section { flex-direction: column; text-align: center; }
    .follow-btn { margin: 10px auto 0 auto; }
  }
</style>


<div class="lab-hero">
  <h1>The Forensic Tennis Lab</h1>
</div>

<div class="profile-section">
  <img src="/assets/images/profile.jpg" alt="Mondrian Syafaat" class="profile-avatar">
  
  <div class="profile-info">
    <h2>Mondrian Syafaat</h2>
    <p>Materials Science & Engineering Student with Computational Emphasis @ UC Merced.</p>
  </div>

  <button class="follow-btn">Follow</button>
</div>


<div class="lab-container">

  <div class="main-content">
    <h2>The Gap Between "Feel" and Physics</h2>
    
    <p>I am a Materials Science student and competitive tennis player obsessed with one question: <em>What is actually happening when ball meets string?</em></p>

    <p>In engineering school, we are taught to find heuristic solutions, maximizing for safe functionality. In tennis, players claim to feel the nuance of a micron. My goal is to bridge this gap.</p>

    <p>I treat the tennis racket not just as a piece of equipment, but as a complex system of viscoelastic polymers and composite laminates that must manage energy transfer (hysteresis) and vibration damping (entropy).</p>
    
    <p>This lab is my open notebook for forensic engineering investigations into sports technology.</p>
  </div>


  <div class="sidebar-column">

    <div class="case-widget active-cases">
      <h3 class="widget-title"><span>⚠️</span> Open Case Files</h3>
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
          <div style="opacity: 0.5;">
            <span class="case-id">CASE 002:</span>
            <span class="case-name">Part 2: Drop Tower Calibration (Pending)</span>
          </div>
        </li>
      </ul>
    </div>

    <div class="case-widget closed-cases">
      <h3 class="widget-title"><span>📁</span> Case Archive</h3>
      <p class="widget-subtitle">Final forensic reports.</p>
      
      <ul class="case-list">
        <li>
          <a href="/autopsies/head-auxetic">
            <span class="case-id">CASE 001:</span>
            <span class="case-name">Decoded: The Physics of HEAD's Auxetic Tech</span>
            <span class="case-date">Dec 12, 2025</span>
          </a>
        </li>
        <li style="border: none; margin-top: 10px;">
          <a href="/autopsies/archive"><button class="archive-btn">View Full Evidence Locker</button></a>
        </li>
      </ul>
    </div>

  </div> </div> ```

### Important Next Steps
1.  **Fix the Banner Image:** Look for `url('/assets/images/banner.jpg')` in the CSS section. Change `/assets/images/banner.jpg` to the actual path of your racket image (the one with the dark background).
2.  **Fix the Avatar:** Look for `<img src="/assets/images/profile.jpg"...` in the HTML section. Change that path to your profile picture location.