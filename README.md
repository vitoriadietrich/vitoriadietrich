<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Vitória de Jesus Dietrich</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Roboto+Mono&display=swap" rel="stylesheet">
  <style>
    /* Reset básico */
    * {margin:0; padding:0; box-sizing:border-box; font-family:'Montserrat', sans-serif;}
    body {
      background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
      color: #333;
      line-height: 1.6;
      padding: 2rem;
    }
    h1 {
      font-size: 2.5rem;
      text-align: center;
      color: #6a1b9a;
      animation: fadeIn 2s ease-in-out;
    }
    p, li {font-size: 1rem; margin-bottom: 0.6rem;}
    a {color: #6a1b9a; text-decoration: none;}
    a:hover {text-decoration: underline; color:#9c27b0;}
    .center {text-align:center;}
    
    /* Efeitos */
    @keyframes fadeIn {0%{opacity:0} 100%{opacity:1}}
    @keyframes typing {
      from {width: 0} 
      to {width: 100%}
    }
    @keyframes blink {50%{border-color: transparent;}}

    .typing {
      width: 22ch;
      animation: typing 3s steps(22), blink 0.75s step-end infinite;
      white-space: nowrap;
      overflow: hidden;
      border-right: 2px solid #6a1b9a;
      font-family: 'Roboto Mono', monospace;
      font-size: 1.2rem;
      margin: 1rem auto;
    }

    /* Cards de projetos */
    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1rem;
      margin-top: 2rem;
    }
    .project-card {
      background: #fff;
      border-radius: 12px;
      padding: 1rem;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .project-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }
    .badge {
      display:inline-block;
      background: #6a1b9a;
      color:#fff;
      padding:0.2rem 0.5rem;
      border-radius:5px;
      font-size:0.8rem;
      margin-right:0.3rem;
      animation: fadeIn 2s ease-in;
    }

    /* Rodapé */
    footer {text-align:center; margin-top:3rem; font-size:0.9rem; color:#555;}
  </style>
</head>
<body>

  <h1>💻 Vitória de Jesus Dietrich</h1>
  <p class="center typing">Desenvolvedora Full Stack Web | UI/UX Designer | Analista de Dados | P.O em Projetos Digitais</p>

  <p class="center">
    📧 <a href="mailto:dietrichvitoria29@email.com">dietrichvitoria29@email.com</a> •
    📱 <a href="https://wa.me/5511944039125" target="_blank">WhatsApp</a> •
    💼 <a href="https://www.linkedin.com/in/vitoriadietrich/" target="_blank">LinkedIn</a> •
    🐙 <a href="https://github.com/vitoriadietrich" target="_blank">GitHub</a>
  </p>

  <hr>

  <h2>👩‍💻 Sobre Mim</h2>
  <p>
    Sou desenvolvedora fullstack web, analista de produtos digitais e dados, e técnica em informática. Amo tecnologia, inovação e automação. Tenho experiência em desenvolvimento web, design digital, análise de dados, produtos e projetos.
  </p>

  <h2>🎓 Formação Acadêmica</h2>
  <ul>
    <li>💻 Engenharia da Computação – Universidade Anhembi Morumbi (EAD)</li>
    <li>🧠 Curso Técnico em Informática - Senac Lapa Tito (Presencial)</li>
    <li>🎓 Programação em Desenvolvimento de Sistemas - Instituto PROA (Presencial)</li>
    <li>Cursos extras em TI (Presencial e EAD)</li>
  </ul>

  <h2>💼 Conhecimentos</h2>
  <ul>
    <li>HTML, CSS, JavaScript, PHP, SQL, MySQL</li>
    <li>Design de artes digitais (convites, cartazes, logotipos etc.)</li>
    <li>Organização de dados em JSON e SQL</li>
    <li>P.O do projeto <span class="badge">PoliBee</span></li>
    <li>Suporte e manutenção de computadores</li>
    <li>Redes de computadores</li>
  </ul>

  <h2>🛠️ Habilidades</h2>
  <ul>
    <li>HTML • CSS • JavaScript • PHP • SQL • MySQL • Python</li>
    <li>Git & GitHub • VS Code • Figma • Canva • Trello • Bootstrap • DB Designer</li>
    <li>Design responsivo • Automação e eletrônica • Trabalho em equipe</li>
  </ul>

  <h2>🚀 Projetos em Destaque</h2>
  <div class="projects">
    <div class="project-card">
      <h3>POLIBEE</h3>
      <p>Conectando apicultores e agricultores para aluguel de colmeias de abelhas.</p>
    </div>
    <div class="project-card">
      <h3>Colmeia Inteligente</h3>
      <p>Monitoramento em tempo real da saúde das abelhas usando Arduino.</p>
    </div>
    <div class="project-card">
      <h3>VersoVivo</h3>
      <p>Site de eventos e batalhas de rap.</p>
    </div>
    <div class="project-card">
      <h3>Dietrich</h3>
      <p>Site de vendas de temperos e produtos naturais.</p>
    </div>
    <div class="project-card">
      <h3>GameOn</h3>
      <p>Site de notícias sobre lançamentos de jogos.</p>
    </div>
    <div class="project-card">
      <h3>Jovem Germânico</h3>
      <p>Curiosidades sobre a cultura alemã.</p>
    </div>
    <div class="project-card">
      <h3>Currículo Online</h3>
      <p>Disponível no GitHub Pages.</p>
    </div>
  </div>

  <footer>Feito com 💜 por Vitória de Jesus Dietrich</footer>

</body>
</html>
