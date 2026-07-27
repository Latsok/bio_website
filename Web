<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ondřej Košťál — CV &amp; Projects</title>
<meta name="description" content="Ondřej Košťál — IT student at CZU. Application support, Python, C#, JavaScript. Personal CV and projects.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700;900&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #0b0f0e;
    --bg-raised: #141a18;
    --bg-raised-2: #182420;
    --line: rgba(255,255,255,0.08);
    --line-strong: rgba(255,255,255,0.14);
    --text: #f3f6f4;
    --text-muted: #9fada6;
    --text-faint: #6b7975;
    --accent: #6EF0C2;
    --accent-dim: #4bb897;
    --accent-ink: #06231a;
    --radius-lg: 20px;
    --radius-md: 14px;
    --radius-sm: 8px;
    --maxw: 1080px;
    --font-display: 'Roboto', sans-serif;
    --font-body: 'Roboto', sans-serif;
    --font-mono: 'JetBrains Mono', monospace;
    --ease: cubic-bezier(.22,.9,.32,1);
  }

  *,*::before,*::after{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  body{
    margin:0;
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    line-height: 1.55;
    -webkit-font-smoothing: antialiased;
  }
  img{ max-width:100%; display:block; }
  a{ color: inherit; text-decoration: none; }
  ul{ list-style:none; margin:0; padding:0; }
  h1,h2,h3{ font-family: var(--font-display); margin:0; }
  section{ padding: 80px 0; }
  .wrap{ max-width: var(--maxw); margin: 0 auto; padding: 0 24px; }

  ::selection{ background: var(--accent); color: var(--accent-ink); }
  :focus-visible{ outline: 2px solid var(--accent); outline-offset: 3px; border-radius: 4px; }

  .eyebrow{
    font-family: var(--font-mono);
    font-size: 12px;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--accent);
    display:flex;
    align-items:center;
    gap:10px;
  }
  .eyebrow::before{
    content:"";
    width:5px; height:5px;
    border-radius: 50%;
    background: var(--accent);
    flex-shrink:0;
  }

  /* ---------- Header ---------- */
  header{
    position: sticky;
    top:0;
    z-index: 100;
    background: rgba(11,15,14,0.82);
    backdrop-filter: blur(14px) saturate(140%);
    border-bottom: 1px solid var(--line);
  }
  .header-inner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding: 16px 24px;
    max-width: var(--maxw);
    margin:0 auto;
  }
  .brand{ display:flex; align-items:center; gap:11px; }
  .brand-text{ display:flex; flex-direction:column; gap:1px; }
  .brand-name{
    font-family: var(--font-display);
    font-weight: 700;
    font-size: 16px;
    letter-spacing: .01em;
  }
  .brand-tag{
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--text-muted);
  }

  nav.primary-nav{ display:none; }
  .primary-nav ul{ display:flex; gap: 30px; }
  .primary-nav a{
    font-size: 14px;
    font-weight: 500;
    color: var(--text-muted);
    transition: color .2s var(--ease);
    position: relative;
    padding: 4px 0;
  }
  .primary-nav a:hover{ color: var(--text); }
  .primary-nav a::after{
    content:"";
    position:absolute; left:0; right:100%; bottom:-2px;
    height:1px; background: var(--accent);
    transition: right .25s var(--ease);
  }
  .primary-nav a:hover::after{ right:0; }

  .header-actions{ display:flex; align-items:center; gap:12px; }
  .btn{
    font-family: var(--font-body);
    font-weight: 600;
    font-size: 14px;
    border-radius: 999px;
    padding: 11px 22px;
    display:inline-flex;
    align-items:center;
    gap:8px;
    cursor:pointer;
    border: 1px solid transparent;
    transition: transform .2s var(--ease), background .2s var(--ease), border-color .2s var(--ease), box-shadow .2s var(--ease);
    white-space: nowrap;
  }
  .btn-accent{
    background: var(--accent);
    color: var(--accent-ink);
  }
  .btn-accent:hover{ transform: translateY(-2px); box-shadow: 0 10px 24px -8px rgba(110,240,194,0.45); }
  .btn-outline{
    background: transparent;
    border-color: var(--line-strong);
    color: var(--text);
    display:none;
  }
  .btn-outline:hover{ border-color: var(--accent); color: var(--accent); }

  .hamburger{
    width: 42px; height: 42px;
    border-radius: 10px;
    border: 1px solid var(--line-strong);
    background: var(--bg-raised);
    display:flex; align-items:center; justify-content:center;
    cursor:pointer;
    flex-shrink:0;
  }
  .hamburger span{ position:relative; width:16px; height:11px; display:block; }
  .hamburger span::before,.hamburger span::after,.hamburger i{
    content:""; position:absolute; left:0; width:100%; height:1.5px; background: var(--text);
    transition: transform .3s var(--ease), opacity .3s var(--ease), top .3s var(--ease);
  }
  .hamburger span::before{ top:0; }
  .hamburger span i{ top:5px; display:block; }
  .hamburger span::after{ top:10px; }
  .hamburger.open span::before{ top:5px; transform: rotate(45deg); }
  .hamburger.open span i{ opacity:0; }
  .hamburger.open span::after{ top:5px; transform: rotate(-45deg); }

  .mobile-nav{
    max-height:0;
    overflow:hidden;
    background: var(--bg-raised);
    border-bottom: 1px solid var(--line);
    transition: max-height .38s var(--ease);
  }
  .mobile-nav.open{ max-height: 320px; }
  .mobile-nav ul{ padding: 8px 24px 20px; display:flex; flex-direction:column; }
  .mobile-nav a{
    padding: 14px 0;
    font-size: 16px;
    font-weight: 500;
    text-align:center;
    border-bottom: 1px solid var(--line);
    color: var(--text-muted);
  }
  .mobile-nav li:last-child a{ border-bottom:none; }
  .mobile-nav a:hover{ color: var(--accent); }

  /* ---------- Reveal animation ---------- */
  .reveal{
    opacity:0;
    transform: translateY(28px);
    transition: opacity .7s var(--ease), transform .7s var(--ease);
  }
  .reveal.in-view{ opacity:1; transform: translateY(0); }
  .reveal-stagger > *{ transition-delay: calc(var(--i,0) * 90ms); }

  @media (prefers-reduced-motion: reduce){
    .reveal, .reveal-stagger > *{ transition: none; opacity:1; transform:none; }
    html{ scroll-behavior:auto; }
  }

  /* ---------- Hero ---------- */
  .hero{ padding: 60px 0 76px; }
  .hero-inner{
    display:flex;
    flex-direction:column;
    gap: 24px;
  }
  .status-chip{
    display:inline-flex; align-items:center; gap:8px;
    font-size: 12.5px; font-weight:500; color: var(--text-muted);
    border: 1px solid var(--line-strong);
    border-radius: 999px;
    padding: 6px 13px;
    width: fit-content;
  }
  .status-dot{
    width:7px; height:7px; border-radius:50%; background: var(--accent);
    box-shadow: 0 0 0 3px rgba(110,240,194,0.18);
    flex-shrink:0;
  }
  .status-chip-sm{
    font-size: 10px;
    padding: 3px 9px 3px 8px;
    margin-top: 4px;
    border-color: var(--line);
    color: var(--text-faint);
  }
  .status-chip-sm .status-dot{ width:5px; height:5px; box-shadow: 0 0 0 2px rgba(110,240,194,0.18); }
  .hero h1{
    font-size: clamp(30px, 7vw, 50px);
    line-height: 1.1;
    font-weight: 700;
    letter-spacing: -0.01em;
  }
  .hero h1 span{ color: var(--accent); }
  .hero blockquote{
    margin:0;
    font-size: 16.5px;
    color: var(--text-muted);
    max-width: 60ch;
    border-left: 2px solid var(--accent-dim);
    padding-left: 18px;
    font-style: normal;
  }
  .hero-cta{ display:flex; gap:14px; margin-top:6px; flex-wrap:wrap; }

  .quick-facts{
    display:grid;
    grid-template-columns: 1fr;
    gap: 12px;
    margin-top: 8px;
  }
  .fact{
    display:flex; align-items:flex-start; gap:12px;
    padding: 14px 16px;
    background: var(--bg-raised);
    border: 1px solid var(--line);
    border-radius: var(--radius-sm);
  }
  .fact svg{ width:18px; height:18px; color: var(--accent); flex-shrink:0; margin-top:2px; }
  .fact strong{ display:block; font-size:13.5px; font-weight:600; }
  .fact span{ font-size:12.5px; color: var(--text-muted); }

  /* ---------- Section headings ---------- */
  .section-head{ margin-bottom: 36px; }
  .section-head h2{
    font-size: clamp(22px, 3.6vw, 30px);
    font-weight: 700;
    margin-top: 10px;
    letter-spacing: -0.01em;
  }

  /* ---------- Skills ---------- */
  .skills-list{ display:flex; flex-direction:column; gap: 18px; }
  .skill-row{
    display:flex; flex-direction:column; gap:8px;
  }
  .skill-top{ display:flex; justify-content:space-between; align-items:baseline; gap:10px; }
  .skill-name{ font-size:14.5px; font-weight:600; }
  .skill-level{ font-family: var(--font-mono); font-size:11px; color: var(--text-faint); text-transform:uppercase; letter-spacing:.06em; }
  .skill-track{ height:6px; border-radius:999px; background: var(--bg-raised-2); overflow:hidden; border:1px solid var(--line); }
  .skill-fill{ height:100%; border-radius:999px; background: linear-gradient(90deg, var(--accent-dim), var(--accent)); width:0%; transition: width 1.1s var(--ease); }
  .skill-fill.in-view{ }

  .exp-list{ display:flex; flex-direction:column; margin-top: 40px; }
  .exp-item{
    display:grid;
    grid-template-columns: 18px 1fr;
    gap: 16px;
    padding-bottom: 26px;
    position:relative;
  }
  .exp-item::before{
    content:"";
    position:absolute; left:8px; top:20px; bottom:0;
    width:1px; background: var(--line);
  }
  .exp-item:last-child::before{ display:none; }
  .exp-dot{
    width:18px; height:18px; border-radius:50%;
    background: var(--bg-raised); border: 2px solid var(--accent);
    margin-top:2px;
  }
  .exp-role{ font-weight:600; font-size:15px; }
  .exp-meta{ font-family: var(--font-mono); font-size:11.5px; color: var(--accent); margin: 3px 0 6px; letter-spacing:.03em; }
  .exp-desc{ font-size: 13.5px; color: var(--text-muted); max-width: 52ch; }

  /* ---------- Projects ---------- */
  .projects-grid{
    display:grid;
    grid-template-columns: 1fr;
    gap: 16px;
  }
  .project-card{
    background: var(--bg-raised);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    padding: 24px;
    display:flex;
    flex-direction:column;
    gap: 14px;
    transition: border-color .25s var(--ease), transform .25s var(--ease), background .25s var(--ease);
  }
  .project-card:hover{
    border-color: var(--accent-dim);
    transform: translateY(-4px);
    background: var(--bg-raised-2);
  }
  .project-top{ display:flex; justify-content:space-between; align-items:flex-start; gap:12px; }
  .project-icon{
    width: 42px; height:42px;
    border-radius: 10px;
    background: var(--bg-raised-2);
    border: 1px solid var(--line-strong);
    color: var(--accent);
    display:flex; align-items:center; justify-content:center;
    flex-shrink:0;
  }
  .project-icon svg{ width:20px; height:20px; }
  .project-status{
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing:.05em;
    text-transform:uppercase;
    padding: 5px 10px;
    border-radius: 999px;
    border: 1px solid var(--line-strong);
    color: var(--text-muted);
    white-space: nowrap;
  }
  .project-status.dev{ color: var(--accent); border-color: var(--accent-dim); }
  .project-card h3{ font-size: 17px; font-weight:600; }
  .project-card p.desc{ font-size:13.5px; color: var(--text-muted); margin:0; }
  .project-tags{ display:flex; flex-wrap:wrap; gap:8px; margin-top:2px; }
  .project-tag{
    font-family: var(--font-mono);
    font-size: 11px;
    padding: 5px 10px;
    border-radius: 6px;
    background: var(--bg-raised-2);
    border: 1px solid var(--line);
    color: var(--text-muted);
  }
  .project-link{
    margin-top: 4px;
    font-size: 13px;
    font-weight: 600;
    color: var(--accent);
    display:inline-flex;
    align-items:center;
    gap:6px;
  }
  .project-link svg{ width:14px; height:14px; transition: transform .2s var(--ease); }
  .project-card:hover .project-link svg{ transform: translate(2px,-2px); }
  .project-link.disabled{ color: var(--text-faint); cursor:default; }

  /* ---------- Contact / links ---------- */
  .contact-section{
    background: var(--bg-raised);
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
    text-align:center;
  }
  .contact-section p.lede{ color: var(--text-muted); max-width: 46ch; margin: 14px auto 30px; }
  .link-grid{
    display:grid;
    grid-template-columns: 1fr;
    gap: 12px;
    max-width: 480px;
    margin: 0 auto;
  }
  .link-card{
    display:flex; align-items:center; gap:14px;
    padding: 15px 18px;
    background: var(--bg);
    border: 1px solid var(--line-strong);
    border-radius: var(--radius-sm);
    text-align:left;
    transition: border-color .2s var(--ease), transform .2s var(--ease);
  }
  .link-card:hover{ border-color: var(--accent); transform: translateY(-2px); }
  .link-icon{
    width: 38px; height:38px; border-radius:9px;
    background: var(--bg-raised-2);
    display:flex; align-items:center; justify-content:center;
    color: var(--accent);
    flex-shrink:0;
  }
  .link-icon svg{ width:18px; height:18px; }
  .link-text strong{ display:block; font-size:14px; font-weight:600; }
  .link-text span{ font-size:12px; color: var(--text-faint); }

  /* ---------- Footer ---------- */
  footer{ padding: 34px 0; }
  .footer-inner{
    display:flex; flex-direction:column; gap:8px;
    text-align:center;
    font-size: 12.5px;
    color: var(--text-faint);
  }

  @media (min-width: 640px){
    .quick-facts{ grid-template-columns: repeat(3,1fr); }
    .link-grid{ grid-template-columns: 1fr 1fr; }
  }

  @media (min-width: 720px){
    .projects-grid{ grid-template-columns: repeat(2,1fr); }
  }

  @media (min-width: 920px){
    .hamburger{ display:none; }
    nav.primary-nav{ display:block; }
    .btn-outline{ display:inline-flex; }
    .hero-top{ display:flex; align-items:center; gap:20px; }
    footer .footer-inner{ flex-direction:row; justify-content:space-between; text-align:left; }
  }
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <a href="#top" class="brand" aria-label="Ondřej Košťál — home">
      <span class="brand-text">
        <span class="brand-name">Ondřej Košťál</span>
        <span class="brand-tag">IT Student · CZU</span>
        <span class="status-chip status-chip-sm">
          <span class="status-dot"></span>
          Open to new opportunities
        </span>
      </span>
    </a>

    <nav class="primary-nav" aria-label="Primary navigation">
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>

    <div class="header-actions">
      <a href="#contact" class="btn btn-outline">Contact</a>
      <a href="#projects" class="btn btn-accent">Projects</a>
      <button class="hamburger" id="hamburgerBtn" aria-label="Toggle navigation menu" aria-expanded="false" aria-controls="mobileNav">
        <span><i></i></span>
      </button>
    </div>
  </div>

  <nav class="mobile-nav" id="mobileNav" aria-label="Mobile navigation">
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main id="top">

  <section class="hero" id="about">
    <div class="wrap hero-inner">
      <p class="eyebrow reveal">IT Student &amp; Application Support</p>
      <h1 class="reveal">Ondřej <span>Košťál</span></h1>

      <blockquote class="reveal">
        Information Technology student at the Czech University of Life Sciences Prague (CZU), committed to continuously growing and taking on new technical challenges. Even-tempered and a fast learner, I value persistence in every project I take on. A good cup of coffee and a positive mindset get my mornings started — rain permitting.
      </blockquote>

      <div class="hero-cta reveal">
        <a href="#projects" class="btn btn-accent">View projects</a>
        <a href="#contact" class="btn btn-outline" style="display:inline-flex;">Get in touch</a>
      </div>

      <div class="quick-facts reveal-stagger">
        <div class="fact reveal" style="--i:0">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 10 12 5 2 10l10 5 10-5Z"/><path d="M6 12v5c0 1.1 2.7 2 6 2s6-.9 6-2v-5"/></svg>
          <div><strong>Education</strong><span>Information Technology, CZU</span></div>
        </div>
        <div class="fact reveal" style="--i:1">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="7" width="20" height="14" rx="2"/><path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"/></svg>
          <div><strong>Experience</strong><span>2 years — Application Support (IS/IT)</span></div>
        </div>
        <div class="fact reveal" style="--i:2">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="4 17 10 11 4 5"/><line x1="12" y1="19" x2="20" y2="19"/></svg>
          <div><strong>Focus</strong><span>Python, C#, JavaScript</span></div>
        </div>
      </div>
    </div>
  </section>

  <section id="skills">
    <div class="wrap">
      <div class="section-head reveal">
        <p class="eyebrow">What I know</p>
        <h2>Skills &amp; Experience</h2>
      </div>

      <div class="skills-list reveal-stagger">
        <div class="skill-row reveal" style="--i:0">
          <div class="skill-top"><span class="skill-name">Python</span><span class="skill-level">Basic level</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="40"></div></div>
        </div>
        <div class="skill-row reveal" style="--i:1">
          <div class="skill-top"><span class="skill-name">C#</span><span class="skill-level">Basic level</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="40"></div></div>
        </div>
        <div class="skill-row reveal" style="--i:2">
          <div class="skill-top"><span class="skill-name">JavaScript</span><span class="skill-level">Very basic</span></div>
          <div class="skill-track"><div class="skill-fill" data-width="20"></div></div>
        </div>
      </div>

      <div class="exp-list reveal-stagger">
        <div class="exp-item reveal" style="--i:0">
          <div class="exp-dot"></div>
          <div>
            <div class="exp-role">Application Support (IS/IT)</div>
            <div class="exp-meta">2 YEARS EXPERIENCE</div>
            <p class="exp-desc">Supported internal information systems, resolved user requests, and built small process automations.</p>
          </div>
        </div>
        <div class="exp-item reveal" style="--i:1">
          <div class="exp-dot"></div>
          <div>
            <div class="exp-role">Student — Information Technology</div>
            <div class="exp-meta">CZU · ONGOING</div>
            <p class="exp-desc">Expanding my knowledge of programming and software development while working on personal and academic projects.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="wrap">
      <div class="section-head reveal">
        <p class="eyebrow">What I've built</p>
        <h2>Selected Projects</h2>
      </div>

      <div class="projects-grid reveal-stagger">

        <div class="project-card reveal" style="--i:0">
          <div class="project-top">
            <div class="project-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="16" rx="2"/><path d="M8 2v4M16 2v4M3 10h18"/></svg>
            </div>
            <span class="project-status dev">In development</span>
          </div>
          <h3>CZU Tridant</h3>
          <p class="desc">A tool for checking and booking exam slots at CZU — automates tracking available dates and reserving them.</p>
          <div class="project-tags">
            <span class="project-tag">Python</span>
          </div>
          <span class="project-link disabled" aria-disabled="true">
            Link coming soon
          </span>
        </div>

        <div class="project-card reveal" style="--i:1">
          <div class="project-top">
            <div class="project-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m2 20 6-6M8 8l8 8M14 2l8 8-4 4-8-8Z"/></svg>
            </div>
            <span class="project-status">School project</span>
          </div>
          <h3>AdventureGuide</h3>
          <p class="desc">A console-based adventure game where random dice rolls shape the story. Built as a school project.</p>
          <div class="project-tags">
            <span class="project-tag">C#</span>
            <span class="project-tag">Console App</span>
          </div>
          <span class="project-link disabled" aria-disabled="true">
            Link coming soon
          </span>
        </div>

        <div class="project-card reveal" style="--i:2">
          <div class="project-top">
            <div class="project-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="11" width="18" height="10" rx="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg>
            </div>
            <span class="project-status">Confidential</span>
          </div>
          <h3>Internal Apps Script Automation</h3>
          <p class="desc">A set of automation scripts built in a work environment to simplify repetitive tasks. Details are private due to confidentiality.</p>
          <div class="project-tags">
            <span class="project-tag">Apps Script</span>
            <span class="project-tag">JavaScript</span>
          </div>
          <span class="project-link disabled" aria-disabled="true">
            Private project
          </span>
        </div>

        <div class="project-card reveal" style="--i:3">
          <div class="project-top">
            <div class="project-icon" aria-hidden="true">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="9"/><path d="M12 3a15 15 0 0 0 0 18M12 3a15 15 0 0 1 0 18M3 12h18"/></svg>
            </div>
            <span class="project-status">This website</span>
          </div>
          <h3>Personal CV Website</h3>
          <p class="desc">This page — a responsive personal bio and project overview, built from scratch with plain HTML, CSS, and JavaScript.</p>
          <div class="project-tags">
            <span class="project-tag">HTML</span>
            <span class="project-tag">CSS</span>
            <span class="project-tag">JavaScript</span>
          </div>
          <a href="#top" class="project-link">
            You're looking at it right now
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M7 17 17 7M7 7h10v10"/></svg>
          </a>
        </div>

      </div>
    </div>
  </section>

  <section class="contact-section" id="contact">
    <div class="wrap reveal">
      <p class="eyebrow" style="justify-content:center;">Let's connect</p>
      <h2 style="margin-top:10px; font-size: clamp(22px,4vw,32px);">Contact &amp; Links</h2>
      <p class="lede">The links below will be added soon — for now, this is a placeholder for LinkedIn, GitHub, and email.</p>

      <div class="link-grid">
        <!-- TODO: add real LinkedIn link -->
        <a href="#" class="link-card" aria-label="LinkedIn profile">
          <div class="link-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="3"/><path d="M8 11v5M8 8v.01M12 16v-3a2 2 0 0 1 4 0v3M12 11v5"/></svg>
          </div>
          <div class="link-text"><strong>LinkedIn</strong><span>Link coming soon</span></div>
        </a>
        <!-- TODO: add real GitHub link -->
        <a href="#" class="link-card" aria-label="GitHub profile">
          <div class="link-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-4.3 1.4-4.3-2.5-6-3m12 5v-3.5c0-1 .1-1.4-.5-2 2.8-.3 5.5-1.4 5.5-6a4.6 4.6 0 0 0-1.3-3.2 4.2 4.2 0 0 0-.1-3.2s-1.1-.3-3.5 1.3a12.3 12.3 0 0 0-6.2 0C6.5 2.8 5.4 3.1 5.4 3.1a4.2 4.2 0 0 0-.1 3.2A4.6 4.6 0 0 0 4 9.5c0 4.6 2.7 5.7 5.5 6-.6.6-.6 1.2-.5 2V21"/></svg>
          </div>
          <div class="link-text"><strong>GitHub</strong><span>Link coming soon</span></div>
        </a>
        <!-- TODO: add real email -->
        <a href="#" class="link-card" aria-label="Email">
          <div class="link-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 6 10-6"/></svg>
          </div>
          <div class="link-text"><strong>Email</strong><span>Coming soon</span></div>
        </a>
        <!-- TODO: add any additional link -->
        <a href="#" class="link-card" aria-label="Additional link">
          <div class="link-icon">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M10 13a5 5 0 0 0 7.5.4l2-2a5 5 0 0 0-7-7l-1.1 1.1"/><path d="M14 11a5 5 0 0 0-7.5-.4l-2 2a5 5 0 0 0 7 7l1.1-1.1"/></svg>
          </div>
          <div class="link-text"><strong>Additional link</strong><span>Optional</span></div>
        </a>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap footer-inner">
    <span>© 2026 Ondřej Košťál</span>
    <span>This site was built as a personal project</span>
  </div>
