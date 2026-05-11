
<style>
  @import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Instrument+Serif:ital@0;1&family=Syne:wght@400;500;700;800&display=swap');

  :root {
    --ink: var(--color-text-primary);
    --ink-muted: var(--color-text-secondary);
    --ink-faint: var(--color-text-tertiary);
    --surface: var(--color-background-tertiary);
    --card: var(--color-background-primary);
    --accent-color: #1a5ca8;
    --mono: 'DM Mono', monospace;
    --serif: 'Instrument Serif', serif;
    --sans: 'Syne', sans-serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: var(--sans);
    color: var(--ink);
    max-width: 760px;
    margin: 0 auto;
    padding: 2rem 1.5rem 3rem;
  }

  .header {
    display: grid;
    grid-template-columns: 1fr auto;
    align-items: end;
    gap: 2rem;
    padding-bottom: 2rem;
    border-bottom: 0.5px solid var(--color-border-tertiary);
    margin-bottom: 2.5rem;
  }

  .header-label {
    font-family: var(--mono);
    font-size: 11px;
    letter-spacing: 0.12em;
    color: var(--color-text-secondary);
    text-transform: uppercase;
    margin-bottom: 0.4rem;
  }

  h1 {
    font-family: var(--serif);
    font-size: 3rem;
    font-weight: 400;
    line-height: 1.05;
    letter-spacing: -0.02em;
    color: var(--color-text-primary);
  }

  h1 em {
    font-style: italic;
    color: #1a5ca8;
  }

  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 1rem;
  }

  .badge {
    font-family: var(--mono);
    font-size: 11px;
    padding: 4px 10px;
    border: 0.5px solid var(--color-border-secondary);
    border-radius: 99px;
    color: var(--color-text-secondary);
    background: var(--color-background-primary);
  }

  .avatar-ring {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background: #E6F1FB;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--serif);
    font-size: 2rem;
    color: #0C447C;
    border: 0.5px solid var(--color-border-tertiary);
  }

  .section {
    margin-bottom: 2.5rem;
  }

  .section-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 1.2rem;
  }

  .section-num {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--color-text-tertiary);
    min-width: 24px;
  }

  .section-title {
    font-size: 13px;
    font-weight: 500;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--color-text-secondary);
  }

  .section-line {
    flex: 1;
    height: 0.5px;
    background: var(--color-border-tertiary);
  }

  .about-text {
    font-family: var(--serif);
    font-size: 1.35rem;
    line-height: 1.65;
    color: var(--color-text-primary);
    max-width: 580px;
  }

  .about-text span.hi {
    font-style: italic;
    color: #1a5ca8;
  }

  .focus-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 12px;
  }

  .focus-card {
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-lg);
    padding: 1rem 1.1rem;
  }

  .focus-icon {
    font-size: 18px;
    margin-bottom: 8px;
    color: #1a5ca8;
  }

  .focus-label {
    font-size: 13px;
    font-weight: 500;
    color: var(--color-text-primary);
    margin-bottom: 4px;
  }

  .focus-desc {
    font-size: 12px;
    color: var(--color-text-secondary);
    line-height: 1.5;
  }

  .stack-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
    gap: 8px;
  }

  .stack-item {
    background: var(--color-background-primary);
    border: 0.5px solid var(--color-border-tertiary);
    border-radius: var(--border-radius-md);
    padding: 8px 12px;
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 13px;
    color: var(--color-text-primary);
  }

  .stack-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    flex-shrink: 0;
  }

  .dot-core   { background: #1a5ca8; }
  .dot-ui     { background: #0F6E56; }
  .dot-back   { background: #b05b1a; }
  .dot-data   { background: #7F77DD; }
  .dot-tools  { background: #888780; }

  .legend {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 14px;
  }

  .legend-item {
    display: flex;
    align-items: center;
    gap: 6px;
    font-family: var(--mono);
    font-size: 11px;
    color: var(--color-text-secondary);
  }

  .legend-dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
  }

  .social-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    align-items: center;
  }

  .social-link {
    display: flex;
    align-items: center;
    gap: 7px;
    font-family: var(--mono);
    font-size: 12px;
    color: var(--color-text-secondary);
    text-decoration: none;
    border: 0.5px solid var(--color-border-secondary);
    padding: 6px 12px;
    border-radius: 99px;
    background: var(--color-background-primary);
  }

  .social-link i { font-size: 14px; }

  .currently {
    background: #E6F1FB;
    border: 0.5px solid #85B7EB;
    border-radius: var(--border-radius-lg);
    padding: 1rem 1.2rem;
    display: flex;
    align-items: flex-start;
    gap: 10px;
  }

  .currently-icon {
    font-size: 18px;
    color: #185FA5;
    margin-top: 2px;
    flex-shrink: 0;
  }

  .currently-text {
    font-size: 14px;
    color: #0C447C;
    line-height: 1.6;
  }

  .currently-text strong {
    font-weight: 600;
    color: #042C53;
  }

  .stats-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .stats-img {
    width: 100%;
    border-radius: var(--border-radius-md);
    border: 0.5px solid var(--color-border-tertiary);
    display: block;
  }

  .snake-wrap {
    background: #0d1117;
    border-radius: var(--border-radius-lg);
    overflow: hidden;
    padding: 0.5rem 0;
  }

  .snake-wrap img {
    width: 100%;
    display: block;
  }

  .footer-line {
    margin-top: 2.5rem;
    padding-top: 1.5rem;
    border-top: 0.5px solid var(--color-border-tertiary);
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 8px;
  }

  .footer-note {
    font-family: var(--mono);
    font-size: 11px;
    color: var(--color-text-tertiary);
  }
</style>

<h2 style="position:absolute;left:-9999px">Ahmad's GitHub Profile README Preview</h2>

<div class="header">
  <div>
    <div class="header-label">full-stack developer</div>
    <h1>Ahmad<br><em>Iyrot</em></h1>
    <div class="badge-row">
      <span class="badge">React</span>
      <span class="badge">Node.js</span>
      <span class="badge">TypeScript</span>
      <span class="badge">MongoDB</span>
      <span class="badge">MySQL</span>
      <span class="badge">UI/UX</span>
    </div>
  </div>
  <div>
    <div class="avatar-ring">A</div>
  </div>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">01</span>
    <span class="section-title">About</span>
    <div class="section-line"></div>
  </div>
  <p class="about-text">
    I build full-stack web applications — from database schema to polished UI.
    I care about <span class="hi">clean architecture, fast APIs,</span> and interfaces that feel effortless to use.
    The whole stack is the job, and I treat every layer of it seriously.
  </p>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">02</span>
    <span class="section-title">Right now</span>
    <div class="section-line"></div>
  </div>
  <div class="currently">
    <i class="ti ti-activity currently-icon" aria-hidden="true"></i>
    <div class="currently-text">
      <strong>Building:</strong> Full-stack projects with React, Node.js, and real databases.<br>
      <strong>Open to:</strong> Collaborating on open-source and product-focused web apps.<br>
      <strong>Ask me about:</strong> JavaScript architecture, REST APIs, React patterns, and UI/UX.
    </div>
  </div>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">03</span>
    <span class="section-title">Focus areas</span>
    <div class="section-line"></div>
  </div>
  <div class="focus-grid">
    <div class="focus-card">
      <div class="focus-icon"><i class="ti ti-layout" aria-hidden="true"></i></div>
      <div class="focus-label">Frontend</div>
      <div class="focus-desc">React, TypeScript, Tailwind — scalable component systems with real attention to UX.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon"><i class="ti ti-server" aria-hidden="true"></i></div>
      <div class="focus-label">Backend & APIs</div>
      <div class="focus-desc">Node.js, Express, Socket.IO — RESTful APIs and real-time systems that hold up.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon"><i class="ti ti-database" aria-hidden="true"></i></div>
      <div class="focus-label">Data layer</div>
      <div class="focus-desc">MongoDB, MySQL, SQLite, Firebase — choosing the right database for the job.</div>
    </div>
    <div class="focus-card">
      <div class="focus-icon"><i class="ti ti-brush" aria-hidden="true"></i></div>
      <div class="focus-label">Design</div>
      <div class="focus-desc">Figma, Photoshop, Illustrator — I can take a design from concept to production code.</div>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">04</span>
    <span class="section-title">Stack</span>
    <div class="section-line"></div>
  </div>
  <div class="legend">
    <div class="legend-item"><div class="legend-dot" style="background:#1a5ca8"></div>Languages</div>
    <div class="legend-item"><div class="legend-dot" style="background:#0F6E56"></div>Frontend</div>
    <div class="legend-item"><div class="legend-dot" style="background:#b05b1a"></div>Backend / runtime</div>
    <div class="legend-item"><div class="legend-dot" style="background:#7F77DD"></div>Databases</div>
    <div class="legend-item"><div class="legend-dot" style="background:#888780"></div>Tools</div>
  </div>
  <div class="stack-grid">
    <div class="stack-item"><div class="stack-dot dot-core"></div>JavaScript</div>
    <div class="stack-item"><div class="stack-dot dot-core"></div>TypeScript</div>
    <div class="stack-item"><div class="stack-dot dot-core"></div>Python</div>
    <div class="stack-item"><div class="stack-dot dot-core"></div>C++</div>
    <div class="stack-item"><div class="stack-dot dot-core"></div>Java</div>
    <div class="stack-item"><div class="stack-dot dot-ui"></div>React</div>
    <div class="stack-item"><div class="stack-dot dot-ui"></div>Tailwind CSS</div>
    <div class="stack-item"><div class="stack-dot dot-ui"></div>Bootstrap</div>
    <div class="stack-item"><div class="stack-dot dot-ui"></div>HTML5 / CSS3</div>
    <div class="stack-item"><div class="stack-dot dot-ui"></div>jQuery</div>
    <div class="stack-item"><div class="stack-dot dot-back"></div>Node.js</div>
    <div class="stack-item"><div class="stack-dot dot-back"></div>Express</div>
    <div class="stack-item"><div class="stack-dot dot-back"></div>Socket.IO</div>
    <div class="stack-item"><div class="stack-dot dot-back"></div>Firebase</div>
    <div class="stack-item"><div class="stack-dot dot-back"></div>Apache Kafka</div>
    <div class="stack-item"><div class="stack-dot dot-data"></div>MongoDB</div>
    <div class="stack-item"><div class="stack-dot dot-data"></div>MySQL</div>
    <div class="stack-item"><div class="stack-dot dot-data"></div>SQLite</div>
    <div class="stack-item"><div class="stack-dot dot-tools"></div>Git / GitHub</div>
    <div class="stack-item"><div class="stack-dot dot-tools"></div>Figma</div>
    <div class="stack-item"><div class="stack-dot dot-tools"></div>Photoshop</div>
    <div class="stack-item"><div class="stack-dot dot-tools"></div>Illustrator</div>
    <div class="stack-item"><div class="stack-dot dot-tools"></div>Vite / npm</div>
    <div class="stack-item"><div class="stack-dot dot-tools"></div>Blender</div>
  </div>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">05</span>
    <span class="section-title">GitHub stats</span>
    <div class="section-line"></div>
  </div>
  <div class="stats-row">
    <img class="stats-img" src="https://github-readme-stats.vercel.app/api/top-langs?username=Ahmadiyrot&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=github_dark&hide_border=false" alt="Top languages" />
    <img class="stats-img" src="https://github-readme-stats.vercel.app/api?username=Ahmadiyrot&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=github_dark&locale=en&hide_border=false" alt="GitHub stats" />
  </div>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">06</span>
    <span class="section-title">Contribution grid</span>
    <div class="section-line"></div>
  </div>
  <div class="snake-wrap">
    <img src="https://raw.githubusercontent.com/Ahmadiyrot/Ahmadiyrot/output/github-contribution-grid-snake.svg" alt="GitHub contribution snake" />
  </div>
</div>

<div class="section">
  <div class="section-header">
    <span class="section-num">07</span>
    <span class="section-title">Contact</span>
    <div class="section-line"></div>
  </div>
  <div class="social-row">
    <a class="social-link" href="https://www.linkedin.com/in/ahmad-iyrot-a68539346/" target="_blank">
      <i class="ti ti-brand-linkedin" aria-hidden="true"></i>LinkedIn
    </a>
    <a class="social-link" href="mailto:ahmadiyroot@gmail.com">
      <i class="ti ti-mail" aria-hidden="true"></i>Email
    </a>
    <a class="social-link" href="https://www.instagram.com/ahmad.iyrot/" target="_blank">
      <i class="ti ti-brand-instagram" aria-hidden="true"></i>Instagram
    </a>
    <a class="social-link" href="https://www.facebook.com/profile.php?id=100080038279314" target="_blank">
      <i class="ti ti-brand-facebook" aria-hidden="true"></i>Facebook
    </a>
    <a class="social-link" href="https://www.twitch.tv/ahmadiyrot" target="_blank">
      <i class="ti ti-brand-twitch" aria-hidden="true"></i>Twitch
    </a>
  </div>
</div>

<div class="footer-line">
  <span class="footer-note">github.com/Ahmadiyrot</span>
  <span class="footer-note">updated 2025</span>
</div>
