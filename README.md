
Name: Oscar Short tagline: System Engineering • Infrastructure • Automation • Software Quality Introduction: Interested in system-level engineering, infrastructure support, automation, and software quality assurance, with a strong focus on understanding how applications interact with operating systems, runtime environments, and underlying system resources. Passionate about building reliable software systems and exploring the technologies that power modern applications behind the scenes. Particularly interested in operating systems, networking, computer vision, artificial intelligence, automation, software architecture, and performance optimization. Driven by curiosity to understand not only how software is built, but also how it executes, communicates, scales, and behaves in real-world environments. Personality:

Curious about how things work under the hood
Enjoys pushing systems to their limits
Likes understanding the "why" behind technologies
Enjoys experimenting, learning, and optimizing
Interested in reliability, performance, and real-world problem solving Areas of Interest:
System Engineering
Operating Systems
Infrastructure
Automation
Software Quality Assurance
Computer Vision
Artificial Intelligence
Networking
Software Architecture
Performance Optimization
Observability
Runtime Environments Technology Stack: Languages:
Python
Java
JavaScript
PHP
SQL Web Technologies:
HTML
CSS
JavaScript Computer Vision & AI:
OpenCV
YOLO Database:
MySQL Tools:
Git
GitHub
VS Code Current Learning Areas:
Software Architecture
Operating Systems
Computer Vision Systems
Infrastructure Engineering
System Design
Performance Optimization
Artificial Intelligence Projects: Orbit A safety-focused communication and coordination platform designed to improve emergency response and location awareness. Key concepts:
Real-time communication
Location sharing
Interactive mapping
Emergency workflows
Reliability during critical situations Sentinel A computer vision and automation platform focused on real-time visual processing and intelligent automation. Key concepts:
Object detection
Computer vision
Automation workflows
Real-time processing
OpenCV
YOLO Development Philosophy:
Understand how systems work beneath the surface.
Build reliable software before optimizing it.
Learn by building, experimenting, and improving.
Focus on maintainability, performance, and reliability.
Curiosity is the foundation of growth. Fun Facts:
Curious about low-level system behavior
Enjoys exploring how applications interact with the operating system
Likes performance tuning and optimization
Interested in both software development and software quality
Constantly learning new technologies Closing Line: "Curious about how things work beneath the surface." make aniamtion to these things and use svg for where its needed like if tehcilogies is mentioned and dont use emoji use svg instead
Show more
9:27 PM

Viewed a file, created a file
Viewed a file, created a file

Reading frontend design skill

Animated personal portfolio/profile page for Oscar with SVG tech icons, animations, and no emojis
oscar_profile.html
Done

You are out of free messages until 2:20 AM
Keep working




Claude is AI and can make mistakes. Please double-check responses.


