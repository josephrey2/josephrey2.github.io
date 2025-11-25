<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Universe Mechanical & Air Conditioning Inc. | Miami A/C & Mechanical</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Universe Mechanical & Air Conditioning Inc. - Miami’s trusted mechanical and A/C contractor for new construction, retrofits and service." />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet" />

  <style>
    :root {
      --blue-main: #00549c;
      --blue-dark: #003b73;
      --blue-light: #e6f0fa;
      --bg-light: #f5f7fb;
      --text-main: #0f172a;
      --text-muted: #64748b;
      --border-subtle: rgba(148, 163, 184, 0.35);
      --radius-lg: 18px;
      --shadow-soft: 0 18px 40px rgba(15, 23, 42, 0.22);
      --transition-fast: 0.18s ease-out;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    html, body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: var(--text-main);
      background: #ffffff;
      scroll-behavior: smooth;
    }

    img { max-width: 100%; display: block; }
    a { color: inherit; text-decoration: none; }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* NAVBAR */
    .navbar {
      position: fixed;
      inset: 0 0 auto 0;
      z-index: 40;
      transition: background var(--transition-fast), box-shadow var(--transition-fast), border-bottom var(--transition-fast), backdrop-filter var(--transition-fast);
    }

    .navbar-inner {
      height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .navbar.scrolled {
      background: rgba(255, 255, 255, 0.96);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(148, 163, 184, 0.25);
      box-shadow: 0 14px 35px rgba(15, 23, 42, 0.08);
    }

    .nav-logo {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .logo-img {
      height: 44px;
      width: auto;
    }

    .logo-text-block {
      display: flex;
      flex-direction: column;
      gap: 0.1rem;
    }

    .logo-main {
      font-size: 0.9rem;
      font-weight: 700;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: #0b1f36;
    }

    .logo-sub {
      font-size: 0.7rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      color: var(--text-muted);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.75rem;
      font-size: 0.9rem;
      font-weight: 500;
    }

    .nav-links a {
      position: relative;
      color: #ffffff;
    }

    .navbar.scrolled .nav-links a {
      color: var(--text-muted);
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.35rem;
      width: 0;
      height: 2px;
      background: var(--blue-main);
      border-radius: 999px;
      transition: width var(--transition-fast);
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 1rem;
      font-size: 0.8rem;
    }

    .nav-phone {
      color: #ffffff;
    }

    .navbar.scrolled .nav-phone {
      color: var(--text-muted);
    }

    .nav-phone strong {
      color: #ffffff;
    }

    .navbar.scrolled .nav-phone strong {
      color: var(--blue-main);
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.55rem 1.3rem;
      border-radius: 999px;
      border: 1px solid transparent;
      font-size: 0.8rem;
      font-weight: 600;
      cursor: pointer;
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), background var(--transition-fast), color var(--transition-fast), border var(--transition-fast);
      white-space: nowrap;
      gap: 0.35rem;
    }

    .btn-primary {
      background: var(--blue-main);
      color: #ffffff;
      box-shadow: 0 12px 30px rgba(0, 84, 156, 0.4);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 16px 40px rgba(0, 84, 156, 0.55);
    }

    .btn-outline {
      background: transparent;
      color: #ffffff;
      border-color: rgba(255, 255, 255, 0.7);
    }

    .navbar.scrolled .btn-outline {
      color: var(--blue-main);
      border-color: var(--blue-main);
    }

    .btn-outline:hover {
      background: #ffffff;
      color: var(--blue-main);
    }

    .nav-toggle {
      display: none;
      width: 40px;
      height: 40px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.8);
      background: rgba(15, 23, 42, 0.5);
      align-items: center;
      justify-content: center;
      cursor: pointer;
    }

    .navbar.scrolled .nav-toggle {
      border-color: rgba(148, 163, 184, 0.9);
      background: #ffffff;
    }

    .nav-toggle span {
      width: 18px;
      height: 2px;
      border-radius: 999px;
      background: #ffffff;
      position: relative;
    }

    .navbar.scrolled .nav-toggle span {
      background: var(--text-main);
    }

    .nav-toggle span::before,
    .nav-toggle span::after {
      content: "";
      position: absolute;
      left: 0;
      width: 100%;
      height: 2px;
      border-radius: 999px;
      background: inherit;
      transition: transform 0.2s ease, top 0.2s ease, bottom 0.2s ease, opacity 0.2s ease;
    }

    .nav-toggle span::before { top: -5px; }
    .nav-toggle span::after { bottom: -5px; }

    .nav-toggle.active span {
      background: transparent;
    }

    .nav-toggle.active span::before {
      top: 0;
      transform: rotate(45deg);
    }

    .nav-toggle.active span::after {
      bottom: 0;
      transform: rotate(-45deg);
    }

    .nav-mobile {
      display: none;
      background: #ffffff;
      border-bottom: 1px solid rgba(148, 163, 184, 0.35);
      box-shadow: 0 16px 35px rgba(15, 23, 42, 0.12);
    }

    .nav-mobile-list {
      padding: 0.9rem 1.5rem 1.1rem;
      display: flex;
      flex-direction: column;
      gap: 0.75rem;
      font-size: 0.9rem;
    }

    .nav-mobile-list a {
      color: var(--text-muted);
    }

    .nav-mobile-list a:hover {
      color: var(--blue-main);
    }

    /* HERO WITH VIDEO */
    .hero {
      position: relative;
      min-height: 90vh;
      color: #ffffff;
      display: flex;
      align-items: center;
    }

    .hero-video-wrap {
      position: absolute;
      inset: 0;
      overflow: hidden;
      z-index: -2;
    }

    .hero-video-wrap video {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .hero-overlay {
      position: absolute;
      inset: 0;
      background:
        linear-gradient(120deg, rgba(0, 59, 115, 0.92), rgba(0, 84, 156, 0.8), rgba(15, 23, 42, 0.75)),
        linear-gradient(to bottom, rgba(15, 23, 42, 0.9), transparent 40%);
      z-index: -1;
    }

    .hero-inner {
      padding-top: 100px;
      padding-bottom: 80px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      gap: 3rem;
      align-items: center;
    }

    .hero-tagline {
      font-size: 0.78rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      margin-bottom: 0.8rem;
      opacity: 0.9;
    }

    .hero-title {
      font-size: 3rem;
      line-height: 1.05;
      font-weight: 700;
      margin-bottom: 0.75rem;
    }

    .hero-title span {
      color: #dbeafe;
    }

    .hero-subtitle {
      font-size: 0.98rem;
      max-width: 32rem;
      opacity: 0.9;
      margin-bottom: 1.6rem;
    }

    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 1.8rem;
      font-size: 0.78rem;
    }

    .hero-badge {
      padding: 0.25rem 0.9rem;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.6);
      background: rgba(15, 23, 42, 0.35);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      align-items: center;
      margin-bottom: 1rem;
    }

    .hero-note {
      font-size: 0.8rem;
      opacity: 0.9;
    }

    .hero-panel {
      background: rgba(255, 255, 255, 0.95);
      border-radius: 22px;
      padding: 1.7rem 1.5rem;
      color: var(--text-main);
      box-shadow: var(--shadow-soft);
    }

    .hero-panel-title {
      font-size: 1rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .hero-panel-sub {
      font-size: 0.82rem;
      color: var(--text-muted);
      margin-bottom: 1rem;
    }

    .hero-panel-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
      margin-bottom: 1.1rem;
      font-size: 0.78rem;
    }

    .hero-metric-label {
      color: var(--text-muted);
      margin-bottom: 0.15rem;
    }

    .hero-metric-value {
      font-weight: 600;
      color: var(--blue-dark);
    }

    .hero-panel-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      font-size: 0.78rem;
    }

    .hero-panel-chip {
      padding: 0.2rem 0.7rem;
      border-radius: 999px;
      background: var(--blue-light);
      color: var(--blue-main);
      font-weight: 500;
      font-size: 0.75rem;
    }

    /* SECTIONS */
    section {
      padding: 80px 0;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 1.5rem;
      margin-bottom: 2rem;
    }

    .section-heading {
      max-width: 32rem;
    }

    .section-eyebrow {
      font-size: 0.78rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--blue-main);
      margin-bottom: 0.5rem;
    }

    .section-title {
      font-size: 1.8rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
      color: #0b1f36;
    }

    .section-subtitle {
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    .section-note {
      font-size: 0.8rem;
      color: var(--text-muted);
      max-width: 18rem;
      text-align: right;
    }

    /* ABOUT */
    #about {
      background: var(--bg-light);
      border-top: 1px solid rgba(148, 163, 184, 0.25);
      border-bottom: 1px solid rgba(148, 163, 184, 0.25);
    }

    .about-layout {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      gap: 2.5rem;
      align-items: flex-start;
    }

    .about-text {
      font-size: 0.9rem;
      color: var(--text-muted);
      display: flex;
      flex-direction: column;
      gap: 0.9rem;
    }

    .about-highlight {
      font-weight: 500;
      color: #0b1f36;
    }

    .leaders-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1rem;
    }

    .leader-card {
      background: #ffffff;
      border-radius: var(--radius-lg);
      padding: 1rem 0.9rem;
      box-shadow: 0 12px 30px rgba(15, 23, 42, 0.06);
      border: 1px solid rgba(148, 163, 184, 0.25);
      text-align: left;
      font-size: 0.85rem;
    }

    .leader-initial {
      width: 32px;
      height: 32px;
      border-radius: 999px;
      background: var(--blue-main);
      display: flex;
      align-items: center;
      justify-content: center;
      color: #ffffff;
      font-weight: 600;
      margin-bottom: 0.6rem;
    }

    .leader-name {
      font-weight: 600;
      color: #0b1f36;
      margin-bottom: 0.15rem;
    }

    .leader-role {
      font-size: 0.78rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--blue-main);
      margin-bottom: 0.35rem;
    }

    .leader-text {
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    /* CARDS (SERVICES) */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.4rem;
    }

    .card {
      border-radius: var(--radius-lg);
      background: #ffffff;
      border: 1px solid var(--border-subtle);
      padding: 1.2rem 1.1rem 1.3rem;
      box-shadow: 0 10px 28px rgba(15, 23, 42, 0.06);
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), border var(--transition-fast);
      font-size: 0.85rem;
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 18px 40px rgba(15, 23, 42, 0.12);
      border-color: rgba(0, 84, 156, 0.6);
    }

    .card-title {
      font-size: 1rem;
      font-weight: 600;
      color: #0b1f36;
      margin-bottom: 0.35rem;
    }

    .card-text {
      font-size: 0.85rem;
      color: var(--text-muted);
      margin-bottom: 0.8rem;
    }

    .card-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-bottom: 0.8rem;
    }

    .card-tag {
      font-size: 0.72rem;
      padding: 0.2rem 0.6rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.6);
      color: var(--text-muted);
      background: #f9fafb;
    }

    .card-footer {
      font-size: 0.78rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 0.6rem;
    }

    .card-link {
      font-weight: 500;
      color: var(--blue-main);
      display: inline-flex;
      align-items: center;
      gap: 0.25rem;
    }

    /* NEW CONSTRUCTION */
    .construction-layout {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      gap: 2rem;
    }

    .timeline {
      border-radius: var(--radius-lg);
      border: 1px solid var(--border-subtle);
      background: #ffffff;
      padding: 1.3rem 1.2rem 1.4rem;
      box-shadow: 0 12px 30px rgba(15, 23, 42, 0.06);
      font-size: 0.85rem;
    }

    .timeline-step {
      display: grid;
      grid-template-columns: 30px minmax(0, 1fr);
      gap: 0.8rem;
      padding: 0.75rem 0;
      align-items: flex-start;
    }

    .timeline-step:not(:last-child) {
      border-bottom: 1px solid rgba(226, 232, 240, 0.9);
    }

    .timeline-marker {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.2rem;
      margin-top: 0.1rem;
    }

    .timeline-badge {
      width: 22px;
      height: 22px;
      border-radius: 999px;
      border: 1px solid var(--blue-main);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      color: var(--blue-main);
    }

    .timeline-line {
      flex: 1;
      width: 1px;
      background: linear-gradient(to bottom, rgba(148, 163, 184, 0.9), transparent);
    }

    .timeline-title {
      font-weight: 600;
      color: #0b1f36;
      margin-bottom: 0.15rem;
    }

    .timeline-text {
      font-size: 0.82rem;
      color: var(--text-muted);
      margin-bottom: 0.3rem;
    }

    .timeline-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.35rem;
      font-size: 0.7rem;
    }

    .timeline-tag {
      padding: 0.16rem 0.55rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.7);
      background: #f9fafb;
      color: var(--text-muted);
    }

    .construction-side {
      border-radius: var(--radius-lg);
      background: var(--blue-light);
      padding: 1.4rem 1.2rem 1.5rem;
      border: 1px solid rgba(148, 163, 184, 0.5);
      font-size: 0.85rem;
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.45rem;
      margin-bottom: 0.8rem;
    }

    .pill {
      font-size: 0.72rem;
      padding: 0.2rem 0.65rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.85);
      color: var(--text-muted);
      background: #ffffff;
    }

    .checklist {
      list-style: none;
      margin: 0.6rem 0 1rem;
      padding: 0;
      display: flex;
      flex-direction: column;
      gap: 0.45rem;
    }

    .checklist li {
      display: flex;
      gap: 0.5rem;
    }

    .checkmark {
      width: 18px;
      height: 18px;
      border-radius: 999px;
      background: #0f766e1a;
      border: 1px solid #0f766e;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      color: #0f766e;
      margin-top: 0.05rem;
    }

    .construction-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      font-size: 0.8rem;
      margin-top: 0.5rem;
    }

    /* CONTACT */
    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
      gap: 2rem;
    }

    .contact-card {
      border-radius: var(--radius-lg);
      background: #ffffff;
      border: 1px solid var(--border-subtle);
      box-shadow: 0 12px 30px rgba(15, 23, 42, 0.06);
      padding: 1.4rem 1.3rem 1.5rem;
      font-size: 0.85rem;
    }

    form { display: flex; flex-direction: column; gap: 0.7rem; }

    .field-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
    }

    .field { flex: 1 1 160px; }

    label {
      display: block;
      font-size: 0.78rem;
      color: var(--text-muted);
      margin-bottom: 0.15rem;
    }

    input, textarea, select {
      width: 100%;
      border-radius: 12px;
      border: 1px solid rgba(148, 163, 184, 0.7);
      padding: 0.55rem 0.75rem;
      font-size: 0.82rem;
      font-family: inherit;
      outline: none;
      transition: border var(--transition-fast), box-shadow var(--transition-fast);
    }

    input:focus, textarea:focus, select:focus {
      border-color: var(--blue-main);
      box-shadow: 0 0 0 1px rgba(0, 84, 156, 0.25);
    }

    textarea { resize: vertical; min-height: 90px; }

    .contact-footer {
      margin-top: 0.9rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    .contact-meta {
      border-radius: var(--radius-lg);
      border: 1px solid rgba(148, 163, 184, 0.5);
      padding: 1.3rem 1.2rem;
      background: var(--bg-light);
      font-size: 0.82rem;
    }

    .contact-meta h4 {
      font-size: 0.95rem;
      font-weight: 600;
      margin-bottom: 0.35rem;
    }

    .contact-meta-row {
      margin-top: 0.5rem;
      display: flex;
      justify-content: space-between;
      gap: 0.9rem;
      font-size: 0.8rem;
    }

    .contact-meta span { color: var(--text-muted); }
    .contact-meta strong { color: #0b1f36; font-weight: 500; }

    /* FOOTER */
    footer {
      border-top: 1px solid rgba(148, 163, 184, 0.25);
      padding: 1.5rem 0 2rem;
      font-size: 0.78rem;
      color: var(--text-muted);
      background: #ffffff;
    }

    .footer-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .footer-links {
      display: flex;
      flex-wrap: wrap;
      gap: 1.1rem;
    }

    .footer-links a:hover {
      color: var(--blue-main);
    }

    /* FLOATING CALL */
    .floating-call {
      position: fixed;
      right: 1.4rem;
      bottom: 1.4rem;
      z-index: 30;
    }

    .floating-call a {
      display: inline-flex;
      align-items: center;
      gap: 0.45rem;
      padding: 0.7rem 1.15rem;
      border-radius: 999px;
      background: #16a34a;
      color: #ffffff;
      font-weight: 600;
      font-size: 0.82rem;
      box-shadow: 0 18px 40px rgba(22, 163, 74, 0.75);
    }

    .floating-call span { font-size: 1.05rem; }

    /* RESPONSIVE */
    @media (max-width: 1024px) {
      .hero-grid,
      .about-layout,
      .construction-layout,
      .contact-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-panel {
        margin-top: 1.5rem;
      }

      .leaders-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .cards-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .section-header {
        flex-direction: column;
        align-items: flex-start;
      }

      .section-note { text-align: left; }
    }

    @media (max-width: 768px) {
      .navbar-inner { height: 70px; }

      .nav-links,
      .nav-right {
        display: none;
      }

      .nav-toggle {
        display: inline-flex;
      }

      .hero-title { font-size: 2.2rem; }
      .hero-inner { padding-top: 90px; }

      .hero-panel-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .leaders-grid,
      .cards-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .floating-call {
        right: 1rem;
        bottom: 1rem;
      }
    }
  </style>
</head>
<body>
  <!-- NAVBAR -->
  <header class="navbar" id="navbar">
    <div class="container navbar-inner">
      <a href="#home" class="nav-logo">
        <!-- Change src to match your logo file in the repo -->
        <img src="universe-logo.png" alt="Universe Mechanical & Air Conditioning Inc. logo" class="logo-img" />
        <div class="logo-text-block">
          <div class="logo-main">Universe Mechanical</div>
          <div class="logo-sub">Mechanical & Air Conditioning, Inc.</div>
        </div>
      </a>

      <nav class="nav-links">
        <a href="#home">Home</a>
        <a href="#about">About Us</a>
        <a href="#services">Services</a>
        <a href="#new-construction">New Construction</a>
        <a href="#contact">Contact</a>
      </nav>

      <div class="nav-right">
        <div class="nav-phone">
          Main Office • <strong>(305) 555-0123</strong>
        </div>
        <a href="#contact" class="btn btn-outline">Request a Visit</a>
      </div>

      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
        <span></span>
      </button>
    </div>

    <!-- Mobile nav -->
    <div class="nav-mobile" id="navMobile">
      <div class="nav-mobile-list container">
        <a href="#home">Home</a>
        <a href="#about">About Us</a>
        <a href="#services">Services</a>
        <a href="#new-construction">New Construction</a>
        <a href="#contact">Contact</a>
        <a href="tel:+13055550123">Call: (305) 555-0123</a>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <main id="home">
    <section class="hero">
      <!-- Replace construction.mp4 with your own video file or hosted URL -->
      <div class="hero-video-wrap">
        <video src="construction.mp4" autoplay muted loop playsinline></video>
      </div>
      <div class="hero-overlay"></div>

      <div class="container hero-inner">
        <div class="hero-grid">
          <div>
            <div class="hero-tagline">Miami • Mechanical & A/C Contractor</div>
            <h1 class="hero-title">
              Building comfort into<br />
              <span>every project we touch.</span>
            </h1>
            <p class="hero-subtitle">
              Universe Mechanical & Air Conditioning Inc. delivers mechanical systems for new construction and existing
              buildings across Miami-Dade & Broward — engineered for performance, schedule and long South Florida summers.
            </p>

            <div class="hero-badges">
              <div class="hero-badge">New construction mechanical & A/C</div>
              <div class="hero-badge">Retrofits & replacements</div>
              <div class="hero-badge">Service & maintenance programs</div>
            </div>

            <div class="hero-actions">
              <a href="#contact" class="btn btn-primary">Request Service</a>
              <a href="#new-construction" class="btn btn-outline">Submit Plans</a>
            </div>

            <div class="hero-note">
              Serving single-family, multifamily & light commercial projects from our Hialeah Gardens hub.
            </div>
          </div>

          <aside class="hero-panel">
            <div class="hero-panel-title">Universe at a glance</div>
            <div class="hero-panel-sub">
              A focused mechanical partner for contractors, owners and property managers across South Florida.
            </div>

            <div class="hero-panel-grid">
              <div>
                <div class="hero-metric-label">Average response (service)</div>
                <div class="hero-metric-value">Same / Next Day</div>
              </div>
              <div>
                <div class="hero-metric-label">New construction capacity</div>
                <div class="hero-metric-value">50+ homes / 200+ units</div>
              </div>
              <div>
                <div class="hero-metric-label">Project focus</div>
                <div class="hero-metric-value">Miami-Dade & Broward</div>
              </div>
            </div>

            <div class="hero-panel-footer">
              <div>
                Licensed & insured mechanical contractor specializing in Florida’s coastal environment, flat roofs and
                high humidity.
              </div>
              <div class="hero-panel-chip">Built for South Florida conditions</div>
            </div>
          </aside>
        </div>
      </div>
    </section>

    <!-- ABOUT US -->
    <section id="about">
      <div class="container">
        <div class="section-header">
          <div class="section-heading">
            <div class="section-eyebrow">About Us</div>
            <h2 class="section-title">Universe Mechanical & Air Conditioning Inc.</h2>
            <p class="section-subtitle">
              A family-led mechanical contractor rooted in Miami. We combine field experience, disciplined project
              management and long-term relationships with builders and owners.
            </p>
          </div>
          <div class="section-note">
            From early budgeting through closeout, our team is involved as a partner — not just a subcontractor.
          </div>
        </div>

        <div class="about-layout">
          <div class="about-text">
            <p class="about-highlight">
              Universe Mechanical & Air Conditioning Inc. was built around one idea: projects run smoother when the
              mechanical team thinks like a builder and acts like an owner.
            </p>
            <p>
              Based in Hialeah Gardens, we serve Miami’s core neighborhoods, surrounding suburbs and Broward’s south
              corridor. Our work ranges from new single-family homes and townhome communities to multifamily buildings
              and select commercial spaces.
            </p>
            <p>
              We bring structure to every job — coordinated drawings, clean installs, clear turnover and support after
              move-in. The result is fewer surprises in the field and systems that perform the way they were designed.
            </p>
          </div>

          <div class="leaders-grid">
            <article class="leader-card">
              <div class="leader-initial">C</div>
              <div class="leader-name">Claudio Rey</div>
              <div class="leader-role">Chief Executive Officer</div>
              <p class="leader-text">
                Leads overall vision, client relationships and project delivery, ensuring every job reflects Universe’s
                standards in the field.
              </p>
            </article>

            <article class="leader-card">
              <div class="leader-initial">J</div>
              <div class="leader-name">Joseph Rey</div>
              <div class="leader-role">Chief Financial Officer</div>
              <p class="leader-text">
                Oversees financial operations, budgets and project controls so owners and GCs have clarity from bid
                through closeout.
              </p>
            </article>

            <article class="leader-card">
              <div class="leader-initial">J</div>
              <div class="leader-name">Jordi Rey</div>
              <div class="leader-role">Chief Operating Officer</div>
              <p class="leader-text">
                Directs day-to-day operations, scheduling and field coordination to keep projects on time and aligned
                with site realities.
              </p>
            </article>
          </div>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services">
      <div class="container">
        <div class="section-header">
          <div class="section-heading">
            <div class="section-eyebrow">Services</div>
            <h2 class="section-title">Mechanical & A/C service for occupied spaces.</h2>
            <p class="section-subtitle">
              Responsive service teams focused on diagnosing root causes, communicating clearly and protecting your
              property while we work.
            </p>
          </div>
          <div class="section-note">
            Ideal for homeowners, property managers and associations needing a dependable mechanical partner.
          </div>
        </div>

        <div class="cards-grid">
          <article class="card">
            <h3 class="card-title">Diagnostics & Repair</h3>
            <p class="card-text">
              Troubleshooting no-cool calls, water leaks, electrical issues and comfort problems on all major brands.
            </p>
            <div class="card-tags">
              <span class="card-tag">Same / next-day</span>
              <span class="card-tag">Clear pricing</span>
              <span class="card-tag">All major brands</span>
            </div>
            <div class="card-footer">
              <span>Most calls resolved in one visit.</span>
              <a href="#contact" class="card-link">Book repair ↗</a>
            </div>
          </article>

          <article class="card">
            <h3 class="card-title">System Replacements</h3>
            <p class="card-text">
              Full change-outs with duct review, proper line-set practices, permitting and homeowner orientation.
            </p>
            <div class="card-tags">
              <span class="card-tag">High-efficiency</span>
              <span class="card-tag">Heat pumps</span>
              <span class="card-tag">Financing options</span>
            </div>
            <div class="card-footer">
              <span>Designed for Miami’s heat and humidity.</span>
              <a href="#contact" class="card-link">Request quote ↗</a>
            </div>
          </article>

          <article class="card">
            <h3 class="card-title">Ductless & Additions</h3>
            <p class="card-text">
              Mini-splits and supplemental systems for additions, garages, home offices and spaces that need extra control.
            </p>
            <div class="card-tags">
              <span class="card-tag">Single & multi-zone</span>
              <span class="card-tag">Inverter technology</span>
            </div>
            <div class="card-footer">
              <span>Great fit for targeted comfort.</span>
              <a href="#contact" class="card-link">Design my zones ↗</a>
            </div>
          </article>

          <article class="card">
            <h3 class="card-title">Indoor Air Quality</h3>
            <p class="card-text">
              Filtration, UV lights, dehumidification and ventilation strategies tailored to coastal living and allergies.
            </p>
            <div class="card-tags">
              <span class="card-tag">Humidity control</span>
              <span class="card-tag">UV / filtration</span>
            </div>
            <div class="card-footer">
              <span>Cleaner air and longer coil life.</span>
              <a href="#contact" class="card-link">IAQ consult ↗</a>
            </div>
          </article>

          <article class="card">
            <h3 class="card-title">Controls & Smart Thermostats</h3>
            <p class="card-text">
              Upgrading controls, zoning and smart thermostats for homes, rentals and small commercial spaces.
            </p>
            <div class="card-tags">
              <span class="card-tag">Nest & Ecobee</span>
              <span class="card-tag">Zoning</span>
            </div>
            <div class="card-footer">
              <span>Control comfort from anywhere.</span>
              <a href="#contact" class="card-link">Upgrade controls ↗</a>
            </div>
          </article>

          <article class="card">
            <h3 class="card-title">Maintenance Programs</h3>
            <p class="card-text">
              Planned inspections, cleaning and checks to keep systems reliable through long cooling seasons.
            </p>
            <div class="card-tags">
              <span class="card-tag">Priority response</span>
              <span class="card-tag">Program pricing</span>
            </div>
            <div class="card-footer">
              <span>Prevent issues before they show up.</span>
              <a href="#contact" class="card-link">Join program ↗</a>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- NEW CONSTRUCTION -->
    <section id="new-construction">
      <div class="container">
        <div class="section-header">
          <div class="section-heading">
            <div class="section-eyebrow">New Construction</div>
            <h2 class="section-title">Mechanical systems that support the schedule.</h2>
            <p class="section-subtitle">
              From early budgets and design-assist to final inspections, our new construction team works alongside your
              supers and PMs to keep projects on track.
            </p>
          </div>
          <div class="section-note">
            Ideal for single-family communities, custom homes, townhomes and mid-rise multifamily.
          </div>
        </div>

        <div class="construction-layout">
          <div class="timeline">
            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">1</div>
                <div class="timeline-line"></div>
              </div>
              <div>
                <div class="timeline-title">Preconstruction & Design</div>
                <p class="timeline-text">
                  Load calculations, equipment selections and layout input so mechanical scopes are coordinated before
                  the job hits the field.
                </p>
                <div class="timeline-tags">
                  <span class="timeline-tag">Budgets & options</span>
                  <span class="timeline-tag">Manual J/S</span>
                  <span class="timeline-tag">Value engineering</span>
                </div>
              </div>
            </div>

            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">2</div>
                <div class="timeline-line"></div>
              </div>
              <div>
                <div class="timeline-title">Rough-in & Set</div>
                <p class="timeline-text">
                  Clean, organized rough-ins tied to your schedule — with attention to penetrations, drains, supports
                  and interaction with other trades.
                </p>
                <div class="timeline-tags">
                  <span class="timeline-tag">Coordinated with framing</span>
                  <span class="timeline-tag">Drain & line-set routing</span>
                </div>
              </div>
            </div>

            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">3</div>
                <div class="timeline-line"></div>
              </div>
              <div>
                <div class="timeline-title">Trim, Startup & Commissioning</div>
                <p class="timeline-text">
                  Verified charge, airflow and controls documented for your closeout package and future service teams.
                </p>
                <div class="timeline-tags">
                  <span class="timeline-tag">Static pressure</span>
                  <span class="timeline-tag">Owner orientation</span>
                  <span class="timeline-tag">Punch support</span>
                </div>
              </div>
            </div>

            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">4</div>
              </div>
              <div>
                <div class="timeline-title">Turnover & Warranty</div>
                <p class="timeline-text">
                  Ongoing support after move-in, protecting your reputation with homeowners and associations.
                </p>
                <div class="timeline-tags">
                  <span class="timeline-tag">Warranty response</span>
                  <span class="timeline-tag">Service partnership</span>
                </div>
              </div>
            </div>
          </div>

          <aside class="construction-side">
            <div class="pill-row">
              <span class="pill">Single-family & customs</span>
              <span class="pill">Townhomes & multifamily</span>
              <span class="pill">Select commercial build-outs</span>
            </div>

            <p>
              One mechanical partner for your community or building, from the first model home to the last warranty call.
              We understand jobsite logistics, inspections and the importance of clean mechanical rooms when you turn over keys.
            </p>

            <ul class="checklist">
              <li>
                <div class="checkmark">✓</div>
                <div><strong>Permit-ready documentation</strong> with equipment schedules, cutsheets and load data.</div>
              </li>
              <li>
                <div class="checkmark">✓</div>
                <div><strong>Schedule-driven manpower</strong> to support multiple phases across your sites.</div>
              </li>
              <li>
                <div class="checkmark">✓</div>
                <div><strong>Warranty & service alignment</strong> so homeowners know who to call and what to expect.</div>
              </li>
            </ul>

            <div class="construction-footer">
              <div>
                Current capacity:<br />
                <strong>Up to 50+ homes or 200+ units per year.</strong>
              </div>
              <a href="#contact" class="btn btn-primary">Send us your plans</a>
            </div>
          </aside>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="container">
        <div class="section-header">
          <div class="section-heading">
            <div class="section-eyebrow">Contact</div>
            <h2 class="section-title">Tell us about your project or service need.</h2>
            <p class="section-subtitle">
              Share a few details and a member of the Universe team will follow up to review scope, timing and next steps.
            </p>
          </div>
          <div class="section-note">
            For urgent no-cool calls, please call our office directly at <strong>(305) 555-0123</strong>.
          </div>
        </div>

        <div class="contact-grid">
          <div class="contact-card">
            <form>
              <div class="field-row">
                <div class="field">
                  <label for="name">Full name</label>
                  <input id="name" type="text" placeholder="Your name" />
                </div>
                <div class="field">
                  <label for="phone">Mobile phone</label>
                  <input id="phone" type="tel" placeholder="(305) 555-0123" />
                </div>
              </div>

              <div class="field-row">
                <div class="field">
                  <label for="email">Email</label>
                  <input id="email" type="email" placeholder="you@example.com" />
                </div>
                <div class="field">
                  <label for="city">City / neighborhood</label>
                  <input id="city" type="text" placeholder="Miami, Doral, Kendall..." />
                </div>
              </div>

              <div class="field-row">
                <div class="field">
                  <label for="serviceType">I’m reaching out about</label>
                  <select id="serviceType">
                    <option>Service / repair</option>
                    <option>System replacement</option>
                    <option>New construction project</option>
                    <option>Maintenance program</option>
                    <option>Other mechanical / A/C need</option>
                  </select>
                </div>
                <div class="field">
                  <label for="timeframe">Ideal timeframe</label>
                  <select id="timeframe">
                    <option>ASAP / emergency</option>
                    <option>This week</option>
                    <option>Within 30 days</option>
                    <option>Longer-term planning / budgeting</option>
                  </select>
                </div>
              </div>

              <div class="field">
                <label for="message">Project or issue details</label>
                <textarea id="message" placeholder="Example: 2nd floor not cooling, planning a remodel, submitting plans for new townhomes, etc."></textarea>
              </div>

              <div class="contact-footer">
                <div>By submitting, you agree we may contact you by phone, text or email regarding your request.</div>
                <button type="button" class="btn btn-primary">Submit request</button>
              </div>
            </form>
          </div>

          <aside class="contact-meta">
            <h4>New construction & plan review</h4>
            <p>
              For bid invitations, design-assist or to review specific plans, send drawings and details to our estimating
              team below.
            </p>

            <div class="contact-meta-row">
              <div>
                <span>Plans & bids</span><br />
                <strong>plans@universeac.com</strong>
              </div>
              <div>
                <span>Main office</span><br />
                <strong>(305) 555-0123</strong>
              </div>
            </div>

            <div class="contact-meta-row" style="margin-top: 0.6rem;">
              <div>
                <span>Shop</span><br />
                <strong>Hialeah Gardens, FL</strong>
              </div>
              <div>
                <span>Hours</span><br />
                <strong>Mon–Sat • 8:00a–7:00p</strong>
              </div>
            </div>
          </aside>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-row">
      <div>© <span id="year"></span> Universe Mechanical & Air Conditioning Inc. All rights reserved.</div>
      <div class="footer-links">
        <a href="#home">Home</a>
        <a href="#about">About Us</a>
        <a href="#services">Services</a>
        <a href="#new-construction">New Construction</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </footer>

  <!-- Floating Call CTA -->
  <div class="floating-call">
    <a href="tel:+13055550123">
      <span>📞</span>
      Call Universe Mechanical
    </a>
  </div>

  <script>
    const navbar = document.getElementById("navbar");
    const navToggle = document.getElementById("navToggle");
    const navMobile = document.getElementById("navMobile");

    window.addEventListener("scroll", () => {
      if (window.scrollY > 10) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    });

    navToggle.addEventListener("click", () => {
      navToggle.classList.toggle("active");
      const isOpen = navMobile.style.display === "block";
      navMobile.style.display = isOpen ? "none" : "block";
    });

    navMobile.addEventListener("click", (e) => {
      if (e.target.tagName.toLowerCase() === "a") {
        navMobile.style.display = "none";
        navToggle.classList.remove("active");
      }
    });

    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
