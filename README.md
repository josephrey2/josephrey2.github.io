<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Universe Services | Miami A/C & Mechanical</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Universe Services — Miami's trusted mechanical and A/C contractor for service, retrofits, and replacements." />
  <link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,300&display=swap" rel="stylesheet" />

  <style>
    :root {
      --blue:        #005aad;
      --blue-dark:   #00336b;
      --blue-mid:    #1a6fbe;
      --blue-light:  #deeeff;
      --blue-xlight: #e6f1ff;
      --sky:         #e8f2ff;
      --white:       #ffffff;
      --ink:         #0a1520;
      --ink-mid:     #1e3048;
      --muted:       #445d78;
      --border:      rgba(80,110,145,.28);
      --shadow-card: 0 8px 32px rgba(0,26,64,.09);
      --shadow-lift: 0 20px 50px rgba(0,26,64,.16);
      --r:           16px;
      --r-lg:        24px;
      --ease:        cubic-bezier(.25,.8,.25,1);
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; font-size: 16px; scroll-padding-top: 175px; }

    body {
      font-family: "DM Sans", system-ui, sans-serif;
      color: var(--ink);
      background: #fff;
      overflow-x: hidden;
      -webkit-font-smoothing: antialiased;
    }

    img { max-width: 100%; display: block; }
    a { color: inherit; text-decoration: none; }

    .container {
      width: 100%;
      max-width: 1180px;
      margin: 0 auto;
      padding: 0 2rem;
    }

    /* ─── UTILITY ─────────────────────────────── */

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: .5rem;
      font-size: .72rem;
      font-weight: 600;
      letter-spacing: .2em;
      text-transform: uppercase;
      color: var(--blue);
      margin-bottom: .9rem;
    }

    .eyebrow::before {
      content: "";
      display: block;
      width: 22px;
      height: 2px;
      background: var(--blue);
      border-radius: 99px;
    }

    .section-title {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: clamp(2rem, 3.5vw, 2.8rem);
      font-weight: 400;
      line-height: 1.1;
      color: var(--ink);
      margin-bottom: .6rem;
    }

    .section-sub {
      font-size: .92rem;
      color: var(--muted);
      max-width: 36rem;
      line-height: 1.7;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: .4rem;
      padding: .7rem 1.5rem;
      border-radius: 99px;
      font-size: .84rem;
      font-weight: 600;
      border: 1.5px solid transparent;
      cursor: pointer;
      transition: transform .18s var(--ease), box-shadow .18s var(--ease), background .18s, color .18s, border-color .18s;
      white-space: nowrap;
      font-family: inherit;
    }

    .btn-primary {
      background: var(--blue);
      color: #fff;
      box-shadow: 0 10px 28px rgba(0,90,173,.4);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 18px 40px rgba(0,90,173,.55);
      background: var(--blue-dark);
    }

    /* Hero-specific primary button — white on blue bg */
    .hero .btn-primary {
      background: #ffffff;
      color: #0a3d7a;
      box-shadow: 0 10px 30px rgba(0,0,0,.22);
    }

    .hero .btn-primary:hover {
      background: #f0f7ff;
      box-shadow: 0 18px 44px rgba(0,0,0,.3);
    }

    .btn-ghost {
      background: rgba(255,255,255,.1);
      color: #fff;
      border-color: rgba(255,255,255,.55);
      backdrop-filter: blur(8px);
    }

    .btn-ghost:hover {
      background: rgba(255,255,255,.22);
      border-color: rgba(255,255,255,.9);
    }

    .btn-outline {
      background: transparent;
      color: var(--blue);
      border-color: var(--blue);
    }

    .btn-outline:hover {
      background: var(--blue);
      color: #fff;
    }

    /* ─── NAVBAR ──────────────────────────────── */

    .navbar {
      position: fixed;
      inset: 0 0 auto 0;
      z-index: 50;
      background: #001f45;
      border-bottom: 1px solid rgba(255,255,255,.08);
      box-shadow: 0 4px 24px rgba(0,10,40,.35);
      transition: background .2s, box-shadow .2s, border-color .2s;
    }

    .navbar.scrolled {
      background: #001f45;
      border-bottom: 1px solid rgba(255,255,255,.1);
      box-shadow: 0 4px 28px rgba(0,10,40,.45);
    }

    .navbar-inner {
      height: 160px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 2rem;
    }

    .nav-logo {
      display: flex;
      align-items: center;
      gap: .8rem;
      flex-shrink: 0;
    }

    .logo-img {
      height: 40px;
      width: auto;
    }

    .logo-wordmark {
      display: flex;
      flex-direction: column;
      gap: .08rem;
    }

    .logo-primary {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.05rem;
      line-height: 1;
      color: #ffffff;
      transition: color .2s;
    }

    .navbar.scrolled .logo-primary { color: #ffffff; }

    .logo-secondary {
      font-size: .64rem;
      letter-spacing: .16em;
      text-transform: uppercase;
      color: rgba(255,255,255,.55);
      transition: color .2s;
    }

    .navbar.scrolled .logo-secondary { color: rgba(255,255,255,.55); }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 2rem;
      font-size: .85rem;
      font-weight: 500;
    }

    .nav-links a {
      color: rgba(255,255,255,.8);
      position: relative;
      transition: color .15s;
    }

    .navbar.scrolled .nav-links a { color: rgba(255,255,255,.8); }

    .nav-links a:hover,
    .navbar.scrolled .nav-links a:hover { color: #ffffff; }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0; bottom: -.3rem;
      width: 0; height: 1.5px;
      background: rgba(255,255,255,.7);
      border-radius: 99px;
      transition: width .18s var(--ease);
    }

    .nav-links a:hover::after { width: 100%; }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 1rem;
      font-size: .8rem;
    }

    .nav-phone {
      font-size: .8rem;
      color: rgba(255,255,255,.7);
      transition: color .2s;
    }

    .nav-phone strong { color: #fff; transition: color .2s; }

    .navbar.scrolled .nav-phone { color: rgba(255,255,255,.7); }
    .navbar.scrolled .nav-phone strong { color: #fff; }

    .nav-toggle {
      display: none;
      width: 42px; height: 42px;
      border-radius: 50%;
      border: 1.5px solid rgba(255,255,255,.5);
      background: rgba(255,255,255,.1);
      align-items: center; justify-content: center;
      cursor: pointer;
      transition: background .2s, border-color .2s;
    }

    .navbar.scrolled .nav-toggle {
      border-color: rgba(255,255,255,.4);
      background: rgba(255,255,255,.1);
    }

    .hamburger span {
      display: block;
      height: 1.5px;
      border-radius: 99px;
      background: #fff;
      transition: transform .2s, opacity .2s, top .2s;
    }

    .navbar.scrolled .hamburger span { background: #fff; }

    .nav-toggle.active .hamburger span:nth-child(1) { transform: translateY(5px) rotate(45deg); }
    .nav-toggle.active .hamburger span:nth-child(2) { opacity: 0; }
    .nav-toggle.active .hamburger span:nth-child(3) { transform: translateY(-5px) rotate(-45deg); }

    .nav-mobile {
      display: none;
      background: #fff;
      border-bottom: 1px solid var(--border);
      box-shadow: 0 12px 30px rgba(0,26,64,.1);
    }

    .nav-mobile-inner {
      padding: 1rem 2rem 1.4rem;
      display: flex;
      flex-direction: column;
      gap: .85rem;
      font-size: .9rem;
    }

    .nav-mobile-inner a { color: var(--muted); }
    .nav-mobile-inner a:hover { color: var(--blue); }

    /* ─── HERO ────────────────────────────────── */

    .hero {
      position: relative;
      min-height: 100vh;
      display: flex;
      align-items: center;
      color: #fff;
      overflow: hidden;
    }

    .hero-overlay {
      position: absolute;
      inset: 0;
      z-index: 1;
      background: linear-gradient(135deg, #0a3d7a 0%, #1565c0 45%, #1e88e5 75%, #29b6f6 100%);
    }

    /* Large decorative orbs for depth */
    .hero-overlay::before {
      content: "";
      position: absolute;
      top: -180px; right: -120px;
      width: 650px; height: 650px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(255,255,255,.13) 0%, transparent 70%);
    }

    .hero-overlay::after {
      content: "";
      position: absolute;
      bottom: -200px; left: -100px;
      width: 700px; height: 700px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(0,20,80,.25) 0%, transparent 70%);
    }



    .hero-inner {
      position: relative;
      z-index: 5;
      padding-top: 130px;
      padding-bottom: 90px;
      width: 100%;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr 400px;
      gap: 4rem;
      align-items: center;
    }

    .hero-badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: .55rem;
      margin-bottom: 1.6rem;
    }

    .hero-badge {
      font-size: .7rem;
      font-weight: 500;
      letter-spacing: .08em;
      padding: .25rem .85rem;
      border-radius: 99px;
      border: 1px solid rgba(255,255,255,.35);
      background: rgba(255,255,255,.08);
      backdrop-filter: blur(6px);
    }

    .hero-tag {
      font-size: .72rem;
      letter-spacing: .22em;
      text-transform: uppercase;
      color: rgba(255,255,255,.9);
      margin-bottom: 1.1rem;
      display: inline-flex;
      align-items: center;
      gap: .6rem;
      background: rgba(255,255,255,.12);
      border: 1px solid rgba(255,255,255,.25);
      padding: .3rem .9rem .3rem .7rem;
      border-radius: 99px;
      backdrop-filter: blur(8px);
    }

    .hero-tag::before {
      content: "📍";
      font-size: .8rem;
    }

    .hero-headline {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: clamp(3rem, 6vw, 5.2rem);
      line-height: 1.0;
      font-weight: 400;
      margin-bottom: 1.4rem;
      text-shadow: 0 2px 20px rgba(0,20,80,.3);
    }

    .hero-headline em {
      font-style: italic;
      color: #fde68a;
      display: block;
    }

    .hero-sub {
      font-size: 1.05rem;
      line-height: 1.75;
      color: rgba(255,255,255,.92);
      max-width: 34rem;
      margin-bottom: 2.4rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
      margin-bottom: 3rem;
    }

    .hero-trust {
      display: flex;
      flex-wrap: wrap;
      gap: 0;
      font-size: .8rem;
      color: rgba(255,255,255,.8);
      background: rgba(0,0,0,.15);
      border: 1px solid rgba(255,255,255,.15);
      border-radius: 14px;
      overflow: hidden;
      backdrop-filter: blur(8px);
      width: fit-content;
    }

    .hero-trust-item {
      display: flex;
      align-items: center;
      gap: .35rem;
      padding: .65rem .75rem;
      border-right: 1px solid rgba(255,255,255,.12);
    }

    .hero-trust-item:last-child { border-right: none; }

    .hero-trust-item strong { color: #fff; font-weight: 600; }

    .hero-trust-icon {
      font-size: 1rem;
      line-height: 1;
    }

    /* Glance panel */
    .glance-panel {
      background: #ffffff;
      border-radius: 20px;
      padding: 2rem 1.8rem;
      color: var(--ink);
      box-shadow: 0 40px 80px rgba(0,15,60,.4), 0 0 0 1px rgba(255,255,255,.6);
      position: relative;
      overflow: hidden;
    }

    .glance-panel::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 4px;
      background: linear-gradient(90deg, #0a3d7a, #1e88e5, #29b6f6);
    }

    /* Decorative circle inside panel */
    .glance-panel::after {
      content: "";
      position: absolute;
      bottom: -60px; right: -60px;
      width: 180px; height: 180px;
      border-radius: 50%;
      background: radial-gradient(circle, #e6f1ff 0%, transparent 70%);
      pointer-events: none;
    }

    .glance-title {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.3rem;
      margin-bottom: .3rem;
      color: var(--ink);
    }

    .glance-sub {
      font-size: .8rem;
      color: #4a6280;
      margin-bottom: 1.6rem;
      line-height: 1.55;
    }

    .glance-stats {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0;
      margin-bottom: 1.4rem;
      border: 1px solid var(--border);
      border-radius: 12px;
      overflow: hidden;
    }

    .glance-stats > div {
      padding: .85rem 1rem;
      border-right: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .glance-stats > div:nth-child(2n) { border-right: none; }
    .glance-stats > div:nth-child(3),
    .glance-stats > div:nth-child(4) { border-bottom: none; }

    .glance-stat-label {
      font-size: .66rem;
      text-transform: uppercase;
      letter-spacing: .1em;
      color: #4a6280;
      margin-bottom: .25rem;
    }

    .glance-stat-value {
      font-size: .95rem;
      font-weight: 700;
      color: #0a3d7a;
      line-height: 1.2;
    }

    .glance-divider {
      height: 1px;
      background: var(--border);
      margin: 1.2rem 0;
    }

    .glance-footer {
      font-size: .76rem;
      color: #4a6280;
      line-height: 1.6;
    }

    .glance-chip {
      display: inline-flex;
      align-items: center;
      gap: .35rem;
      margin-top: .9rem;
      padding: .35rem .9rem;
      border-radius: 99px;
      background: #ecfdf5;
      border: 1px solid #bbf7d0;
      color: #15803d;
      font-size: .72rem;
      font-weight: 600;
      letter-spacing: .04em;
    }

    .glance-chip::before {
      content: "";
      width: 7px; height: 7px;
      border-radius: 50%;
      background: #22c55e;
      box-shadow: 0 0 0 3px rgba(34,197,94,.2);
    }

    /* ─── MARQUEE BAND ────────────────────────── */

    .marquee-band {
      background: var(--ink);
      padding: .9rem 0;
      overflow: hidden;
    }

    .marquee-track {
      display: flex;
      gap: 0;
      animation: marquee 28s linear infinite;
      white-space: nowrap;
    }

    @keyframes marquee {
      from { transform: translateX(0); }
      to   { transform: translateX(-50%); }
    }

    .marquee-item {
      display: inline-flex;
      align-items: center;
      gap: .6rem;
      padding: 0 2.5rem;
      font-size: .72rem;
      letter-spacing: .14em;
      text-transform: uppercase;
      color: rgba(255,255,255,.72);
    }

    .marquee-dot {
      width: 4px; height: 4px;
      border-radius: 50%;
      background: var(--blue);
      flex-shrink: 0;
    }

    /* ─── ABOUT ───────────────────────────────── */

    #about {
      padding: 110px 0;
      background: var(--white);
    }

    .about-layout {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem;
      align-items: start;
    }

    .about-left .section-title { max-width: 24rem; }

    .about-body {
      margin-top: 1.5rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      font-size: .9rem;
      line-height: 1.8;
      color: var(--muted);
    }

    .about-body strong { color: var(--ink); font-weight: 600; }

    .about-stat-row {
      display: flex;
      gap: 2.5rem;
      margin-top: 2.2rem;
      padding-top: 2rem;
      border-top: 1px solid var(--border);
    }

    .about-stat-number {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 2.4rem;
      line-height: 1;
      color: var(--blue);
      margin-bottom: .2rem;
    }

    .about-stat-label {
      font-size: .75rem;
      color: var(--muted);
      line-height: 1.4;
    }

    /* Leader cards */
    .leaders-wrap {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .leader-card {
      display: flex;
      align-items: flex-start;
      gap: 1rem;
      padding: 1.1rem 1.2rem;
      border-radius: var(--r);
      border: 1px solid var(--border);
      background: var(--white);
      box-shadow: var(--shadow-card);
      transition: transform .18s var(--ease), box-shadow .18s var(--ease), border-color .18s;
    }

    .leader-card:hover {
      transform: translateX(4px);
      box-shadow: var(--shadow-lift);
      border-color: rgba(0,90,173,.25);
    }

    .leader-avatar {
      width: 44px; height: 44px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--blue), var(--blue-mid));
      display: flex;
      align-items: center; justify-content: center;
      color: #fff;
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.2rem;
      flex-shrink: 0;
    }

    .leader-info { flex: 1; }

    .leader-name {
      font-weight: 600;
      font-size: .9rem;
      color: var(--ink);
      margin-bottom: .12rem;
    }

    .leader-role {
      font-size: .68rem;
      text-transform: uppercase;
      letter-spacing: .14em;
      color: var(--blue);
      margin-bottom: .35rem;
    }

    .leader-text {
      font-size: .78rem;
      color: var(--muted);
      line-height: 1.55;
    }

    /* ─── SERVICES ────────────────────────────── */

    #services {
      padding: 100px 0;
      background: var(--blue-xlight);
      position: relative;
    }

    #services::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--border), transparent);
    }

    .services-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 2rem;
      margin-bottom: 3rem;
    }

    .services-note {
      font-size: .8rem;
      color: var(--muted);
      max-width: 16rem;
      text-align: right;
      line-height: 1.6;
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 1.2rem;
    }

    .service-card {
      background: var(--white);
      border-radius: var(--r-lg);
      padding: 1.6rem 1.4rem;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-card);
      display: flex;
      flex-direction: column;
      transition: transform .2s var(--ease), box-shadow .2s var(--ease), border-color .2s;
      position: relative;
      overflow: hidden;
    }

    .service-card::after {
      content: "";
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 2px;
      background: linear-gradient(90deg, var(--blue), #56b4e9);
      transform: scaleX(0);
      transform-origin: left;
      transition: transform .25s var(--ease);
    }

    .service-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-lift);
      border-color: rgba(0,90,173,.2);
    }

    .service-card:hover::after { transform: scaleX(1); }

    .service-icon {
      width: 42px; height: 42px;
      border-radius: 12px;
      background: var(--blue-light);
      display: flex;
      align-items: center; justify-content: center;
      font-size: 1.2rem;
      margin-bottom: 1.1rem;
    }

    .service-name {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.1rem;
      color: var(--ink);
      margin-bottom: .5rem;
      line-height: 1.2;
    }

    .service-desc {
      font-size: .82rem;
      color: var(--muted);
      line-height: 1.7;
      flex: 1;
      margin-bottom: 1.1rem;
    }

    .service-tags {
      display: flex;
      flex-wrap: wrap;
      gap: .35rem;
      margin-bottom: 1rem;
    }

    .service-tag {
      font-size: .68rem;
      padding: .18rem .6rem;
      border-radius: 99px;
      border: 1px solid rgba(0,90,173,.25);
      color: var(--blue);
      background: var(--blue-xlight);
      font-weight: 500;
    }

    .service-cta {
      margin-top: auto;
      font-size: .8rem;
      font-weight: 600;
      color: var(--blue);
      display: inline-flex;
      align-items: center;
      gap: .3rem;
      transition: gap .15s;
    }

    .service-cta:hover { gap: .55rem; }

    /* ─── PROCESS STRIP ───────────────────────── */

    .process-strip {
      padding: 80px 0;
      background: var(--white);
      border-top: 1px solid var(--border);
    }

    .process-header {
      text-align: center;
      margin-bottom: 3rem;
    }

    .process-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 0;
      position: relative;
    }

    .process-grid::before {
      content: "";
      position: absolute;
      top: 28px;
      left: calc(12.5% + 16px);
      right: calc(12.5% + 16px);
      height: 1px;
      background: var(--border);
      z-index: 0;
    }

    .process-step {
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      padding: 0 1.5rem;
      position: relative;
      z-index: 1;
    }

    .process-num {
      width: 56px; height: 56px;
      border-radius: 50%;
      background: var(--white);
      border: 2px solid var(--blue);
      display: flex;
      align-items: center; justify-content: center;
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.2rem;
      color: var(--blue);
      margin-bottom: 1.2rem;
    }

    .process-step-title {
      font-weight: 600;
      font-size: .95rem;
      color: var(--ink);
      margin-bottom: .4rem;
    }

    .process-step-text {
      font-size: .84rem;
      color: var(--muted);
      line-height: 1.65;
    }

    /* ─── CONTACT ─────────────────────────────── */

    #contact {
      padding: 100px 0;
      background: var(--blue-xlight);
      border-top: 1px solid var(--border);
    }

    .contact-layout {
      display: grid;
      grid-template-columns: 1fr 360px;
      gap: 2.5rem;
      align-items: start;
    }

    .contact-form-card {
      background: var(--white);
      border-radius: var(--r-lg);
      padding: 2rem 1.8rem;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-card);
    }

    .form-title {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.3rem;
      margin-bottom: .35rem;
    }

    .form-sub {
      font-size: .8rem;
      color: var(--muted);
      margin-bottom: 1.5rem;
      line-height: 1.5;
    }

    form { display: flex; flex-direction: column; gap: .85rem; }

    .field-row {
      display: flex;
      gap: .85rem;
    }

    .field { flex: 1; }

    label {
      display: block;
      font-size: .72rem;
      font-weight: 500;
      letter-spacing: .04em;
      color: var(--muted);
      margin-bottom: .3rem;
      text-transform: uppercase;
    }

    input, textarea, select {
      width: 100%;
      border-radius: 10px;
      border: 1.5px solid var(--border);
      padding: .62rem .85rem;
      font-size: .84rem;
      font-family: inherit;
      color: var(--ink);
      outline: none;
      background: #f9fbff;
      transition: border-color .18s, box-shadow .18s, background .18s;
    }

    input:focus, textarea:focus, select:focus {
      border-color: var(--blue);
      background: var(--white);
      box-shadow: 0 0 0 3px rgba(0,90,173,.12);
    }

    textarea { resize: vertical; min-height: 100px; }

    .form-footer {
      display: flex;
      flex-direction: column;
      gap: 0;
      margin-top: .4rem;
    }

    .form-disclaimer {
      font-size: .7rem;
      color: var(--muted);
      max-width: 18rem;
      line-height: 1.5;
    }

    /* Contact sidebar */
    .contact-sidebar {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .contact-info-card {
      background: var(--white);
      border-radius: var(--r);
      padding: 1.5rem;
      border: 1px solid var(--border);
      box-shadow: var(--shadow-card);
    }

    .contact-info-card h4 {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.05rem;
      margin-bottom: .9rem;
    }

    .contact-info-row {
      display: flex;
      flex-direction: column;
      gap: .7rem;
      font-size: .82rem;
    }

    .contact-info-item {
      display: flex;
      flex-direction: column;
      gap: .1rem;
    }

    .contact-info-label {
      font-size: .68rem;
      text-transform: uppercase;
      letter-spacing: .12em;
      color: var(--muted);
    }

    .contact-info-value {
      font-weight: 600;
      color: var(--ink);
    }

    .contact-info-value a:hover { color: var(--blue); }

    .contact-cta-card {
      background: linear-gradient(135deg, var(--blue-dark), var(--blue));
      border-radius: var(--r);
      padding: 1.5rem;
      color: #fff;
      position: relative;
      overflow: hidden;
    }

    .contact-cta-card::after {
      content: "";
      position: absolute;
      top: -30px; right: -30px;
      width: 120px; height: 120px;
      border-radius: 50%;
      background: rgba(255,255,255,.06);
    }

    .contact-cta-card h4 {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: 1.05rem;
      margin-bottom: .4rem;
    }

    .contact-cta-card p {
      font-size: .78rem;
      color: rgba(255,255,255,.7);
      margin-bottom: 1rem;
      line-height: 1.55;
    }

    .contact-cta-card a {
      display: inline-flex;
      align-items: center;
      gap: .4rem;
      padding: .6rem 1.2rem;
      border-radius: 99px;
      background: rgba(255,255,255,.15);
      border: 1px solid rgba(255,255,255,.4);
      font-size: .8rem;
      font-weight: 600;
      color: #fff;
      backdrop-filter: blur(8px);
      transition: background .18s, border-color .18s;
    }

    .contact-cta-card a:hover {
      background: rgba(255,255,255,.25);
      border-color: rgba(255,255,255,.8);
    }

    /* ─── FOOTER ──────────────────────────────── */

    footer {
      padding: 2rem 0 2.4rem;
      background: var(--ink);
      color: rgba(255,255,255,.45);
      font-size: .78rem;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }

    .footer-links {
      display: flex;
      gap: 1.5rem;
    }

    .footer-links a {
      color: rgba(255,255,255,.4);
      transition: color .15s;
    }

    .footer-links a:hover { color: rgba(255,255,255,.9); }

    .footer-logo {
      font-family: "DM Serif Display", Georgia, serif;
      font-size: .95rem;
      color: rgba(255,255,255,.7);
    }

    /* ─── FLOATING CALL ───────────────────────── */

    .floating-call {
      position: fixed;
      right: 1.5rem;
      bottom: 1.5rem;
      z-index: 40;
    }

    .floating-call a {
      display: inline-flex;
      align-items: center;
      gap: .5rem;
      padding: .75rem 1.3rem;
      border-radius: 99px;
      background: #16a34a;
      color: #fff;
      font-weight: 600;
      font-size: .82rem;
      box-shadow: 0 12px 35px rgba(22,163,74,.55), 0 0 0 0 rgba(22,163,74,.4);
      animation: pulse-green 2.8s infinite;
      transition: transform .18s, box-shadow .18s;
    }

    .floating-call a:hover { transform: scale(1.04); }

    @keyframes pulse-green {
      0%, 100% { box-shadow: 0 12px 35px rgba(22,163,74,.55), 0 0 0 0 rgba(22,163,74,.4); }
      50%       { box-shadow: 0 12px 35px rgba(22,163,74,.55), 0 0 0 10px rgba(22,163,74,.0); }
    }

    /* ─── PAGE LOAD ANIMATIONS ────────────────── */

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .hero-tag      { animation: fadeUp .5s var(--ease) .1s both; }
    .hero-headline { animation: fadeUp .55s var(--ease) .25s both; }
    .hero-sub      { animation: fadeUp .55s var(--ease) .4s both; }
    .hero-actions  { animation: fadeUp .55s var(--ease) .52s both; }
    .hero-trust    { animation: fadeUp .5s var(--ease) .62s both; }
    .glance-panel  { animation: fadeUp .6s var(--ease) .35s both; }

    /* ─── RESPONSIVE ──────────────────────────── */

    @media (max-width: 1024px) {
      .hero-grid, .about-layout, .contact-layout {
        grid-template-columns: 1fr;
      }

      .glance-panel { max-width: 480px; }

      .services-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .services-header {
        flex-direction: column;
        align-items: flex-start;
      }

      .services-note { text-align: left; max-width: 100%; }

      .process-grid {
        grid-template-columns: repeat(2, 1fr);
        gap: 2rem;
      }

      .process-grid::before { display: none; }
    }

    @media (max-width: 768px) {
      .nav-links, .nav-right { display: none; }
      .nav-toggle { display: inline-flex; }

      .hero-headline { font-size: 2.5rem; }
      .hero-inner { padding-top: 100px; }

      .services-grid, .about-layout {
        grid-template-columns: 1fr;
      }

      .field-row { flex-direction: column; }

      .process-grid { grid-template-columns: 1fr 1fr; }

      .about-stat-row { gap: 1.5rem; }

      .floating-call a { font-size: 0; padding: .85rem; }
      .floating-call a span { font-size: 1.2rem; }
    }
  </style>
</head>
<body>

  <!-- ─── NAVBAR ──────────────────────────────── -->
  <header class="navbar" id="navbar">
    <div class="container navbar-inner">
      <a href="#home" class="nav-logo">
        <img src="Universe Services Logo White.png" alt="Universe Services logo" class="logo-img" style="height:150px;" />
      </a>

      <nav class="nav-links">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </nav>

      <div class="nav-right">
        <div class="nav-phone">
          Main Office &bull; <strong>(305) 555-0123</strong>
        </div>
        <a href="#contact" class="btn btn-primary" style="font-size:.78rem;padding:.5rem 1.15rem;">Request Service</a>
      </div>

      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
        <div class="hamburger">
          <span></span><span></span><span></span>
        </div>
      </button>
    </div>

    <div class="nav-mobile" id="navMobile">
      <div class="nav-mobile-inner container">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
        <a href="tel:+13055550123" style="color:var(--blue);font-weight:600;">📞 (305) 555-0123</a>
      </div>
    </div>
  </header>

  <main id="home">

    <!-- ─── HERO ─────────────────────────────── -->
    <section class="hero">
      <div class="hero-overlay"></div>
      <canvas id="snowCanvas" style="position:absolute;top:0;left:0;width:100%;height:100%;z-index:3;pointer-events:none;display:block;"></canvas>
      <!-- Thermostat widget -->
      <div id="thermostat" style="
        position:absolute;
        bottom:2.5rem;
        right:2.5rem;
        z-index:6;
        width:110px;
        background:rgba(10,30,80,.35);
        border:1px solid rgba(255,255,255,.22);
        border-radius:20px;
        padding:1rem .85rem 1.1rem;
        backdrop-filter:blur(16px);
        -webkit-backdrop-filter:blur(16px);
        text-align:center;
        pointer-events:none;
        box-shadow:0 8px 32px rgba(0,10,40,.4), inset 0 1px 0 rgba(255,255,255,.15);
      ">
        <div style="font-size:.6rem;letter-spacing:.18em;text-transform:uppercase;color:rgba(255,255,255,.6);margin-bottom:.5rem;">TEMPERATURE</div>
        <svg viewBox="0 0 60 105" width="50" style="display:block;margin:0 auto .7rem;overflow:visible;" id="thermoSvg">
          <defs>
            <clipPath id="tubeClip">
              <rect x="24" y="10" width="12" height="68" rx="6"/>
            </clipPath>
          </defs>
          <!-- Tube background (empty) -->
          <rect x="24" y="10" width="12" height="68" rx="6"
                fill="rgba(255,255,255,.1)" stroke="rgba(255,255,255,.4)" stroke-width="1.5"/>
          <!-- Mercury fill — clipped to tube, grows/shrinks via JS -->
          <rect id="mercury" x="24" y="20" width="12" height="58" rx="4"
                fill="#7dd3fc" clip-path="url(#tubeClip)"/>
          <!-- Tick marks on right -->
          <line x1="36" y1="18" x2="42" y2="18" stroke="rgba(255,255,255,.5)" stroke-width="1.2"/>
          <line x1="36" y1="29" x2="40" y2="29" stroke="rgba(255,255,255,.35)" stroke-width="1"/>
          <line x1="36" y1="40" x2="42" y2="40" stroke="rgba(255,255,255,.5)" stroke-width="1.2"/>
          <line x1="36" y1="51" x2="40" y2="51" stroke="rgba(255,255,255,.35)" stroke-width="1"/>
          <line x1="36" y1="62" x2="42" y2="62" stroke="rgba(255,255,255,.5)" stroke-width="1.2"/>
          <line x1="36" y1="73" x2="40" y2="73" stroke="rgba(255,255,255,.35)" stroke-width="1"/>
          <!-- Tube glass shine -->
          <rect x="26" y="13" width="3" height="58" rx="2" fill="rgba(255,255,255,.18)"/>
          <!-- Bulb outer -->
          <circle id="thermoBulb" cx="30" cy="89" r="11"
                  fill="#7dd3fc" stroke="rgba(255,255,255,.4)" stroke-width="1.5"/>
          <!-- Bulb inner shine -->
          <circle cx="26" cy="85" r="3" fill="rgba(255,255,255,.35)"/>
        </svg>
        <div id="thermoTemp" style="font-family:'DM Serif Display',Georgia,serif;font-size:1.6rem;color:#fff;line-height:1;margin-bottom:.15rem;">78°</div>
        <div style="font-size:.58rem;letter-spacing:.1em;text-transform:uppercase;color:rgba(255,255,255,.55);">Cooling down</div>
        <!-- Snowflake accents -->
        <div style="font-size:.9rem;margin-top:.5rem;letter-spacing:.2rem;color:rgba(255,255,255,.5);">❄ ❄ ❄</div>
      </div>

      <div class="container hero-inner">
        <div class="hero-grid">
          <div>
            <div class="hero-tag">Mechanical Contractor</div>

            <h1 class="hero-headline">
              Air Conditioning
              <em>Done Right.</em>
            </h1>

            <p class="hero-sub">
              Universe Services delivers expert A/C repairs, system replacements, and maintenance programs for homes and properties across Miami-Dade and Broward.
            </p>

            <div class="hero-actions">
              <a href="#contact" class="btn btn-primary">Request Service</a>
              <a href="tel:+13055550123" class="btn btn-ghost">📞 Call Us Now</a>
            </div>

            <div class="hero-trust">
              <div class="hero-trust-item"><span class="hero-trust-icon">⚡</span><strong>Same/Next-Day</strong> Response</div>
              <div class="hero-trust-item"><span class="hero-trust-icon">📍</span><strong>Miami-Dade</strong> &amp; Broward</div>
              <div class="hero-trust-item"><span class="hero-trust-icon">✓</span>Licensed &amp; <strong>Insured</strong></div>
            </div>
          </div>

          <aside class="glance-panel">
            <div class="glance-title">Universe at a Glance</div>
            <p class="glance-sub">A focused mechanical partner for homeowners, property managers, and associations across South Florida.</p>

            <div class="glance-stats">
              <div>
                <div class="glance-stat-label">Service Response</div>
                <div class="glance-stat-value">Same / Next Day</div>
              </div>
              <div>
                <div class="glance-stat-label">Service Hours</div>
                <div class="glance-stat-value">Mon–Fri 8am–7pm</div>
                <div style="margin-top:.3rem;font-size:.65rem;color:#2563eb;background:#eff6ff;border:1px solid #bfdbfe;border-radius:6px;padding:.2rem .45rem;display:inline-block;line-height:1.4;">⏱ After-hours & weekends available at premium rates</div>
              </div>
              <div>
                <div class="glance-stat-label">Coverage Area</div>
                <div class="glance-stat-value">Miami-Dade &amp; Broward</div>
              </div>
              <div>
                <div class="glance-stat-label">Based In</div>
                <div class="glance-stat-value">South Florida</div>
              </div>
            </div>

            <div class="glance-divider"></div>

            <p class="glance-footer">
              Licensed and insured mechanical contractor specializing in Florida's coastal environment — flat roofs, high humidity, and the long South Florida cooling season.
            </p>

            <div class="glance-chip">Accepting new service clients</div>
          </aside>
        </div>
      </div>
    </section>

    <!-- ─── MARQUEE ───────────────────────────── -->
    <div class="marquee-band" aria-hidden="true">
      <div class="marquee-track">
        <!-- Doubled for seamless loop -->
        <span class="marquee-item"><span class="marquee-dot"></span>A/C Repairs &amp; Diagnostics</span>
        <span class="marquee-item"><span class="marquee-dot"></span>System Replacements</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Ductless Mini-Splits</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Indoor Air Quality</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Smart Thermostats</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Maintenance Programs</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Florida Licensed</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Same &amp; Next-Day Service</span>
        <span class="marquee-item"><span class="marquee-dot"></span>A/C Repairs &amp; Diagnostics</span>
        <span class="marquee-item"><span class="marquee-dot"></span>System Replacements</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Ductless Mini-Splits</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Indoor Air Quality</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Smart Thermostats</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Maintenance Programs</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Florida Licensed</span>
        <span class="marquee-item"><span class="marquee-dot"></span>Same &amp; Next-Day Service</span>
      </div>
    </div>

    <!-- ─── ABOUT ─────────────────────────────── -->
    <section id="about">
      <div class="container">
        <div class="about-layout" style="grid-template-columns:1fr;max-width:780px;">
          <div class="about-left">
            <div class="eyebrow">About Us</div>
            <h2 class="section-title">A family-owned team<br />built on <em style="font-style:italic;color:var(--blue);">trust</em>.</h2>

            <div class="about-body">
              <p><strong>Universe Services</strong> is a family-owned HVAC company built on a simple idea: show up, do the job right, and treat every home like our own.</p>
              <p>Based in South Florida, we serve Miami-Dade and Broward. We handle everything from repairs and service calls to full system replacements and maintenance plans for homeowners, property managers, and associations.</p>
              <p>We keep things simple: clear communication, clean work, and support after the job is done. Our clients know exactly who to call and what to expect every time.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ─── SERVICES ──────────────────────────── -->
    <section id="services">
      <div class="container">
        <div class="services-header">
          <div>
            <div class="eyebrow">Services</div>
            <h2 class="section-title">Everything your A/C needs,<br />handled in one call.</h2>
            <p class="section-sub">Responsive teams focused on diagnosing root causes, communicating clearly, and protecting your property while we work.</p>
          </div>
          <div class="services-note">Trusted by homeowners, property managers, and associations throughout South Florida.</div>
        </div>

        <div class="services-grid">
          <article class="service-card">
            <div class="service-icon">🔧</div>
            <div class="service-name">Diagnostics &amp; Repair</div>
            <p class="service-desc">Troubleshooting no-cool calls, water leaks, electrical issues, and comfort problems on all major brands — most resolved in a single visit.</p>
            <div class="service-tags">
              <span class="service-tag">Same / Next-day</span>
              <span class="service-tag">Clear pricing</span>
              <span class="service-tag">All brands</span>
            </div>
            <a href="#contact" class="service-cta">Book a repair →</a>
          </article>

          <article class="service-card">
            <div class="service-icon">🏠</div>
            <div class="service-name">System Replacements</div>
            <p class="service-desc">Full change-outs with duct review, proper line-set practices, permitting, and a thorough homeowner orientation upon completion.</p>
            <div class="service-tags">
              <span class="service-tag">High-efficiency</span>
              <span class="service-tag">Heat pumps</span>
              <span class="service-tag">Financing available</span>
            </div>
            <a href="#contact" class="service-cta">Request a quote →</a>
          </article>

          <article class="service-card">
            <div class="service-icon">📱</div>
            <div class="service-name">Controls &amp; Smart Thermostats</div>
            <p class="service-desc">Upgrading thermostats, zoning systems, and controls for homes, rentals, and small commercial spaces — manage comfort from anywhere.</p>
            <div class="service-tags">
              <span class="service-tag">Nest &amp; Ecobee</span>
              <span class="service-tag">Zoning systems</span>
            </div>
            <a href="#contact" class="service-cta">Upgrade controls →</a>
          </article>

          <article class="service-card">
            <div class="service-icon">📋</div>
            <div class="service-name">Maintenance Programs</div>
            <p class="service-desc">Planned inspections, cleaning, and checks to keep your system reliable through South Florida's long and demanding cooling seasons.</p>
            <div class="service-tags">
              <span class="service-tag">Priority response</span>
              <span class="service-tag">Program pricing</span>
            </div>
            <a href="#contact" class="service-cta">Join a program →</a>
          </article>
        </div>
      </div>
    </section>

    <!-- ─── PROCESS STRIP ─────────────────────── -->
    <div class="process-strip">
      <div class="container">
        <div class="process-header">
          <div class="eyebrow" style="justify-content:center;">How It Works</div>
          <h2 class="section-title" style="text-align:center;">Service made simple.</h2>
        </div>

        <div class="process-grid">
          <div class="process-step">
            <div class="process-num">1</div>
            <div class="process-step-title">Reach Out</div>
            <p class="process-step-text">Call us directly or submit a request online. We'll confirm same or next-day availability.</p>
          </div>
          <div class="process-step">
            <div class="process-num">2</div>
            <div class="process-step-title">Diagnose</div>
            <p class="process-step-text">Our tech inspects the system, explains the issue clearly, and provides upfront pricing before any work begins.</p>
          </div>
          <div class="process-step">
            <div class="process-num">3</div>
            <div class="process-step-title">Repair or Replace</div>
            <p class="process-step-text">We complete the work cleanly and efficiently, respecting your home and your schedule.</p>
          </div>
          <div class="process-step">
            <div class="process-num">4</div>
            <div class="process-step-title">Stay Supported</div>
            <p class="process-step-text">Follow-up support and maintenance programs keep your system running long after we leave.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- ─── CONTACT ───────────────────────────── -->
    <section id="contact">
      <div class="container">
        <div class="eyebrow">Contact</div>
        <h2 class="section-title" style="margin-bottom:.5rem;">Tell us what you need.</h2>
        <p class="section-sub" style="margin-bottom:2.5rem;">Share a few details and our team will follow up to review scope, timing, and next steps.</p>

        <div class="contact-layout">
          <div class="contact-form-card">
            <div class="form-title">Request Service</div>
            <p class="form-sub">For urgent no-cool calls, please call <strong>(305) 555-0123</strong> directly.</p>

            <form>
              <div class="field-row">
                <div class="field">
                  <label for="name">Full Name</label>
                  <input id="name" type="text" placeholder="Your name" />
                </div>
                <div class="field">
                  <label for="phone">Mobile Phone</label>
                  <input id="phone" type="tel" placeholder="(305) 555-0123" />
                </div>
              </div>

              <div class="field-row">
                <div class="field">
                  <label for="email">Email</label>
                  <input id="email" type="email" placeholder="you@example.com" />
                </div>
                <div class="field">
                  <label for="city">City / Neighborhood</label>
                  <input id="city" type="text" placeholder="Miami, Doral, Kendall…" />
                </div>
              </div>

              <div class="field-row">
                <div class="field">
                  <label for="serviceType">I'm Reaching Out About</label>
                  <select id="serviceType">
                    <option>Service / repair</option>
                    <option>System replacement</option>
                    <option>Controls / smart thermostat</option>
                    <option>Maintenance program</option>
                    <option>Other A/C need</option>
                  </select>
                </div>
                <div class="field">
                  <label for="timeframe">Ideal Timeframe</label>
                  <select id="timeframe">
                    <option>ASAP / emergency</option>
                    <option>This week</option>
                    <option>Within 30 days</option>
                    <option>Planning / budgeting</option>
                  </select>
                </div>
              </div>

              <div class="field">
                <label for="message">Describe the Issue or Request</label>
                <textarea id="message" placeholder="E.g. 2nd floor not cooling, system is 15 years old, looking for a maintenance plan, etc."></textarea>
              </div>

              <div class="form-footer">
                <button type="button" class="btn btn-primary" style="width:100%;justify-content:center;padding:.75rem 1.5rem;font-size:.88rem;">Submit Request</button>
                <p class="form-disclaimer" style="text-align:center;margin-top:.6rem;">By submitting, you agree we may contact you by phone, text, or email about your request.</p>
              </div>
            </form>
          </div>

          <div class="contact-sidebar">
            <div class="contact-info-card">
              <h4>Get in Touch</h4>
              <div class="contact-info-row">
                <div class="contact-info-item">
                  <span class="contact-info-label">Main Office</span>
                  <span class="contact-info-value"><a href="tel:+13055550123">(305) 555-0123</a></span>
                </div>
                <div class="contact-info-item">
                  <span class="contact-info-label">Email</span>
                  <span class="contact-info-value"><a href="/cdn-cgi/l/email-protection#325b5c545d72475c5b445740415753511c515d5f"><span class="__cf_email__" data-cfemail="8de4e3ebe2cdf8e3e4fbe8fffee8eceea3eee2e0">[email&#160;protected]</span></a></span>
                </div>
              </div>
            </div>

            <div class="contact-cta-card">
              <h4>No cool? Call now.</h4>
              <p>For emergency no-cool calls, don't wait. Call our office directly for the fastest response.</p>
              <a href="tel:+13055550123">📞 (305) 555-0123</a>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>

  <!-- ─── FOOTER ────────────────────────────── -->
  <footer>
    <div class="container footer-inner">
      <div class="footer-logo">Universe Services</div>
      <div>© <span id="year"></span> All rights reserved. South Florida</div>
      <div class="footer-links">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </div>
    </div>
  </footer>

  <!-- ─── FLOATING CALL ─────────────────────── -->
  <script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
    // Navbar scroll state
    const navbar = document.getElementById("navbar");
    window.addEventListener("scroll", () => {
      navbar.classList.toggle("scrolled", window.scrollY > 10);
    }, { passive: true });

    // Mobile nav
    const navToggle = document.getElementById("navToggle");
    const navMobile = document.getElementById("navMobile");

    navToggle.addEventListener("click", () => {
      const isOpen = navMobile.style.display === "block";
      navMobile.style.display = isOpen ? "none" : "block";
      navToggle.classList.toggle("active", !isOpen);
    });

    navMobile.addEventListener("click", (e) => {
      if (e.target.tagName.toLowerCase() === "a") {
        navMobile.style.display = "none";
        navToggle.classList.remove("active");
      }
    });

    // Footer year
    document.getElementById("year").textContent = new Date().getFullYear();

    // Simple scroll-reveal for sections
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = "1";
          entry.target.style.transform = "translateY(0)";
        }
      });
    }, { threshold: 0.08 });

    document.querySelectorAll(".service-card, .leader-card, .process-step, .contact-info-card, .contact-cta-card").forEach(el => {
      el.style.opacity = "0";
      el.style.transform = "translateY(20px)";
      el.style.transition = "opacity .45s ease, transform .45s ease";
      observer.observe(el);
    });

    // ── Snow effect ──────────────────────────────────────
    (function initSnow() {
      var canvas = document.getElementById('snowCanvas');
      if (!canvas) { console.warn('No snow canvas'); return; }
      var ctx = canvas.getContext('2d');
      var hero = document.querySelector('.hero');
      var flakes = [];
      var COUNT = 150;

      function setSize() {
        var r = hero.getBoundingClientRect();
        canvas.width  = r.width  || window.innerWidth;
        canvas.height = r.height || window.innerHeight;
      }

      function rand(a, b) { return Math.random() * (b - a) + a; }

      function newFlake(atTop) {
        return {
          x:       rand(0, canvas.width),
          y:       atTop ? rand(0, canvas.height) : -rand(2, 15),
          r:       rand(2, 5),
          vy:      rand(0.6, 2.2),
          vx:      rand(-0.5, 0.5),
          alpha:   rand(0.4, 0.9),
          wobble:  rand(0, Math.PI * 2),
          wFreq:   rand(0.01, 0.03),
          wAmp:    rand(0.3, 0.8)
        };
      }

      setSize();
      for (var i = 0; i < COUNT; i++) flakes.push(newFlake(true));
      window.addEventListener('resize', setSize, { passive: true });

      function tick() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        for (var i = 0; i < flakes.length; i++) {
          var f = flakes[i];
          f.wobble += f.wFreq;
          f.x += f.vx + Math.sin(f.wobble) * f.wAmp;
          f.y += f.vy;
          if (f.y > canvas.height + 10) {
            flakes[i] = newFlake(false);
            continue;
          }
          // Draw snowflake as circle with soft glow
          ctx.save();
          ctx.globalAlpha = f.alpha;
          ctx.shadowColor = 'rgba(255,255,255,0.8)';
          ctx.shadowBlur  = f.r * 2;
          ctx.beginPath();
          ctx.arc(f.x, f.y, f.r, 0, Math.PI * 2);
          ctx.fillStyle = '#ffffff';
          ctx.fill();
          ctx.restore();
        }
        requestAnimationFrame(tick);
      }
      tick();
      console.log('Snow started — flakes:', COUNT, 'canvas:', canvas.width, 'x', canvas.height);
    })();

    // ── Thermostat animation ──────────────────────────────
    (function initThermostat() {
      var tempEl  = document.getElementById('thermoTemp');
      var mercury = document.getElementById('mercury');
      var bulb    = document.getElementById('thermoBulb');
      if (!tempEl || !mercury) { console.warn('Thermostat elements not found'); return; }

      var MIN = 62, MAX = 84;
      var TUBE_TOP    = 10;
      var TUBE_BOTTOM = 78;  // y where tube meets bulb
      var TUBE_HEIGHT = TUBE_BOTTOM - TUBE_TOP; // 68px

      var current   = MAX;
      var SPEED     = 0.025;  // degrees per frame

      function getColor(t) {
        if (t >= 80) {
          // 84→80: dark red to light red (fast, 4 degrees)
          var p = (t - 80) / (84 - 80); // 1=dark red, 0=light red
          var r = Math.round(220 - p * 30);   // 190→220
          var g = Math.round(p * 40);          // 40→0
          var b = Math.round(p * 40);          // 40→0
          return 'rgb(' + r + ',' + g + ',' + b + ')';
        } else {
          // 80→62: dark blue to light blue (gradual, 18 degrees)
          var p = (t - 62) / (80 - 62); // 1=dark blue, 0=light blue
          var r = Math.round(30  + (1 - p) * 120); // 30→150
          var g = Math.round(80  + (1 - p) * 130); // 80→210
          var b = Math.round(180 + (1 - p) * 72);  // 180→252
          return 'rgb(' + r + ',' + g + ',' + b + ')';
        }
      }

      function draw(t) {
        t = Math.max(MIN, Math.min(MAX, t));

        // Update text
        tempEl.textContent = Math.round(t) + '°F';

        // Map temperature to mercury rect
        var pct    = (t - MIN) / (MAX - MIN);
        var minH   = 6,  maxH = 62;
        var h = minH + pct * (maxH - minH);
        var y = TUBE_BOTTOM - h;  // bottom of mercury always at tube bottom

        mercury.setAttribute('y', y.toFixed(2));
        mercury.setAttribute('height', h.toFixed(2));

        var col = getColor(t);
        mercury.setAttribute('fill', col);
        if (bulb) bulb.setAttribute('fill', col);
      }

      function frame() {
        current -= SPEED;
        if (current <= MIN) { current = MAX; } // instant jump back to top
        draw(current);
        requestAnimationFrame(frame);
      }

      draw(current);
      requestAnimationFrame(frame);
    })();

  </script>
</body>
</html>
