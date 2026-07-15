<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vitória de Jesus Dietrich — Portfólio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #0a0512;
    --panel: #120a1e;
    --panel-2: #170e26;
    --border: #2a1a40;
    --border-soft: #1e1230;
    --purple: #9333ea;
    --purple-2: #a855f7;
    --pink: #ec4899;
    --violet: #7c3aed;
    --text: #f3edfb;
    --text-dim: #b8a9cf;
    --text-faint: #6f6086;
    --grad: linear-gradient(135deg, var(--purple) 0%, var(--pink) 100%);
  }

  *{ box-sizing:border-box; margin:0; padding:0; }

  body{
    background: radial-gradient(ellipse 900px 500px at 15% 0%, #1a0d2e 0%, var(--bg) 55%), var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    line-height: 1.5;
    padding: 32px;
  }

  .wrap{
    max-width: 1240px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 320px 1fr;
    gap: 22px;
  }

  h1,h2,h3,.mono{ font-family:'Space Grotesk', sans-serif; }
  .tag-mono{ font-family:'JetBrains Mono', monospace; }

  /* ---------- SIDEBAR ---------- */
  .sidebar{
    background: var(--panel);
    border: 1px solid var(--border-soft);
    border-radius: 20px;
    padding: 28px 24px;
  }

  .brand-icon{
    width:34px; height:34px; border-radius:9px;
    background: var(--panel-2); border:1px solid var(--border);
    display:flex; align-items:center; justify-content:center;
    color: var(--purple-2); margin-bottom: 26px;
  }

  .avatar-ring{
    width: 132px; height:132px; border-radius:50%;
    padding: 4px;
    background: conic-gradient(from 210deg, var(--purple), var(--pink), var(--purple));
    margin: 0 auto 18px;
  }
  .avatar{
    width:100%; height:100%; border-radius:50%;
    background: var(--panel-2);
    display:flex; align-items:center; justify-content:center;
    font-family:'Space Grotesk',sans-serif; font-weight:700; font-size:40px;
    color: var(--purple-2);
    border: 3px solid var(--bg);
  }

  .name-block{ text-align:center; margin-bottom: 22px; }
  .name-block h1{ font-size: 24px; font-weight:700; line-height:1.25; }
  .roles{ margin-top:10px; display:flex; flex-direction:column; gap:3px; }
  .roles span{ font-size: 10.5px; letter-spacing: .06em; color: var(--purple-2); text-transform: uppercase; font-weight:600; }

  .sb-section{ margin-top: 24px; padding-top:22px; border-top:1px solid var(--border-soft); }
  .sb-label{
    display:flex; align-items:center; gap:8px;
    font-size: 11px; letter-spacing:.08em; text-transform:uppercase;
    color: var(--text-faint); font-weight:600; margin-bottom:14px;
  }
  .sb-label::before{
    content:""; width:6px; height:6px; border-radius:50%; background: var(--pink);
    box-shadow: 0 0 8px var(--pink);
  }

  .contact-list{ display:flex; flex-direction:column; gap:12px; }
  .contact-list a{
    display:flex; align-items:center; gap:10px;
    color: var(--text-dim); text-decoration:none; font-size:13.5px;
    transition: color .15s;
  }
  .contact-list a:hover{ color: var(--text); }
  .contact-list svg{ flex-shrink:0; color: var(--purple-2); }

  .about-text{ font-size: 13.5px; color: var(--text-dim); }
  .about-text p{ margin-bottom: 12px; }
  .about-text strong{ color: var(--text); font-weight:600; }

  .quote-box{
    margin-top:20px;
    background: linear-gradient(160deg, rgba(147,51,234,.14), rgba(236,72,153,.06));
    border: 1px solid rgba(147,51,234,.35);
    border-radius: 14px;
    padding: 18px 18px 16px;
    position: relative;
  }
  .quote-box .qmark{ font-size: 30px; color: var(--purple-2); font-family: Georgia, serif; line-height:0; position:relative; top:10px; }
  .quote-box p{ font-size: 13px; color: var(--text); font-style: italic; line-height:1.55; margin: 4px 0 10px; }
  .quote-box .sig{ font-size: 12px; color: var(--purple-2); font-family:'Space Grotesk'; text-align:right; }

  .stat-grid{ display:grid; grid-template-columns: 1fr 1fr; gap:10px; margin-bottom:16px; }
  .stat-card{
    background: var(--panel-2); border:1px solid var(--border-soft); border-radius:12px;
    padding: 12px 14px;
  }
  .stat-card .num{ font-family:'Space Grotesk'; font-size:20px; font-weight:700; color:var(--text); }
  .stat-card .lbl{ font-size:10.5px; color:var(--text-faint); margin-top:2px; text-transform:uppercase; letter-spacing:.04em; }

  .lang-row{
    display:flex; align-items:center; gap:16px;
    background: var(--panel-2); border:1px solid var(--border-soft); border-radius:14px;
    padding:16px;
  }
  .donut{
    width:76px; height:76px; border-radius:50%; flex-shrink:0;
    background: conic-gradient(#f7df1e 0% 42.3%, #e34f26 42.3% 64%, #2965f1 64% 79.6%, #3776ab 79.6% 88.5%, #7f52ff 88.5% 94.7%, #6f6086 94.7% 100%);
    display:flex; align-items:center; justify-content:center;
  }
  .donut::after{
    content:""; width:48px; height:48px; border-radius:50%; background: var(--panel-2);
  }
  .lang-legend{ font-size:11.5px; display:flex; flex-direction:column; gap:5px; flex:1; }
  .lang-legend .lg-item{ display:flex; align-items:center; gap:7px; color:var(--text-dim); }
  .lang-legend .dot{ width:7px; height:7px; border-radius:50%; }
  .lang-legend b{ color:var(--text); margin-left:auto; font-family:'JetBrains Mono'; }

  /* ---------- MAIN ---------- */
  .main{ display:flex; flex-direction:column; gap:20px; }

  .topbar{
    background: var(--panel); border:1px solid var(--border-soft); border-radius:16px;
    padding: 15px 22px; display:flex; align-items:center; gap:10px;
    font-family:'JetBrains Mono'; font-size:13px; color:var(--text-faint);
  }
  .topbar svg{ color: var(--purple-2); }

  .hero{
    background: var(--panel);
    border:1px solid var(--border-soft);
    border-radius:20px;
    padding: 40px 40px;
    position: relative;
    overflow:hidden;
    display:grid;
    grid-template-columns: 1.3fr 1fr;
    gap: 20px;
    align-items:center;
  }
  .hero::before{
    content:""; position:absolute; inset:0;
    background: radial-gradient(circle at 85% 20%, rgba(147,51,234,.22), transparent 55%);
    pointer-events:none;
  }
  .hero h2{
    font-size: 30px; line-height:1.2; font-weight:700; position:relative; z-index:1;
  }
  .hero h2 .accent{
    background: var(--grad); -webkit-background-clip:text; background-clip:text; color:transparent;
  }
  .hero p.sub{ margin-top:14px; color: var(--text-dim); font-size:14.5px; max-width:440px; position:relative; z-index:1; }

  .feature-row{ display:flex; gap:12px; margin-top:24px; position:relative; z-index:1; }
  .feature-card{
    background: var(--panel-2); border:1px solid var(--border-soft); border-radius:14px;
    padding: 14px 16px; display:flex; gap:11px; align-items:flex-start; flex:1;
  }
  .feature-card .ic{
    width:32px; height:32px; border-radius:9px; flex-shrink:0;
    background: rgba(147,51,234,.18); border:1px solid rgba(147,51,234,.4);
    display:flex; align-items:center; justify-content:center; color: var(--purple-2);
  }
  .feature-card .ttl{ font-size:11px; letter-spacing:.05em; text-transform:uppercase; color:var(--text-faint); font-weight:600; }
  .feature-card .desc{ font-size:12.5px; color:var(--text-dim); margin-top:3px; line-height:1.4; }

  .illustration{ position:relative; z-index:1; display:flex; justify-content:center; }

  .panel{
    background: var(--panel); border:1px solid var(--border-soft); border-radius:20px;
    padding: 28px 32px;
  }
  .panel-title{
    display:flex; align-items:center; gap:9px;
    font-size: 15px; font-weight:700; letter-spacing:.02em; text-transform:uppercase;
    margin-bottom: 22px;
  }
  .panel-title::before{
    content:""; width:7px; height:7px; border-radius:50%; background: var(--pink);
    box-shadow: 0 0 10px var(--pink);
  }

  /* timeline */
  .timeline{ display:flex; flex-direction:column; }
  .t-item{
    display:flex; justify-content:space-between; align-items:flex-start;
    padding: 14px 0; border-left: 2px solid var(--border); padding-left:22px; position:relative;
  }
  .t-item::before{
    content:""; position:absolute; left:-6px; top:19px; width:10px; height:10px; border-radius:50%;
    background: var(--panel); border:2px solid var(--purple-2);
  }
  .t-item:last-child{ border-left-color: transparent; }
  .t-item h4{ font-size:14.5px; font-weight:600; }
  .t-item span.inst{ font-size:12.5px; color:var(--text-faint); display:block; margin-top:2px; }
  .t-item .mode{
    font-size: 10.5px; color: var(--purple-2); background: rgba(147,51,234,.14);
    border:1px solid rgba(147,51,234,.35); padding: 3px 10px; border-radius: 20px;
    white-space:nowrap; margin-top:2px;
  }

  /* skills */
  .skills-grid{ display:grid; grid-template-columns: 1.1fr 1fr; gap:20px; }
  .tool-grid{ display:grid; grid-template-columns: repeat(4, 1fr); gap:12px; }
  .tool{
    background: var(--panel-2); border:1px solid var(--border-soft); border-radius:14px;
    padding: 16px 8px; display:flex; flex-direction:column; align-items:center; gap:8px;
    font-size:11px; color:var(--text-dim); text-align:center;
  }
  .tool svg{ color: var(--purple-2); }

  .bar-list{ display:flex; flex-direction:column; gap:13px; }
  .bar-row .top{ display:flex; justify-content:space-between; font-size:12.5px; margin-bottom:6px; color: var(--text-dim); }
  .bar-row .top b{ color: var(--text); font-family:'JetBrains Mono'; font-weight:500; }
  .bar-track{ height:7px; background: var(--panel-2); border-radius:20px; overflow:hidden; border:1px solid var(--border-soft); }
  .bar-fill{ height:100%; border-radius:20px; background: var(--grad); }

  /* projects */
  .proj-grid{ display:grid; grid-template-columns: repeat(3, 1fr); gap:16px; }
  .proj-card{
    background: var(--panel-2); border:1px solid var(--border-soft); border-radius:16px;
    overflow:hidden; display:flex; flex-direction:column;
  }
  .proj-thumb{
    height: 92px; display:flex; align-items:center; justify-content:center;
    font-family:'Space Grotesk'; font-weight:700; font-size:13px; letter-spacing:.03em;
    color: rgba(255,255,255,.92); text-transform:uppercase;
  }
  .proj-body{ padding: 14px 16px 16px; }
  .proj-body h4{ font-size:13.5px; font-weight:600; }
  .proj-body p{ font-size:11.5px; color:var(--text-faint); margin-top:5px; line-height:1.4; min-height: 30px; }
  .proj-tags{ display:flex; flex-wrap:wrap; gap:5px; margin-top:11px; }
  .proj-tags span{
    font-size: 9.5px; padding:3px 8px; border-radius:20px;
    background: rgba(168,85,247,.12); border:1px solid rgba(168,85,247,.3); color: var(--purple-2);
    font-family:'JetBrains Mono';
  }
  .more-row{
    text-align:center; padding: 13px; margin-top:14px;
    background: var(--panel-2); border:1px dashed var(--border); border-radius:12px;
    font-size:12px; color:var(--text-faint); letter-spacing:.04em; text-transform:uppercase;
  }

  /* deep tech */
  .deep-grid{ display:grid; grid-template-columns: repeat(4,1fr); gap:14px; }
  .deep-card{
    background: var(--panel-2); border:1px solid var(--border-soft); border-radius:14px; padding:18px 16px;
  }
  .deep-card .ic{
    width:34px; height:34px; border-radius:9px; background: rgba(236,72,153,.14);
    border:1px solid rgba(236,72,153,.35); display:flex; align-items:center; justify-content:center;
    color: var(--pink); margin-bottom:12px;
  }
  .deep-card h5{ font-size:12.5px; font-weight:700; text-transform:uppercase; letter-spacing:.03em; }
  .deep-card p{ font-size:11.5px; color:var(--text-faint); margin-top:6px; line-height:1.45; }

  footer{
    text-align:center; font-size:12px; color: var(--text-faint); padding: 8px 0 4px;
  }
  footer .accent{ color: var(--purple-2); }

  @media (max-width: 980px){
    .wrap{ grid-template-columns: 1fr; }
    .hero{ grid-template-columns: 1fr; }
    .illustration{ display:none; }
    .skills-grid{ grid-template-columns: 1fr; }
    .proj-grid{ grid-template-columns: 1fr 1fr; }
    .deep-grid{ grid-template-columns: 1fr 1fr; }
    .tool-grid{ grid-template-columns: repeat(3,1fr); }
  }
  @media (max-width: 600px){
    body{ padding:16px; }
    .proj-grid, .deep-grid{ grid-template-columns: 1fr; }
    .feature-row{ flex-direction:column; }
  }
</style>
</head>
<body>

<div class="wrap">

  <!-- ===================== SIDEBAR ===================== -->
  <aside class="sidebar">
    <div class="brand-icon">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
    </div>

    <div class="avatar-ring">
      <div class="avatar">VD</div>
    </div>

    <div class="name-block">
      <h1>Vitória<br/>de Jesus Dietrich</h1>
      <div class="roles">
        <span>Desenvolvedora Full Stack Web</span>
        <span>Estudante de ADS e Inteligência Artificial</span>
        <span>Técnica em Informática</span>
        <span>Analista de Produtos Digitais e Dados</span>
        <span>UI/UX Designer</span>
      </div>
    </div>

    <div class="sb-section">
      <div class="sb-label">Conecte-se comigo</div>
      <div class="contact-list">
        <a href="mailto:dietrichvitoria29@gmail.com">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 6-10 7L2 6"/></svg>
          dietrichvitoria29@gmail.com
        </a>
        <a href="https://wa.me/5511944039125" target="_blank">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M3 21l1.65-3.8a9 9 0 1 1 3.4 3.2z"/></svg>
          (11) 94403-9125
        </a>
        <a href="https://www.linkedin.com/in/vitoriadietrich/" target="_blank">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          linkedin.com/in/vitoriadietrich
        </a>
        <a href="https://github.com/vitoriadietrich" target="_blank">
          <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-4.3 1.4-4.3-2.5-6-3m12 5v-3.5c0-1 .1-1.4-.5-2 2.8-.3 5.5-1.4 5.5-6a4.6 4.6 0 0 0-1.3-3.2 4.2 4.2 0 0 0-.1-3.2s-1.1-.3-3.5 1.3a12.3 12.3 0 0 0-6.2 0C6.5 2.8 5.4 3.1 5.4 3.1a4.2 4.2 0 0 0-.1 3.2A4.6 4.6 0 0 0 4 9.5c0 4.6 2.7 5.7 5.5 6-.6.6-.6 1.2-.5 2V21"/></svg>
          github.com/vitoriadietrich
        </a>
      </div>
    </div>

    <div class="sb-section">
      <div class="sb-label">Sobre mim</div>
      <div class="about-text">
        <p>Sou <strong>desenvolvedora fullstack web</strong>, analista de produtos digitais e dados, e técnica em informática apaixonada por tecnologia e inovação.</p>
        <p>Atualmente cursando <strong>Análise e Desenvolvimento de Sistemas e Inteligência Artificial</strong>.</p>
        <p>Tenho experiência com desenvolvimento web, organização de projetos e produtos digitais. Amo criar soluções que impactam pessoas e negócios.</p>
      </div>

      <div class="quote-box">
        <div class="qmark">&ldquo;</div>
        <p>Transformo ideias em soluções digitais funcionais, bonitas e inteligentes.</p>
        <div class="sig">— Vitória Dietrich</div>
      </div>
    </div>

    <div class="sb-section">
      <div class="sb-label">GitHub stats</div>
      <div class="stat-grid">
        <div class="stat-card"><div class="num">28</div><div class="lbl">Repos públicos</div></div>
        <div class="stat-card"><div class="num">5</div><div class="lbl">Linguagens ativas</div></div>
      </div>
      <div class="lang-row">
        <div class="donut"></div>
        <div class="lang-legend">
          <div class="lg-item"><span class="dot" style="background:#f7df1e"></span>JavaScript <b>42.3%</b></div>
          <div class="lg-item"><span class="dot" style="background:#e34f26"></span>HTML <b>21.7%</b></div>
          <div class="lg-item"><span class="dot" style="background:#2965f1"></span>CSS <b>15.6%</b></div>
          <div class="lg-item"><span class="dot" style="background:#3776ab"></span>Python <b>8.9%</b></div>
          <div class="lg-item"><span class="dot" style="background:#7f52ff"></span>Kotlin <b>6.2%</b></div>
          <div class="lg-item"><span class="dot" style="background:#6f6086"></span>Outros <b>5.3%</b></div>
        </div>
      </div>
    </div>
  </aside>

  <!-- ===================== MAIN ===================== -->
  <main class="main">

    <div class="topbar">
      <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/></svg>
      README.md
    </div>

    <!-- HERO -->
    <section class="hero">
      <div>
        <h2>Desenvolvendo tecnologia<br/>com <span class="accent">propósito e criatividade.</span></h2>
        <p class="sub">Unindo lógica, design e estratégia para criar produtos digitais que fazem a diferença.</p>

        <div class="feature-row">
          <div class="feature-card">
            <div class="ic"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><circle cx="12" cy="12" r="6"/><circle cx="12" cy="12" r="2"/></svg></div>
            <div>
              <div class="ttl">Foco</div>
              <div class="desc">Soluções inteligentes com impacto real</div>
            </div>
          </div>
          <div class="feature-card">
            <div class="ic"><svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></svg></div>
            <div>
              <div class="ttl">Missão</div>
              <div class="desc">Inovar, aprender e evoluir constantemente</div>
            </div>
          </div>
        </div>
      </div>

      <div class="illustration">
        <svg width="230" height="200" viewBox="0 0 230 200" fill="none">
          <defs>
            <linearGradient id="lap" x1="0" y1="0" x2="1" y2="1">
              <stop offset="0" stop-color="#a855f7"/>
              <stop offset="1" stop-color="#ec4899"/>
            </linearGradient>
          </defs>
          <rect x="35" y="30" width="140" height="95" rx="8" fill="#170e26" stroke="url(#lap)" stroke-width="1.5"/>
          <rect x="43" y="38" width="124" height="79" rx="3" fill="#0a0512"/>
          <rect x="50" y="48" width="60" height="4" rx="2" fill="#9333ea"/>
          <rect x="50" y="58" width="90" height="4" rx="2" fill="#3b2a55"/>
          <rect x="50" y="68" width="45" height="4" rx="2" fill="#ec4899"/>
          <rect x="50" y="78" width="75" height="4" rx="2" fill="#3b2a55"/>
          <rect x="50" y="88" width="55" height="4" rx="2" fill="#9333ea"/>
          <path d="M15 130 L195 130 L180 148 L30 148 Z" fill="#1e1230" stroke="url(#lap)" stroke-width="1"/>
          <circle cx="90" cy="15" r="10" fill="#170e26" stroke="url(#lap)" stroke-width="1.5"/>
          <path d="M85 12 Q90 5 95 12" stroke="#22c55e" stroke-width="1.5" fill="none"/>
          <rect x="185" y="100" width="30" height="26" rx="4" fill="#170e26" stroke="url(#lap)" stroke-width="1.2"/>
          <text x="200" y="112" font-size="5" fill="#a855f7" text-anchor="middle" font-family="JetBrains Mono">CODE</text>
          <text x="200" y="119" font-size="5" fill="#ec4899" text-anchor="middle" font-family="JetBrains Mono">DATA</text>
        </svg>
      </div>
    </section>

    <!-- FORMAÇÃO -->
    <section class="panel">
      <div class="panel-title">Formação Acadêmica</div>
      <div class="timeline">
        <div class="t-item">
          <div><h4>Análise e Desenvolvimento de Sistemas</h4><span class="inst">Faculdade Flamingo</span></div>
          <div class="mode">Presencial</div>
        </div>
        <div class="t-item">
          <div><h4>Inteligência Artificial</h4><span class="inst">Univesp</span></div>
          <div class="mode">EAD</div>
        </div>
        <div class="t-item">
          <div><h4>Curso Técnico em Informática</h4><span class="inst">Senac Lapa Tito</span></div>
          <div class="mode">Presencial</div>
        </div>
        <div class="t-item">
          <div><h4>Programação em Desenvolvimento de Sistemas</h4><span class="inst">Instituto PROA</span></div>
          <div class="mode">Presencial</div>
        </div>
        <div class="t-item">
          <div><h4>Cursos extras de TI</h4><span class="inst">Diversos</span></div>
          <div class="mode">EAD / Presencial</div>
        </div>
      </div>
    </section>

    <!-- HABILIDADES -->
    <section class="panel">
      <div class="panel-title">Habilidades &amp; Tecnologias</div>
      <div class="skills-grid">
        <div>
          <div style="font-size:11px;color:var(--text-faint);letter-spacing:.05em;text-transform:uppercase;margin-bottom:12px;">Ferramentas &amp; Frameworks</div>
          <div class="tool-grid">
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 19c-4.3 1.4-4.3-2.5-6-3m12 5v-3.5c0-1 .1-1.4-.5-2 2.8-.3 5.5-1.4 5.5-6a4.6 4.6 0 0 0-1.3-3.2 4.2 4.2 0 0 0-.1-3.2s-1.1-.3-3.5 1.3a12.3 12.3 0 0 0-6.2 0C6.5 2.8 5.4 3.1 5.4 3.1a4.2 4.2 0 0 0-.1 3.2A4.6 4.6 0 0 0 4 9.5c0 4.6 2.7 5.7 5.5 6-.6.6-.6 1.2-.5 2V21"/></svg>Git &amp; GitHub</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>VS Code</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2a5 5 0 0 1 5 5 5 5 0 0 1-5 5 5 5 0 0 1 0-10z"/><path d="M12 12a5 5 0 0 1 5 5 5 5 0 0 1-5 5v-10z"/><path d="M12 2a5 5 0 0 0-5 5 5 5 0 0 0 5 5V2z"/></svg>Figma</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><line x1="3" y1="9" x2="21" y2="9"/></svg>Bootstrap</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M3 5v14a9 3 0 0 0 18 0V5"/></svg>DB Designer</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/></svg>Trello</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M8 15s1.5 2 4 2 4-2 4-2"/></svg>Canva</div>
            <div class="tool"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="6" cy="6" r="1.3"/><circle cx="12" cy="6" r="1.3"/><circle cx="18" cy="6" r="1.3"/><circle cx="6" cy="12" r="1.3"/><circle cx="12" cy="12" r="1.3"/><circle cx="18" cy="12" r="1.3"/><circle cx="6" cy="18" r="1.3"/><circle cx="12" cy="18" r="1.3"/><circle cx="18" cy="18" r="1.3"/></svg>Outros</div>
          </div>
        </div>
        <div>
          <div style="font-size:11px;color:var(--text-faint);letter-spacing:.05em;text-transform:uppercase;margin-bottom:12px;">Outras Competências</div>
          <div class="bar-list">
            <div class="bar-row"><div class="top"><span>Design Responsivo</span><b>95%</b></div><div class="bar-track"><div class="bar-fill" style="width:95%"></div></div></div>
            <div class="bar-row"><div class="top"><span>UX/UI Design</span><b>90%</b></div><div class="bar-track"><div class="bar-fill" style="width:90%"></div></div></div>
            <div class="bar-row"><div class="top"><span>Análise de Dados</span><b>85%</b></div><div class="bar-track"><div class="bar-fill" style="width:85%"></div></div></div>
            <div class="bar-row"><div class="top"><span>Automação &amp; Eletrônica</span><b>80%</b></div><div class="bar-track"><div class="bar-fill" style="width:80%"></div></div></div>
            <div class="bar-row"><div class="top"><span>Gestão de Projetos (P.O)</span><b>95%</b></div><div class="bar-track"><div class="bar-fill" style="width:95%"></div></div></div>
            <div class="bar-row"><div class="top"><span>Produtos Digitais</span><b>90%</b></div><div class="bar-track"><div class="bar-fill" style="width:90%"></div></div></div>
          </div>
        </div>
      </div>
    </section>

    <!-- PROJETOS -->
    <section class="panel">
      <div class="panel-title">Projetos em Destaque</div>
      <div class="proj-grid">

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#b45309,#78350f)">POLIBEE</div>
          <div class="proj-body">
            <h4>Polibee <span style="color:var(--text-faint);font-weight:400">— Mobile &amp; Web</span></h4>
            <p>Conexão entre apicultores e agricultores para aluguel de colmeias</p>
            <div class="proj-tags"><span>HTML</span><span>CSS</span><span>JS</span><span>Kotlin</span><span>MongoDB</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#166534,#052e16)">COLMEIA</div>
          <div class="proj-body">
            <h4>Colmeia Inteligente</h4>
            <p>Monitoramento em tempo real da saúde das abelhas com sensores</p>
            <div class="proj-tags"><span>Arduino</span><span>C++</span><span>DHT11</span><span>Sensores</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#7c2d12,#1c1917)">VERSOVIVO</div>
          <div class="proj-body">
            <h4>Verso Vivo</h4>
            <p>Site de eventos e batalhas de rap</p>
            <div class="proj-tags"><span>HTML</span><span>CSS</span><span>JS</span><span>PHP</span><span>MySQL</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#166534,#14532d)">DIETRICH</div>
          <div class="proj-body">
            <h4>Dietrich</h4>
            <p>E-commerce de produtos naturais</p>
            <div class="proj-tags"><span>HTML</span><span>CSS</span><span>JS</span><span>PHP</span><span>MySQL</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#5b21b6,#1e1b4b)">GAMEON</div>
          <div class="proj-body">
            <h4>GameOn</h4>
            <p>Portal de notícias de jogos</p>
            <div class="proj-tags"><span>HTML</span><span>CSS</span><span>JS</span><span>SQL</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#92400e,#451a03)">GERMÂNICO</div>
          <div class="proj-body">
            <h4>Jovem Germânico</h4>
            <p>Curiosidades sobre a cultura alemã</p>
            <div class="proj-tags"><span>HTML</span><span>CSS</span><span>JS</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#0369a1,#0c4a6e)">WATIFY</div>
          <div class="proj-body">
            <h4>Watify</h4>
            <p>App interativo que mostra em tempo real o quanto você está gastando de água</p>
            <div class="proj-tags"><span>Figma</span><span>Canva</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#9333ea,#4c1d95)">LEVSONG</div>
          <div class="proj-body">
            <h4>LevSong</h4>
            <p>Aplicativo para escutar louvores tranquilos</p>
            <div class="proj-tags"><span>Kotlin</span><span>Android</span><span>Figma</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#334155,#0f172a)">KITO</div>
          <div class="proj-body">
            <h4>Kito</h4>
            <p>Ensino de matemática com níveis básico, intermediário e avançado</p>
            <div class="proj-tags"><span>Canva</span><span>Figma</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#be185d,#4a044e)">ASTROSPACE</div>
          <div class="proj-body">
            <h4>AstroSPACE <span style="color:var(--text-faint);font-weight:400">— Mobile &amp; Web</span></h4>
            <p>Música e artistas, com playlists, lançamentos e novidades do cenário musical</p>
            <div class="proj-tags"><span>Canva</span><span>Figma</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#78350f,#451a03)">JAVACOFFEE</div>
          <div class="proj-body">
            <h4>Java Coffee</h4>
            <p>Aplicativo que mostra opções de cafés para escolher</p>
            <div class="proj-tags"><span>Kotlin</span><span>Android</span><span>Figma</span></div>
          </div>
        </div>

        <div class="proj-card">
          <div class="proj-thumb" style="background:linear-gradient(135deg,#1e293b,#020617)">CURRÍCULO</div>
          <div class="proj-body">
            <h4>Currículo Online</h4>
            <p>Disponível no GitHub Pages</p>
            <div class="proj-tags"><span>HTML</span><span>CSS</span><span>JS</span></div>
          </div>
        </div>

      </div>
      <div class="more-row">e muitos outros projetos...</div>
    </section>

    <!-- DEEP TECH -->
    <section class="panel">
      <div class="panel-title">Tecnologias que Domino Profundamente</div>
      <div class="deep-grid">
        <div class="deep-card">
          <div class="ic"><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg></div>
          <h5>Front-End</h5>
          <p>HTML, CSS, JavaScript, Bootstrap e outros</p>
        </div>
        <div class="deep-card">
          <div class="ic"><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M3 5v14a9 3 0 0 0 18 0V5"/><path d="M3 12a9 3 0 0 0 18 0"/></svg></div>
          <h5>Back-End</h5>
          <p>PHP, MySQL, Python, Golang e outros</p>
        </div>
        <div class="deep-card">
          <div class="ic"><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="6" cy="6" r="3"/><circle cx="6" cy="18" r="3"/><path d="M20 4 8.12 15.88M14.47 14.48 20 20M8.12 8.12 12 12"/></svg></div>
          <h5>Ferramentas</h5>
          <p>Git, GitHub, VS Code, Trello, DB Designer e outros</p>
        </div>
        <div class="deep-card">
          <div class="ic"><svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="4" y="4" width="16" height="16" rx="2"/><rect x="9" y="9" width="6" height="6"/><line x1="9" y1="2" x2="9" y2="4"/><line x1="15" y1="2" x2="15" y2="4"/><line x1="9" y1="20" x2="9" y2="22"/><line x1="15" y1="20" x2="15" y2="22"/></svg></div>
          <h5>Outras Áreas</h5>
          <p>Automação, Produtos Digitais, Análise de Dados, P.O e outros</p>
        </div>
      </div>
    </section>

    <footer>Vitória de Jesus Dietrich — <span class="accent">Desenvolvendo Hoje o Amanhã</span></footer>
  </main>
</div>

</body>
</html>