raw
Oscar profile · HTML
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Oscar — System Engineering</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #080c10;
    --surface: #0d1520;
    --border: #1a2535;
    --accent: #00d4ff;
    --accent2: #00ff9d;
    --accent3: #ff6b35;
    --text: #e8f0fe;
    --muted: #4a5568;
    --glow: rgba(0, 212, 255, 0.15);
  }
 
  * { margin: 0; padding: 0; box-sizing: border-box; }
 
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    overflow-x: hidden;
    cursor: none;
  }
 
  /* Custom cursor */
  .cursor {
    width: 8px; height: 8px;
    background: var(--accent);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9999;
    transition: transform 0.1s;
    mix-blend-mode: screen;
  }
  .cursor-ring {
    width: 32px; height: 32px;
    border: 1px solid rgba(0,212,255,0.4);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9998;
    transition: transform 0.15s, width 0.2s, height 0.2s;
    transform: translate(-50%, -50%);
  }
 
  /* Grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 48px 48px;
    pointer-events: none;
    z-index: 0;
  }
 
  /* Noise overlay */
  body::after {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
    opacity: 0.5;
  }
 
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 2rem;
    position: relative;
    z-index: 1;
  }
 
  /* ─── HERO ─── */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    position: relative;
    padding: 6rem 0 4rem;
  }
 
  .hero-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4rem;
    align-items: center;
  }
 
  .hero-label {
    font-size: 0.65rem;
    letter-spacing: 0.3em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 1.5rem;
    opacity: 0;
    animation: fadeUp 0.8s 0.2s forwards;
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }
  .hero-label::before {
    content: '';
    width: 32px; height: 1px;
    background: var(--accent);
    display: inline-block;
  }
 
  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(3.5rem, 7vw, 6rem);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -0.03em;
    opacity: 0;
    animation: fadeUp 0.8s 0.4s forwards;
  }
 
  .hero-name span {
    display: block;
    color: transparent;
    -webkit-text-stroke: 1px rgba(0,212,255,0.4);
  }
 
  .tagline {
    margin-top: 2rem;
    font-size: 0.7rem;
    letter-spacing: 0.15em;
    color: var(--muted);
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 0.8s 0.6s forwards;
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
  .tagline-item {
    padding: 0.3rem 0.7rem;
    border: 1px solid var(--border);
    color: var(--text);
    font-size: 0.6rem;
    letter-spacing: 0.12em;
    transition: border-color 0.3s, color 0.3s;
  }
  .tagline-item:hover {
    border-color: var(--accent);
    color: var(--accent);
  }
 
  .hero-intro {
    font-size: 0.82rem;
    line-height: 1.9;
    color: rgba(232,240,254,0.65);
    opacity: 0;
    animation: fadeUp 0.8s 0.8s forwards;
  }
 
  .hero-visual {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    animation: fadeIn 1.2s 0.6s forwards;
  }
 
  /* Orbiting rings */
  .orbit-container {
    position: relative;
    width: 340px;
    height: 340px;
  }
 
  .orbit-core {
    position: absolute;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    width: 80px; height: 80px;
    background: radial-gradient(circle, rgba(0,212,255,0.2), transparent 70%);
    border: 1px solid rgba(0,212,255,0.5);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .orbit-core::before {
    content: '';
    position: absolute;
    inset: -20px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(0,212,255,0.08), transparent 70%);
    animation: pulse 2s ease-in-out infinite;
  }
 
  .orbit-ring {
    position: absolute;
    top: 50%; left: 50%;
    border-radius: 50%;
    border: 1px dashed rgba(0,212,255,0.15);
    transform-origin: 50% 50%;
  }
  .orbit-ring-1 {
    width: 160px; height: 160px;
    margin: -80px 0 0 -80px;
    animation: spin 12s linear infinite;
  }
  .orbit-ring-2 {
    width: 240px; height: 240px;
    margin: -120px 0 0 -120px;
    animation: spin 20s linear infinite reverse;
    border-style: solid;
    border-color: rgba(0,255,157,0.1);
  }
  .orbit-ring-3 {
    width: 320px; height: 320px;
    margin: -160px 0 0 -160px;
    animation: spin 30s linear infinite;
    border-style: dashed;
    border-color: rgba(255,107,53,0.08);
  }
 
  .orbit-dot {
    position: absolute;
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--accent);
    top: -4px; left: 50%;
    margin-left: -4px;
    box-shadow: 0 0 8px var(--accent);
  }
  .orbit-dot-2 {
    background: var(--accent2);
    box-shadow: 0 0 8px var(--accent2);
    top: auto; bottom: -4px;
    left: 50%; margin-left: -4px;
  }
  .orbit-dot-3 {
    background: var(--accent3);
    box-shadow: 0 0 8px var(--accent3);
    left: auto; right: -4px;
    top: 50%; margin-top: -4px;
  }
 
  /* ─── SECTION COMMON ─── */
  section {
    padding: 6rem 0;
    border-top: 1px solid var(--border);
  }
 
  .section-header {
    display: flex;
    align-items: baseline;
    gap: 1.5rem;
    margin-bottom: 3rem;
  }
 
  .section-num {
    font-size: 0.6rem;
    color: var(--accent);
    letter-spacing: 0.2em;
  }
 
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 1.8rem;
    font-weight: 800;
    letter-spacing: -0.02em;
  }
 
  .section-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }
 
  /* ─── AREAS OF INTEREST ─── */
  .interests-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
  }
 
  .interest-item {
    background: var(--bg);
    padding: 1.5rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    transition: background 0.3s;
    position: relative;
    overflow: hidden;
  }
  .interest-item::after {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, var(--glow), transparent);
    opacity: 0;
    transition: opacity 0.3s;
  }
  .interest-item:hover {
    background: var(--surface);
  }
  .interest-item:hover::after { opacity: 1; }
 
  .interest-icon {
    flex-shrink: 0;
    width: 32px; height: 32px;
    color: var(--accent);
  }
 
  .interest-name {
    font-size: 0.72rem;
    letter-spacing: 0.05em;
    color: var(--text);
  }
 
  /* ─── TECH STACK ─── */
  .tech-section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
  }
 
  .tech-group {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 1.5rem;
    position: relative;
    overflow: hidden;
  }
  .tech-group::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), transparent);
  }
 
  .tech-group-label {
    font-size: 0.55rem;
    letter-spacing: 0.3em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 1.25rem;
  }
 
  .tech-icons {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
  }
 
  .tech-badge {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.4rem 0.75rem;
    border: 1px solid var(--border);
    font-size: 0.65rem;
    letter-spacing: 0.05em;
    color: rgba(232,240,254,0.7);
    transition: border-color 0.3s, color 0.3s, transform 0.2s;
    background: var(--bg);
  }
  .tech-badge:hover {
    border-color: var(--accent);
    color: var(--accent);
    transform: translateY(-2px);
  }
  .tech-badge svg {
    width: 16px; height: 16px;
    flex-shrink: 0;
  }
 
  /* ─── PROJECTS ─── */
  .projects-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    background: var(--border);
  }
 
  .project-card {
    background: var(--bg);
    padding: 2.5rem;
    position: relative;
    overflow: hidden;
    transition: background 0.3s;
  }
  .project-card:hover { background: var(--surface); }
 
  .project-card::before {
    content: '';
    position: absolute;
    bottom: 0; right: 0;
    width: 200px; height: 200px;
    background: radial-gradient(circle, var(--glow), transparent 70%);
    opacity: 0;
    transition: opacity 0.5s;
  }
  .project-card:hover::before { opacity: 1; }
 
  .project-num {
    font-size: 0.55rem;
    letter-spacing: 0.3em;
    color: var(--muted);
    margin-bottom: 1.5rem;
  }
 
  .project-name {
    font-family: 'Syne', sans-serif;
    font-size: 2rem;
    font-weight: 800;
    letter-spacing: -0.03em;
    margin-bottom: 1rem;
    line-height: 1;
  }
 
  .project-name.orbit { color: var(--accent); }
  .project-name.sentinel { color: var(--accent2); }
 
  .project-desc {
    font-size: 0.75rem;
    line-height: 1.8;
    color: rgba(232,240,254,0.55);
    margin-bottom: 1.5rem;
  }
 
  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }
 
  .project-tag {
    font-size: 0.6rem;
    letter-spacing: 0.1em;
    padding: 0.25rem 0.6rem;
    border: 1px solid var(--border);
    color: var(--muted);
    text-transform: uppercase;
  }
 
  /* ─── PHILOSOPHY ─── */
  .philosophy-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 1.5rem;
  }
 
  .philosophy-item {
    padding: 1.5rem;
    border-left: 2px solid var(--border);
    transition: border-color 0.3s;
    position: relative;
  }
  .philosophy-item:hover {
    border-color: var(--accent2);
  }
 
  .philosophy-num {
    font-size: 0.55rem;
    color: var(--muted);
    letter-spacing: 0.2em;
    margin-bottom: 0.75rem;
  }
 
  .philosophy-text {
    font-size: 0.78rem;
    line-height: 1.7;
    color: rgba(232,240,254,0.7);
  }
 
  /* ─── PERSONALITY ─── */
  .personality-flow {
    display: flex;
    flex-wrap: wrap;
    gap: 1.5rem;
  }
 
  .personality-chip {
    display: flex;
    align-items: center;
    gap: 0.75rem;
    padding: 0.75rem 1.25rem;
    background: var(--surface);
    border: 1px solid var(--border);
    font-size: 0.72rem;
    letter-spacing: 0.05em;
    transition: border-color 0.3s, transform 0.3s;
    position: relative;
    overflow: hidden;
  }
  .personality-chip::after {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 2px;
    background: var(--accent2);
    transform: scaleY(0);
    transition: transform 0.3s;
  }
  .personality-chip:hover {
    border-color: var(--accent2);
    transform: translateX(4px);
  }
  .personality-chip:hover::after { transform: scaleY(1); }
 
  /* ─── CLOSING ─── */
  .closing {
    padding: 8rem 0;
    text-align: center;
    border-top: 1px solid var(--border);
  }
 
  .closing-quote {
    font-family: 'Syne', sans-serif;
    font-size: clamp(1.5rem, 4vw, 2.5rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    color: transparent;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: shimmer 4s ease-in-out infinite;
  }
 
  .closing-line {
    display: inline-block;
    width: 1px;
    height: 60px;
    background: linear-gradient(180deg, var(--accent), transparent);
    margin-top: 2rem;
    animation: fadeIn 1s 0.5s both;
  }
 
  /* ─── SCROLL ANIMATIONS ─── */
  .reveal {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.8s, transform 0.8s;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }
 
  /* ─── KEYFRAMES ─── */
  @keyframes fadeUp {
    to { opacity: 1; transform: translateY(0); }
    from { opacity: 0; transform: translateY(20px); }
  }
  @keyframes fadeIn {
    to { opacity: 1; }
    from { opacity: 0; }
  }
  @keyframes spin {
    to { transform: rotate(360deg); }
  }
  @keyframes pulse {
    0%, 100% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.3); opacity: 0.3; }
  }
  @keyframes shimmer {
    0%, 100% { filter: hue-rotate(0deg); }
    50% { filter: hue-rotate(30deg); }
  }
  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }
 
  .cursor-blink {
    display: inline-block;
    width: 2px; height: 1em;
    background: var(--accent);
    margin-left: 4px;
    vertical-align: text-bottom;
    animation: blink 1s step-end infinite;
  }
 
  /* Progress bar */
  .progress-bar {
    position: fixed;
    top: 0; left: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--accent2));
    z-index: 1000;
    transition: width 0.1s;
  }
 
  /* Nav */
  .nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.25rem 2rem;
    background: rgba(8,12,16,0.8);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid rgba(26,37,53,0.5);
  }
 
  .nav-logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 1rem;
    letter-spacing: 0.05em;
    color: var(--accent);
  }
 
  .nav-links {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
 
  .nav-links a {
    font-size: 0.6rem;
    letter-spacing: 0.2em;
    text-decoration: none;
    color: var(--muted);
    text-transform: uppercase;
    transition: color 0.3s;
  }
  .nav-links a:hover { color: var(--accent); }
 
  /* Stagger reveal delay helpers */
  .stagger-1 { transition-delay: 0.1s; }
  .stagger-2 { transition-delay: 0.2s; }
  .stagger-3 { transition-delay: 0.3s; }
  .stagger-4 { transition-delay: 0.4s; }
  .stagger-5 { transition-delay: 0.5s; }
</style>
</head>
<body>
 
<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursor-ring"></div>
<div class="progress-bar" id="progress"></div>
 
<nav class="nav">
  <div class="nav-logo">OSCAR</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#stack">Stack</a></li>
    <li><a href="#projects">Projects</a></li>
    <li><a href="#philosophy">Philosophy</a></li>
  </ul>
</nav>
 
<main>
 
  <!-- HERO -->
  <div class="hero" id="about">
    <div class="container">
      <div class="hero-grid">
        <div>
          <div class="hero-label">System Engineer</div>
          <h1 class="hero-name">
            Oscar
            <span>Systems<br>Thinker</span>
          </h1>
          <div class="tagline">
            <span class="tagline-item">System Engineering</span>
            <span class="tagline-item">Infrastructure</span>
            <span class="tagline-item">Automation</span>
            <span class="tagline-item">Software Quality</span>
          </div>
          <p class="hero-intro" style="margin-top:2rem;">
            Interested in system-level engineering, infrastructure support, automation, and software quality assurance — with a strong focus on understanding how applications interact with operating systems, runtime environments, and underlying system resources.<span class="cursor-blink"></span>
          </p>
        </div>
        <div class="hero-visual">
          <div class="orbit-container">
            <!-- Core -->
            <div class="orbit-core">
              <svg width="36" height="36" viewBox="0 0 36 36" fill="none">
                <circle cx="18" cy="18" r="8" stroke="#00d4ff" stroke-width="1"/>
                <circle cx="18" cy="18" r="3" fill="#00d4ff"/>
                <path d="M18 6 L18 12 M18 24 L18 30 M6 18 L12 18 M24 18 L30 18" stroke="#00d4ff" stroke-width="0.8" opacity="0.5"/>
              </svg>
            </div>
            <!-- Rings -->
            <div class="orbit-ring orbit-ring-1">
              <div class="orbit-dot"></div>
            </div>
            <div class="orbit-ring orbit-ring-2">
              <div class="orbit-dot orbit-dot-2"></div>
            </div>
            <div class="orbit-ring orbit-ring-3">
              <div class="orbit-dot orbit-dot-3"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
 
  <!-- AREAS OF INTEREST -->
  <section>
    <div class="container">
      <div class="section-header reveal">
        <span class="section-num">01</span>
        <h2 class="section-title">Areas of Interest</h2>
        <div class="section-line"></div>
      </div>
      <div class="interests-grid">
        <!-- System Engineering -->
        <div class="interest-item reveal stagger-1">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <rect x="4" y="8" width="24" height="16" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <path d="M4 12h24" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="7" cy="10" r="1" fill="currentColor"/>
            <circle cx="10" cy="10" r="1" fill="currentColor"/>
            <circle cx="13" cy="10" r="1" fill="currentColor"/>
            <path d="M8 17h6M8 20h4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
          </svg>
          <span class="interest-name">System Engineering</span>
        </div>
        <!-- Operating Systems -->
        <div class="interest-item reveal stagger-2">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <circle cx="16" cy="16" r="10" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="16" cy="16" r="4" stroke="currentColor" stroke-width="1.5"/>
            <path d="M16 6v4M16 22v4M6 16h4M22 16h4" stroke="currentColor" stroke-width="1.5"/>
          </svg>
          <span class="interest-name">Operating Systems</span>
        </div>
        <!-- Infrastructure -->
        <div class="interest-item reveal stagger-3">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <rect x="6" y="6" width="20" height="6" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <rect x="6" y="14" width="20" height="6" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <rect x="6" y="22" width="20" height="4" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="23" cy="9" r="1" fill="currentColor"/>
            <circle cx="23" cy="17" r="1" fill="currentColor"/>
          </svg>
          <span class="interest-name">Infrastructure</span>
        </div>
        <!-- Automation -->
        <div class="interest-item reveal stagger-4">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <path d="M12 8l-4 8h8l-4 8" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <circle cx="22" cy="12" r="4" stroke="currentColor" stroke-width="1.5"/>
            <path d="M22 10v4M20 12h4" stroke="currentColor" stroke-width="1" stroke-linecap="round"/>
          </svg>
          <span class="interest-name">Automation</span>
        </div>
        <!-- Software Quality -->
        <div class="interest-item reveal stagger-1">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <path d="M16 4l3 7 7.5 1.1-5.4 5.3 1.3 7.5L16 21.5l-6.4 3.4 1.3-7.5-5.4-5.3 7.5-1.1z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/>
          </svg>
          <span class="interest-name">Software Quality</span>
        </div>
        <!-- Computer Vision -->
        <div class="interest-item reveal stagger-2">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <ellipse cx="16" cy="16" rx="12" ry="7" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="16" cy="16" r="4" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="16" cy="16" r="1.5" fill="currentColor"/>
          </svg>
          <span class="interest-name">Computer Vision</span>
        </div>
        <!-- AI -->
        <div class="interest-item reveal stagger-3">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <rect x="10" y="8" width="12" height="12" rx="2" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="13" cy="14" r="1" fill="currentColor"/>
            <circle cx="19" cy="14" r="1" fill="currentColor"/>
            <path d="M13 17.5c0 1.7 6 1.7 6 0" stroke="currentColor" stroke-width="1.2" stroke-linecap="round"/>
            <path d="M13 8V6M19 8V6M8 13H6M26 13h-2M8 19H6M26 19h-2M13 24v2M19 24v2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
          </svg>
          <span class="interest-name">Artificial Intelligence</span>
        </div>
        <!-- Networking -->
        <div class="interest-item reveal stagger-4">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <circle cx="8" cy="16" r="3" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="24" cy="8" r="3" stroke="currentColor" stroke-width="1.5"/>
            <circle cx="24" cy="24" r="3" stroke="currentColor" stroke-width="1.5"/>
            <path d="M11 16l10-6M11 16l10 6" stroke="currentColor" stroke-width="1.5"/>
          </svg>
          <span class="interest-name">Networking</span>
        </div>
        <!-- Software Architecture -->
        <div class="interest-item reveal stagger-1">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <rect x="5" y="5" width="8" height="8" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <rect x="19" y="5" width="8" height="8" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <rect x="12" y="19" width="8" height="8" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <path d="M9 13v3h14v-3M16 13v6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
          </svg>
          <span class="interest-name">Software Architecture</span>
        </div>
        <!-- Performance -->
        <div class="interest-item reveal stagger-2">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <path d="M6 26L12 16l5 6 4-10 5 10" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M6 26h20" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
          </svg>
          <span class="interest-name">Performance Optimization</span>
        </div>
        <!-- Observability -->
        <div class="interest-item reveal stagger-3">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <rect x="5" y="10" width="22" height="14" rx="1" stroke="currentColor" stroke-width="1.5"/>
            <path d="M9 22v-4l3 2 3-5 3 3 3-6v6" stroke="currentColor" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M13 8h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
          </svg>
          <span class="interest-name">Observability</span>
        </div>
        <!-- Runtime Environments -->
        <div class="interest-item reveal stagger-4">
          <svg class="interest-icon" viewBox="0 0 32 32" fill="none">
            <path d="M8 10l8-4 8 4v8l-8 4-8-4v-8z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/>
            <path d="M8 10l8 4 8-4M16 14v8" stroke="currentColor" stroke-width="1.5"/>
          </svg>
          <span class="interest-name">Runtime Environments</span>
        </div>
      </div>
    </div>
  </section>
 
  <!-- TECH STACK -->
  <section id="stack">
    <div class="container">
      <div class="section-header reveal">
        <span class="section-num">02</span>
        <h2 class="section-title">Technology Stack</h2>
        <div class="section-line"></div>
      </div>
      <div class="tech-section">
 
        <!-- Languages -->
        <div class="tech-group reveal stagger-1">
          <div class="tech-group-label">Languages</div>
          <div class="tech-icons">
 
            <!-- Python -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M11.97 0C5.813 0 6.2 2.656 6.2 2.656l.007 2.752h5.87v.826H3.887S0 5.789 0 12.003c0 6.213 3.437 5.99 3.437 5.99h2.051v-2.883s-.11-3.437 3.382-3.437h5.822s3.269.052 3.269-3.157V3.259S18.478 0 11.97 0zm-3.24 1.88a1.049 1.049 0 1 1 0 2.097 1.049 1.049 0 0 1 0-2.097z"/>
                <path d="M12.03 24c6.157 0 5.77-2.657 5.77-2.657l-.007-2.751h-5.87v-.826h8.19S24 18.211 24 11.997c0-6.213-3.437-5.99-3.437-5.99h-2.051v2.883s.11 3.437-3.382 3.437H9.308S6.04 12.274 6.04 15.483v5.257S5.522 24 12.029 24zm3.24-1.88a1.049 1.049 0 1 1 0-2.097 1.049 1.049 0 0 1 0 2.097z"/>
              </svg>
              Python
            </div>
 
            <!-- Java -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M8.851 18.56s-.917.534.653.714c1.902.218 2.874.187 4.969-.211 0 0 .552.346 1.321.646-4.699 2.013-10.633-.118-6.943-1.149M8.276 15.933s-1.028.761.542.924c2.032.209 3.636.227 6.413-.308 0 0 .384.389.987.602-5.679 1.661-12.007.13-7.942-1.218M13.116 11.475c1.158 1.333-.304 2.533-.304 2.533s2.939-1.518 1.589-3.418c-1.261-1.772-2.228-2.652 3.007-5.688 0 0-8.216 2.051-4.292 6.573M19.33 20.504s.679.559-.747.991c-2.712.822-11.288 1.069-13.669.033-.856-.373.749-.89 1.254-.998.527-.114.828-.093.828-.093-.953-.671-6.156 1.317-2.643 1.887 9.58 1.553 17.462-.7 14.977-1.82M9.292 13.21s-4.362 1.036-1.544 1.412c1.189.159 3.561.123 5.77-.062 1.806-.152 3.618-.477 3.618-.477s-.637.272-1.098.587c-4.429 1.165-12.986.623-10.522-.568 2.082-1.006 3.776-.892 3.776-.892M17.116 17.584c4.503-2.34 2.421-4.589.968-4.285-.355.074-.515.138-.515.138s.132-.207.385-.297c2.875-1.011 5.086 2.981-.928 4.562 0 0 .07-.062.09-.118"/>
              </svg>
              Java
            </div>
 
            <!-- JavaScript -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M0 0h24v24H0V0zm22.034 18.276c-.175-1.095-.888-2.015-3.003-2.873-.736-.345-1.554-.585-1.797-1.14-.091-.33-.105-.51-.046-.705.15-.646.915-.84 1.515-.66.39.12.75.42.976.9 1.034-.676 1.034-.676 1.755-1.125-.27-.42-.404-.601-.586-.78-.63-.705-1.469-1.065-2.834-1.034l-.705.089c-.676.165-1.32.525-1.71 1.005-1.14 1.291-.811 3.541.569 4.471 1.365 1.02 3.361 1.244 3.616 2.205.24 1.17-.87 1.545-1.966 1.41-.811-.18-1.26-.586-1.755-1.336l-1.83 1.051c.21.48.45.689.81 1.109 1.74 1.756 6.09 1.666 6.871-1.004.029-.09.24-.705.074-1.65l.046.067zm-8.983-7.245h-2.248c0 1.938-.009 3.864-.009 5.805 0 1.232.063 2.363-.138 2.711-.33.689-1.18.601-1.566.48-.396-.196-.597-.466-.83-.855-.063-.105-.11-.196-.127-.196l-1.825 1.125c.305.63.75 1.172 1.324 1.517.855.51 2.004.675 3.207.405.783-.226 1.458-.691 1.811-1.411.51-.93.402-2.07.397-3.346.012-2.054 0-4.109 0-6.179l.004-.056z"/>
              </svg>
              JavaScript
            </div>
 
            <!-- PHP -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm0 2c5.514 0 10 4.486 10 10s-4.486 10-10 10S2 17.514 2 12 6.486 2 12 2zm-1.717 4.764H8.059L6.53 14.534h2.226l.417-2.116h1.977c2.227 0 3.445-1.157 3.698-2.974.229-1.64-.698-2.68-2.565-2.68zm.2 1.79c.792 0 1.19.383 1.056 1.39-.126.928-.673 1.459-1.48 1.459H8.95l.474-2.849h1.059zm7.36-1.79h-2.224l-1.529 7.77h2.224l.419-2.116h1.977c2.225 0 3.445-1.157 3.697-2.974.229-1.64-.698-2.68-2.565-2.68zm.2 1.79c.793 0 1.192.383 1.056 1.39-.126.928-.673 1.459-1.48 1.459h-1.058l.474-2.849h1.008z"/>
              </svg>
              PHP
            </div>
 
            <!-- SQL -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <ellipse cx="12" cy="7" rx="8" ry="3"/>
                <path d="M4 7v5c0 1.657 3.582 3 8 3s8-1.343 8-3V7"/>
                <path d="M4 12v5c0 1.657 3.582 3 8 3s8-1.343 8-3v-5"/>
              </svg>
              SQL
            </div>
          </div>
        </div>
 
        <!-- Web & CV/AI -->
        <div class="tech-group reveal stagger-2">
          <div class="tech-group-label">Web &amp; Computer Vision</div>
          <div class="tech-icons">
 
            <!-- HTML -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M1.5 0h21l-1.91 21.563L11.977 24l-8.565-2.438L1.5 0zm7.031 9.75l-.232-2.718 10.059.003.23-2.622L5.412 4.41l.698 8.01h9.126l-.326 3.426-2.91.804-2.955-.81-.188-2.11H6.248l.33 4.171L12 19.351l5.379-1.443.744-8.157H8.531z"/>
              </svg>
              HTML
            </div>
 
            <!-- CSS -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M1.5 0h21l-1.91 21.563L11.977 24l-8.564-2.438L1.5 0zm17.09 4.413L5.41 4.41l.213 2.622 10.125.002-.255 2.716h-6.64l.24 2.573h6.182l-.366 3.523-2.91.804-2.956-.81-.188-2.11h-2.61l.29 3.855L12 19.288l5.373-1.53L18.59 4.414z"/>
              </svg>
              CSS
            </div>
 
            <!-- OpenCV -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="none">
                <circle cx="12" cy="12" r="3" stroke="currentColor" stroke-width="1.5"/>
                <circle cx="5" cy="7" r="3" stroke="currentColor" stroke-width="1.5" fill="none"/>
                <circle cx="19" cy="7" r="3" stroke="currentColor" stroke-width="1.5" fill="none"/>
                <circle cx="12" cy="19" r="3" stroke="currentColor" stroke-width="1.5" fill="none"/>
              </svg>
              OpenCV
            </div>
 
            <!-- YOLO -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                <rect x="3" y="3" width="18" height="18" rx="1"/>
                <rect x="7" y="7" width="10" height="10" rx="0.5" stroke-dasharray="2 1"/>
                <circle cx="12" cy="12" r="2" fill="currentColor" stroke="none"/>
              </svg>
              YOLO
            </div>
 
            <!-- MySQL -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M16.405 5.501c-.115 0-.193.014-.274.033v.013h.014c.054.104.146.18.214.273.054.107.1.214.154.32l.014-.015c.094-.066.14-.172.14-.333-.04-.047-.046-.094-.08-.14-.04-.046-.136-.08-.182-.151zm-8.58 6.627c-.05-.015-.09-.03-.134-.031-.19.03-.335.116-.451.286.021.013.027.02.031.027.175.041.334.046.495-.046.046-.014.088-.085.08-.13-.012-.04-.07-.071-.021-.106z"/>
                <path d="M21.037 16.273c-.278-.066-.68-.026-.926.107-.063.033-.188.04-.2.14.041.027.047.066.094.093.101.065.276.117.38.05a5.267 5.267 0 0 0 .66-.393c0-.003.013-.007.01-.013-.005-.003-.01-.003-.018-.003v.019zm-7.72-12.98c-.133-.017-.267-.016-.406-.016-.026.007-.053.017-.079.028-.031.01-.063.018-.094.027-.015.004-.031.01-.047.015a2.17 2.17 0 0 0-.088.036l-.035.015c-.016.006-.031.013-.046.02l-.044.022-.042.022-.04.022-.039.023-.036.025-.034.025-.033.026-.03.027-.03.028-.028.03-.026.03-.024.032-.023.033-.02.033-.02.034-.017.036-.015.036-.014.038-.012.039-.01.04-.01.04-.007.042-.006.043-.004.044-.002.044-.001.046.001.046.002.047.004.047.006.047.008.048.01.048.012.049.014.05.016.05.018.05.02.051.021.052.024.052.026.053.028.054.03.054.032.055.034.055.037.056.038.056.04.057.043.058.045.058.047.058.049.059.051.059.053.06.056.06.058.06.06.061.062.061.064.061.066.062.068.062.07.062.072.062.074.062.077.062.079.062.081.062.083.062.085.062.088.061.09.061.092.061.094.06.096.06.098.06.1.059.103.059.105.058.107.058.11.057.112.056.113.056.116.055.117.054.12.053.12.053.123.052.124.05.127.05.128.049.13.048.132.047.133.046.135.045.137.044.138.043.14.042.14.04.142.04.144.038.145.037.146.035.148.034.149.033.15.031.152.03.153.028.154.027.156.025.156.024.158.022.158.02.16.019.16.017.162.015.162.014.163.012.164.01.164.009.165.007.165.005.166.003.166.001.167-.001.167-.003.167-.005.168-.007.168-.009.168-.011.169-.013.169-.015.169-.017.169-.019.17-.021.17-.023.17-.025.17-.027.17-.029.17-.031.17-.033.17-.035.171-.037.171-.039.17-.04.17-.043.17-.044.17-.046.17-.048.17-.05.169-.051.17-.053.169-.055.169-.056.168-.058.168-.06.167-.061.167-.062.166-.064.165-.065.165-.067.164-.068.163-.069.163-.07.162-.072.161-.073.16-.074.16-.075.158-.076.158-.077.157-.078.156-.079.155-.08.153-.08.153-.082.151-.082.15-.083.149-.083.148-.084.147-.084.145-.085.144-.085.142-.085.141-.086.14-.086.138-.086.136-.086.135-.086.133-.086.132-.086.13-.086.128-.086.127-.086.125-.085.123-.085.121-.084.12-.084.118-.083.116-.082.114-.082.112-.081.11-.08.108-.079.106-.079.104-.077.102-.077.1-.075.098-.074.095-.073.093-.072.091-.07.089-.069.086-.068.084-.066.081-.065.079-.063.077-.062.074-.06.071-.059.069-.057.066-.056.063-.054.061-.052.058-.051.056-.049.053-.047.05-.046.047-.043.045-.042.042-.04.039-.038.036-.036.034-.034.031-.032.028-.03.025-.028.023-.026.02-.024.017-.021.014-.019.011-.017.008-.014.005-.012.002-.01-.001.022-.003.012-.006.003-.008-.006-.011-.016-.015-.025-.018-.034-.022-.044-.025-.053-.028-.062-.032-.072-.035-.08-.038-.09-.041-.099-.044-.108-.047-.117-.05-.126-.053-.135-.056-.143-.058-.152-.061-.16-.063-.17-.066-.178-.068-.186-.07-.195-.072-.203-.074-.211-.076-.22-.078-.228-.08-.235-.082-.244-.083-.251-.085-.259-.086-.267-.087-.274-.089-.282-.089-.289-.09-.296-.091-.303-.092-.31-.092-.317-.093-.323-.093-.33-.094-.336-.094-.342-.094-.348-.094-.354-.094-.36-.094-.365-.094-.371-.093-.376-.093-.381-.092-.386-.092-.391-.091-.396-.09-.4-.09-.405-.089-.409-.088-.413-.087-.417-.086-.421-.084-.425-.083-.428-.082-.432-.08-.435-.079-.438-.077-.441-.076-.444-.074-.447-.072-.45-.07-.452-.068-.454-.067-.457-.064-.459-.063-.461-.06-.463-.058-.465-.056-.467-.054-.468-.051-.47-.049-.471-.047-.472-.044-.473-.042-.474-.039-.475-.037-.475-.034-.476-.032-.476-.029-.476-.026-.477-.024-.476-.021-.476-.018-.476-.015-.476-.012-.475-.009-.475-.006-.474-.003-.473 0-.473.003-.471.006-.47.009-.469.013-.467.016-.466.019-.464.022-.462.025-.46.028-.458.031-.456.034-.454.037-.451.04-.449.043-.446.045-.443.048-.441.05-.438.053-.435.055-.432.057-.428.06-.425.062-.421.064-.418.066-.414.068-.41.07-.406.071-.402.073-.397.075-.393.076-.388.078-.384.079-.379.08-.374.081-.369.082-.364.083-.358.084-.353.085-.347.085-.341.086-.335.086-.329.087-.323.087-.317.087-.31.087-.303.087-.296.087-.289.087-.282.086-.275.086-.267.086-.26.085-.252.084-.244.083-.236.082-.228.081-.22.08-.211.079-.203.077-.194.076-.185.074-.176.073-.167.071-.158.069-.148.067-.139.065-.129.063-.119.06-.109.058-.099.056-.089.053-.079.05-.069.047-.059.044-.048.041-.037.038-.027.034-.016.031-.005.028.005.025.016.022.026.019.036.016.046.013.056.01.066.007.076.004.086.001.096-.002.106-.005.115-.007.125-.01.135-.013.145-.016.154-.019.164-.022.173-.025.182-.028.191-.031.2-.034.209-.037.218-.04.226-.043.234-.046.243-.049.25-.052.258-.055.266-.058.273-.06.281-.063.288-.066.295-.069.302-.071.309-.074.315-.077.321-.079.328-.082.334-.084.339-.087.345-.09.35-.092.355-.095.36-.097.365-.1.37-.102.374-.104.378-.107.382-.109.386-.111.39-.114.393-.116.397-.118.4-.12.403-.123.406-.125.409-.127.411-.129.414-.131.416-.133.418-.135.42-.137.422-.139.424-.141.425-.143.427-.145.428-.147.429-.149.43-.15.431-.152.432-.154.432-.156.433-.157.433-.159.434-.161.434-.162.434-.164.434-.166.434-.167.434-.169.433-.17.433-.172.433-.173.432-.175.431-.176.431-.178.43-.179.429-.181.428-.182.428-.183.426-.185.425-.186.424-.188.423-.189.421-.19.42-.191.418-.193.417-.194.415-.195.413-.196.411-.197.41-.199.407-.2.405-.201.403-.202.4-.203.398-.204.395-.205.393-.206.39-.207.387-.208.385-.209.381-.21.378-.211.376-.212.372-.212.369-.213.366-.214.362-.215.358-.215.355-.216.351-.217.347-.217.343-.218.339-.218.335-.219.331-.219.327-.22.322-.22.318-.22.313-.221.309-.221.304-.222.3-.222.295-.222.29-.222.285-.222.28-.223.275-.223.27-.223.265-.223.26-.223.254-.223.249-.223.244-.223.238-.223.232-.223.227-.223.221-.223.215-.223.21-.222.204-.222.198-.222.192-.221.186-.221.18-.22.174-.22.168-.22.162-.219.156-.218.149-.218.143-.217.137-.216.13-.215.124-.215.117-.214.111-.213.104-.212.098-.211.091-.21.084-.209.078-.208.071-.207.064-.206.057-.205.05-.203.043-.202.036-.201.029-.199.022-.198.015-.196.008-.195.001-.193-.006-.191-.013-.189-.02-.188-.027-.186-.034-.184-.041-.182-.048-.18-.055-.178-.062-.176-.069-.174-.076-.172-.083-.17-.09-.168-.097-.166-.103-.164-.11-.162-.117-.16-.124-.157-.131-.155-.138-.153-.144-.151-.151-.148-.158-.146-.165-.144-.171-.142-.178-.139-.185-.137-.191-.135-.198-.133-.204-.13-.211-.128-.217-.126-.224-.123-.23-.121-.236-.119-.243-.116-.249-.114-.255-.112-.261-.109-.267-.107-.273-.105-.279-.102-.285-.1-.291-.097-.297-.095-.303-.092-.309-.09-.314-.087-.32-.085-.326-.082-.331-.08-.337-.077-.342-.075-.347-.072-.353-.07-.358-.067-.363-.064-.368-.062-.373-.059-.378-.057-.383-.054-.388-.051-.393-.049-.398-.046-.402-.043-.407-.04-.411-.038-.416-.035-.42-.032-.425-.03-.429-.027-.433-.024-.437-.021-.441-.018-.445-.015-.449-.012-.453-.009-.457-.006-.461-.003-.465v-.466l.003-.465.006-.462.009-.459.012-.455.015-.452.018-.449.021-.445.024-.441.027-.437.03-.433.032-.428.035-.424.038-.42.04-.415.043-.41.046-.405.049-.4.051-.395.054-.39.057-.384.059-.379.062-.373.064-.367.067-.362.07-.356.072-.35.075-.344.077-.337.08-.332.082-.325.085-.319.087-.313.09-.306.092-.3.095-.293.097-.287.1-.28.102-.274.105-.267.107-.26.109-.254.112-.247.114-.24.116-.234.119-.227.121-.22.123-.213.126-.207.128-.2.13-.193.133-.186.135-.179.137-.172.139-.166.142-.159.144-.152.146-.145.148-.138.151-.131.153-.124.155-.117.157-.11.16-.103.162-.096.164-.089.166-.082.168-.075.17-.068.172-.061.174-.053.176-.046.178-.039.18-.032.182-.024.184-.017.186-.01.188-.003.19.005.191.012.193.019.195.027.196.034.198.042.199.049.201.056.202.064.203.071.205.079.206.086.207.093.208.101.209.108.21.116.211.123.212.13.213.138.214.145.215.152.216.16.217.167.218.174.218.181.219.189.22.196.22.203.221.21.222.217.222.225.222.232.223.239.223.246.223.252.223.259.223.266.223.273.223.279.223.286.222.292.222.299.222.305.221.311.221.318.22.324.22.33.22.336.219.341.219.347.218.353.218.358.217.363.217.369.216.374.215.379.215.384.214.389.213.394.212.399.211.403.21.408.209.412.208.416.207.421.206.425.205.429.203.433.202.437.201.44.199.444.198.448.196.451.195.454.193.458.191.461.19.464.188.467.186.47.184.472.182.475.18.478.178.48.176.482.174.484.172.487.169.489.167.491.164.492.162.494.16.496.157.497.154.499.152.5.149.501.146.503.143.504.14.505.138.506.135.506.132.507.129.508.126.508.123.508.12.509.116.509.113.509.11.509.107.509.103.509.1.509.096.508.093.508.09.507.086.507.082.506.079.505.075.504.071.503.068.502.064.501.06.499.056.498.052.496.049.494.045.492.041.49.037.488.033.486.029.484.025.481.021.479.017.476.013.473.009.47.005.467.001.464-.003.461-.007.458-.011.454-.015.45-.019.447-.023.443-.027.439-.031.435-.035.431-.039.427-.043.422-.047.418-.05.413-.054.409-.058.404-.062.399-.066.394-.07.389-.073.384-.077.378-.081.373-.085.367-.089.362-.092.356-.096.35-.1.344-.103.338-.107.332-.111.326-.114.32-.118.313-.122.307-.125.3-.129.293-.132.287-.136.28-.139.273-.143.266-.146.259-.15.252-.153.245-.156.238-.16.23-.163.223-.166.216-.169.208-.172.201-.176.193-.179.186-.182.178-.185.17-.188.162-.191.155-.194.147-.197.139-.2.131-.202.123-.205.115-.208.107-.211.099-.213.091-.216.083-.218.074-.221.066-.223.058-.225.05-.228.041-.23.033-.232.025-.234.016-.236.008-.239-.001-.241-.009-.243-.017-.245-.026-.247-.034-.249-.042-.251-.05-.253-.059-.254-.067-.256-.075-.258-.084-.259-.092-.261-.1-.262-.109-.264-.117-.265-.125-.267-.133-.268-.141-.269-.149-.27-.157-.271-.165-.272-.173-.273-.181-.274-.189-.274-.197-.275-.205-.275-.213-.276-.22-.276-.228-.276-.235-.276-.243-.276-.25-.276-.258-.276-.265-.276-.272-.275-.28-.275-.287-.274-.294-.274-.301-.273-.308-.273-.315-.272-.321-.271-.328-.27-.334-.269-.34-.268-.347-.267-.353-.266-.359-.265-.365-.264-.371-.262-.377-.261-.383-.26-.388-.258-.394-.257-.399-.255-.404-.254-.409-.252-.415-.25-.42-.249-.424-.247-.429-.245-.434-.243-.438-.241-.443-.239-.447-.237-.451-.235-.455-.233-.459-.231-.463-.228-.467-.226-.471-.224-.474-.222-.478-.219-.481-.217-.485-.214-.488-.212-.491-.209-.494-.207-.497-.204-.5-.202-.503-.199-.505-.196-.508-.193-.51-.191-.512-.188-.515-.185-.517-.182-.519-.179-.521-.176-.522-.173-.524-.17-.526-.167-.527-.164-.529-.161-.53-.158-.531-.154-.533-.151-.534-.148-.535-.145-.535-.141-.536-.138-.537-.135-.537-.131-.538-.128-.538-.124-.538-.121-.538-.117-.539-.114-.539-.11-.539-.106-.539-.103-.539-.099-.538-.095-.538-.092-.538-.088-.537-.084-.537-.08-.536-.077-.536-.073-.535-.069-.534-.065-.533-.061-.532-.058-.531-.054-.53-.05-.529-.046-.528-.042-.527-.038-.525-.034-.524-.03-.522-.026-.521-.022-.519-.018-.518-.015-.516-.011-.514-.007-.512-.003-.511.001-.509.005-.507.009-.505.013-.503.017-.501.021-.498.025-.496.029-.494.033-.491.037-.489.041-.486.045-.484.049-.481.053-.479.057-.476.061-.473.065-.47.069-.467.073-.464.077-.461.081-.458.085-.455.089-.451.093-.448.097-.445.1-.441.104-.438.108-.434.112-.43.116-.426.12-.422.124-.418.127-.414.131-.41.135-.406.139-.402.143-.397.146-.393.15-.388.154-.384.158-.379.161-.374.165-.369.169-.364.172-.359.176-.354.18-.349.183-.344.187-.339.19-.333.194-.328.198-.322.201-.317.205-.311.208-.305.212-.3.215-.294.218-.288.222-.282.225-.276.228-.27.232-.264.235-.258.238-.251.241-.245.245-.238.248-.232.251-.225.254-.219.257-.212.26-.205.263-.198.266-.191.269-.184.272-.177.275-.17.278-.163.281-.156.283-.149.286-.141.289-.134.292-.127.294-.119.297-.112.299-.104.302-.097.304-.089.307-.082.309-.074.311-.066.314-.059.316-.051.318-.043.321-.035.323-.028.325-.02.327-.012.329-.004.332.004.333.011.335.019.337.027.339.035.341.043.343.05.345.058.347.066.349.073.351.081.352.089.354.097.356.104.358.112.359.12.361.127.362.135.364.142.365.15.367.157.368.165.369.172.371.18.372.187.373.195.374.202.375.21.376.217.377.225.378.232.379.239.38.246.381.254.381.261.382.268.383.275.383.282.384.289.384.296.385.303.385.31.386.317.386.324.386.33.387.337.387.343.387.35.387.356.387.363.387.369.387.375.387.381.387.387.387.393.387.399.387.405.387.411.386.416.386.422.386.428.385.433.385.438.385.444.384.449.384.454.383.459.383.464.382.469.381.474.381.479.38.483.379.488.379.492.378.497.377.501.376.505.375.509.374.513.373.517.372.521.371.525.37.529.369.532.368.536.367.539.366.543.365.546.363.549.362.553.361.556.359.559.358.562.357.564.355.567.354.57.352.572.351.575.349.577.348.58.346.582.344.584.343.586.341.589.339.591.337.593.336.595.334.596.332.598.33.6.328.602.326.603.324.605.322.606.32.608.318.609.316.61.314.611.312.613.309.614.307.615.305.616.303.617.3.618.298.619.296.62.293.62.291.621.288.622.286.622.283.623.281.624.278.624.276.624.273.625.27.625.268.625.265.626.262.626.26.626.257.626.254.626.251.626.249.626.246.627.243.627.24.627.237.627.234.627.231.627.228.627.225.627.222.627.219.627.216.627.213.626.21.626.207.626.204.626.201.625.198.625.195.625.192.624.189.624.186.623.183.623.18.622.177.622.174.621.171.62.168.62.165.619.162.618.159.617.156.617.153.616.15.615.147.614.144.613.141.612.138.611.135.61.132.609.129.608.126.606.123.605.12.604.117.603.114.601.111.6.108.598.105.597.102.595.099.594.096.592.093.591.09.589.087.587.084.585.081.583.078.582.075.58.072.578.069.576.066.574.063.572.06.57.056.567.053.565.05.563.047.56.044.558.041.555.038.553.034.55.031.548.028.545.025.542.022.54.018.537.015.534.012.531.009.529.005.526.002.523-.001.52-.004.517-.007.515-.01.512-.013.509-.016.506-.019.503-.022.5-.025.497-.028.494-.031.491-.034.488-.037.485-.04.482-.043.479-.046.476-.049.473-.052.47-.055.467-.058.464-.061.461-.063.458-.066.455-.069.452-.072.449-.075.446-.078.443-.08.44-.083.437-.086.434-.089.431-.092.428-.094.425-.097.422-.1.419-.103.416-.105.413-.108.41-.111.407-.114.404-.116.401-.119.398-.122.394-.124.391-.127.388-.13.385-.132.382-.135.379-.138.376-.14.373-.143.369-.146.366-.148.363-.151.36-.153.357-.156.354-.158.351-.161.347-.163.344-.166.341-.168.338-.171.335-.173.332-.176.329-.178.326-.18.323-.183.32-.185.317-.188.313-.19.31-.192.307-.195.304-.197.301-.2.298-.202.295-.204.292-.207.289-.209.286-.211.283-.213.28-.216.277-.218.274-.22.271-.222.268-.225.265-.227.262-.229.259-.231.256-.234.253-.236.25-.238.247-.24.244-.243.241-.245.238-.247.235-.249.232-.251.229-.254.226-.256.223-.258.22-.26.217-.262.214-.264.211-.266.208-.269.205-.271.202-.273.199-.275.196-.277.193-.279.19-.281.187-.283.184-.285.181-.287.178-.289.175-.291.172-.293.169-.295.166-.297.163-.299.16-.301.157-.303.154-.305.151-.307.148-.309.145-.311.142-.313.139-.315.136-.317.133-.318.13-.32.127-.322.124-.324.121-.325.118-.327.115-.329.112-.331.109-.332.106-.334.103-.336.1-.337.097-.339.094-.341.091-.342.088-.344.085-.345.082-.347.079-.348.076-.35.073-.351.07-.353.067-.354.064-.356.061-.357.058-.359.055-.36.052-.361.049-.363.046-.364.043-.365.04-.367.037-.368.034-.369.031-.37.028-.372.025-.373.022-.374.019-.375.016-.376.013-.378.01-.379.007-.38.004-.381.001-.382-.002-.383-.005-.384-.008-.385-.011-.386-.014-.387-.017-.388-.02-.389-.023-.39-.026-.391-.029-.392-.032-.393-.035-.394-.038-.395-.041-.396-.044-.396-.047-.397-.05-.398-.053-.399-.056-.399-.059-.4-.062-.401-.065-.401-.068-.402-.071-.402-.074-.403-.077-.403-.08-.404-.083-.404-.086-.405-.089-.405-.092-.406-.095-.406-.098-.407-.101-.407-.104-.407-.107-.408-.11-.408-.113-.408-.116-.409-.119-.409-.122-.409-.125-.41-.128-.41-.131-.41-.134-.41-.137-.41-.14-.411-.143-.411-.146-.411-.149-.411-.152-.411-.155-.411-.158-.411-.161-.411-.164-.412-.167-.412-.17-.412-.173-.412-.175-.412-.178-.412-.181-.412-.184-.412-.187-.412-.19-.412-.193-.412-.196-.412-.199-.412-.202-.412-.204-.412-.207-.412-.21-.412-.213-.412-.216-.412-.219-.412-.221-.412-.224-.411-.227-.411-.23-.411-.233-.411-.235-.411-.238-.411-.241-.41-.244-.41-.246-.41-.249-.41-.252-.409-.255-.409-.257-.409-.26-.408-.263-.408-.265-.408-.268-.407-.271-.407-.273-.406-.276-.406-.279-.406-.281-.405-.284-.405-.286-.404-.289-.404-.292-.403-.294-.402-.297-.402-.299-.401-.302-.4-.305-.4-.307-.399-.31-.398-.312-.398-.315-.397-.317-.396-.32-.395-.322-.394-.325-.394-.327-.393-.33-.392-.332-.391-.334-.39-.337-.389-.339-.388-.342-.387-.344-.386-.346-.385-.349-.384-.351-.383-.354-.382-.356-.381-.358-.38-.361-.379-.363-.378-.365-.376-.368-.375-.37-.374-.372-.373-.375-.372-.377-.37-.379-.369-.382-.368-.384-.367-.386-.365-.388-.364-.391-.362-.393-.361-.395-.36-.397-.358-.4-.357-.402-.355-.404-.354-.406-.352-.408-.351-.411-.349-.413-.348-.415-.346-.417-.344-.419-.343-.422-.341-.424-.339-.426-.338-.428-.336-.43-.334-.432-.332-.434-.331-.436-.329-.438-.327-.44-.325-.442-.323-.444-.322-.446-.32-.448-.318-.45-.316-.452-.314-.454-.312-.456-.31-.458-.308-.46-.306-.461-.304-.463-.302-.465-.3-.467-.298-.469-.296-.47-.293-.472-.291-.474-.289-.476-.287-.477-.285-.479-.282-.481-.28-.482-.278-.484-.276-.486-.273-.487-.271-.489-.269-.49-.266-.492-.264-.494-.261-.495-.259-.497-.256-.498-.254-.5-.251-.501-.249-.503-.246-.504-.244-.505-.241-.507-.239-.508-.236-.509-.234-.511-.231-.512-.228-.513-.226-.515-.223-.516-.22-.517-.218-.518-.215-.52-.212-.521-.209-.522-.207-.523-.204-.524-.201-.525-.198-.526-.196-.527-.193-.528-.19-.529-.187-.53-.185-.531-.182-.532-.179-.533-.176-.534-.173-.535-.17-.535-.168-.536-.165-.537-.162-.538-.159-.538-.156-.539-.153-.54-.15-.54-.147-.541-.144-.542-.141-.542-.138-.543-.135-.543-.132-.544-.129-.544-.126-.545-.123-.545-.12-.546-.117-.546-.114-.546-.111-.547-.108-.547-.105-.547-.102-.548-.099-.548-.096-.548-.093-.548-.09-.549-.087-.549-.084-.549-.081-.549-.078-.549-.075-.549-.072-.549-.069-.55-.066-.55-.063-.55-.06-.55-.057-.549-.054-.549-.051-.549-.048-.549-.045-.549-.042-.549-.039-.548-.036-.548-.033-.548-.03-.547-.027-.547-.024-.547-.021-.546-.018-.546-.015-.545-.012-.545-.009-.544-.006-.544-.003-.543 0-.543.003-.542.006-.541.009-.541.012-.54.015-.539.018-.539.021-.538.024-.537.027-.536.03-.536.033-.535.036-.534.039-.533.042-.532.045-.531.048-.53.051-.529.054-.528.057-.527.06-.526.063-.525.066-.524.069-.523.072-.522.075-.521.078-.52.081-.518.084-.517.087-.516.09-.515.093-.513.096-.512.099-.511.102-.51.105-.508.108-.507.111-.505.114-.504.117-.502.12-.501.123-.499.126-.498.129-.496.132-.494.135-.493.138-.491.141-.489.144-.487.147-.486.15-.484.153-.482.156-.48.159-.478.162-.476.165-.474.168-.472.171-.47.173-.468.176-.466.179-.464.182-.461.185-.459.188-.457.19-.455.193-.452.196-.45.199-.447.202-.445.204-.442.207-.44.21-.437.213-.435.215-.432.218-.429.221-.427.223-.424.226-.421.229-.418.231-.416.234-.413.237-.41.239-.407.242-.404.244-.401.247-.398.249-.395.252-.392.255-.389.257-.386.26-.383.262-.38.264-.376.267-.373.269-.37.272-.367.274-.363.277-.36.279-.356.281-.353.284-.35.286-.346.289-.342.291-.339.293-.335.296-.331.298-.328.3-.324.303-.32.305-.316.307-.312.31-.308.312-.305.314-.301.316-.296.319-.292.321-.288.323-.284.326-.28.328-.276.33-.271.332-.267.334-.263.337-.258.339-.254.341-.249.343-.245.345-.24.347-.236.35-.231.352-.227.354-.222.356-.217.358-.212.36-.207.362-.203.364-.198.366-.193.368-.188.37-.183.372-.178.374-.173.376-.168.378-.163.38-.158.382-.152.384-.147.386-.142.388-.137.39-.131.392-.126.394-.121.395-.115.397-.11.399-.104.401-.099.402-.093.404-.088.406-.082.407-.077.409-.071.411-.065.412-.06.414-.054.415-.048.417-.043.418-.037.42-.031.421-.025.423-.019.424-.014.426-.008.427-.002.428.004.43.01.431.016.432.022.434.028.435.034.436.04.437.046.439.052.44.058.441.063.442.069.443.075.445.081.446.087.447.093.448.099.449.105.45.111.451.117.452.122.453.128.454.134.455.14.456.146.457.152.458.157.459.163.46.169.461.175.461.181.462.186.463.192.464.198.464.204.465.209.466.215.467.221.467.226.468.232.469.238.469.243.47.249.47.255.471.26.471.266.472.272.472.277.473.283.473.288.474.294.474.3.474.305.475.311.475.316.475.322.476.327.476.333.476.338.476.344.477.349.477.355.477.36.477.366.477.371.477.377.477.382.477.388.477.393.477.399.477.404.477.41.477.415.477.42.477.426.477.431.477.437.477.442.477.447.477.453.477.458.477.463.477.469.477.474.476.479.476.485.476.49.476.495.476.501.475.506.475.511.475.516.474.522.474.527.474.532.473.537.473.543.472.548.472.553.471.558.471.563.47.569.47.574.469.579.468.584.468.589.467.594.466.599.466.604.465.609.464.614.463.619.463.624.462.629.461.634.46.639.459.644.458.649.457.654.456.659.455.664.454.669.453.674.452.679.451.684.45.688.449.693.448.698.447.703.445.708.444.712.443.717.442.722.44.726.439.731.438.736.436.74.435.745.433.749.432.754.43.759.429.763.427.768.426.772.424.777.422.781.421.786.419.79.417.794.416.799.414.803.412.807.41.812.408.816.407.82.405.824.403.828.401.833.399.837.397.841.395.845.393.849.391.853.389.857.387.861.385.865.383.869.381.873.379.877.377.881.374.885.372.889.37.892.368.896.365.9.363.904.361.907.358.911.356.915.354.918.351.922.349.925.346.929.344.932.341.936.339.939.336.943.334.946.331.949.328.953.326.956.323.959.32.962.318.966.315.969.312.972.309.975.306.978.304.981.301.984.298.987.295.99.292.993.289.996.286.999.283 1.002.28 1.005.277 1.007.274 1.01.271 1.013.268 1.015.265 1.018.262 1.021.259 1.023.255 1.026.252 1.028.249 1.031.246 1.033.242 1.036.239 1.038.236 1.04.232 1.043.229 1.045.225 1.047.222 1.05.218 1.052.215 1.054.211 1.056.208 1.059.204 1.061.201 1.063.197 1.065.193 1.067.19 1.069.186 1.071.182 1.073.179 1.075.175 1.077.171 1.079.167 1.081.164 1.083.16 1.085.156 1.087.152 1.088.148 1.09.144 1.092.14 1.094.136 1.095.132 1.097.128 1.099.124 1.1.12 1.102.116 1.103.112 1.105.108 1.106.104 1.108.1 1.109.096 1.111.092 1.112.088 1.113.084 1.115.079 1.116.075 1.117.071 1.119.067 1.12.063 1.121.058 1.122.054 1.123.05 1.125.046 1.126.041 1.127.037 1.128.033 1.129.028 1.13.024 1.131.02 1.132.015 1.133.011 1.134.007 1.135.002 1.136-.002 1.137-.006 1.138-.011 1.139-.015 1.14-.02 1.141-.024 1.141-.028 1.142-.033 1.143-.037 1.143-.042 1.144-.046 1.145-.051 1.145-.055 1.146-.059 1.146-.064 1.147-.068 1.148-.073 1.148-.077 1.149-.082 1.149-.086 1.15-.09 1.15-.095 1.15-.099 1.151-.104 1.151-.108 1.151-.113 1.152-.117 1.152-.121 1.152-.126 1.152-.13 1.153-.135 1.153-.139 1.153-.143 1.153-.148 1.153-.152 1.153-.157 1.153-.161 1.153-.165 1.154-.17 1.154-.174 1.154-.178 1.154-.183 1.154-.187 1.154-.192 1.154-.196 1.154-.2 1.154-.205 1.154-.209 1.154-.213 1.154-.218 1.154-.222 1.154-.226 1.154-.231 1.154-.235 1.154-.239 1.154-.244"/>
              </svg>
              MySQL
            </div>
          </div>
        </div>
 
        <!-- Tools -->
        <div class="tech-group reveal stagger-3">
          <div class="tech-group-label">Tools &amp; Platforms</div>
          <div class="tech-icons">
 
            <!-- Git -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M23.546 10.93L13.067.452c-.604-.603-1.582-.603-2.188 0L8.708 2.627l2.76 2.76c.645-.215 1.379-.07 1.889.441.516.515.658 1.258.438 1.9l2.658 2.66c.645-.223 1.387-.078 1.9.435.721.72.721 1.884 0 2.604-.719.719-1.881.719-2.6 0-.539-.541-.674-1.337-.404-1.996L12.86 8.955v6.525c.176.086.342.203.488.348.713.721.713 1.883 0 2.6-.719.721-1.889.721-2.609 0-.719-.719-.719-1.879 0-2.598.182-.18.387-.316.605-.406V8.835c-.217-.091-.424-.222-.604-.405-.545-.545-.676-1.342-.396-2.009L7.636 3.7.45 10.881c-.6.605-.6 1.584 0 2.189l10.48 10.477c.604.604 1.582.604 2.186 0l10.43-10.43c.605-.603.605-1.582 0-2.187"/>
              </svg>
              Git
            </div>
 
            <!-- GitHub -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
              </svg>
              GitHub
            </div>
 
            <!-- VS Code -->
            <div class="tech-badge">
              <svg viewBox="0 0 24 24" fill="currentColor">
                <path d="M23.15 2.587L18.21.21a1.494 1.494 0 0 0-1.705.29l-9.46 8.63-4.12-3.128a.999.999 0 0 0-1.276.057L.327 7.261A1 1 0 0 0 .326 8.74L3.899 12 .326 15.26a1 1 0 0 0 .001 1.479L1.65 17.94a.999.999 0 0 0 1.276.057l4.12-3.128 9.46 8.63a1.492 1.492 0 0 0 1.704.29l4.942-2.377A1.5 1.5 0 0 0 24 20.06V3.939a1.5 1.5 0 0 0-.85-1.352zm-5.146 14.861L10.826 12l7.178-5.448v10.896z"/>
              </svg>
              VS Code
            </div>
 
          </div>
        </div>
      </div>
    </div>
  </section>
 
  <!-- PROJECTS -->
  <section id="projects">
    <div class="container">
      <div class="section-header reveal">
        <span class="section-num">03</span>
        <h2 class="section-title">Projects</h2>
        <div class="section-line"></div>
      </div>
      <div class="projects-grid">
        <div class="project-card reveal stagger-1">
          <div class="project-num">PROJECT / 01</div>
          <div class="project-name orbit">Orbit</div>
          <p class="project-desc">
            A safety-focused communication and coordination platform designed to improve emergency response and location awareness. Built for reliability during the moments that matter most.
          </p>
          <div class="project-tags">
            <span class="project-tag">Real-time Comm</span>
            <span class="project-tag">Location Sharing</span>
            <span class="project-tag">Mapping</span>
            <span class="project-tag">Emergency Workflows</span>
            <span class="project-tag">Reliability</span>
          </div>
        </div>
        <div class="project-card reveal stagger-2">
          <div class="project-num">PROJECT / 02</div>
          <div class="project-name sentinel">Sentinel</div>
          <p class="project-desc">
            A computer vision and automation platform focused on real-time visual processing and intelligent automation. Powered by OpenCV and YOLO for accurate, fast detection.
          </p>
          <div class="project-tags">
            <span class="project-tag">Object Detection</span>
            <span class="project-tag">Computer Vision</span>
            <span class="project-tag">OpenCV</span>
            <span class="project-tag">YOLO</span>
            <span class="project-tag">Real-time</span>
          </div>
        </div>
      </div>
    </div>
  </section>
 
  <!-- PHILOSOPHY -->
  <section id="philosophy">
    <div class="container">
      <div class="section-header reveal">
        <span class="section-num">04</span>
        <h2 class="section-title">Development Philosophy</h2>
        <div class="section-line"></div>
      </div>
      <div class="philosophy-grid">
        <div class="philosophy-item reveal stagger-1">
          <div class="philosophy-num">01 —</div>
          <p class="philosophy-text">Understand how systems work beneath the surface.</p>
        </div>
        <div class="philosophy-item reveal stagger-2">
          <div class="philosophy-num">02 —</div>
          <p class="philosophy-text">Build reliable software before optimizing it.</p>
        </div>
        <div class="philosophy-item reveal stagger-3">
          <div class="philosophy-num">03 —</div>
          <p class="philosophy-text">Learn by building, experimenting, and improving.</p>
        </div>
        <div class="philosophy-item reveal stagger-4">
          <div class="philosophy-num">04 —</div>
          <p class="philosophy-text">Focus on maintainability, performance, and reliability.</p>
        </div>
        <div class="philosophy-item reveal stagger-5">
          <div class="philosophy-num">05 —</div>
          <p class="philosophy-text">Curiosity is the foundation of growth.</p>
        </div>
      </div>
    </div>
  </section>
 
  <!-- PERSONALITY -->
  <section>
    <div class="container">
      <div class="section-header reveal">
        <span class="section-num">05</span>
        <h2 class="section-title">Personality</h2>
        <div class="section-line"></div>
      </div>
      <div class="personality-flow reveal">
        <div class="personality-chip">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <circle cx="8" cy="8" r="6" stroke="var(--accent2)" stroke-width="1.2"/>
            <circle cx="8" cy="8" r="2" fill="var(--accent2)"/>
          </svg>
          Curious about how things work under the hood
        </div>
        <div class="personality-chip">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M3 13L7 3l3 5 2-3 1 3" stroke="var(--accent2)" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          Enjoys pushing systems to their limits
        </div>
        <div class="personality-chip">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M8 2v4M8 10v4M2 8h4M10 8h4" stroke="var(--accent2)" stroke-width="1.2" stroke-linecap="round"/>
          </svg>
          Likes understanding the "why" behind technologies
        </div>
        <div class="personality-chip">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <path d="M2 8c0-3.314 2.686-6 6-6s6 2.686 6 6-2.686 6-6 6" stroke="var(--accent2)" stroke-width="1.2" stroke-linecap="round"/>
            <path d="M8 5v3l2 2" stroke="var(--accent2)" stroke-width="1.2" stroke-linecap="round"/>
          </svg>
          Enjoys experimenting, learning, and optimizing
        </div>
        <div class="personality-chip">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none">
            <rect x="2" y="5" width="12" height="8" rx="1" stroke="var(--accent2)" stroke-width="1.2"/>
            <path d="M5 5V4a3 3 0 016 0v1" stroke="var(--accent2)" stroke-width="1.2"/>
          </svg>
          Interested in reliability, performance, and real-world problem solving
        </div>
      </div>
    </div>
  </section>
 
  <!-- CLOSING -->
  <div class="closing">
    <div class="container">
      <p class="closing-quote">"Curious about how things work beneath the surface."</p>
      <div class="closing-line"></div>
    </div>
  </div>
 
</main>
 
<script>
  // Cursor
  const cursor = document.getElementById('cursor');
  const ring = document.getElementById('cursor-ring');
  let mx = 0, my = 0, rx = 0, ry = 0;
 
  document.addEventListener('mousemove', e => {
    mx = e.clientX; my = e.clientY;
    cursor.style.left = mx - 4 + 'px';
    cursor.style.top = my - 4 + 'px';
  });
 
  function animateRing() {
    rx += (mx - rx) * 0.12;
    ry += (my - ry) * 0.12;
    ring.style.left = rx + 'px';
    ring.style.top = ry + 'px';
    requestAnimationFrame(animateRing);
  }
  animateRing();
 
  document.querySelectorAll('a, button, .tech-badge, .interest-item, .project-card, .personality-chip').forEach(el => {
    el.addEventListener('mouseenter', () => {
      ring.style.width = '48px';
      ring.style.height = '48px';
      ring.style.borderColor = 'rgba(0,212,255,0.7)';
    });
    el.addEventListener('mouseleave', () => {
      ring.style.width = '32px';
      ring.style.height = '32px';
      ring.style.borderColor = 'rgba(0,212,255,0.4)';
    });
  });
 
  // Scroll progress
  const progress = document.getElementById('progress');
  window.addEventListener('scroll', () => {
    const pct = window.scrollY / (document.body.scrollHeight - window.innerHeight) * 100;
    progress.style.width = pct + '%';
  });
 
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
      }
    });
  }, { threshold: 0.12 });
 
  reveals.forEach(el => observer.observe(el));
 
  // Typing effect for hero intro
  const intro = document.querySelector('.hero-intro');
  if (intro) {
    const text = intro.textContent.replace('\uFEFF', '').trim().replace(/\s+/g, ' ');
    const blink = intro.querySelector('.cursor-blink');
    intro.textContent = '';
    if (blink) intro.appendChild(blink);
 
    let i = 0;
    const interval = setInterval(() => {
      if (i < text.length) {
        intro.insertBefore(document.createTextNode(text[i]), blink);
        i++;
      } else {
        clearInterval(interval);
      }
    }, 14);
  }
</script>
</body>
</html>
 
