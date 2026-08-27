<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S4ndulos – Technical Informatics Student</title>
  <meta name="description" content="S4ndulos – Técnico en Informática, Python, FastAPI, C#, Ethical Hacking y redes. Buenos Aires, Argentina." />
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg:        #0D1117;
      --bg2:       #161B22;
      --bg3:       #1C2430;
      --accent:    #0E75B6;
      --accent2:   #1A8FD1;
      --accent3:   #0A5A8A;
      --text:      #E6EDF3;
      --muted:     #8B949E;
      --border:    #21262D;
      --green:     #3FB950;
      --purple:    #7C3AED;
      --glow:      0 0 20px rgba(14,117,182,0.35);
      --glow2:     0 0 40px rgba(14,117,182,0.15);
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Inter', sans-serif;
      min-height: 100vh;
      overflow-x: hidden;
    }

    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(14,117,182,0.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(14,117,182,0.04) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
      z-index: 0;
    }

    .orb {
      position: fixed;
      border-radius: 50%;
      filter: blur(80px);
      pointer-events: none;
      z-index: 0;
      animation: floatOrb 12s ease-in-out infinite;
    }
    .orb1 { width: 400px; height: 400px; background: rgba(14,117,182,0.12); top: -100px; right: -100px; animation-delay: 0s; }
    .orb2 { width: 300px; height: 300px; background: rgba(124,58,237,0.08); bottom: 200px; left: -80px; animation-delay: -4s; }
    .orb3 { width: 250px; height: 250px; background: rgba(63,185,80,0.06); top: 50%; left: 50%; animation-delay: -8s; }

    @keyframes floatOrb {
      0%, 100% { transform: translate(0, 0) scale(1); }
      33%       { transform: translate(30px, -20px) scale(1.05); }
      66%       { transform: translate(-20px, 15px) scale(0.95); }
    }

    .container {
      position: relative;
      z-index: 1;
      max-width: 900px;
      margin: 0 auto;
      padding: 0 1.5rem 4rem;
    }

    .hero {
      text-align: center;
      padding: 4rem 0 2.5rem;
    }

    .hero-avatar {
      width: 110px;
      height: 110px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--accent), var(--purple));
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 1.5rem;
      font-size: 2.2rem;
      font-weight: 700;
      color: #fff;
      box-shadow: var(--glow), 0 0 0 4px var(--bg2);
      animation: pulse 3s ease-in-out infinite;
      font-family: 'Fira Code', monospace;
    }

    @keyframes pulse {
      0%, 100% { box-shadow: var(--glow), 0 0 0 4px var(--bg2); }
      50%       { box-shadow: 0 0 35px rgba(14,117,182,0.6), 0 0 0 4px var(--bg2); }
    }

    .hero h1 {
      font-size: clamp(2rem, 5vw, 3rem);
      font-weight: 800;
      background: linear-gradient(135deg, #fff 30%, var(--accent2));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      letter-spacing: -0.5px;
      margin-bottom: 0.5rem;
    }

    .typing-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.5rem;
      margin: 1rem 0 1.5rem;
    }

    .tag {
      font-family: 'Fira Code', monospace;
      font-size: 0.78rem;
      padding: 0.3rem 0.75rem;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: var(--bg2);
      color: var(--accent2);
      transition: all 0.25s;
    }
    .tag:hover {
      border-color: var(--accent);
      background: var(--bg3);
      box-shadow: 0 0 12px rgba(14,117,182,0.25);
      transform: translateY(-2px);
    }

    .views-badge {
      display: inline-block;
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 0.35rem 0.9rem;
      font-family: 'Fira Code', monospace;
      font-size: 0.8rem;
      color: var(--muted);
    }

    .divider {
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--accent3), transparent);
      margin: 2.5rem 0;
    }

    .section-title {
      font-size: 1.25rem;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 1.25rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }
    .section-title .icon { font-size: 1.1rem; }

    .about-grid { display: grid; gap: 0.65rem; }

    .about-item {
      display: flex;
      align-items: flex-start;
      gap: 0.75rem;
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 0.75rem 1rem;
      transition: all 0.25s;
    }
    .about-item:hover {
      border-color: var(--accent3);
      background: var(--bg3);
      transform: translateX(4px);
    }
    .about-item .emoji { font-size: 1.1rem; flex-shrink: 0; margin-top: 0.05rem; }
    .about-item .label { font-weight: 600; color: var(--accent2); margin-right: 0.4rem; }
    .about-item .value { color: var(--muted); font-size: 0.9rem; }

    .fancy-table {
      width: 100%;
      border-collapse: collapse;
      font-size: 0.88rem;
      border-radius: 12px;
      overflow: hidden;
      border: 1px solid var(--border);
    }
    .fancy-table thead tr {
      background: linear-gradient(135deg, var(--accent3), #0a3d5c);
    }
    .fancy-table thead th {
      padding: 0.8rem 1rem;
      text-align: left;
      font-weight: 600;
      color: #fff;
      font-size: 0.82rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
    }
    .fancy-table tbody tr {
      background: var(--bg2);
      border-top: 1px solid var(--border);
      transition: background 0.2s;
    }
    .fancy-table tbody tr:hover { background: var(--bg3); }
    .fancy-table tbody td {
      padding: 0.75rem 1rem;
      color: var(--muted);
      vertical-align: top;
    }
    .fancy-table tbody td strong { color: var(--text); font-weight: 500; }

    .badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      justify-content: center;
    }
    .badge-img {
      height: 28px;
      border-radius: 6px;
      transition: transform 0.2s, filter 0.2s;
      filter: brightness(0.92);
    }
    .badge-img:hover {
      transform: translateY(-3px) scale(1.05);
      filter: brightness(1.1);
    }

    .project-card {
      background: var(--bg2);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 1.5rem;
      position: relative;
      overflow: hidden;
      transition: all 0.3s;
    }
    .project-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 3px;
      background: linear-gradient(90deg, var(--accent), var(--purple));
    }
    .project-card:hover {
      border-color: var(--accent3);
      box-shadow: var(--glow2);
      transform: translateY(-3px);
    }
    .project-title {
      font-size: 1.15rem;
      font-weight: 700;
      color: var(--text);
      margin-bottom: 0.5rem;
    }
    .project-title a {
      color: inherit;
      text-decoration: none;
      transition: color 0.2s;
    }
    .project-title a:hover { color: var(--accent2); }
    .project-desc {
      color: var(--muted);
      font-size: 0.9rem;
      line-height: 1.6;
      margin-bottom: 1rem;
    }
    .feature-list {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 0.6rem;
      margin-top: 1rem;
    }
    .feature-item {
      background: var(--bg3);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 0.6rem 0.9rem;
      font-size: 0.82rem;
      color: var(--muted);
    }
    .feature-item strong { color: var(--accent2); }
    .note-box {
      background: rgba(14,117,182,0.08);
      border: 1px solid rgba(14,117,182,0.3);
      border-radius: 8px;
      padding: 0.75rem 1rem;
      font-size: 0.85rem;
      color: var(--muted);
      margin-top: 1rem;
      display: flex;
      gap: 0.5rem;
      align-items: flex-start;
    }
    .note-box::before { content: 'ℹ️'; flex-shrink: 0; }

    .socials {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.75rem;
    }
    .social-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      padding: 0.6rem 1.2rem;
      border-radius: 10px;
      font-weight: 600;
      font-size: 0.85rem;
      text-decoration: none;
      transition: all 0.25s;
      border: 1px solid transparent;
    }
    .social-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 20px rgba(0,0,0,0.4); }
    .social-twitter  { background: #1DA1F2; color: #fff; }
    .social-discord  { background: #5865F2; color: #fff; }
    .social-email    { background: #8B89CC; color: #fff; }
    .social-github   { background: #161B22; color: #fff; border-color: var(--border); }

    .footer {
      text-align: center;
      margin-top: 3rem;
      padding-top: 2rem;
    }
    .footer-quote {
      font-style: italic;
      color: var(--muted);
      font-family: 'Fira Code', monospace;
      font-size: 0.9rem;
    }
    .footer-quote span { color: var(--accent2); }

    .fade-in {
      opacity: 0;
      transform: translateY(24px);
      transition: opacity 0.55s ease, transform 0.55s ease;
    }
    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    @media (max-width: 600px) {
      .fancy-table thead th, .fancy-table tbody td { padding: 0.6rem 0.7rem; font-size: 0.8rem; }
      .hero h1 { font-size: 2rem; }
    }
  </style>
</head>
<body>

  <div class="orb orb1"></div>
  <div class="orb orb2"></div>
  <div class="orb orb3"></div>

  <div class="container">

    <!-- HERO -->
    <section class="hero fade-in">
      <div class="hero-avatar">S4</div>
      <h1>S4ndulos</h1>
      <div class="typing-row">
        <span class="tag">Technical Informatics Student</span>
        <span class="tag">Python · FastAPI · C#</span>
        <span class="tag">Ethical Hacking &amp; Networks</span>
        <span class="tag">Arch Linux enthusiast</span>
      </div>
      <div class="views-badge">👁️ Profile Views · sqx</div>
    </section>

    <div class="divider"></div>

    <!-- SOBRE MÍ -->
    <section class="fade-in">
      <h2 class="section-title"><span class="icon">👤</span> Sobre mí</h2>
      <div class="about-grid">
        <div class="about-item"><span class="emoji">🏅</span><div><span class="label">Certificados:</span><span class="value">EJPT · EJPTV2</span></div></div>
        <div class="about-item"><span class="emoji">🎂</span><div><span class="label">Edad:</span><span class="value">16 años</span></div></div>
        <div class="about-item"><span class="emoji">📍</span><div><span class="label">Ubicación:</span><span class="value">Buenos Aires, Argentina</span></div></div>
        <div class="about-item"><span class="emoji">📚</span><div><span class="label">Estudios:</span><span class="value">Técnico en Informática</span></div></div>
        <div class="about-item"><span class="emoji">💻</span><div><span class="label">Lenguajes favoritos:</span><span class="value">Python (FastAPI), C/C++ (bajo nivel), C# (.NET 10 en aprendizaje)</span></div></div>
        <div class="about-item"><span class="emoji">🔐</span><div><span class="label">Intereses:</span><span class="value">Seguridad informática, hacking ético, redes, automatización</span></div></div>
        <div class="about-item"><span class="emoji">🐧</span><div><span class="label">Personalización:</span><span class="value">Arch Linux + BlackArch tools, configuro mi propio entorno</span></div></div>
        <div class="about-item"><span class="emoji">🧪</span><div><span class="label">Laboratorios:</span><span class="value">Packet Tracer, GNS3, y VMs para pruebas de penetración</span></div></div>
        <div class="about-item"><span class="emoji">🤝</span><div><span class="label">Comunidad:</span><span class="value">Ayudo en servidores de Discord de programación y ciberseguridad</span></div></div>
      </div>
    </section>

    <div class="divider"></div>

    <!-- ENTORNOS -->
    <section class="fade-in">
      <h2 class="section-title"><span class="icon">🛠️</span> Entornos y herramientas</h2>
      <table class="fancy-table">
        <thead>
          <tr><th>Sistema / Distro</th><th>Editores / IDEs</th><th>Terminal / Shell</th></tr>
        </thead>
        <tbody>
          <tr><td>🪟 Windows 11/10/7</td><td>VS Code / Visual Studio</td><td>CMD / PowerShell</td></tr>
          <tr><td>🐧 Arch Linux + BlackArch</td><td>Linux Terminal</td><td>pacman / yay</td></tr>
          <tr><td>🐉 Kali Linux</td><td>Neovim (personalizado)</td><td>Alacritty</td></tr>
          <tr><td>🍓 Raspberry Pi 5 (PiOS)</td><td>Vim</td><td>Zsh + Oh My Zsh</td></tr>
          <tr><td>🟠 Debian / Ubuntu Server</td><td>Sublime Text</td><td>Bash</td></tr>
        </tbody>
      </table>
    </section>

    <div class="divider"></div>

    <!-- TECH STACK -->
    <section class="fade-in">
      <h2 class="section-title"><span class="icon">⚡</span> Tech Stack</h2>
      <div class="badges">
        <img class="badge-img" src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
        <img class="badge-img" src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
        <img class="badge-img" src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
        <img class="badge-img" src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT" />
        <img class="badge-img" src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
        <img class="badge-img" src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++" />
        <img class="badge-img" src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white" alt="C#" />
        <img class="badge-img" src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET" />
        <img class="badge-img" src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
        <img class="badge-img" src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
        <img class="badge-img" src="https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" alt="Wireshark" />
        <img class="badge-img" src="https://img.shields.io/badge/Nmap-0E83CD?style=for-the-badge&logo=nmap&logoColor=white" alt="Nmap" />
        <img class="badge-img" src="https://img.shields.io/badge/Metasploit-2596CD?style=for-the-badge&logo=metasploit&logoColor=white" alt="Metasploit" />
      </div>
    </section>

    <div class="divider"></div>

    <!-- REDES Y SEGURIDAD -->
    <section class="fade-in">
      <h2 class="section-title"><span class="icon">🌐</span> Conocimientos de redes y seguridad</h2>
      <table class="fancy-table">
        <thead>
          <tr><th>Área</th><th>Tecnologías / Herramientas</th><th>Proyectos / Labs</th></tr>
        </thead>
        <tbody>
          <tr><td><strong>Protocolos</strong></td><td>TCP/IP, HTTP/2, DNS, DHCP, VPN (WireGuard)</td><td>Configuración de servidor DHCP en Linux</td></tr>
          <tr><td><strong>Firewall</strong></td><td>iptables, nftables, Windows Defender Firewall</td><td>Reglas personalizadas en Arch y Windows</td></tr>
          <tr><td><strong>DNS</strong></td><td>Pi-hole (Raspberry Pi 5), Unbound</td><td>Bloqueo de anuncios y filtrado en red local</td></tr>
          <tr><td><strong>Análisis de tráfico</strong></td><td>Wireshark, tcpdump, Nmap</td><td>Escaneos de red, detección de vulnerabilidades</td></tr>
          <tr><td><strong>Pentesting</strong></td><td>Metasploit, BlackArch tools, keylogger bypass</td><td>Laboratorios propios con máquinas vulnerables</td></tr>
          <tr><td><strong>VPN</strong></td><td>WireGuard, PiVPN</td><td>Levantamiento de servicios fuera del router</td></tr>
        </tbody>
      </table>
    </section>

    <div class="divider"></div>

    <!-- PROYECTO DESTACADO -->
    <section class="fade-in">
      <h2 class="section-title"><span class="icon">🚀</span> Proyecto destacado</h2>
      <div class="project-card">
        <div class="project-title">
          <a href="https://github.com/sqx/DesktopManagerStock" target="_blank" rel="noopener">
            📦 DesktopManagerStock API
          </a>
        </div>
        <p class="project-desc">
          API REST para gestión de inventario y stock, desarrollada con <strong>FastAPI + SQLite + JWT</strong>.
          Incluye autenticación por roles, rate limiting, registro de movimientos y despliegue con Docker.
        </p>
        <div class="feature-list">
          <div class="feature-item"><strong>Framework:</strong> FastAPI (Python)</div>
          <div class="feature-item"><strong>Base de datos:</strong> SQLite + SQLAlchemy ORM</div>
          <div class="feature-item"><strong>Autenticación:</strong> JWT + bcrypt (passlib)</div>
          <div class="feature-item"><strong>Roles:</strong> admin · editor · lector</div>
          <div class="feature-item"><strong>Seguridad:</strong> Pydantic Settings, CORS, SlowAPI</div>
          <div class="feature-item"><strong>Movimientos:</strong> Auditoría con usuario, fecha y stock</div>
          <div class="feature-item"><strong>Logging:</strong> app.log + consola, rotación automática</div>
          <div class="feature-item"><strong>Despliegue:</strong> Docker + docker-compose (Raspberry Pi 5)</div>
          <div class="feature-item"><strong>Docs:</strong> /docs (Swagger) y /redoc</div>
        </div>
        <div class="note-box">
          La API está en constante evolución. Actualmente en versión <strong>0.1.3</strong>.
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <!-- PYTHON LIBS -->
    <section class="fade-in">
      <h2 class="section-title"><span class="icon">🐍</span> Python: Librerías que uso / aprendo</h2>
      <table class="fancy-table">
        <thead>
          <tr><th>Categoría</th><th>Librerías</th></tr>
        </thead>
        <tbody>
          <tr><td><strong>Web frameworks</strong></td><td>FastAPI, Flask (básico)</td></tr>
          <tr><td><strong>Seguridad</strong></td><td>cryptography (Fernet), python-jose, passlib, bcrypt</td></tr>
          <tr><td><strong>Bases de datos</strong></td><td>SQLAlchemy, SQLite3, Alembic (planeado)</td></tr>
          <tr><td><strong>Validación</strong></td><td>Pydantic, Pydantic Settings</td></tr>
          <tr><td><strong>Testing</strong></td><td>pytest, pytest-cov, factory_boy</td></tr>
          <tr><td><strong>Rate limiting</strong></td><td>slowapi</td></tr>
          <tr><td><strong>Logging</strong></td><td>logging estándar + rotación</td></tr>
          <tr><td><strong>Networking</strong></td><td>requests, httpx, scapy (aprendiendo)</td></tr>
        </tbody>
      </table>
    </section>

    <div class="divider"></div>

    <!-- CONECTA -->
    <section class="fade-in" style="text-align:center;">
      <h2 class="section-title" style="justify-content:center;"><span class="icon">🤝</span> Conecta conmigo</h2>
      <div class="socials">
        <a href="https://twitter.com/sqx" class="social-btn social-twitter" target="_blank" rel="noopener">🐦 Twitter</a>
        <a href="https://discord.com/users/wwwwwwwwwwwvvwvwvwvvvwv" class="social-btn social-discord" target="_blank" rel="noopener">💬 Discord</a>
        <a href="mailto:sqx@atlassoftware.org" class="social-btn social-email">✉️ atlassoftware.xyz</a>
        <a href="https://github.com/sqx" class="social-btn social-github" target="_blank" rel="noopener">🐙 GitHub</a>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer fade-in">
      <div class="divider"></div>
      <div class="footer-quote"><span>"</span>S4ndulos !<span>"</span></div>
      <p style="color:var(--muted);font-size:0.75rem;margin-top:0.75rem;font-family:'Fira Code',monospace;">
        © 2026 S4ndulos · Buenos Aires, Argentina
      </p>
    </footer>

  </div>

  <script>
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry, i) => {
        if (entry.isIntersecting) {
          setTimeout(() => entry.target.classList.add('visible'), i * 80);
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1 });

    document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));
  </script>
</body>
</html>
