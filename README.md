<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Universe Mechanical & Air Conditioning Inc. | Miami A/C Experts</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Universe Mechanical & Air Conditioning Inc. - Miami's trusted A/C experts for new construction, installs, repairs and maintenance." />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-dark: #050814;
      --bg-darker: #02030a;
      --bg-card: #0c1020;
      --accent: #23b1ff;
      --accent-soft: rgba(35, 177, 255, 0.2);
      --accent-2: #2effb9;
      --text-main: #f5f7ff;
      --text-muted: #a3aed0;
      --border-subtle: rgba(255, 255, 255, 0.06);
      --danger: #ff4d4f;
      --radius-xl: 22px;
      --shadow-soft: 0 18px 55px rgba(0, 0, 0, 0.65);
      --transition-fast: 0.18s ease-out;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html, body {
      scroll-behavior: smooth;
      background: radial-gradient(circle at top left, #132043 0, #050814 40%, #02030a 100%);
      color: var(--text-main);
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      line-height: 1.5;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    /* Layout helpers */
    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.85rem 1.8rem;
      border-radius: 999px;
      border: 1px solid transparent;
      font-size: 0.95rem;
      font-weight: 600;
      cursor: pointer;
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), background var(--transition-fast), border var(--transition-fast), color var(--transition-fast);
      white-space: nowrap;
      gap: 0.45rem;
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--accent), #4f46e5);
      color: white;
      box-shadow: 0 16px 45px rgba(0, 0, 0, 0.7);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.85);
    }

    .btn-ghost {
      background: rgba(9, 12, 28, 0.8);
      color: var(--text-main);
      border-color: rgba(255, 255, 255, 0.15);
    }

    .btn-ghost:hover {
      background: rgba(16, 22, 52, 0.95);
      transform: translateY(-1px);
    }

    .badge {
      display: inline-flex;
      align-items: center;
      padding: 0.35rem 0.8rem;
      font-size: 0.7rem;
      border-radius: 999px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      border: 1px solid rgba(255, 255, 255, 0.18);
      background: rgba(8, 13, 33, 0.85);
      color: var(--text-muted);
      gap: 0.4rem;
    }

    .badge-dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: var(--accent-2);
      box-shadow: 0 0 14px rgba(46, 255, 185, 0.9);
    }

    /* NAVBAR */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 40;
      transition: background var(--transition-fast), box-shadow var(--transition-fast), border-bottom var(--transition-fast), backdrop-filter var(--transition-fast);
    }

    .navbar-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 76px;
    }

    .navbar.scrolled {
      background: rgba(3, 5, 18, 0.88);
      backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(255, 255, 255, 0.06);
      box-shadow: 0 18px 45px rgba(0, 0, 0, 0.72);
    }

    .nav-logo {
      display: flex;
      align-items: center;
      gap: 0.65rem;
      font-weight: 600;
    }

    .logo-mark {
      width: 34px;
      height: 34px;
      border-radius: 16px;
      background: radial-gradient(circle at 30% 0, #ffffff, #4f46e5 45%, #23b1ff 100%);
      box-shadow: 0 10px 30px rgba(35, 177, 255, 0.6);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.9rem;
      color: var(--bg-dark);
      font-weight: 700;
    }

    .logo-text-main {
      font-size: 0.95rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
    }

    .logo-text-sub {
      font-size: 0.67rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--text-muted);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.75rem;
      font-size: 0.9rem;
    }

    .nav-links a {
      color: var(--text-muted);
      position: relative;
      padding-bottom: 0.1rem;
      transition: color var(--transition-fast);
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.3rem;
      width: 0;
      height: 2px;
      background: linear-gradient(90deg, var(--accent), var(--accent-2));
      border-radius: 999px;
      transition: width var(--transition-fast);
    }

    .nav-links a:hover {
      color: var(--text-main);
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .nav-phone {
      font-size: 0.8rem;
      color: var(--text-muted);
    }

    .nav-phone strong {
      color: var(--accent-2);
      font-weight: 600;
    }

    .nav-cta {
      font-size: 0.8rem;
      padding-inline: 1.2rem;
      padding-block: 0.55rem;
    }

    .nav-toggle {
      display: none;
      width: 38px;
      height: 38px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.3);
      align-items: center;
      justify-content: center;
      cursor: pointer;
      background: rgba(3, 7, 18, 0.8);
    }

    .nav-toggle span {
      width: 18px;
      height: 2px;
      background: white;
      position: relative;
      border-radius: 999px;
    }

    .nav-toggle span::before,
    .nav-toggle span::after {
      content: "";
      position: absolute;
      left: 0;
      width: 100%;
      height: 2px;
      background: white;
      border-radius: 999px;
      transition: transform 0.2s ease, opacity 0.2s ease, top 0.2s ease, bottom 0.2s ease;
    }

    .nav-toggle span::before {
      top: -5px;
    }

    .nav-toggle span::after {
      bottom: -5px;
    }

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
    }

    /* HERO */
    .hero {
      padding-top: 110px;
      padding-bottom: 90px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 3rem;
      align-items: center;
    }

    .hero-eyebrow {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      margin-bottom: 1.2rem;
      flex-wrap: wrap;
    }

    .hero-tag {
      background: rgba(10, 19, 48, 0.9);
      border-radius: 999px;
      padding: 0.1rem;
      display: inline-flex;
      align-items: center;
    }

    .hero-tag span {
      display: inline-flex;
      align-items: center;
      padding: 0.35rem 0.7rem;
      font-size: 0.68rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--text-muted);
    }

    .hero-tag span:nth-child(1) {
      border-radius: 999px;
      background: radial-gradient(circle at 20% 0, rgba(255, 255, 255, 0.3), var(--accent) 55%, #4f46e5 100%);
      color: #050814;
      font-weight: 600;
    }

    .hero-title {
      font-size: 2.9rem;
      line-height: 1.1;
      font-weight: 700;
      margin-bottom: 1.1rem;
    }

    .hero-title span {
      background: linear-gradient(135deg, #ffffff, var(--accent-2));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero-subtitle {
      font-size: 0.98rem;
      color: var(--text-muted);
      max-width: 32rem;
      margin-bottom: 1.6rem;
    }

    .hero-bullets {
      display: flex;
      flex-wrap: wrap;
      gap: 0.85rem;
      margin-bottom: 2.1rem;
      font-size: 0.8rem;
    }

    .hero-bullet {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.4rem 0.9rem;
      border-radius: 999px;
      background: rgba(8, 13, 33, 0.85);
      border: 1px solid rgba(255, 255, 255, 0.06);
      color: var(--text-muted);
    }

    .hero-bullet-dot {
      width: 9px;
      height: 9px;
      border-radius: 999px;
      background: radial-gradient(circle, var(--accent-2), var(--accent));
      box-shadow: 0 0 12px rgba(46, 255, 185, 0.9);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.9rem;
      align-items: center;
      margin-bottom: 1.7rem;
    }

    .hero-note {
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    .hero-note span {
      color: var(--accent-2);
      font-weight: 500;
    }

    .hero-right {
      position: relative;
    }

    .hero-card {
      background: radial-gradient(circle at top, rgba(35, 177, 255, 0.16), rgba(5, 8, 20, 0.95));
      border-radius: 32px;
      padding: 1.6rem 1.5rem;
      border: 1px solid rgba(255, 255, 255, 0.06);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: -40%;
      background:
        radial-gradient(circle at 15% 0, rgba(35, 177, 255, 0.32), transparent 55%),
        radial-gradient(circle at 85% 100%, rgba(79, 70, 229, 0.38), transparent 55%);
      opacity: 0.75;
      pointer-events: none;
    }

    .hero-card-inner {
      position: relative;
      z-index: 2;
    }

    .hero-card-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 0.8rem;
      gap: 1rem;
    }

    .hero-card-title {
      font-size: 0.92rem;
      font-weight: 600;
    }

    .hero-card-pill {
      font-size: 0.7rem;
      color: var(--accent-2);
      background: rgba(2, 6, 23, 0.9);
      padding: 0.3rem 0.6rem;
      border-radius: 999px;
      border: 1px solid rgba(35, 177, 255, 0.25);
    }

    .hero-metrics {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 0.9rem;
      margin-bottom: 1.2rem;
      font-size: 0.75rem;
    }

    .metric-label {
      color: var(--text-muted);
      margin-bottom: 0.25rem;
    }

    .metric-value {
      font-weight: 600;
      font-size: 0.95rem;
    }

    .metric-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.25rem;
      font-size: 0.7rem;
      color: var(--accent-2);
      padding: 0.15rem 0.45rem;
      border-radius: 999px;
      border: 1px solid rgba(46, 255, 185, 0.35);
      background: rgba(3, 7, 18, 0.88);
    }

    .hero-card-row {
      display: flex;
      gap: 1rem;
      font-size: 0.8rem;
      margin-bottom: 0.4rem;
    }

    .hero-card-row > div {
      flex: 1;
    }

    .hero-card-row strong {
      font-size: 0.8rem;
    }

    .hero-card-divider {
      height: 1px;
      border-radius: 999px;
      background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
      margin: 0.9rem 0 0.7rem;
    }

    .hero-card-bottom {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1.2rem;
      font-size: 0.75rem;
    }

    .hero-avatar-row {
      display: flex;
      align-items: center;
      gap: 0.45rem;
    }

    .hero-avatars {
      display: inline-flex;
      align-items: center;
    }

    .hero-avatars span {
      width: 20px;
      height: 20px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 0, #ffffff, var(--accent));
      border: 1px solid rgba(5, 8, 20, 0.9);
      display: inline-block;
      margin-left: -6px;
    }

    .hero-avatars span:first-child {
      margin-left: 0;
      background: radial-gradient(circle at 30% 0, #ffffff, #f97316);
    }

    .hero-card-badge {
      font-size: 0.7rem;
      padding: 0.3rem 0.7rem;
      border-radius: 999px;
      background: rgba(2, 6, 23, 0.9);
      border: 1px solid rgba(35, 177, 255, 0.28);
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
    }

    .hero-floating {
      position: absolute;
      inset: auto 0 -26px auto;
      transform: translateX(15%);
      width: 220px;
      padding: 0.8rem 0.95rem;
      border-radius: 999px;
      background: rgba(3, 7, 18, 0.95);
      border: 1px solid rgba(255, 255, 255, 0.1);
      font-size: 0.7rem;
      display: flex;
      align-items: center;
      gap: 0.7rem;
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.85);
    }

    .hero-floating-dot {
      width: 16px;
      height: 16px;
      border-radius: 999px;
      background: radial-gradient(circle, var(--accent), var(--accent-2));
      box-shadow: 0 0 16px rgba(35, 177, 255, 0.9);
    }

    .hero-floating span {
      color: var(--text-muted);
    }

    .hero-floating strong {
      color: var(--accent-2);
      font-weight: 600;
    }

    /* Strip */
    .trust-strip {
      border-radius: var(--radius-xl);
      margin-bottom: 3.2rem;
      padding: 0.85rem 1.1rem;
      background: radial-gradient(circle at 0 0, rgba(35, 177, 255, 0.24), rgba(5, 8, 20, 0.96));
      border: 1px solid rgba(255, 255, 255, 0.08);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1.2rem;
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    .trust-strip strong {
      color: var(--text-main);
    }

    .trust-items {
      display: flex;
      gap: 1.8rem;
      flex-wrap: wrap;
    }

    .trust-item {
      display: flex;
      align-items: center;
      gap: 0.4rem;
      white-space: nowrap;
    }

    .trust-badge {
      width: 16px;
      height: 16px;
      border-radius: 999px;
      border: 1px solid rgba(46, 255, 185, 0.6);
      display: inline-flex;
      align-items: center;
      justify-content: center;
      font-size: 0.6rem;
      color: var(--accent-2);
    }

    /* Sections base */
    section {
      padding: 0 0 80px;
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      gap: 1.5rem;
      margin-bottom: 1.8rem;
    }

    .section-title-wrap {
      max-width: 28rem;
    }

    .section-badge {
      margin-bottom: 0.5rem;
    }

    .section-title {
      font-size: 1.6rem;
      font-weight: 600;
      margin-bottom: 0.3rem;
    }

    .section-subtitle {
      font-size: 0.9rem;
      color: var(--text-muted);
    }

    .section-note {
      font-size: 0.78rem;
      color: var(--text-muted);
      max-width: 18rem;
      text-align: right;
    }

    /* SERVICES */
    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.5rem;
    }

    .card {
      border-radius: var(--radius-xl);
      padding: 1.3rem 1.2rem;
      background: radial-gradient(circle at top, rgba(35, 177, 255, 0.15), rgba(9, 12, 30, 0.98));
      border: 1px solid var(--border-subtle);
      box-shadow: 0 16px 40px rgba(0, 0, 0, 0.78);
      position: relative;
      overflow: hidden;
      transition: transform var(--transition-fast), box-shadow var(--transition-fast), border var(--transition-fast), background var(--transition-fast);
    }

    .card::after {
      content: "";
      position: absolute;
      inset: auto -40% -65%;
      background: radial-gradient(circle at 50% 0, rgba(35, 177, 255, 0.28), transparent 55%);
      opacity: 0;
      transition: opacity 0.25s ease-out, transform 0.25s ease-out;
      transform: translateY(10px);
    }

    .card:hover {
      transform: translateY(-6px);
      border-color: rgba(35, 177, 255, 0.55);
      box-shadow: 0 24px 60px rgba(0, 0, 0, 0.9);
      background: radial-gradient(circle at top, rgba(35, 177, 255, 0.22), rgba(4, 7, 20, 0.98));
    }

    .card:hover::after {
      opacity: 1;
      transform: translateY(0);
    }

    .card-icon {
      width: 32px;
      height: 32px;
      border-radius: 14px;
      background: rgba(15, 23, 42, 0.95);
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 0.85rem;
      font-size: 1.1rem;
    }

    .card-title {
      font-size: 0.98rem;
      font-weight: 600;
      margin-bottom: 0.45rem;
    }

    .card-text {
      font-size: 0.82rem;
      color: var(--text-muted);
      margin-bottom: 0.9rem;
      min-height: 3rem;
    }

    .card-tags {
      display: flex;
      gap: 0.4rem;
      flex-wrap: wrap;
      margin-bottom: 0.9rem;
    }

    .card-tag {
      font-size: 0.7rem;
      padding: 0.2rem 0.55rem;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.12);
      color: var(--text-muted);
    }

    .card-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.75rem;
    }

    .card-link {
      display: inline-flex;
      align-items: center;
      gap: 0.25rem;
      color: var(--accent);
    }

    .card-link span {
      font-size: 0.9rem;
    }

    /* NEW CONSTRUCTION */
    .construction-layout {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 2rem;
      align-items: flex-start;
    }

    .timeline {
      border-radius: var(--radius-xl);
      padding: 1.5rem 1.4rem;
      background: radial-gradient(circle at 0 0, rgba(79, 70, 229, 0.2), rgba(7, 11, 31, 0.98));
      border: 1px solid var(--border-subtle);
      box-shadow: var(--shadow-soft);
    }

    .timeline-step {
      display: grid;
      grid-template-columns: 32px minmax(0, 1fr);
      gap: 0.9rem;
      align-items: flex-start;
      padding: 0.7rem 0;
    }

    .timeline-step:not(:last-child) {
      border-bottom: 1px solid rgba(148, 163, 184, 0.18);
    }

    .timeline-marker {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.2rem;
    }

    .timeline-badge {
      width: 22px;
      height: 22px;
      border-radius: 999px;
      border: 1px solid rgba(35, 177, 255, 0.8);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.7rem;
      background: rgba(15, 23, 42, 0.96);
    }

    .timeline-line {
      flex: 1;
      width: 1px;
      background: linear-gradient(180deg, rgba(148, 163, 184, 0.6), transparent);
    }

    .timeline-title {
      font-size: 0.9rem;
      font-weight: 600;
      margin-bottom: 0.1rem;
    }

    .timeline-text {
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-bottom: 0.3rem;
    }

    .timeline-chip-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      font-size: 0.7rem;
    }

    .timeline-chip {
      padding: 0.18rem 0.55rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.55);
      color: var(--text-muted);
    }

    .construction-right {
      border-radius: var(--radius-xl);
      padding: 1.4rem 1.3rem;
      background: radial-gradient(circle at 100% 0, rgba(35, 177, 255, 0.22), rgba(7, 11, 31, 0.98));
      border: 1px solid var(--border-subtle);
      box-shadow: var(--shadow-soft);
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 0.8rem;
    }

    .pill {
      font-size: 0.7rem;
      padding: 0.25rem 0.7rem;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.6);
      color: var(--text-muted);
    }

    .construction-subtitle {
      font-size: 0.9rem;
      margin-bottom: 0.7rem;
    }

    .checklist {
      list-style: none;
      margin: 0.4rem 0 1.1rem;
      padding: 0;
    }

    .checklist li {
      display: flex;
      align-items: flex-start;
      gap: 0.5rem;
      font-size: 0.8rem;
      color: var(--text-muted);
      margin-bottom: 0.4rem;
    }

    .checkmark {
      margin-top: 0.1rem;
      width: 16px;
      height: 16px;
      border-radius: 999px;
      background: rgba(34, 197, 94, 0.15);
      border: 1px solid rgba(74, 222, 128, 0.7);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.75rem;
      color: #4ade80;
    }

    .construction-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 1.2rem;
      font-size: 0.78rem;
    }

    .construction-footer span {
      color: var(--text-muted);
    }

    .construction-footer strong {
      color: var(--accent-2);
    }

    /* WHY / SERVICE AREA */
    .two-col {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 2rem;
      align-items: flex-start;
    }

    .stack {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .feature-row {
      display: flex;
      gap: 0.85rem;
      font-size: 0.8rem;
      padding: 0.8rem 0.85rem;
      border-radius: 18px;
      background: rgba(15, 23, 42, 0.85);
      border: 1px solid rgba(148, 163, 184, 0.2);
    }

    .feature-icon {
      width: 20px;
      height: 20px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 0, #ffffff, var(--accent));
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.8rem;
      color: var(--bg-dark);
    }

    .feature-row strong {
      font-size: 0.85rem;
    }

    .mini {
      font-size: 0.78rem;
      color: var(--text-muted);
    }

    .map-card {
      border-radius: var(--radius-xl);
      padding: 1.3rem 1.3rem;
      background: radial-gradient(circle at 0 0, rgba(56, 189, 248, 0.26), rgba(7, 11, 31, 0.98));
      border: 1px solid var(--border-subtle);
      box-shadow: var(--shadow-soft);
      font-size: 0.8rem;
    }

    .map-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.65rem;
    }

    .map-title {
      font-size: 0.9rem;
      font-weight: 600;
    }

    .map-tag {
      font-size: 0.72rem;
      padding: 0.2rem 0.55rem;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.5);
      color: var(--text-muted);
    }

    .map-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 0.6rem;
      margin-top: 0.4rem;
    }

    .map-pill {
      padding: 0.32rem 0.55rem;
      border-radius: 999px;
      border: 1px dashed rgba(148, 163, 184, 0.7);
      font-size: 0.78rem;
      color: var(--text-muted);
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .map-pill span {
      font-size: 0.7rem;
      opacity: 0.8;
    }

    /* CONTACT */
    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 2rem;
      align-items: flex-start;
    }

    .contact-card {
      border-radius: var(--radius-xl);
      padding: 1.4rem 1.3rem 1.6rem;
      background: radial-gradient(circle at 100% 0, rgba(46, 255, 185, 0.24), rgba(7, 11, 31, 0.98));
      border: 1px solid var(--border-subtle);
      box-shadow: var(--shadow-soft);
    }

    form {
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
    }

    .field-group {
      display: flex;
      gap: 0.7rem;
      flex-wrap: wrap;
    }

    .field {
      flex: 1 1 150px;
    }

    label {
      display: block;
      font-size: 0.75rem;
      color: var(--text-muted);
      margin-bottom: 0.2rem;
    }

    input, textarea, select {
      width: 100%;
      border-radius: 14px;
      border: 1px solid rgba(148, 163, 184, 0.35);
      background: rgba(15, 23, 42, 0.92);
      padding: 0.55rem 0.75rem;
      font-size: 0.8rem;
      color: var(--text-main);
      outline: none;
      transition: border var(--transition-fast), box-shadow var(--transition-fast), background var(--transition-fast);
      font-family: inherit;
    }

    input::placeholder,
    textarea::placeholder {
      color: rgba(148, 163, 184, 0.7);
    }

    input:focus,
    textarea:focus,
    select:focus {
      border-color: rgba(35, 177, 255, 0.8);
      box-shadow: 0 0 0 1px rgba(35, 177, 255, 0.5);
      background: rgba(15, 23, 42, 0.98);
    }

    textarea {
      resize: vertical;
      min-height: 90px;
    }

    .contact-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 0.9rem;
      gap: 1rem;
      font-size: 0.75rem;
      color: var(--text-muted);
    }

    .contact-meta {
      border-radius: var(--radius-xl);
      padding: 1.2rem 1.1rem;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.35);
      font-size: 0.8rem;
    }

    .contact-meta h4 {
      font-size: 0.9rem;
      margin-bottom: 0.3rem;
    }

    .contact-meta-row {
      margin-top: 0.6rem;
      display: flex;
      justify-content: space-between;
      gap: 1rem;
      font-size: 0.78rem;
    }

    .contact-meta-row span {
      color: var(--text-muted);
    }

    .contact-meta-row strong {
      color: var(--text-main);
      font-weight: 500;
    }

    /* FOOTER */
    footer {
      border-top: 1px solid rgba(148, 163, 184, 0.25);
      padding: 1.5rem 0 2rem;
      font-size: 0.78rem;
      color: var(--text-muted);
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
      gap: 1.1rem;
      flex-wrap: wrap;
    }

    .footer-links a:hover {
      color: var(--text-main);
    }

    /* Floating Call CTA */
    .floating-call {
      position: fixed;
      right: 1.4rem;
      bottom: 1.4rem;
      z-index: 50;
    }

    .floating-call a {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.75rem 1.2rem;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 0, #ffffff, #22c55e 40%, #16a34a 100%);
      color: #020617;
      font-size: 0.85rem;
      font-weight: 600;
      box-shadow: 0 18px 50px rgba(22, 163, 74, 0.9);
      gap: 0.45rem;
    }

    .floating-call span {
      font-size: 1.05rem;
    }

    /* RESPONSIVE */
    @media (max-width: 960px) {
      .hero-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-right {
        order: -1;
      }

      .hero-floating {
        right: 0;
        left: 0;
        margin-inline: auto;
        transform: translateX(0);
      }

      .cards-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .construction-layout,
      .two-col,
      .contact-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .section-header {
        flex-direction: column;
        align-items: flex-start;
      }

      .section-note {
        text-align: left;
      }
    }

    @media (max-width: 768px) {
      .navbar-inner {
        height: 70px;
      }

      .nav-links,
      .nav-right {
        display: none;
      }

      .nav-toggle {
        display: inline-flex;
      }

      .nav-mobile {
        display: none;
        background: rgba(3, 7, 18, 0.98);
        border-bottom: 1px solid rgba(148, 163, 184, 0.3);
        box-shadow: 0 16px 40px rgba(0, 0, 0, 0.92);
      }

      .nav-mobile-list {
        padding: 0.8rem 1.5rem 1.1rem;
        display: flex;
        flex-direction: column;
        gap: 0.75rem;
      }

      .nav-mobile-list a {
        font-size: 0.9rem;
        color: var(--text-muted);
      }

      .nav-mobile-list a:hover {
        color: var(--text-main);
      }

      .trust-strip {
        flex-direction: column;
        align-items: flex-start;
      }

      .cards-grid {
        grid-template-columns: minmax(0, 1fr);
      }

      .hero-title {
        font-size: 2.25rem;
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
        <div class="logo-mark">U</div>
        <div>
          <div class="logo-text-main">Universe Mechanical</div>
          <div class="logo-text-sub">Air Conditioning • Miami, FL</div>
        </div>
      </a>

      <nav class="nav-links">
        <a href="#services">Services</a>
        <a href="#new-construction">New Construction</a>
        <a href="#why">Why Universe</a>
        <a href="#contact">Contact</a>
      </nav>

      <div class="nav-right">
        <div class="nav-phone">
          24/7 Support • <strong>(305) 555-0123</strong>
        </div>
        <a href="#contact" class="btn btn-primary nav-cta">Book Service</a>
      </div>

      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
        <span></span>
      </button>
    </div>

    <!-- Mobile Nav -->
    <div class="nav-mobile" id="navMobile">
      <div class="nav-mobile-list container">
        <a href="#services">Services</a>
        <a href="#new-construction">New Construction</a>
        <a href="#why">Why Universe</a>
        <a href="#contact">Contact</a>
        <a href="tel:+13055550123">Call: (305) 555-0123</a>
      </div>
    </div>
  </header>

  <main id="home">
    <div class="container hero">
      <div class="hero-grid">
        <div class="hero-left">
          <div class="hero-eyebrow">
            <div class="badge">
              <span class="badge-dot"></span> Miami’s Modern A/C Experience
            </div>
            <div class="hero-tag">
              <span>24/7</span>
              <span>Emergency Cooling • Same-Day Installs</span>
            </div>
          </div>

          <h1 class="hero-title">
            Precision-built comfort for
            <span>Miami heat.</span>
          </h1>
          <p class="hero-subtitle">
            Universe Mechanical & Air Conditioning Inc. engineers, installs and maintains high-performance A/C systems for
            Miami homes, condos & new construction projects — with craftsmanship you can actually feel.
          </p>

          <div class="hero-bullets">
            <div class="hero-bullet">
              <div class="hero-bullet-dot"></div>
              Licensed & insured mechanical contractors
            </div>
            <div class="hero-bullet">
              <div class="hero-bullet-dot"></div>
              New builds, retrofits & service
            </div>
            <div class="hero-bullet">
              <div class="hero-bullet-dot"></div>
              Serving Miami-Dade & Broward
            </div>
          </div>

          <div class="hero-actions">
            <a href="#contact" class="btn btn-primary">
              Book A/C Service
              <span>➜</span>
            </a>
            <a href="#new-construction" class="btn btn-ghost">
              New Construction Bid
            </a>
          </div>

          <div class="hero-note">
            <span>Same-day availability</span> for most calls placed before 2:00 PM.
          </div>
        </div>

        <div class="hero-right">
          <div class="hero-card">
            <div class="hero-card-inner">
              <div class="hero-card-header">
                <div>
                  <div class="hero-card-title">Miami Cooling Performance Panel</div>
                  <div class="mini">Live look at your project with Universe Mechanical.</div>
                </div>
                <div class="hero-card-pill">Optimized for South Florida</div>
              </div>

              <div class="hero-metrics">
                <div>
                  <div class="metric-label">Average response</div>
                  <div class="metric-value">1 hr 42 min</div>
                  <div class="metric-pill">On-call 24/7</div>
                </div>
                <div>
                  <div class="metric-label">Install turnaround</div>
                  <div class="metric-value">1–3 days</div>
                  <div class="metric-pill">Permit-ready</div>
                </div>
                <div>
                  <div class="metric-label">Customer rating</div>
                  <div class="metric-value">4.9 ★</div>
                  <div class="metric-pill">310+ locals</div>
                </div>
              </div>

              <div class="hero-card-row">
                <div>
                  <strong>Smart load design</strong>
                  <p class="mini">
                    Manual J/S/D sizing for every project — no “one-size-fits-all” tonnage guesses in Miami humidity.
                  </p>
                </div>
                <div>
                  <strong>Energy savings</strong>
                  <p class="mini">
                    High-SEER heat pumps & variable-speed systems tuned to Florida Power & Light incentives.
                  </p>
                </div>
              </div>

              <div class="hero-card-divider"></div>

              <div class="hero-card-bottom">
                <div class="hero-avatar-row">
                  <div class="hero-avatars">
                    <span></span>
                    <span></span>
                    <span></span>
                  </div>
                  <div class="mini">
                    <strong>120+</strong> units installed in Brickell, Doral & Miami Beach this year.
                  </div>
                </div>
                <div class="hero-card-badge">
                  <span class="badge-dot"></span>
                  Real-time project tracking
                </div>
              </div>
            </div>
          </div>

          <div class="hero-floating">
            <div class="hero-floating-dot"></div>
            <div>
              <span>Condos, single-family & mid-rise builds.</span><br/>
              <strong>Universe Mechanical keeps Miami cold.</strong>
            </div>
          </div>
        </div>
      </div>

      <!-- trust strip -->
      <div class="trust-strip">
        <div>
          <strong>Trusted across Miami’s skyline.</strong> From single-family homes to multi-family projects.
        </div>
        <div class="trust-items">
          <div class="trust-item">
            <div class="trust-badge">FL</div>
            Licensed & Insured
          </div>
          <div class="trust-item">
            <div class="trust-badge">24</div>
            24/7 Emergency Cooling
          </div>
          <div class="trust-item">
            <div class="trust-badge">QC</div>
            QC’d by Lead Mechanic
          </div>
        </div>
      </div>
    </div>

    <!-- SERVICES -->
    <section id="services">
      <div class="container">
        <div class="section-header">
          <div class="section-title-wrap">
            <div class="badge section-badge">
              <span class="badge-dot"></span> A/C Services
            </div>
            <h2 class="section-title">Cooling services built for Miami’s climate.</h2>
            <p class="section-subtitle">
              From late-night no-cool calls to full-system change-outs, we engineer every visit around performance
              and reliability — not just quick fixes.
            </p>
          </div>
          <div class="section-note">
            Need something specific? Describe the issue in the form below and we’ll map the right service tier & technician.
          </div>
        </div>

        <div class="cards-grid">
          <article class="card">
            <div class="card-icon">❄️</div>
            <h3 class="card-title">Diagnostics & Repair</h3>
            <p class="card-text">
              Fast, precise troubleshooting on all major brands — from coastal corrosion to refrigerant issues.
            </p>
            <div class="card-tags">
              <span class="card-tag">Same-day</span>
              <span class="card-tag">All brands</span>
              <span class="card-tag">Transparent pricing</span>
            </div>
            <div class="card-footer">
              <span>Most issues solved in one visit.</span>
              <a href="#contact" class="card-link">
                Book repair <span>↗</span>
              </a>
            </div>
          </article>

          <article class="card">
            <div class="card-icon">🔁</div>
            <h3 class="card-title">System Change-Outs</h3>
            <p class="card-text">
              High-efficiency replacements with proper duct evaluation, line-set practices & permit handling.
            </p>
            <div class="card-tags">
              <span class="card-tag">High-SEER</span>
              <span class="card-tag">Heat pumps</span>
              <span class="card-tag">Financing available</span>
            </div>
            <div class="card-footer">
              <span>Designed for long Miami summers.</span>
              <a href="#contact" class="card-link">
                Request quote <span>↗</span>
              </a>
            </div>
          </article>

          <article class="card">
            <div class="card-icon">🌀</div>
            <h3 class="card-title">Ductless Mini-Splits</h3>
            <p class="card-text">
              Sleek, quiet comfort for condos, garages & additions where traditional ductwork doesn’t make sense.
            </p>
            <div class="card-tags">
              <span class="card-tag">Single & multi-zone</span>
              <span class="card-tag">Inverter tech</span>
            </div>
            <div class="card-footer">
              <span>Perfect for home offices & studios.</span>
              <a href="#contact" class="card-link">
                Design my zones <span>↗</span>
              </a>
            </div>
          </article>

          <article class="card">
            <div class="card-icon">🧪</div>
            <h3 class="card-title">Indoor Air Quality</h3>
            <p class="card-text">
              Filtration, UV lights & dehumidification to handle Miami moisture, allergies & coastal living.
            </p>
            <div class="card-tags">
              <span class="card-tag">Humidity control</span>
              <span class="card-tag">UV & HEPA</span>
            </div>
            <div class="card-footer">
              <span>Better air, better coils, better comfort.</span>
              <a href="#contact" class="card-link">
                IAQ consult <span>↗</span>
              </a>
            </div>
          </article>

          <article class="card">
            <div class="card-icon">📱</div>
            <h3 class="card-title">Smart Thermostats</h3>
            <p class="card-text">
              Wi-Fi thermostats & zoning controls tuned for condos, short-term rentals & busy Miami schedules.
            </p>
            <div class="card-tags">
              <span class="card-tag">Nest & Ecobee</span>
              <span class="card-tag">Energy insights</span>
            </div>
            <div class="card-footer">
              <span>Control your comfort from anywhere.</span>
              <a href="#contact" class="card-link">
                Upgrade controls <span>↗</span>
              </a>
            </div>
          </article>

          <article class="card">
            <div class="card-icon">🛡️</div>
            <h3 class="card-title">Maintenance Memberships</h3>
            <p class="card-text">
              Planned tune-ups, coil cleaning, drain line protection & priority response when Miami heat spikes.
            </p>
            <div class="card-tags">
              <span class="card-tag">Priority service</span>
              <span class="card-tag">Member pricing</span>
            </div>
            <div class="card-footer">
              <span>Protect your system before it fails.</span>
              <a href="#contact" class="card-link">
                Join membership <span>↗</span>
              </a>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- NEW CONSTRUCTION -->
    <section id="new-construction">
      <div class="container">
        <div class="section-header">
          <div class="section-title-wrap">
            <div class="badge section-badge">
              <span class="badge-dot"></span> New Construction
            </div>
            <h2 class="section-title">Mechanical systems for projects that matter.</h2>
            <p class="section-subtitle">
              Universe Mechanical & Air Conditioning Inc. partners with GCs, developers and owners to deliver
              clean, code-tight mechanical systems — from design-assist to final inspection.
            </p>
          </div>
          <div class="section-note">
            Serving single-family, luxury homes, townhomes & mid-rise multifamily across Miami-Dade & Broward.
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
                <div class="timeline-title">Design & Load Calculations</div>
                <p class="timeline-text">
                  Heat-gain calculations (Manual J/S) modeled for Miami’s humidity, glazing, orientation and envelope.
                </p>
                <div class="timeline-chip-row">
                  <span class="timeline-chip">Manual J/S/D</span>
                  <span class="timeline-chip">Duct design</span>
                  <span class="timeline-chip">Equipment schedules</span>
                </div>
              </div>
            </div>

            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">2</div>
                <div class="timeline-line"></div>
              </div>
              <div>
                <div class="timeline-title">Rough-In & Set</div>
                <p class="timeline-text">
                  Clean install, pitched drain lines, strapped duct, sealed air handlers and hurricane-rated pads.
                </p>
                <div class="timeline-chip-row">
                  <span class="timeline-chip">Condensate management</span>
                  <span class="timeline-chip">Inspected supports</span>
                </div>
              </div>
            </div>

            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">3</div>
                <div class="timeline-line"></div>
              </div>
              <div>
                <div class="timeline-title">Startup & Commissioning</div>
                <p class="timeline-text">
                  Charge verification, static pressure testing & control checks documented for your close-out package.
                </p>
                <div class="timeline-chip-row">
                  <span class="timeline-chip">Static pressure</span>
                  <span class="timeline-chip">Refrigerant charge</span>
                  <span class="timeline-chip">Owner training</span>
                </div>
              </div>
            </div>

            <div class="timeline-step">
              <div class="timeline-marker">
                <div class="timeline-badge">4</div>
              </div>
              <div>
                <div class="timeline-title">Warranty & Turnover</div>
                <p class="timeline-text">
                  Builder & homeowner support, documentation and maintenance options to keep your reputation strong.
                </p>
                <div class="timeline-chip-row">
                  <span class="timeline-chip">GC-friendly scheduling</span>
                  <span class="timeline-chip">Post-move-in support</span>
                </div>
              </div>
            </div>
          </div>

          <aside class="construction-right">
            <div class="pill-row">
              <span class="pill">Single-family & luxury customs</span>
              <span class="pill">Townhomes & multifamily</span>
              <span class="pill">Light commercial build-outs</span>
            </div>

            <p class="construction-subtitle">
              One team that understands drawings, inspections and what it takes to pass in Miami-Dade the first time.
            </p>

            <ul class="checklist">
              <li>
                <div class="checkmark">✓</div>
                <div>
                  <strong>Permit-ready submittals.</strong> We help assemble the mechanical portion of your permit package
                  with specs, cutsheets & load calcs.
                </div>
              </li>
              <li>
                <div class="checkmark">✓</div>
                <div>
                  <strong>Schedule-driven installs.</strong> We coordinate with your super to align rough, trim and startup
                  around critical path items.
                </div>
              </li>
              <li>
                <div class="checkmark">✓</div>
                <div>
                  <strong>Post-turnover partnership.</strong> Warranty service that treats your homeowners like our own clients.
                </div>
              </li>
            </ul>

            <div class="construction-footer">
              <div>
                <span>Current capacity:</span><br/>
                <strong>Up to 50+ houses or 200+ units/year.</strong>
              </div>
              <a href="#contact" class="btn btn-primary btn-sm" style="padding: 0.55rem 1.2rem; font-size: 0.8rem;">
                Submit plans
              </a>
            </div>
          </aside>
        </div>
      </div>
    </section>

    <!-- WHY & SERVICE AREA -->
    <section id="why">
      <div class="container">
        <div class="section-header">
          <div class="section-title-wrap">
            <div class="badge section-badge">
              <span class="badge-dot"></span> Why Universe
            </div>
            <h2 class="section-title">Built like a high-end brand, focused on your comfort.</h2>
            <p class="section-subtitle">
              We combine mechanical engineering discipline with hospitality-level customer experience — so every visit
              feels clean, sharp and under control.
            </p>
          </div>
        </div>

        <div class="two-col">
          <div class="stack">
            <div class="feature-row">
              <div class="feature-icon">⚙️</div>
              <div>
                <strong>Engineered – not guessed.</strong>
                <p class="mini">
                  We size and design your system based on actual loads, not rules of thumb — critical in Miami’s humidity
                  where oversizing kills comfort.
                </p>
              </div>
            </div>

            <div class="feature-row">
              <div class="feature-icon">🧼</div>
              <div>
                <strong>Clean, respectful installs.</strong>
                <p class="mini">
                  Drop cloths, shoe covers, organized trucks and post-job cleanups are standard. Your home shouldn’t feel
                  like a job site.
                </p>
              </div>
            </div>

            <div class="feature-row">
              <div class="feature-icon">📊</div>
              <div>
                <strong>Transparent, modern quoting.</strong>
                <p class="mini">
                  Clear options with good/better/best equipment tiers, financing paths and energy savings estimates — no
                  surprise line items.
                </p>
              </div>
            </div>

            <div class="feature-row">
              <div class="feature-icon">📍</div>
              <div>
                <strong>Miami-first expertise.</strong>
                <p class="mini">
                  Salt air, flat roofs, hurricane shutters & older condos each change how systems should be designed.
                  We live and build here too.
                </p>
              </div>
            </div>
          </div>

          <aside class="map-card">
            <div class="map-header">
              <div>
                <div class="map-title">Service Area Coverage</div>
                <div class="mini">Fast response from our Hialeah Gardens hub.</div>
              </div>
              <div class="map-tag">Miami-Dade • Broward</div>
            </div>

            <div class="map-grid">
              <div class="map-pill">
                Miami & Brickell
                <span>Core city</span>
              </div>
              <div class="map-pill">
                Doral & Hialeah
                <span>Shop-adjacent</span>
              </div>
              <div class="map-pill">
                Miami Beach
                <span>Barrier island</span>
              </div>
              <div class="map-pill">
                Kendall & Pinecrest
                <span>South corridor</span>
              </div>
              <div class="map-pill">
                Aventura & North Miami
                <span>NE corridor</span>
              </div>
              <div class="map-pill">
                Hollywood & Pembroke Pines
                <span>Broward south</span>
              </div>
            </div>

            <p class="mini" style="margin-top: 0.8rem;">
              Not sure if you’re in range? Send your address and we’ll confirm response times and scheduling windows.
            </p>
          </aside>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="container">
        <div class="section-header">
          <div class="section-title-wrap">
            <div class="badge section-badge">
              <span class="badge-dot"></span> Book A Visit
            </div>
            <h2 class="section-title">Tell us what’s going on with your A/C.</h2>
            <p class="section-subtitle">
              A dispatcher from Universe Mechanical & Air Conditioning Inc. will review your request and confirm a time
              by text or phone.
            </p>
          </div>
          <div class="section-note">
            For emergencies, call us directly at <strong>(305) 555-0123</strong> — 24/7. We’ll still log the job in our system.
          </div>
        </div>

        <div class="contact-grid">
          <div class="contact-card">
            <form>
              <div class="field-group">
                <div class="field">
                  <label for="name">Full Name</label>
                  <input id="name" type="text" placeholder="Your name" />
                </div>
                <div class="field">
                  <label for="phone">Mobile Phone</label>
                  <input id="phone" type="tel" placeholder="(305) 555-0123" />
                </div>
              </div>

              <div class="field-group">
                <div class="field">
                  <label for="email">Email</label>
                  <input id="email" type="email" placeholder="you@example.com" />
                </div>
                <div class="field">
                  <label for="city">City / Neighborhood</label>
                  <input id="city" type="text" placeholder="Miami, Doral, Kendall..." />
                </div>
              </div>

              <div class="field-group">
                <div class="field">
                  <label for="serviceType">I’m interested in</label>
                  <select id="serviceType">
                    <option>Service / Repair</option>
                    <option>System Replacement</option>
                    <option>New Construction Project</option>
                    <option>Maintenance Membership</option>
                    <option>Indoor Air Quality / Other</option>
                  </select>
                </div>
                <div class="field">
                  <label for="timeframe">Ideal timeframe</label>
                  <select id="timeframe">
                    <option>ASAP (no cooling / emergency)</option>
                    <option>This week</option>
                    <option>Within 30 days</option>
                    <option>Project planning / bidding</option>
                  </select>
                </div>
              </div>

              <div class="field">
                <label for="message">Describe what’s happening</label>
                <textarea id="message" placeholder="Example: 2nd floor not cooling, unit is 8 years old, breaker tripped last night..."></textarea>
              </div>

              <div class="contact-footer">
                <div>
                  By submitting, you agree to be contacted by phone, text or email about your request.
                </div>
                <button type="button" class="btn btn-primary">
                  Send request
                </button>
              </div>
            </form>
          </div>

          <aside class="contact-meta">
            <h4>Need a new construction bid?</h4>
            <p class="mini">
              Email your plans or drawings and we’ll follow up with any mechanical questions before pricing your project.
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
                <strong>Mon–Sat • 8a–7p</strong>
              </div>
            </div>
          </aside>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-row">
      <div>
        © <span id="year"></span> Universe Mechanical & Air Conditioning Inc. All rights reserved.
      </div>
      <div class="footer-links">
        <a href="#home">Home</a>
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
    // Navbar scroll effect
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

    // Mobile nav toggle
    navToggle.addEventListener("click", () => {
      navToggle.classList.toggle("active");
      const isOpen = navMobile.style.display === "block";
      navMobile.style.display = isOpen ? "none" : "block";
    });

    // Close mobile nav on link click
    navMobile.addEventListener("click", (e) => {
      if (e.target.tagName.toLowerCase() === "a") {
        navMobile.style.display = "none";
        navToggle.classList.remove("active");
      }
    });

    // Set current year
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
