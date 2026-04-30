<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Alleluia Cervi — Software Engineer</title>
  <meta name="description" content="Software Engineer specializing in AI systems, infrastructure engineering, and DevOps. Based in Kigali, Rwanda."/>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;700;800&family=DM+Mono:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #0a0c10;
      --bg2: #0f1318;
      --surface: #141920;
      --surface2: #1a2030;
      --border: rgba(255,255,255,0.07);
      --border2: rgba(255,255,255,0.13);
      --text: #e8eaf0;
      --text2: #8892a4;
      --text3: #4a5568;
      --accent: #4f9eff;
      --accent2: #38d9a9;
      --accent3: #f59e0b;
      --font-display: 'Syne', sans-serif;
      --font-mono: 'DM Mono', monospace;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: var(--font-display);
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }

    .site { max-width: 900px; margin: 0 auto; padding: 0 32px; }

    /* ── NAV ── */
    nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 24px 0;
      border-bottom: 0.5px solid var(--border);
      position: sticky;
      top: 0;
      background: rgba(10,12,16,0.92);
      backdrop-filter: blur(12px);
      z-index: 100;
    }
    .nav-logo {
      font-size: 14px;
      font-weight: 700;
      letter-spacing: .12em;
      text-transform: uppercase;
      font-family: var(--font-mono);
    }
    .nav-logo span { color: var(--accent); }
    .nav-links { display: flex; align-items: center; gap: 28px; }
    .nav-links a {
      font-size: 12px;
      letter-spacing: .1em;
      text-transform: uppercase;
      color: var(--text2);
      text-decoration: none;
      font-family: var(--font-mono);
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--text); }
    .nav-dot {
      width: 6px; height: 6px;
      border-radius: 50%;
      background: var(--accent2);
      animation: pulse 2s infinite;
    }

    /* ── HERO ── */
    .hero { padding: 100px 0 72px; }
    .hero-eyebrow {
      font-size: 11px;
      font-family: var(--font-mono);
      letter-spacing: .2em;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 28px;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .hero-eyebrow::before {
      content: '';
      display: block;
      width: 40px; height: 1px;
      background: var(--accent);
    }
    .hero-name {
      font-size: clamp(52px, 9vw, 88px);
      font-weight: 800;
      line-height: 1;
      letter-spacing: -.03em;
      margin-bottom: 20px;
    }
    .hero-name em { font-style: normal; color: var(--accent); }
    .hero-role {
      font-size: 13px;
      font-family: var(--font-mono);
      color: var(--text2);
      letter-spacing: .06em;
      margin-bottom: 36px;
      line-height: 2;
    }
    .hero-role span { color: var(--accent2); }
    .hero-desc {
      font-size: 17px;
      color: var(--text2);
      line-height: 1.8;
      max-width: 580px;
      margin-bottom: 44px;
    }
    .hero-desc strong { color: var(--text); font-weight: 500; }
    .hero-actions { display: flex; gap: 12px; flex-wrap: wrap; }
    .btn-primary {
      padding: 14px 32px;
      background: var(--accent);
      color: #fff;
      border: none;
      border-radius: 6px;
      font-size: 13px;
      font-family: var(--font-mono);
      font-weight: 500;
      letter-spacing: .06em;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: opacity .2s, transform .15s;
    }
    .btn-primary:hover { opacity: .85; transform: translateY(-1px); }
    .btn-ghost {
      padding: 14px 32px;
      background: transparent;
      color: var(--text2);
      border: 0.5px solid var(--border2);
      border-radius: 6px;
      font-size: 13px;
      font-family: var(--font-mono);
      letter-spacing: .06em;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: all .2s;
    }
    .btn-ghost:hover { color: var(--text); border-color: var(--text3); transform: translateY(-1px); }

    /* ── DIVIDER ── */
    .divider { height: 0.5px; background: var(--border); }

    /* ── SECTIONS ── */
    .section { padding: 72px 0; }
    .section-label {
      font-size: 10px;
      font-family: var(--font-mono);
      letter-spacing: .25em;
      text-transform: uppercase;
      color: var(--text3);
      margin-bottom: 44px;
      display: flex;
      align-items: center;
      gap: 14px;
    }
    .section-label::after {
      content: '';
      flex: 1;
      height: 0.5px;
      background: var(--border);
    }

    /* ── EXPERTISE ── */
    .expertise-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1px;
      background: var(--border);
      border: 0.5px solid var(--border);
    }
    @media (max-width: 640px) { .expertise-grid { grid-template-columns: 1fr; } }
    .expertise-card {
      background: var(--bg);
      padding: 32px 28px;
      transition: background .2s;
    }
    .expertise-card:hover { background: var(--surface); }
    .expertise-icon {
      font-size: 11px;
      font-family: var(--font-mono);
      color: var(--accent);
      margin-bottom: 20px;
      letter-spacing: .15em;
    }
    .expertise-title {
      font-size: 16px;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 16px;
    }
    .expertise-list { list-style: none; display: flex; flex-direction: column; gap: 8px; }
    .expertise-list li {
      font-size: 12px;
      color: var(--text2);
      font-family: var(--font-mono);
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .expertise-list li::before { content: '→'; color: var(--text3); font-size: 10px; }

    /* ── STACK ── */
    .stack-section { display: flex; flex-direction: column; gap: 24px; }
    .stack-group-label {
      font-size: 10px;
      font-family: var(--font-mono);
      color: var(--text3);
      letter-spacing: .2em;
      text-transform: uppercase;
      margin-bottom: 10px;
    }
    .stack-tags { display: flex; flex-wrap: wrap; gap: 8px; }
    .tag {
      padding: 7px 16px;
      border: 0.5px solid var(--border2);
      border-radius: 4px;
      font-size: 11px;
      font-family: var(--font-mono);
      color: var(--text2);
      letter-spacing: .06em;
      transition: all .2s;
      cursor: default;
    }
    .tag:hover { border-color: var(--accent); color: var(--accent); }
    .tag.blue { border-color: rgba(79,158,255,.4); color: var(--accent); background: rgba(79,158,255,.06); }
    .tag.green { border-color: rgba(56,217,169,.4); color: var(--accent2); background: rgba(56,217,169,.06); }
    .tag.amber { border-color: rgba(245,158,11,.4); color: var(--accent3); background: rgba(245,158,11,.06); }

    /* ── PROJECT ── */
    .project-card {
      border: 0.5px solid var(--border);
      border-radius: 10px;
      overflow: hidden;
      margin-bottom: 20px;
      transition: border-color .2s;
    }
    .project-card:hover { border-color: var(--border2); }
    .project-header { padding: 28px 32px 24px; }
    .project-badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      font-size: 10px;
      font-family: var(--font-mono);
      letter-spacing: .15em;
      text-transform: uppercase;
      color: var(--accent2);
      background: rgba(56,217,169,.08);
      border: 0.5px solid rgba(56,217,169,.25);
      padding: 5px 12px;
      border-radius: 4px;
      margin-bottom: 16px;
    }
    .badge-dot {
      width: 5px; height: 5px;
      border-radius: 50%;
      background: var(--accent2);
      animation: pulse 2s infinite;
    }
    .project-name {
      font-size: 22px;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 10px;
      letter-spacing: -.01em;
    }
    .project-desc { font-size: 14px; color: var(--text2); line-height: 1.75; max-width: 540px; }
    .project-body {
      border-top: 0.5px solid var(--border);
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
    @media (max-width: 640px) { .project-body { grid-template-columns: 1fr; } }
    .project-col { padding: 24px 32px; }
    .project-col:first-child { border-right: 0.5px solid var(--border); }
    .project-col-label {
      font-size: 10px;
      font-family: var(--font-mono);
      letter-spacing: .2em;
      text-transform: uppercase;
      color: var(--text3);
      margin-bottom: 14px;
    }
    .project-col ul { list-style: none; display: flex; flex-direction: column; gap: 8px; }
    .project-col li {
      font-size: 13px;
      color: var(--text2);
      display: flex;
      align-items: flex-start;
      gap: 10px;
      line-height: 1.6;
    }
    .project-col li::before {
      content: '▸';
      color: var(--accent);
      font-size: 10px;
      margin-top: 4px;
      flex-shrink: 0;
    }

    /* ── PRIVATE NOTE ── */
    .private-note {
      border: 0.5px solid var(--border);
      border-radius: 10px;
      padding: 28px 32px;
      background: var(--bg2);
      display: flex;
      gap: 20px;
      align-items: flex-start;
    }
    .private-icon {
      width: 40px; height: 40px;
      border-radius: 8px;
      background: var(--surface);
      border: 0.5px solid var(--border2);
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      font-size: 18px;
    }
    .private-text h3 { font-size: 14px; font-weight: 700; color: var(--text); margin-bottom: 8px; }
    .private-text p { font-size: 13px; color: var(--text2); line-height: 1.75; }
    .private-text strong { color: var(--accent); font-weight: 500; }

    /* ── AVAILABILITY ── */
    .availability {
      display: flex;
      align-items: center;
      gap: 14px;
      padding: 16px 20px;
      border: 0.5px solid rgba(56,217,169,.2);
      border-radius: 6px;
      background: rgba(56,217,169,.04);
      margin-bottom: 32px;
    }
    .avail-dot {
      width: 7px; height: 7px;
      border-radius: 50%;
      background: var(--accent2);
      flex-shrink: 0;
      animation: pulse 2s infinite;
    }
    .avail-text { font-size: 13px; font-family: var(--font-mono); color: var(--accent2); }
    .avail-text span { color: var(--text2); }

    /* ── CONTACT ── */
    .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
    @media (max-width: 500px) { .contact-grid { grid-template-columns: 1fr; } }
    .contact-item {
      border: 0.5px solid var(--border);
      border-radius: 8px;
      padding: 18px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      transition: border-color .2s, background .2s;
      cursor: pointer;
      text-decoration: none;
    }
    .contact-item:hover { border-color: var(--border2); background: var(--surface); }
    .contact-label {
      font-size: 10px;
      font-family: var(--font-mono);
      color: var(--text3);
      letter-spacing: .15em;
      text-transform: uppercase;
      margin-bottom: 5px;
    }
    .contact-value { font-size: 13px; color: var(--text); font-family: var(--font-mono); }
    .contact-arrow { font-size: 18px; color: var(--text3); }

    /* ── FOOTER ── */
    footer {
      padding: 32px 0;
      border-top: 0.5px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 12px;
    }
    .footer-copy {
      font-size: 11px;
      font-family: var(--font-mono);
      color: var(--text3);
      letter-spacing: .06em;
    }
    .footer-copy span { color: var(--accent2); }

    @keyframes pulse { 0%, 100% { opacity: 1; } 50% { opacity: .25; } }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to { opacity: 1; transform: translateY(0); }
    }
    .hero > * {
      animation: fadeUp .7s ease both;
    }
    .hero > *:nth-child(1) { animation-delay: .05s; }
    .hero > *:nth-child(2) { animation-delay: .15s; }
    .hero > *:nth-child(3) { animation-delay: .25s; }
    .hero > *:nth-child(4) { animation-delay: .35s; }
    .hero > *:nth-child(5) { animation-delay: .45s; }
  </style>
