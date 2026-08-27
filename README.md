<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=28&duration=3000&pause=500&color=0E75B6&center=true&vCenter=true&width=500&lines=Hi!+I'm+S4ndulos;Technical+Informatics+Student;Python+%7C+FastAPI+%7C+C%23;Ethical+Hacking+%26+Networks;Arch+Linux+enthusiast" alt="Typing SVG" />
  <br/>
  <img src="https://komarev.com/ghpvc/?username=sqx&label=Profile%20Views&color=0e75b6&style=flat" alt="Profile Views" />
</div>

---

### Sobre mí

<tr>
<td width="60%">

- **Certificados:** EJPT EJPTV2
-  **Edad:** 16 años  
-  **Ubicación:** Buenos Aires, Argentina  
-  **Estudios:** Técnico en Informática  
-  **Lenguajes favoritos:** Python (FastAPI), C/C++ (bajo nivel), C# (.NET 10 en aprendizaje)  
-  **Intereses:** Seguridad informática, hacking ético, redes, automatización  
-  **Personalización:** Arch Linux + BlackArch tools, configuro mi propio entorno  
-  **Laboratorios:** Escenarios con Packet Tracer, GNS3, y máquinas virtuales para pruebas de penetración  
-  **Comunidad:** Ayudo a nuevos usuarios en servidores de Discord (programación y ciberseguridad)  

---

### Entornos y herramientas

| Sistema / Distro         | Editores / IDEs             | Terminal / Shell      |
| ------------------------ | --------------------------- | --------------------- |
| Windows 11/10/7       | VS Code / Visual Studio  |  CMD / PowerShell    |
| Arch Linux + BlackArch| Linux Terminal           |  pacman / yay       |
| Kali Linux            | Neovim (personalizado)   |  Alacritty          |
| Raspberry Pi 5 (PiOS) | Vim                      |  Zsh + Oh My Zsh    |
| Debian / Ubuntu Server| Sublime Text             |  Bash               |

---

### Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" />
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" />
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white" />
  <img src="https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white" />
  <img src="https://img.shields.io/badge/Nmap-0E83CD?style=for-the-badge&logo=nmap&logoColor=white" />
  <img src="https://img.shields.io/badge/Metasploit-2596CD?style=for-the-badge&logo=metasploit&logoColor=white" />
</p>

---

### Conocimientos de redes y seguridad

| Área | Tecnologías / Herramientas | Proyectos / Labs |
|------|----------------------------|------------------|
| **Protocolos** | TCP/IP, HTTP/2, DNS, DHCP, VPN (WireGuard) | Configuración de servidor DHCP en Linux |
| **Firewall** | iptables, nftables, Windows Defender Firewall | Reglas personalizadas en Arch y Windows |
| **DNS** | Pi-hole (Raspberry Pi 5), Unbound | Bloqueo de anuncios y filtrado en red local |
| **Análisis de tráfico** | Wireshark, tcpdump, Nmap | Escaneos de red, detección de vulnerabilidades |
| **Pentesting** | Metasploit, BlackArch tools, keylogger bypass | Laboratorios propios con máquinas vulnerables |
| **VPN** | WireGuard, PiVPN | Levantamiento de servicios fuera del router |

---

### Proyecto destacado: DesktopManagerStock API

> **Repositorio:** [sqx/DesktopManagerStock](https://github.com/sqx/DesktopManagerStock)

API REST para gestión de inventario y stock, desarrollada con **FastAPI + SQLite + JWT**. Incluye autenticación por roles (admin, editor, lector), rate limiting, registro de movimientos, y despliegue con Docker.

#### Características técnicas

- **Framework:** FastAPI (Python)
- **Base de datos:** SQLite con SQLAlchemy ORM (índices optimizados)
- **Autenticación:** JWT (python-jose) + bcrypt (passlib)
- **Roles:** `admin` (total), `editor` (puede modificar stock), `lector` (solo lectura)
- **Seguridad:** Variables de entorno con Pydantic Settings, validación de SECRET_KEY, CORS configurable, rate limiting por endpoint (SlowAPI)
- **Movimientos:** Registro automático de cada entrada/salida de stock con auditoría (usuario, fecha, stock resultante)
- **Logging:** Archivo `app.log` + consola, rotación automática
- **Despliegue:** Docker + docker-compose, listo para Raspberry Pi 5
- **Documentación interactiva:** `/docs` (Swagger) y `/redoc`

> [!NOTE]
> La API está en constante evolución. Actualmente en versión `0.1.3` (ver `.env.example`).  

<p align="center">
  <a href="https://github.com/sqx/DesktopManagerStock">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=MauroKpoxD&repo=DesktopManagerStock&theme=radical&hide_border=true&bg_color=0D1117&title_color=0E75B6&icon_color=0E75B6&text_color=FFFFFF" />
  </a>
</p>

---

### Python: Librerías que uso / aprendo

| Categoría | Librerías |
|-----------|------------|
| **Web frameworks** | FastAPI, Flask (básico) |
| **Seguridad** | cryptography (Fernet), python-jose, passlib, bcrypt |
| **Bases de datos** | SQLAlchemy, SQLite3, Alembic (planeado) |
| **Validación** | Pydantic, Pydantic Settings |
| **Testing** | pytest, pytest-cov, factory_boy |
| **Rate limiting** | slowapi |
| **Logging** | logging estándar + rotación |
| **Networking** | requests, httpx, scapy (aprendiendo) |

---

### Conecta conmigo

<p align="center">
  <a href="https://twitter.com/sqx"><img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" /></a>
  <a href="https://discord.com/users/wwwwwwwwwwwvvwvwvwvvvwv
"><img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" /></a>
  <a href="mailto:sqx@atlassoftware.org"><img src="https://img.shields.io/badge/atlassoftware.xyz-8B89CC?style=for-the-badge&logoColor=white" /></a>
  <a href="https://github.com/sqx"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0E75B6&height=100&section=footer" />
  <p><i>"sandulos !"</i></p>
</div>
