<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Prudhvi Simha Reddy — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #060810;
    --bg2: #0C0F1E;
    --accent: #4F8EFF;
    --accent2: #FF6B6B;
    --gold: #FFD166;
    --text: #E8EDF8;
    --muted: #6B7699;
    --card: rgba(255,255,255,0.04);
    --border: rgba(255,255,255,0.07);
  }
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── NOISE OVERLAY ── */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none; z-index: 0; opacity: 0.4;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0;
    display: flex; align-items: center; justify-content: space-between;
    padding: 18px 6vw;
    background: rgba(6,8,16,0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid var(--border);
    z-index: 100;
  }
  .nav-logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800; font-size: 18px;
    background: linear-gradient(90deg, var(--accent), var(--gold));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    letter-spacing: -0.5px;
  }
  .nav-links { display: flex; gap: 28px; }
  .nav-links a {
    color: var(--muted); text-decoration: none; font-size: 13px;
    font-weight: 500; letter-spacing: 0.5px; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--text); }

  /* ── SECTIONS ── */
  section { position: relative; z-index: 1; }
  .container { max-width: 900px; margin: 0 auto; padding: 0 6vw; }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex; align-items: center;
    padding: 100px 6vw 60px;
    position: relative; overflow: hidden;
  }
  .hero-glow {
    position: absolute; top: -100px; right: -100px;
    width: 600px; height: 600px; border-radius: 50%;
    background: radial-gradient(circle, rgba(79,142,255,0.12) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-glow2 {
    position: absolute; bottom: -80px; left: -80px;
    width: 400px; height: 400px; border-radius: 50%;
    background: radial-gradient(circle, rgba(255,107,107,0.08) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-inner { max-width: 900px; margin: 0 auto; width: 100%; }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(79,142,255,0.12); border: 1px solid rgba(79,142,255,0.25);
    border-radius: 30px; padding: 6px 16px;
    font-size: 12px; font-weight: 500; color: var(--accent);
    letter-spacing: 0.5px; margin-bottom: 28px;
    animation: fadeUp 0.6s ease both;
  }
  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(42px, 8vw, 78px);
    font-weight: 800; line-height: 1.0;
    letter-spacing: -2px;
    animation: fadeUp 0.6s 0.1s ease both;
  }
  .hero-name span {
    background: linear-gradient(135deg, var(--accent) 0%, var(--gold) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  .hero-title {
    font-size: 18px; color: var(--muted); margin-top: 16px; font-weight: 300;
    animation: fadeUp 0.6s 0.2s ease both;
  }
  .hero-desc {
    font-size: 15px; color: var(--muted); max-width: 520px;
    margin-top: 14px; line-height: 1.8;
    animation: fadeUp 0.6s 0.3s ease both;
  }
  .hero-actions {
    display: flex; gap: 14px; margin-top: 36px; flex-wrap: wrap;
    animation: fadeUp 0.6s 0.4s ease both;
  }
  .btn-primary {
    display: inline-flex; align-items: center; gap: 8px;
    background: linear-gradient(135deg, var(--accent), #2563EB);
    color: #fff; text-decoration: none;
    padding: 14px 28px; border-radius: 14px;
    font-weight: 600; font-size: 14px;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 4px 20px rgba(79,142,255,0.3);
  }
  .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(79,142,255,0.4); }
  .btn-secondary {
    display: inline-flex; align-items: center; gap: 8px;
    background: var(--card); border: 1px solid var(--border);
    color: var(--text); text-decoration: none;
    padding: 14px 28px; border-radius: 14px;
    font-weight: 600; font-size: 14px;
    transition: all 0.2s;
  }
  .btn-secondary:hover { background: rgba(255,255,255,0.08); border-color: rgba(255,255,255,0.15); }

  .hero-stats {
    display: flex; gap: 36px; margin-top: 52px; flex-wrap: wrap;
    animation: fadeUp 0.6s 0.5s ease both;
  }
  .stat-item { }
  .stat-num {
    font-family: 'Syne', sans-serif; font-size: 30px;
    font-weight: 800; color: var(--text);
    background: linear-gradient(90deg, var(--accent), var(--gold));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  .stat-label { font-size: 12px; color: var(--muted); margin-top: 2px; }

  /* ── SECTION HEADING ── */
  .sec-label {
    font-size: 11px; font-weight: 600; letter-spacing: 3px;
    color: var(--accent); text-transform: uppercase; margin-bottom: 10px;
  }
  .sec-title {
    font-family: 'Syne', sans-serif; font-size: clamp(26px, 4vw, 38px);
    font-weight: 800; letter-spacing: -1px; line-height: 1.1;
    margin-bottom: 12px;
  }
  .sec-sub { color: var(--muted); font-size: 14px; max-width: 480px; }

  /* ── ABOUT ── */
  #about { padding: 100px 6vw; }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 48px; align-items: center; margin-top: 48px; }
  .about-card {
    background: var(--card); border: 1px solid var(--border);
    border-radius: 24px; padding: 28px;
  }
  .contact-row { display: flex; flex-direction: column; gap: 14px; margin-top: 20px; }
  .contact-item {
    display: flex; align-items: center; gap: 14px;
    background: rgba(255,255,255,0.03); border-radius: 12px; padding: 12px 16px;
    border: 1px solid var(--border);
  }
  .contact-icon { font-size: 20px; width: 32px; text-align: center; flex-shrink: 0; }
  .contact-val { font-size: 13px; font-weight: 500; color: var(--text); }
  .contact-key { font-size: 11px; color: var(--muted); }
  .about-text p { color: var(--muted); line-height: 1.9; margin-bottom: 14px; font-size: 14px; }
  .skill-chips { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 20px; }
  .chip {
    background: rgba(79,142,255,0.1); border: 1px solid rgba(79,142,255,0.2);
    color: var(--accent); border-radius: 8px; padding: 5px 12px;
    font-size: 12px; font-weight: 500;
  }
  .chip.orange { background: rgba(255,209,102,0.1); border-color: rgba(255,209,102,0.2); color: var(--gold); }
  .chip.red { background: rgba(255,107,107,0.1); border-color: rgba(255,107,107,0.2); color: var(--accent2); }

  /* ── PROJECTS ── */
  #projects { padding: 100px 6vw; background: linear-gradient(180deg, transparent, rgba(79,142,255,0.03), transparent); }
  .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; margin-top: 48px; }
  .project-card {
    background: var(--card); border: 1px solid var(--border);
    border-radius: 20px; padding: 26px; position: relative; overflow: hidden;
    transition: transform 0.25s, border-color 0.25s, box-shadow 0.25s;
  }
  .project-card::before {
    content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, var(--accent), var(--gold));
    opacity: 0; transition: opacity 0.3s;
  }
  .project-card:hover { transform: translateY(-6px); border-color: rgba(79,142,255,0.3); box-shadow: 0 20px 50px rgba(0,0,0,0.4); }
  .project-card:hover::before { opacity: 1; }
  .project-icon { font-size: 32px; margin-bottom: 16px; }
  .project-title { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 16px; margin-bottom: 8px; }
  .project-desc { font-size: 13px; color: var(--muted); line-height: 1.7; margin-bottom: 16px; }
  .patent-badge {
    display: inline-flex; align-items: center; gap: 6px;
    background: rgba(255,209,102,0.1); border: 1px solid rgba(255,209,102,0.25);
    color: var(--gold); border-radius: 8px; padding: 4px 10px;
    font-size: 11px; font-weight: 600;
  }

  /* ── EDUCATION ── */
  #education { padding: 100px 6vw; }
  .edu-timeline { margin-top: 48px; position: relative; }
  .edu-timeline::before {
    content: ''; position: absolute; left: 20px; top: 0; bottom: 0;
    width: 2px; background: linear-gradient(180deg, var(--accent), transparent);
  }
  .edu-item {
    display: flex; gap: 28px; padding-left: 60px; margin-bottom: 36px;
    position: relative;
  }
  .edu-dot {
    position: absolute; left: 12px; top: 8px;
    width: 18px; height: 18px; border-radius: 50%;
    background: var(--accent); border: 3px solid var(--bg);
    box-shadow: 0 0 0 3px rgba(79,142,255,0.3);
  }
  .edu-card {
    background: var(--card); border: 1px solid var(--border);
    border-radius: 18px; padding: 22px 24px; flex: 1;
    transition: border-color 0.2s;
  }
  .edu-card:hover { border-color: rgba(79,142,255,0.3); }
  .edu-school { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 16px; }
  .edu-degree { font-size: 13px; color: var(--muted); margin-top: 4px; }
  .edu-meta { display: flex; gap: 16px; margin-top: 12px; flex-wrap: wrap; }
  .edu-tag {
    font-size: 11px; font-weight: 600; padding: 3px 10px;
    border-radius: 6px; background: rgba(79,142,255,0.1);
    color: var(--accent); border: 1px solid rgba(79,142,255,0.2);
  }
  .edu-tag.year { background: rgba(255,255,255,0.05); color: var(--muted); border-color: var(--border); }

  /* ── ACHIEVEMENTS ── */
  #achievements { padding: 100px 6vw; background: linear-gradient(180deg, transparent, rgba(255,107,107,0.03), transparent); }
  .ach-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px; margin-top: 48px; }
  .ach-card {
    background: var(--card); border: 1px solid var(--border);
    border-radius: 18px; padding: 22px;
    transition: transform 0.2s, border-color 0.2s;
  }
  .ach-card:hover { transform: translateY(-4px); border-color: rgba(255,209,102,0.3); }
  .ach-icon { font-size: 28px; margin-bottom: 12px; }
  .ach-title { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 14px; margin-bottom: 6px; }
  .ach-desc { font-size: 12px; color: var(--muted); line-height: 1.6; }

  /* ── CONTACT ── */
  #contact { padding: 100px 6vw 60px; }
  .contact-hero {
    text-align: center; max-width: 560px; margin: 0 auto;
  }
  .contact-cards { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; margin-top: 40px; }
  .contact-card {
    display: flex; align-items: center; gap: 14px;
    background: var(--card); border: 1px solid var(--border);
    border-radius: 18px; padding: 18px 24px;
    text-decoration: none; color: var(--text);
    transition: all 0.2s; min-width: 200px;
  }
  .contact-card:hover { background: rgba(79,142,255,0.1); border-color: rgba(79,142,255,0.3); transform: translateY(-3px); }
  .cc-icon { font-size: 24px; }
  .cc-label { font-size: 11px; color: var(--muted); }
  .cc-val { font-size: 13px; font-weight: 600; }

  /* ── FOOTER ── */
  footer {
    text-align: center; padding: 32px 6vw;
    border-top: 1px solid var(--border);
    font-size: 12px; color: var(--muted);
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
  }

  /* ── SOCIAL LINKS BAR ── */
  .social-bar {
    display: flex; gap: 10px; margin-top: 28px; flex-wrap: wrap;
    animation: fadeUp 0.6s 0.45s ease both;
  }
  .social-link {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 8px 16px; border-radius: 10px;
    text-decoration: none; font-size: 13px; font-weight: 600;
    border: 1px solid var(--border); background: var(--card);
    color: var(--text); transition: all 0.2s;
    position: relative; overflow: hidden;
  }
  .social-link::before {
    content: ''; position: absolute; inset: 0;
    opacity: 0; transition: opacity 0.2s;
  }
  .social-link:hover { transform: translateY(-2px); }
  .social-link.linkedin { border-color: rgba(10,102,194,0.4); }
  .social-link.linkedin::before { background: rgba(10,102,194,0.12); }
  .social-link.linkedin:hover { border-color: rgba(10,102,194,0.7); color: #0a66c2; }
  .social-link.linkedin:hover::before { opacity: 1; }
  .social-link.github { border-color: rgba(255,255,255,0.12); }
  .social-link.github::before { background: rgba(255,255,255,0.06); }
  .social-link.github:hover { border-color: rgba(255,255,255,0.3); color: #fff; }
  .social-link.github:hover::before { opacity: 1; }
  .social-link.leetcode { border-color: rgba(255,161,22,0.3); }
  .social-link.leetcode::before { background: rgba(255,161,22,0.08); }
  .social-link.leetcode:hover { border-color: rgba(255,161,22,0.6); color: #FFA116; }
  .social-link.leetcode:hover::before { opacity: 1; }
  .social-link svg { flex-shrink: 0; position: relative; z-index: 1; }
  .social-link span { position: relative; z-index: 1; }

  /* ── OPEN TO WORK BADGE ── */
  .open-to-work {
    display: inline-flex; align-items: center; gap: 8px;
    background: rgba(34,197,94,0.1); border: 1px solid rgba(34,197,94,0.3);
    border-radius: 30px; padding: 6px 16px;
    font-size: 12px; font-weight: 600; color: #22c55e;
    letter-spacing: 0.3px; margin-bottom: 16px;
    animation: fadeUp 0.6s ease both;
  }
  .open-to-work::before {
    content: ''; width: 7px; height: 7px; border-radius: 50%;
    background: #22c55e;
    box-shadow: 0 0 0 0 rgba(34,197,94,0.4);
    animation: pulse-green 2s infinite;
  }
  @keyframes pulse-green {
    0% { box-shadow: 0 0 0 0 rgba(34,197,94,0.5); }
    70% { box-shadow: 0 0 0 8px rgba(34,197,94,0); }
    100% { box-shadow: 0 0 0 0 rgba(34,197,94,0); }
  }

  /* ── FLOATING HIRE ME BUTTON ── */
  .hire-me-float {
    position: fixed; bottom: 28px; right: 28px;
    display: flex; align-items: center; gap: 8px;
    background: linear-gradient(135deg, var(--accent), #2563EB);
    color: #fff; text-decoration: none;
    padding: 13px 22px; border-radius: 50px;
    font-weight: 700; font-size: 13px;
    box-shadow: 0 8px 30px rgba(79,142,255,0.45);
    z-index: 200; transition: transform 0.2s, box-shadow 0.2s;
    letter-spacing: 0.3px;
  }
  .hire-me-float:hover { transform: translateY(-3px) scale(1.03); box-shadow: 0 14px 40px rgba(79,142,255,0.55); }
  .hire-me-float .dot {
    width: 7px; height: 7px; border-radius: 50%; background: #22c55e;
    animation: pulse-green 2s infinite;
  }

  /* ── SKILLS WITH BARS ── */
  .skills-section { margin-top: 28px; }
  .skill-bar-item { margin-bottom: 14px; }
  .skill-bar-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 6px; }
  .skill-bar-name { font-size: 12px; font-weight: 600; color: var(--text); }
  .skill-bar-pct { font-size: 11px; color: var(--muted); font-weight: 500; }
  .skill-bar-track {
    height: 5px; background: rgba(255,255,255,0.06);
    border-radius: 10px; overflow: hidden;
  }
  .skill-bar-fill {
    height: 100%; border-radius: 10px;
    background: linear-gradient(90deg, var(--accent), var(--gold));
    width: 0; transition: width 1.2s cubic-bezier(0.4,0,0.2,1);
  }
  .skill-bar-fill.red { background: linear-gradient(90deg, var(--accent2), var(--gold)); }

  /* ── LINKEDIN CARD IN ABOUT (upgraded) ── */
  .linkedin-card-link {
    display: flex; align-items: center; gap: 14px;
    background: rgba(10,102,194,0.08); border: 1px solid rgba(10,102,194,0.25);
    border-radius: 12px; padding: 12px 16px;
    text-decoration: none; transition: all 0.2s;
  }
  .linkedin-card-link:hover { background: rgba(10,102,194,0.15); border-color: rgba(10,102,194,0.5); transform: translateX(4px); }
  .linkedin-card-link .contact-key { color: var(--muted); }
  .linkedin-card-link .contact-val { color: #0a66c2; font-weight: 600; }

  /* ── RESPONSIVE ── */
  @media (max-width: 680px) {
    .about-grid { grid-template-columns: 1fr; }
    .hero-stats { gap: 24px; }
    nav .nav-links { display: none; }
    .hire-me-float { bottom: 16px; right: 16px; padding: 11px 18px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Prudhvi.dev</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#education">Education</a>
    <a href="#achievements">Achievements</a>
    <a href="#contact">Contact</a>
    <a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" style="display:inline-flex;align-items:center;gap:5px;color:#0a66c2 !important;">
      <svg width="13" height="13" viewBox="0 0 24 24" fill="#0a66c2"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-glow"></div>
  <div class="hero-glow2"></div>
  <div class="hero-inner">
    <div class="open-to-work">Open to Work — Fresher · CSE · 2026</div>
    <div class="hero-badge" style="margin-bottom:20px;">🎓 B.Tech CSE · Mohan Babu University · 2026</div>
    <h1 class="hero-name">
      Machupalli<br/><span>Prudhvi Simha</span><br/>Reddy
    </h1>
    <div class="hero-title">Computer Science Engineer · Innovator · 3× Patent Holder</div>
    <p class="hero-desc">
      Final-year CSE student passionate about building tech that matters — from AI-powered battery systems to web applications. Hands-on experience in community development and frontend engineering.
    </p>
    <div class="hero-actions">
      <a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" class="btn-primary">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        Connect on LinkedIn
      </a>
      <a href="#projects" class="btn-secondary">🔬 View Projects</a>
    </div>

    <!-- SOCIAL BAR -->
    <div class="social-bar">
      <a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" class="social-link linkedin">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        <span>LinkedIn</span>
      </a>
      <a href="https://github.com/prudhvi-reddy" target="_blank" class="social-link github">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
        <span>GitHub</span>
      </a>
      <a href="https://leetcode.com/prudhvi" target="_blank" class="social-link leetcode">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.545 2.545 0 0 1 .619-1.164L9.13 8.114c1.058-1.134 3.204-1.27 4.43-.278l3.501 2.831c.593.48 1.461.387 1.94-.207a1.384 1.384 0 0 0-.207-1.943l-3.5-2.831c-.8-.647-1.766-1.045-2.774-1.202l2.015-2.158A1.384 1.384 0 0 0 13.483 0zm-2.866 12.815a1.38 1.38 0 0 0-1.38 1.382 1.38 1.38 0 0 0 1.38 1.382H19.48a1.38 1.38 0 0 0 1.38-1.382 1.38 1.38 0 0 0-1.38-1.382z"/></svg>
        <span>LeetCode</span>
      </a>
      <a href="mailto:prudhvireddy00091@gmail.com" class="social-link" style="border-color:rgba(255,107,107,0.3);" onmouseover="this.style.borderColor='rgba(255,107,107,0.6)';this.style.color='#FF6B6B'" onmouseout="this.style.borderColor='rgba(255,107,107,0.3)';this.style.color=''">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="currentColor"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
        <span>Email</span>
      </a>
    </div>
    <div class="hero-stats">
      <div class="stat-item">
        <div class="stat-num">3</div>
        <div class="stat-label">Patents Filed</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">4+</div>
        <div class="stat-label">Projects Built</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">2026</div>
        <div class="stat-label">Graduating</div>
      </div>
      <div class="stat-item">
        <div class="stat-num">5+</div>
        <div class="stat-label">Certifications</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="sec-label">Who I Am</div>
    <h2 class="sec-title">About Me</h2>
    <p class="sec-sub">A driven engineer from Tirupati with a love for innovation and community impact.</p>

    <div class="about-grid">
      <div class="about-text">
        <p>
          I'm Prudhvi Simha Reddy, a final-year B.Tech Computer Science student at Mohan Babu University, Tirupati. I'm passionate about solving real-world problems through technology — whether that's developing AI systems, building web apps, or leading community projects.
        </p>
        <p>
          I've successfully filed 3 patents in areas like AI-based battery management and sustainable energy — reflecting my drive to create meaningful, patentable innovations before even graduating.
        </p>
        <p>
          Beyond coding, I'm a team leader and communicator who has actively participated in NSS and CSR activities, working with villagers using KoboToolKit for rural development.
        </p>
        <div class="skills-section">
          <div style="font-size:11px;font-weight:600;letter-spacing:2px;color:var(--accent);text-transform:uppercase;margin-bottom:16px;">Technical Proficiency</div>
          <div class="skill-bar-item">
            <div class="skill-bar-header"><span class="skill-bar-name">HTML / CSS</span><span class="skill-bar-pct">85%</span></div>
            <div class="skill-bar-track"><div class="skill-bar-fill" data-width="85"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-header"><span class="skill-bar-name">JavaScript</span><span class="skill-bar-pct">70%</span></div>
            <div class="skill-bar-track"><div class="skill-bar-fill" data-width="70"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-header"><span class="skill-bar-name">Java</span><span class="skill-bar-pct">75%</span></div>
            <div class="skill-bar-track"><div class="skill-bar-fill" data-width="75"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-header"><span class="skill-bar-name">Python</span><span class="skill-bar-pct">65%</span></div>
            <div class="skill-bar-track"><div class="skill-bar-fill red" data-width="65"></div></div>
          </div>
          <div class="skill-bar-item">
            <div class="skill-bar-header"><span class="skill-bar-name">Git & Version Control</span><span class="skill-bar-pct">70%</span></div>
            <div class="skill-bar-track"><div class="skill-bar-fill red" data-width="70"></div></div>
          </div>
        </div>
        <div class="skill-chips" style="margin-top:18px;">
          <span class="chip orange">Git</span>
          <span class="chip orange">VS Code</span>
          <span class="chip orange">KoboToolKit</span>
          <span class="chip orange">MS Office</span>
          <span class="chip red">Team Lead</span>
          <span class="chip red">Project Management</span>
          <span class="chip red">Problem Solving</span>
        </div>
      </div>
      <div>
        <div class="about-card">
          <div class="sec-label" style="margin-bottom:6px;">Contact Info</div>
          <div class="contact-row">
            <div class="contact-item">
              <div class="contact-icon">📱</div>
              <div>
                <div class="contact-key">Phone</div>
                <div class="contact-val">+91 9392994305</div>
              </div>
            </div>
            <div class="contact-item">
              <div class="contact-icon">📧</div>
              <div>
                <div class="contact-key">Email</div>
                <div class="contact-val" style="font-size:12px;">prudhvireddy00091@gmail.com</div>
              </div>
            </div>
            <a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" class="linkedin-card-link">
              <div style="font-size:20px; width:32px; text-align:center; flex-shrink:0; display:flex; align-items:center; justify-content:center;">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="#0a66c2"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
              </div>
              <div>
                <div class="contact-key">LinkedIn — Click to Visit ↗</div>
                <div class="contact-val">prudhvi-reddy-81b839295</div>
              </div>
            </a>
            <div class="contact-item">
              <div class="contact-icon">📍</div>
              <div>
                <div class="contact-key">Location</div>
                <div class="contact-val">Tirupati, Andhra Pradesh</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="container">
    <div class="sec-label">What I've Built</div>
    <h2 class="sec-title">Projects & Patents</h2>
    <p class="sec-sub">From AI systems to web apps — built with purpose and backed by patents.</p>

    <div class="projects-grid">
      <div class="project-card">
        <div class="project-icon">🔋</div>
        <div class="project-title">EV Battery Management System Using AI</div>
        <div class="project-desc">
          An AI-powered system designed to intelligently manage Electric Vehicle batteries — optimizing charge cycles, predicting failures, and extending battery life using machine learning techniques.
        </div>
        <div class="patent-badge">🏅 Patent: 202541038428</div>
      </div>

      <div class="project-card">
        <div class="project-icon">⚡</div>
        <div class="project-title">Energy from Rotational Motors</div>
        <div class="project-desc">
          An innovative energy harvesting system that converts rotational motion from fans and motors into usable electrical energy — promoting sustainable and renewable energy solutions.
        </div>
        <div class="patent-badge">🏅 Patent: 202541015013</div>
      </div>

      <div class="project-card">
        <div class="project-icon">🤖</div>
        <div class="project-title">Fire Fighting Robot</div>
        <div class="project-desc">
          An autonomous robot capable of detecting fires using sensors and suppressing them without human intervention — designed for industrial and emergency use cases.
        </div>
        <div class="patent-badge">🏅 Patent: 202541017699</div>
      </div>

      <div class="project-card">
        <div class="project-icon">✈️</div>
        <div class="project-title">Trip Buddy — Budget Planner</div>
        <div class="project-desc">
          A web application designed to help travelers plan and manage their trip budgets efficiently. Built with HTML, CSS, and JavaScript with an intuitive, user-friendly interface.
        </div>
        <div style="margin-top:12px;">
          <span class="chip" style="font-size:11px;">HTML</span>
          <span class="chip" style="font-size:11px; margin-left:6px;">CSS</span>
          <span class="chip" style="font-size:11px; margin-left:6px;">JavaScript</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="container">
    <div class="sec-label">Academic Journey</div>
    <h2 class="sec-title">Education</h2>
    <p class="sec-sub">A consistent academic journey from school to engineering.</p>

    <div class="edu-timeline">
      <div class="edu-item">
        <div class="edu-dot"></div>
        <div class="edu-card">
          <div class="edu-school">Mohan Babu University</div>
          <div class="edu-degree">B.Tech in Computer Science and Engineering</div>
          <div class="edu-meta">
            <span class="edu-tag year">📅 2022 – 2026</span>
            <span class="edu-tag">📍 Tirupati</span>
            <span class="edu-tag" style="background:rgba(255,209,102,0.1);color:var(--gold);border-color:rgba(255,209,102,0.2);">🎓 Final Year</span>
          </div>
        </div>
      </div>

      <div class="edu-item">
        <div class="edu-dot" style="background: var(--gold); box-shadow: 0 0 0 3px rgba(255,209,102,0.3);"></div>
        <div class="edu-card">
          <div class="edu-school">Blue Moon Jr. College</div>
          <div class="edu-degree">Secondary Education (Intermediate)</div>
          <div class="edu-meta">
            <span class="edu-tag year">📅 2020 – 2022</span>
            <span class="edu-tag" style="background:rgba(255,209,102,0.1);color:var(--gold);border-color:rgba(255,209,102,0.2);">Board of Intermediate Education</span>
          </div>
        </div>
      </div>

      <div class="edu-item">
        <div class="edu-dot" style="background: var(--accent2); box-shadow: 0 0 0 3px rgba(255,107,107,0.3);"></div>
        <div class="edu-card">
          <div class="edu-school">Sree Valmeeki High School</div>
          <div class="edu-degree">SSC — Secondary School Certificate</div>
          <div class="edu-meta">
            <span class="edu-tag year">📅 2019 – 2020</span>
            <span class="edu-tag" style="background:rgba(255,107,107,0.1);color:var(--accent2);border-color:rgba(255,107,107,0.2);">Board of Secondary Education</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements">
  <div class="container">
    <div class="sec-label">Recognition & Involvement</div>
    <h2 class="sec-title">Achievements</h2>
    <p class="sec-sub">Certifications, community work, and leadership experience.</p>

    <div class="ach-grid">
      <div class="ach-card">
        <div class="ach-icon">☁️</div>
        <div class="ach-title">Salesforce Virtual Internship</div>
        <div class="ach-desc">Successfully completed Salesforce's virtual internship program, gaining hands-on CRM and cloud platform experience.</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">🏆</div>
        <div class="ach-title">TCS ION Career Edge</div>
        <div class="ach-desc">Completed the TCS ION Young Professional certification — covering professional skills, communication, and workplace readiness.</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">🤝</div>
        <div class="ach-title">NSS — National Service Scheme</div>
        <div class="ach-desc">Active NSS volunteer contributing to community service, social awareness, environmental initiatives, and building leadership skills.</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">🌾</div>
        <div class="ach-title">CSR Community Projects — ICCSPL</div>
        <div class="ach-desc">Led CSR fundraising projects using KoboToolKit to engage with villagers and support rural community development.</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">💡</div>
        <div class="ach-title">3× Patent Holder</div>
        <div class="ach-desc">Filed and received approval numbers for 3 innovative patents in AI, renewable energy, and robotics — all before graduation.</div>
      </div>
      <div class="ach-card">
        <div class="ach-icon">👨‍💼</div>
        <div class="ach-title">Team Lead & Project Manager</div>
        <div class="ach-desc">Proven track record of leading teams in academic projects, community initiatives, and technical competitions.</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="contact-hero">
      <div class="sec-label">Let's Connect</div>
      <h2 class="sec-title">Get In Touch</h2>
      <p class="sec-sub" style="margin: 0 auto;">Whether it's a job opportunity, project collaboration, or just a hello — I'd love to hear from you.</p>
      <div class="contact-cards">
        <a href="tel:+919392994305" class="contact-card">
          <div class="cc-icon">📱</div>
          <div>
            <div class="cc-label">Phone</div>
            <div class="cc-val">+91 9392994305</div>
          </div>
        </a>
        <a href="mailto:prudhvireddy00091@gmail.com" class="contact-card">
          <div class="cc-icon">📧</div>
          <div>
            <div class="cc-label">Email</div>
            <div class="cc-val">Gmail</div>
          </div>
        </a>
        <a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" class="contact-card" style="border-color:rgba(10,102,194,0.3);">
          <div class="cc-icon" style="display:flex;align-items:center;">
            <svg width="22" height="22" viewBox="0 0 24 24" fill="#0a66c2"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          </div>
          <div>
            <div class="cc-label">LinkedIn</div>
            <div class="cc-val">View Profile ↗</div>
          </div>
        </a>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div style="display:flex;gap:16px;justify-content:center;align-items:center;margin-bottom:12px;flex-wrap:wrap;">
    <a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" style="display:inline-flex;align-items:center;gap:6px;color:#0a66c2;text-decoration:none;font-size:12px;font-weight:600;">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      LinkedIn
    </a>
    <span style="color:var(--border)">|</span>
    <a href="https://github.com/prudhvi-reddy" target="_blank" style="display:inline-flex;align-items:center;gap:6px;color:var(--muted);text-decoration:none;font-size:12px;font-weight:600;">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
      GitHub
    </a>
    <span style="color:var(--border)">|</span>
    <a href="mailto:prudhvireddy00091@gmail.com" style="color:var(--muted);text-decoration:none;font-size:12px;font-weight:600;">prudhvireddy00091@gmail.com</a>
  </div>
  <div>Built with ❤️ by <strong style="color:var(--accent);">Machupalli Prudhvi Simha Reddy</strong> · B.Tech CSE 2026</div>
  <div style="margin-top:4px;font-size:11px;">Tirupati, Andhra Pradesh</div>
</footer>

<!-- FLOATING HIRE ME -->
<a href="https://www.linkedin.com/in/prudhvi-reddy-81b839295/" target="_blank" class="hire-me-float">
  <div class="dot"></div>
  Hire Me
</a>

<script>
  // Smooth reveal on scroll
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.style.opacity = '1';
        e.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.project-card, .edu-card, .ach-card, .about-card').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(30px)';
    el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
    observer.observe(el);
  });

  // Skill bar animation on scroll into view
  const barObserver = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.querySelectorAll('.skill-bar-fill').forEach(bar => {
          const w = bar.getAttribute('data-width');
          bar.style.width = w + '%';
        });
        barObserver.unobserve(e.target);
      }
    });
  }, { threshold: 0.3 });

  const skillsSection = document.querySelector('.skills-section');
  if (skillsSection) barObserver.observe(skillsSection);

  // Hide floating button when contact section is in view
  const contactSection = document.querySelector('#contact');
  const hireBtn = document.querySelector('.hire-me-float');
  if (contactSection && hireBtn) {
    const hideObserver = new IntersectionObserver(entries => {
      entries.forEach(e => {
        hireBtn.style.opacity = e.isIntersecting ? '0' : '1';
        hireBtn.style.pointerEvents = e.isIntersecting ? 'none' : 'auto';
      });
    }, { threshold: 0.3 });
    hideObserver.observe(contactSection);
    hireBtn.style.transition = 'opacity 0.3s, transform 0.2s, box-shadow 0.2s';
  }
</script>
</body>
</html>