</footer>

<script>
  // Mobile nav toggle
  const hamburgerBtn = document.getElementById('hamburgerBtn');
  const mobileNav = document.getElementById('mobileNav');

  hamburgerBtn.addEventListener('click', () => {
    const isOpen = mobileNav.classList.toggle('open');
    hamburgerBtn.classList.toggle('open', isOpen);
    hamburgerBtn.setAttribute('aria-expanded', String(isOpen));
  });

  mobileNav.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', () => {
      mobileNav.classList.remove('open');
      hamburgerBtn.classList.remove('open');
      hamburgerBtn.setAttribute('aria-expanded', 'false');
    });
  });

  // Scroll-triggered reveal animations
  const revealEls = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window) {
    const io = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('in-view');
          io.unobserve(entry.target);
        }
      });
    }, { threshold: 0.15, rootMargin: '0px 0px -40px 0px' });

    revealEls.forEach(el => io.observe(el));
  } else {
    revealEls.forEach(el => el.classList.add('in-view'));
  }

  // Animate skill bars once visible
  const skillFills = document.querySelectorAll('.skill-fill');
  if ('IntersectionObserver' in window) {
    const skillIo = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const el = entry.target;
          el.style.width = el.dataset.width + '%';
          skillIo.unobserve(el);
        }
      });
    }, { threshold: 0.4 });
    skillFills.forEach(el => skillIo.observe(el));
  } else {
    skillFills.forEach(el => { el.style.width = el.dataset.width + '%'; });
  }
</script>

</body>
</html>
