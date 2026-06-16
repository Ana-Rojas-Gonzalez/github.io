# github.io
Welcome to my dossier | Ana Rojas G
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Ana Rojas González — Services Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Inter:wght@300;400;500&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --navy: #0D1B2A;
      --gold: #C9A84C;
      --gold-light: #E8D08A;
      --cream: #F7F4EE;
      --silver: #8A9BB0;
      --text: #1A1A2E;
      --text-muted: #5C6B7E;
      --border: rgba(13, 27, 42, 0.12);
      --card-bg: #FFFFFF;
      --bg: #F7F4EE;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      min-height: 100vh;
    }

    /* NAV */
    nav {
      position: sticky;
      top: 0;
      z-index: 100;
      background: rgba(247, 244, 238, 0.92);
      backdrop-filter: blur(8px);
      border-bottom: 0.5px solid var(--border);
      padding: 0 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 56px;
    }

    .nav-brand {
      font-family: 'Playfair Display', serif;
      font-size: 1.1rem;
      font-weight: 600;
      color: var(--navy);
      text-decoration: none;
    }

    .nav-brand span { color: var(--gold); }

    .nav-links {
      display: flex;
      gap: 1.5rem;
      list-style: none;
    }

    .nav-links a {
      font-size: 13px;
      color: var(--text-muted);
      text-decoration: none;
      transition: color 0.2s;
    }

    .nav-links a:hover { color: var(--gold); }

    /* HERO */
    .hero {
      max-width: 900px;
      margin: 0 auto;
      padding: 5rem 2rem 4rem;
      position: relative;
      overflow: hidden;
    }

    .hero-watermark {
      position: absolute;
      top: 50%;
      right: -2rem;
      transform: translateY(-60%);
      font-family: 'Playfair Display', serif;
      font-size: 10rem;
      font-weight: 600;
      color: rgba(201, 168, 76, 0.08);
      letter-spacing: 0.2em;
      pointer-events: none;
      user-select: none;
      line-height: 1;
    }

    .hero-tag {
      display: inline-block;
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--gold);
      border: 1px solid var(--gold);
      border-radius: 99px;
      padding: 4px 14px;
      margin-bottom: 1.5rem;
    }

    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.5rem, 6vw, 4rem);
      font-weight: 600;
      line-height: 1.1;
      margin-bottom: 0.75rem;
      color: var(--navy);
    }

    .hero h1 span { color: var(--gold); }

    .hero-tagline {
      font-size: 15px;
      color: var(--text-muted);
      line-height: 1.7;
      max-width: 540px;
      margin-bottom: 2rem;
    }

    .hero-contact {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      align-items: center;
    }

    .hero-contact a,
    .hero-contact span {
      display: flex;
      align-items: center;
      gap: 7px;
      font-size: 13px;
      color: var(--text-muted);
      text-decoration: none;
      transition: color 0.2s;
    }

    .hero-contact a:hover { color: var(--gold); }

    .hero-contact svg {
      width: 16px;
      height: 16px;
      stroke: currentColor;
      fill: none;
      stroke-width: 1.8;
      stroke-linecap: round;
      stroke-linejoin: round;
      flex-shrink: 0;
    }

    /* SECTIONS */
    section {
      max-width: 900px;
      margin: 0 auto;
      padding: 3rem 2rem;
      border-top: 0.5px solid var(--border);
    }

    .section-label {
      font-size: 11px;
      font-weight: 500;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 0.4rem;
    }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.6rem;
      font-weight: 600;
      color: var(--navy);
      margin-bottom: 0.3rem;
    }

    .section-sub {
      font-size: 13px;
      color: var(--text-muted);
      margin-bottom: 2rem;
    }

    /* SERVICES GRID */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
      gap: 14px;
    }

    .service-card {
      background: var(--card-bg);
      border: 0.5px solid var(--border);
      border-radius: 14px;
      padding: 1.5rem;
      transition: border-color 0.25s, box-shadow 0.25s, transform 0.2s;
    }

    .service-card:hover {
      border-color: var(--gold);
      box-shadow: 0 4px 24px rgba(201, 168, 76, 0.12);
      transform: translateY(-2px);
    }

    .service-icon {
      width: 40px;
      height: 40px;
      background: rgba(201, 168, 76, 0.1);
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1rem;
    }

    .service-icon svg {
      width: 20px;
      height: 20px;
      stroke: var(--gold);
      fill: none;
      stroke-width: 1.8;
      stroke-linecap: round;
      stroke-linejoin: round;
    }

    .service-name-es {
      font-weight: 500;
      font-size: 14px;
      color: var(--navy);
      margin-bottom: 2px;
    }

    .service-name-en {
      font-size: 11px;
      color: var(--silver);
      font-style: italic;
      margin-bottom: 0.75rem;
    }

    .service-desc {
      font-size: 12.5px;
      color: var(--text-muted);
      line-height: 1.7;
    }

    /* SKILLS */
    .pills {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 2rem;
    }

    .pill {
      font-size: 11.5px;
      padding: 5px 13px;
      border-radius: 99px;
      border: 0.5px solid var(--border);
      color: var(--text-muted);
      background: var(--card-bg);
    }

    /* CLIENTS */
    .clients-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 10px;
    }

    .client-item {
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 12.5px;
      color: var(--text-muted);
      background: var(--card-bg);
      border: 0.5px solid var(--border);
      border-radius: 10px;
      padding: 10px 14px;
    }

    .client-item svg {
      width: 15px;
      height: 15px;
      stroke: var(--gold);
      fill: none;
      stroke-width: 1.8;
      stroke-linecap: round;
      flex-shrink: 0;
    }

    /* PROCESS */
    .process-steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 14px;
    }

    .process-step {
      background: var(--card-bg);
      border: 0.5px solid var(--border);
      border-radius: 14px;
      padding: 1.25rem;
      text-align: center;
    }

    .step-num {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      font-weight: 600;
      color: rgba(201, 168, 76, 0.3);
      margin-bottom: 0.25rem;
    }

    .step-title {
      font-size: 13px;
      font-weight: 500;
      color: var(--navy);
      margin-bottom: 0.25rem;
    }

    .step-desc {
      font-size: 11.5px;
      color: var(--text-muted);
      line-height: 1.6;
    }

    /* CTA */
    .cta-section {
      background: var(--navy);
      max-width: 100%;
      padding: 4rem 2rem;
      text-align: center;
      margin-top: 1rem;
    }

    .cta-inner {
      max-width: 560px;
      margin: 0 auto;
    }

    .cta-section .section-label {
      color: var(--gold-light);
    }

    .cta-section h2 {
      font-family: 'Playfair Display', serif;
      font-size: 2rem;
      font-weight: 600;
      color: #fff;
      margin-bottom: 0.75rem;
    }

    .cta-section p {
      font-size: 14px;
      color: var(--silver);
      margin-bottom: 2rem;
      line-height: 1.7;
    }

    .cta-btn {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-family: 'Inter', sans-serif;
      font-size: 14px;
      font-weight: 500;
      color: var(--navy);
      background: var(--gold);
      border: none;
      border-radius: 99px;
      padding: 12px 28px;
      cursor: pointer;
      text-decoration: none;
      transition: background 0.2s, transform 0.15s;
    }

    .cta-btn:hover {
      background: var(--gold-light);
      transform: translateY(-1px);
    }

    .cta-btn svg {
      width: 16px;
      height: 16px;
      stroke: currentColor;
      fill: none;
      stroke-width: 2;
      stroke-linecap: round;
    }

    /* FOOTER */
    footer {
      background: var(--navy);
      border-top: 0.5px solid rgba(255,255,255,0.08);
      padding: 1.5rem 2rem;
      text-align: center;
    }

    footer p {
      font-size: 11.5px;
      color: var(--silver);
    }

    footer p a {
      color: var(--gold);
      text-decoration: none;
    }

    /* RESPONSIVE */
    @media (max-width: 600px) {
      .hero { padding: 3rem 1.25rem 2.5rem; }
      .hero-watermark { font-size: 5rem; }
      section { padding: 2rem 1.25rem; }
      .nav-links { display: none; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <a href="#" class="nav-brand">Ana <span>Rojas</span></a>
    <ul class="nav-links">
      <li><a href="#servicios">Servicios</a></li>
      <li><a href="#clientes">Clientes</a></li>
      <li><a href="#proceso">Proceso</a></li>
      <li><a href="#contacto">Contacto</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <div class="hero">
    <div class="hero-watermark">ARG</div>
    <div class="hero-tag">Services Portfolio · Dossier de Servicios</div>
    <h1>Ana <span>Rojas</span> González</h1>
    <p class="hero-tagline">
      Project Manager &amp; Digital Strategist con 4.5+ años liderando proyectos de alto impacto con clientes globales.<br>
      <em style="color:#8A9BB0; font-style:normal;">4.5+ years leading high-impact global projects across virtual events, marketing &amp; education.</em>
    </p>
    <div class="hero-contact">
      <a href="mailto:ana.rglez@gmail.com">
        <svg viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 7 10-7"/></svg>
        ana.rglez@gmail.com
      </a>
      <span>
        <svg viewBox="0 0 24 24"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.26 12 19.79 19.79 0 0 1 1.17 3.39 2 2 0 0 1 3.15 1h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L7.09 8.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 21 16z"/></svg>
        +52 122 258 8857
      </span>
      <span>
        <svg viewBox="0 0 24 24"><path d="M20 10c0 6-8 12-8 12s-8-6-8-12a8 8 0 0 1 16 0Z"/><circle cx="12" cy="10" r="3"/></svg>
        Puebla, México · Remote
      </span>
    </div>
  </div>

  <!-- SERVICES -->
  <section id="servicios">
    <div class="section-label">Servicios · Services</div>
    <div class="section-title">¿En qué puedo ayudarte?</div>
    <p class="section-sub">How can I help you? — Soluciones que combinan estrategia, tecnología y ejecución</p>

    <div class="services-grid">

      <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24"><rect x="3" y="3" width="7" height="7" rx="1"/><rect x="14" y="3" width="7" height="7" rx="1"/><rect x="3" y="14" width="7" height="7" rx="1"/><rect x="14" y="14" width="7" height="7" rx="1"/></svg>
        </div>
        <p class="service-name-es">Gestión de Proyectos</p>
        <p class="service-name-en">Project Management</p>
        <p class="service-desc">Planificación, seguimiento y entrega de proyectos complejos con metodologías Agile/Scrum. Desde kickoff hasta cierre y reporte final.</p>
      </div>

      <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24"><rect x="3" y="4" width="18" height="18" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/><path d="M8 14h.01M12 14h.01M16 14h.01M8 18h.01M12 18h.01"/></svg>
        </div>
        <p class="service-name-es">Eventos Virtuales e Híbridos</p>
        <p class="service-name-en">Virtual &amp; Hybrid Events</p>
        <p class="service-desc">Producción integral de eventos digitales: plataforma, cronograma, coordinación de equipos y reportes post-evento con analítica.</p>
      </div>

      <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24"><path d="M22 12h-4l-3 9L9 3l-3 9H2"/></svg>
        </div>
        <p class="service-name-es">Marketing Digital</p>
        <p class="service-name-en">Digital Marketing</p>
        <p class="service-desc">Campañas de email marketing, estrategia SEO y optimización de plataformas digitales orientadas a resultados medibles.</p>
      </div>

      <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
        </div>
        <p class="service-name-es">Coordinación Educativa</p>
        <p class="service-name-en">Educational Coordination</p>
        <p class="service-desc">Diseño y gestión de programas de formación, scheduling, comunicación con participantes y distribución de materiales.</p>
      </div>

      <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        </div>
        <p class="service-name-es">Gestión Web</p>
        <p class="service-name-en">Web Operations</p>
        <p class="service-desc">Administración de sitios WordPress/cPanel, actualizaciones, optimización de rendimiento, accesibilidad y SEO on-page.</p>
      </div>

      <div class="service-card">
        <div class="service-icon">
          <svg viewBox="0 0 24 24"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87M16 3.13a4 4 0 0 1 0 7.75"/></svg>
        </div>
        <p class="service-name-es">Consultoría para PYMEs</p>
        <p class="service-name-en">SME Consulting</p>
        <p class="service-desc">Implementación de flujos de trabajo, selección de herramientas (JIRA, Asana, Zoho) y mejora de procesos operativos.</p>
      </div>

    </div>

    <div class="pills">
      <span class="pill">Agile / Scrum</span>
      <span class="pill">JIRA · Asana · Zoho</span>
      <span class="pill">SEO</span>
      <span class="pill">Email Marketing</span>
      <span class="pill">WordPress / cPanel</span>
      <span class="pill">MS Teams · G-Suite</span>
      <span class="pill">Virtual Events</span>
      <span class="pill">Risk Management</span>
      <span class="pill">Español · English · Français</span>
    </div>
  </section>

  <!-- CLIENTS -->
  <section id="clientes">
    <div class="section-label">Experiencia Internacional · Global Track Record</div>
    <div class="section-title">Clientes y organizaciones</div>
    <p class="section-sub">Organizations I've worked with · Empresas con las que he colaborado</p>
    <div class="clients-grid">
      <div class="client-item">
        <svg viewBox="0 0 24 24"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
        Nestlé Venezuela
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
        Nestlé Argentina
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><rect x="2" y="7" width="20" height="14" rx="2"/><path d="M16 7V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v2"/></svg>
        CIMSOFT Canada
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
        Universidad de Navarra
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
        University of Helsinki
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        Prevent Blindness
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><rect x="2" y="7" width="20" height="14" rx="2"/><path d="M16 7V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v2"/></svg>
        VMUG
      </div>
      <div class="client-item">
        <svg viewBox="0 0 24 24"><path d="M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z"/><line x1="7" y1="7" x2="7.01" y2="7"/></svg>
        Ryley Salon Resources
      </div>
    </div>
  </section>

  <!-- PROCESS -->
  <section id="proceso">
    <div class="section-label">Metodología · How I Work</div>
    <div class="section-title">Así trabajo contigo</div>
    <p class="section-sub">Simple, clear, results-oriented · Simple, claro y orientado a resultados</p>
    <div class="process-steps">
      <div class="process-step">
        <div class="step-num">01</div>
        <p class="step-title">Diagnóstico · Discovery</p>
        <p class="step-desc">Entendemos tus objetivos, alcance y restricciones desde el inicio.</p>
      </div>
      <div class="process-step">
        <div class="step-num">02</div>
        <p class="step-title">Planificación · Planning</p>
        <p class="step-desc">Creamos un plan claro con hitos, responsables y herramientas adecuadas.</p>
      </div>
      <div class="process-step">
        <div class="step-num">03</div>
        <p class="step-title">Ejecución · Execution</p>
        <p class="step-desc">Coordinamos equipos y entregables con comunicación constante y Agile.</p>
      </div>
      <div class="process-step">
        <div class="step-num">04</div>
        <p class="step-title">Cierre · Delivery</p>
        <p class="step-desc">Entrega, reporte final y recomendaciones para la siguiente etapa.</p>
      </div>
    </div>
  </section>

  <!-- CTA -->
  <div class="cta-section" id="contacto">
    <div class="cta-inner">
      <div class="section-label">¿Tienes un proyecto? · Got a project?</div>
      <h2>Hablemos</h2>
      <p>
        Disponible para proyectos freelance, retainer mensual o consultoría puntual.<br>
        <em style="color:#8A9BB0;">Available for freelance projects, monthly retainers, or one-off consulting.</em>
      </p>
      <a href="mailto:ana.rglez@gmail.com" class="cta-btn">
        <svg viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 7 10-7"/></svg>
        ana.rglez@gmail.com
      </a>
    </div>
  </div>

  <footer>
    <p>© 2026 Ana Rojas González · Puebla, México · <a href="mailto:ana.rglez@gmail.com">ana.rglez@gmail.com</a></p>
  </footer>

</body>
</html>