</head>
<body>

<div class="site">

  <nav>
    <div class="nav-logo">AC<span>.</span>dev</div>
    <div class="nav-links">
      <a href="#expertise">Work</a>
      <a href="#stack">Stack</a>
      <a href="#contact">Contact</a>
      <div class="nav-dot"></div>
    </div>
  </nav>

  <div class="hero">
    <div class="hero-eyebrow">Software Engineer · Kigali, Rwanda</div>
    <h1 class="hero-name">Alleluia<br><em>Cervi</em></h1>
    <div class="hero-role">
      AI Systems &nbsp;// &nbsp;Infrastructure Engineering &nbsp;//&nbsp; DevOps<br>
      <span>Quiet execution. Permanent results.</span>
    </div>
    <p class="hero-desc">
      I design and build systems that <strong>scale, adapt, and outlast their requirements.</strong>
      Most of my work lives in private repositories and production infrastructure —
      measured not in commit counts, but in the problems it permanently solves.
    </p>
    <div class="hero-actions">
      <a class="btn-primary" href="#contact">Get in touch →</a>
      <a class="btn-ghost" href="#work">View work</a>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section" id="expertise">
    <div class="section-label">Expertise</div>
    <div class="expertise-grid">
      <div class="expertise-card">
        <div class="expertise-icon">01 / AI</div>
        <div class="expertise-title">AI & LLM Systems</div>
        <ul class="expertise-list">
          <li>LLM application architecture</li>
          <li>Prompt engineering & RAG</li>
          <li>Intelligent automation pipelines</li>
          <li>Multi-model orchestration</li>
        </ul>
      </div>
      <div class="expertise-card">
        <div class="expertise-icon">02 / ENG</div>
        <div class="expertise-title">Software Engineering</div>
        <ul class="expertise-list">
          <li>Full-stack system design</li>
          <li>High-performance backend services</li>
          <li>API design & microservices</li>
          <li>Database architecture & optimization</li>
        </ul>
      </div>
      <div class="expertise-card">
        <div class="expertise-icon">03 / OPS</div>
        <div class="expertise-title">DevOps & Infrastructure</div>
        <ul class="expertise-list">
          <li>CI/CD pipeline engineering</li>
          <li>Container orchestration (Docker · K8s)</li>
          <li>Cloud-native deployment strategies</li>
          <li>System reliability & monitoring</li>
        </ul>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section" id="stack">
    <div class="section-label">Tech Stack</div>
    <div class="stack-section">
      <div>
        <div class="stack-group-label">Languages</div>
        <div class="stack-tags">
          <div class="tag blue">TypeScript</div>
          <div class="tag blue">Python</div>
          <div class="tag">JavaScript</div>
          <div class="tag">Java</div>
          <div class="tag">C++</div>
          <div class="tag">SQL</div>
        </div>
      </div>
      <div>
        <div class="stack-group-label">Frontend & Backend</div>
        <div class="stack-tags">
          <div class="tag">React</div>
          <div class="tag">Next.js</div>
          <div class="tag">Node.js</div>
          <div class="tag">Express</div>
          <div class="tag">FastAPI</div>
          <div class="tag">PostgreSQL</div>
          <div class="tag">MongoDB</div>
          <div class="tag">Redis</div>
          <div class="tag">Firebase</div>
        </div>
      </div>
      <div>
        <div class="stack-group-label">Infrastructure & DevOps</div>
        <div class="stack-tags">
          <div class="tag green">Docker</div>
          <div class="tag green">Kubernetes</div>
          <div class="tag green">AWS</div>
          <div class="tag green">GitHub Actions</div>
          <div class="tag">Linux</div>
          <div class="tag">Nginx</div>
          <div class="tag amber">CI/CD Pipelines</div>
          <div class="tag amber">Cloud-Native</div>
        </div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section" id="work">
    <div class="section-label">Selected Work</div>

    <div class="project-card">
      <div class="project-header">
        <div class="project-badge"><div class="badge-dot"></div>Active · Production</div>
        <div class="project-name">Tech-Agrivision Rwanda</div>
        <p class="project-desc">
          Infrastructure-level thinking applied to agriculture. A distributed platform connecting rural farmers
          to predictive analytics, real-time data, and AI-driven advisory systems — built for scale across East Africa.
        </p>
      </div>
      <div class="project-body">
        <div class="project-col">
          <div class="project-col-label">Architecture</div>
          <ul>
            <li>Real-time distributed data collection via SMS & web platform</li>
            <li>Predictive analytics engine for weather and yield forecasting</li>
            <li>Designed for low-bandwidth, high-reach rural environments</li>
          </ul>
        </div>
        <div class="project-col">
          <div class="project-col-label">Roadmap</div>
          <ul>
            <li>IoT sensor network integration (soil, humidity, temperature)</li>
            <li>AI-driven crop advisory engine at scale</li>
            <li>Cross-regional data federation across East Africa</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="private-note">
      <div class="private-icon">🔒</div>
      <div class="private-text">
        <h3>Private & Enterprise Work</h3>
        <p>
          A significant portion of my portfolio is under NDA or deployed to private infrastructure.
          <strong>Commit counts don't reflect production systems.</strong> Work includes production deployments,
          enterprise integrations, and long-cycle infrastructure projects built for organizations across Rwanda and beyond.
          Details available on request.
        </p>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section" id="contact">
    <div class="section-label">Contact</div>
    <div class="availability">
      <div class="avail-dot"></div>
      <div class="avail-text">
        Available for new projects &nbsp;—&nbsp;
        <span>AI systems, infrastructure, and serious builds</span>
      </div>
    </div>
    <div class="contact-grid">
      <a class="contact-item" href="https://github.com/alleluiacervi-tech" target="_blank" rel="noopener">
        <div>
          <div class="contact-label">GitHub</div>
          <div class="contact-value">alleluiacervi-tech</div>
        </div>
        <div class="contact-arrow">↗</div>
      </a>
      <div class="contact-item">
        <div>
          <div class="contact-label">Location</div>
          <div class="contact-value">Kigali, Rwanda</div>
        </div>
        <div class="contact-arrow" style="font-size:16px">🌍</div>
      </div>
    </div>
  </div>

  <footer>
    <div class="footer-copy">Alleluia Cervi <span>·</span> Software Engineer <span>·</span> 2025</div>
    <div class="footer-copy" style="color: rgba(56,217,169,.7)">Systems that last.</div>
  </footer>

</div>

</body>
</html>
