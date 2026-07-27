<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ondřej Košťál — Design & Development</title>
<meta name="description" content="Ondřej Košťál — multi-disciplinary graphic designer specializing in brand identity, packaging, and digital experiences.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500;600;700;800&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
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
    --maxw: 1180px;
    --font-display: 'Poppins', sans-serif;
    --font-body: 'Inter', sans-serif;
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
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
  }
  img{ max-width:100%; display:block; }
  a{ color: inherit; text-decoration: none; }
  ul{ list-style:none; margin:0; padding:0; }
  h1,h2,h3{ font-family: var(--font-display); margin:0; }
  section{ padding: 88px 0; }
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
    width:18px; height:1px;
    background: var(--accent);
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
  .brand{ display:flex; flex-direction:column; gap:1px; }
  .brand-name{
    font-family: var(--font-display);
    font-weight: 700;
    font-size: 17px;
    letter-spacing: .02em;
  }
  .brand-tag{
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing: .16em;
    text-transform: uppercase;
    color: var(--text-muted);
  }

  nav.primary-nav{ display:none; }
  .primary-nav ul{ display:flex; gap: 34px; }
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

  .header-actions{ display:flex; align-items:center; gap:14px; }
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
  .btn-ghost{
    background: transparent;
    border-color: var(--line-strong);
    color: var(--text);
    display:none;
  }
  .btn-ghost:hover{ border-color: var(--accent); color: var(--accent); }

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

  /* ---------- Hero ---------- */
  .hero{ padding: 64px 0 72px; }
  .hero-inner{
    display:flex;
    flex-direction:column;
    gap: 22px;
  }
  .hero-eyebrow{ margin-bottom: 4px; }
  .hero h1{
    font-size: clamp(34px, 8vw, 64px);
    line-height: 1.06;
    font-weight: 700;
    letter-spacing: -0.01em;
  }
  .hero h1 mark{
    background: var(--accent);
    color: var(--accent-ink);
    padding: 0 10px;
    box-decoration-break: clone;
    -webkit-box-decoration-break: clone;
  }
  .hero p.lede{
    font-size: 17px;
    color: var(--text-muted);
    max-width: 46ch;
  }
  .hero-cta{ display:flex; gap:14px; margin-top:6px; flex-wrap:wrap; }
  .btn-outline{
    background: transparent;
    border-color: var(--line-strong);
    color: var(--text);
  }
  .btn-outline:hover{ border-color: var(--accent); color: var(--accent); transform: translateY(-2px); }

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

  /* ---------- Section headings ---------- */
  .section-head{ margin-bottom: 40px; }
  .section-head h2{
    font-size: clamp(24px, 4.2vw, 34px);
    font-weight: 700;
    margin-top: 10px;
    letter-spacing: -0.01em;
  }

  /* ---------- Services ---------- */
  .services-grid{
    display:grid;
    grid-template-columns: 1fr;
    gap: 16px;
  }
  .service-card{
    background: var(--bg-raised);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    padding: 24px;
    display:flex;
    gap: 16px;
    align-items:flex-start;
    transition: border-color .25s var(--ease), transform .25s var(--ease), background .25s var(--ease);
  }
  .service-card:hover{
    border-color: var(--accent-dim);
    transform: translateY(-4px);
    background: var(--bg-raised-2);
  }
  .service-icon{
    width: 44px; height:44px;
    border-radius: 10px;
    background: var(--accent);
    color: var(--accent-ink);
    display:flex; align-items:center; justify-content:center;
    flex-shrink:0;
  }
  .service-icon svg{ width:22px; height:22px; }
  .service-card h3{ font-size: 17px; font-weight:600; margin-bottom:6px; }
  .service-card p{ font-size:14px; color: var(--text-muted); margin:0; }

  /* ---------- Work grid ---------- */
  .work-grid{
    display:grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
  }
  .work-card{
    border-radius: var(--radius-md);
    overflow:hidden;
    background: var(--bg-raised);
    border: 1px solid var(--line);
    transition: transform .3s var(--ease), border-color .3s var(--ease);
    cursor:pointer;
  }
  .work-card:hover{ transform: translateY(-6px); border-color: var(--accent-dim); }
  .work-thumb{
    aspect-ratio: 4/3;
    overflow:hidden;
    background: var(--bg-raised-2);
  }
  .work-thumb img{
    width:100%; height:100%; object-fit:cover;
    transition: transform .5s var(--ease);
  }
  .work-card:hover .work-thumb img{ transform: scale(1.07); }
  .work-meta{
    padding: 12px 14px 14px;
    display:flex;
    align-items:center;
    justify-content:space-between;
  }
  .work-meta span.name{ font-size:13.5px; font-weight:600; }
  .work-meta span.tag{
    font-family: var(--font-mono);
    font-size: 10px;
    color: var(--text-faint);
    letter-spacing: .05em;
  }

  /* ---------- Tech stack ---------- */
  .stack-section{
    background: var(--bg-raised);
    border-top: 1px solid var(--line);
    border-bottom: 1px solid var(--line);
  }
  .stack-layout{
    display:grid;
    grid-template-columns: 1fr;
    gap: 34px;
    align-items:center;
  }
  .stack-copy p{ color: var(--text-muted); font-size:15px; max-width: 48ch; margin-top: 10px;}
  .stack-list{ margin-top: 22px; display:flex; flex-wrap:wrap; gap:10px; }
  .stack-chip{
    font-family: var(--font-mono);
    font-size: 12px;
    padding: 7px 13px;
    border-radius: 999px;
    border: 1px solid var(--line-strong);
    color: var(--text-muted);
  }
  .terminal{
    background: #0d1210;
    border: 1px solid var(--line-strong);
    border-radius: var(--radius-md);
    overflow:hidden;
    box-shadow: 0 30px 60px -30px rgba(0,0,0,0.6);
  }
  .terminal-bar{
    display:flex; gap:7px;
    padding: 12px 14px;
    background: #101714;
    border-bottom: 1px solid var(--line);
  }
  .terminal-bar span{ width:11px; height:11px; border-radius:50%; }
  .terminal-bar span:nth-child(1){ background:#ff5f56; }
  .terminal-bar span:nth-child(2){ background:#ffbd2e; }
  .terminal-bar span:nth-child(3){ background:#27c93f; }
  .terminal-body{
    font-family: var(--font-mono);
    font-size: 12.5px;
    line-height: 1.9;
    padding: 20px;
    color: #b7c4bd;
    overflow-x:auto;
  }
  .terminal-body .k{ color: var(--accent); }
  .terminal-body .v{ color: #dfe7e3; }
  .terminal-body .c{ color: var(--text-faint); }
  .caret{
    display:inline-block; width:7px; height:14px; background: var(--accent);
    animation: blink 1.1s steps(1) infinite; vertical-align: -2px;
  }
  @keyframes blink{ 50%{ opacity:0; } }

  /* ---------- CTA band ---------- */
  .cta-band{
    text-align:center;
    padding: 100px 0;
  }
  .cta-band h2{ font-size: clamp(26px,5vw,42px); }
  .cta-band p{ color: var(--text-muted); margin: 14px auto 28px; max-width: 44ch; }

  /* ---------- Footer ---------- */
  footer{ border-top: 1px solid var(--line); padding-top: 56px; }
  .footer-grid{
    display:grid;
    grid-template-columns: 1fr;
    gap: 40px;
    padding-bottom: 40px;
  }
  .footer-brand p{ color: var(--text-muted); font-size: 14px; margin-top:12px; max-width: 34ch; }
  .footer-col h4{
    font-family: var(--font-mono);
    font-size: 11px;
    letter-spacing: .12em;
    text-transform: uppercase;
    color: var(--text-faint);
    margin-bottom: 16px;
  }
  .footer-col ul{ display:flex; flex-direction:column; gap: 11px; }
  .footer-col a{ font-size: 14px; color: var(--text-muted); transition: color .2s; }
  .footer-col a:hover{ color: var(--accent); }
  .socials{ display:flex; gap:10px; margin-top:18px; }
  .socials a{
    width:38px; height:38px; border-radius:50%;
    border: 1px solid var(--line-strong);
    display:flex; align-items:center; justify-content:center;
    transition: border-color .2s, color .2s, transform .2s;
  }
  .socials a:hover{ border-color: var(--accent); color: var(--accent); transform: translateY(-3px); }
  .socials svg{ width:16px; height:16px; }
  .footer-bottom{
    border-top: 1px solid var(--line);
    padding: 22px 0 32px;
    display:flex;
    flex-direction:column;
    gap:10px;
    font-size: 12.5px;
    color: var(--text-faint);
  }

  @media (min-width: 700px){
    .work-grid{ grid-template-columns: repeat(3,1fr); }
    .footer-grid{ grid-template-columns: 1.4fr 1fr 1fr 1fr; }
    .services-grid{ grid-template-columns: repeat(3,1fr); }
    .footer-bottom{ flex-direction:row; justify-content:space-between; }
  }

  @media (min-width: 920px){
    .hamburger{ display:none; }
    nav.primary-nav{ display:block; }
    .btn-ghost{ display:inline-flex; }
    .hero-inner{ max-width: 780px; }
    .stack-layout{ grid-template-columns: 1fr 1.15fr; }
  }
</style>
</head>
<body>

<header>
  <div class="header-inner">
    <a href="#top" class="brand" aria-label="Ondřej Košťál — home">
      <span class="brand-name">ONDŘEJ KOŠŤÁL</span>
      <span class="brand-tag">Design &amp; Development</span>
    </a>

    <nav class="primary-nav" aria-label="Primary">
      <ul>
        <li><a href="#top">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#work">Work</a></li>
        <li><a href="#stack">Process</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>

    <div class="header-actions">
      <a href="#contact" class="btn btn-ghost">Get a quote</a>
      <a href="#contact" class="btn btn-accent">Contact</a>
      <button class="hamburger" id="hamburgerBtn" aria-label="Toggle navigation menu" aria-expanded="false" aria-controls="mobileNav">
        <span><i></i></span>
      </button>
    </div>
  </div>

  <nav class="mobile-nav" id="mobileNav" aria-label="Mobile">
    <ul>
      <li><a href="#top">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#stack">Process</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main id="top">

  <section class="hero">
    <div class="wrap hero-inner">
      <p class="eyebrow reveal hero-eyebrow">Brand &amp; Product Designer</p>
      <h1 class="reveal">Engineering <mark>digital experiences</mark> that connect.</h1>
      <p class="lede reveal">A multi-disciplinary graphic designer specializing in brand identity, packaging, and digital experiences — from first sketch to shipped product.</p>
      <div class="hero-cta reveal">
        <a href="#work" class="btn btn-accent">View my portfolio</a>
        <a href="#contact" class="btn btn-outline">Start a project</a>
      </div>
    </div>
  </section>

  <section id="services">
    <div class="wrap">
      <div class="section-head reveal">
        <p class="eyebrow">What I do</p>
        <h2>My creative services</h2>
      </div>
      <div class="services-grid reveal-stagger">
        <div class="service-card reveal" style="--i:0">
          <div class="service-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="8" r="4"/><path d="M4 21c0-4.4 3.6-8 8-8s8 3.6 8 8"/></svg>
          </div>
          <div>
            <h3>Brand Identity</h3>
            <p>Logos, type systems, and visual guidelines built to hold up across every touchpoint a brand shows up in.</p>
          </div>
        </div>
        <div class="service-card reveal" style="--i:1">
          <div class="service-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 8 12 3 3 8l9 5 9-5Z"/><path d="M3 8v8l9 5 9-5V8"/><path d="M12 13v8"/></svg>
          </div>
          <div>
            <h3>Packaging Design</h3>
            <p>Structural and surface design for physical products — from concept sketches to print-ready files.</p>
          </div>
        </div>
        <div class="service-card reveal" style="--i:2">
          <div class="service-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="13" rx="2"/><path d="M8 21h8M12 17v4"/></svg>
          </div>
          <div>
            <h3>Digital Experience</h3>
            <p>Interfaces and interactions for web and mobile, designed and built with equal attention to both.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="work">
    <div class="wrap">
      <div class="section-head reveal">
        <p class="eyebrow">Selected work</p>
        <h2>Recent projects</h2>
      </div>
      <div class="work-grid reveal-stagger">
        <div class="work-card reveal" style="--i:0">
          <div class="work-thumb"><img src="https://placehold.co/480x360/1a1512/e8ddd3?text=Cosmetics" alt="Cosmetics brand packaging set on a warm neutral backdrop" loading="lazy"></div>
          <div class="work-meta"><span class="name">Cosmetics</span><span class="tag">BRANDING</span></div>
        </div>
        <div class="work-card reveal" style="--i:1">
          <div class="work-thumb"><img src="https://placehold.co/480x360/2b1f16/d8b98d?text=K%C3%A1va" alt="Coffee bag packaging design mockup" loading="lazy"></div>
          <div class="work-meta"><span class="name">Káva</span><span class="tag">PACKAGING</span></div>
        </div>
        <div class="work-card reveal" style="--i:2">
          <div class="work-thumb"><img src="https://placehold.co/480x360/2f3fae/ffffff?text=Aplikace" alt="Mobile app UI shown on three phone mockups" loading="lazy"></div>
          <div class="work-meta"><span class="name">Aplikace</span><span class="tag">PRODUCT</span></div>
        </div>
        <div class="work-card reveal" style="--i:3">
          <div class="work-thumb"><img src="https://placehold.co/480x360/6ef0c2/06231a?text=Aplikace" alt="Mobile onboarding app screens with mint accent" loading="lazy"></div>
          <div class="work-meta"><span class="name">Aplikace</span><span class="tag">PRODUCT</span></div>
        </div>
        <div class="work-card reveal" style="--i:4">
          <div class="work-thumb"><img src="https://placehold.co/480x360/4a3a2c/e0c9a6?text=Apince" alt="E-reader device product photography" loading="lazy"></div>
          <div class="work-meta"><span class="name">Apince</span><span class="tag">PRODUCT</span></div>
        </div>
        <div class="work-card reveal" style="--i:5">
          <div class="work-thumb"><img src="https://placehold.co/480x360/d9d9d9/2b2b2b?text=%C4%8Casopis" alt="Magazine cover layout design" loading="lazy"></div>
          <div class="work-meta"><span class="name">Časopis</span><span class="tag">EDITORIAL</span></div>
        </div>
      </div>
    </div>
  </section>

  <section id="stack" class="stack-section">
    <div class="wrap">
      <div class="stack-layout">
        <div class="stack-copy reveal">
          <p class="eyebrow">How it gets built</p>
          <h2 style="font-size: clamp(22px,3.6vw,30px); margin-top:10px; font-weight:700;">Technical stack &amp; process</h2>
          <p>Design and development live in the same hands here, so what ships matches what was designed — no handoff drift, no lost detail.</p>
          <div class="stack-list">
            <span class="stack-chip">Figma</span>
            <span class="stack-chip">React</span>
            <span class="stack-chip">JavaScript</span>
            <span class="stack-chip">CSS</span>
            <span class="stack-chip">Node.js</span>
            <span class="stack-chip">Framer Motion</span>
          </div>
        </div>
        <div class="terminal reveal">
          <div class="terminal-bar"><span></span><span></span><span></span></div>
          <div class="terminal-body">
<span class="c">~/studio</span> <span class="k">$</span> <span class="v">./process.sh</span>
<span class="c">01</span> <span class="k">discover</span>  <span class="v">brief, audience, constraints</span>
<span class="c">02</span> <span class="k">design</span>    <span class="v">system, layout, prototype</span>
<span class="c">03</span> <span class="k">build</span>     <span class="v">component-driven, responsive</span>
<span class="c">04</span> <span class="k">review</span>    <span class="v">a11y, performance, QA</span>
<span class="c">05</span> <span class="k">ship</span>      <span class="v">deploy &amp; hand off</span>

<span class="c">status</span>  <span class="v">available for new projects</span><span class="caret"></span>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="cta-band" id="contact">
    <div class="wrap reveal">
      <p class="eyebrow" style="justify-content:center;">Let's work together</p>
      <h2 style="margin-top:10px;">Have a project in mind?</h2>
      <p>I'm currently taking on a small number of new engagements — tell me about your brand and where it needs to go.</p>
      <a href="mailto:info@ondfal.com" class="btn btn-accent">info@ondfal.com</a>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">
    <div class="footer-grid">
      <div class="footer-brand reveal">
        <span class="brand-name" style="font-size:18px;">ONDŘEJ KOŠŤÁL</span>
        <p>Multi-disciplinary graphic designer specializing in brand identity, packaging, and digital experiences.</p>
        <div class="socials">
          <a href="#" aria-label="Facebook"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M17 3h-3a4 4 0 0 0-4 4v3H7v4h3v7h4v-7h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg></a>
          <a href="#" aria-label="Instagram"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1"/></svg></a>
          <a href="#" aria-label="Twitter / X"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="m4 4 16 16M20 4 4 20"/></svg></a>
          <a href="#" aria-label="LinkedIn"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="3"/><path d="M8 11v5M8 8v.01M12 16v-3a2 2 0 0 1 4 0v3M12 11v5"/></svg></a>
        </div>
      </div>
      <div class="footer-col reveal">
        <h4>Sitemap</h4>
        <ul>
          <li><a href="#top">Home</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#work">Work</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
      <div class="footer-col reveal">
        <h4>Studio</h4>
        <ul>
          <li><a href="#">About</a></li>
          <li><a href="#">Blog</a></li>
          <li><a href="#">Careers</a></li>
        </ul>
      </div>
      <div class="footer-col reveal">
        <h4>Contact</h4>
        <ul>
          <li><a href="tel:+420903533630">+420 903 533 630</a></li>
          <li><a href="mailto:info@ondfal.com">info@ondfal.com</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 Ondřej Košťál. All rights reserved.</span>
      <span>Design &amp; Development by Ondřej Košťál</span>
    </div>
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
</script>

</body>
</html>
