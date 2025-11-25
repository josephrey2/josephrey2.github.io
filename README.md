<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Universe Services — Miami A/C Experts | Repair • Installation • Maintenance</title>
  <meta name="description" content="Universe Services — Miami's trusted HVAC company. Fast A/C repair, energy-efficient installations, duct cleaning, and maintenance plans. 24/7 emergency service." />
  <meta name="theme-color" content="#0d47a1" />

  <!-- Open Graph -->
  <meta property="og:title" content="Universe Services — Miami A/C Experts" />
  <meta property="og:description" content="Fast, reliable A/C repair, installation and maintenance in Miami. 24/7 emergency service and affordable maintenance plans." />
  <meta property="og:image" content="https://images.unsplash.com/photo-1581093448799-ecf9c7c8e1f0?auto=format&fit=crop&w=1200&q=80" />
  <meta property="og:type" content="website" />

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --brand:#0d47a1;
      --brand-dark:#09367c;
      --accent:#00bcd4;
      --muted:#6b7280;
      --radius:12px;
      --container:1200px;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
      color:#111827;
      background:linear-gradient(180deg,#f6fbfc 0%, #eef6f9 100%);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
    }

    /* Top bar */
    .topbar{
      background:var(--brand);
      color:white;
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:10px 20px;
    }
    .topbar .contact{font-weight:600}
    .topbar a{color:white; text-decoration:none}

    header.hero{
      background-image:linear-gradient(rgba(13,71,161,0.6), rgba(9,54,124,0.55)), url('https://images.unsplash.com/photo-1581093448799-ecf9c7c8e1f0?auto=format&fit=crop&w=1800&q=80');
      background-size:cover;
      background-position:center center;
      color:white;
      padding:72px 20px;
      text-align:left;
    }
    .wrap{max-width:var(--container);margin:0 auto}
    .hero-grid{display:grid;grid-template-columns:1fr 380px;gap:30px;align-items:center}

    .brand{display:flex;gap:14px;align-items:center}
    .logo{
      width:64px;height:64px;border-radius:14px;background:white;display:flex;align-items:center;justify-content:center;box-shadow:0 8px 20px rgba(13,71,161,0.18)
    }
    .logo svg{width:36px;height:36px}

    h1{font-size:2.25rem;margin:0 0 10px 0;line-height:1.05}
    p.lead{font-size:1.05rem;margin:0;color:rgba(255,255,255,0.95)}

    .cta {
      margin-top:18px;
      display:flex;gap:12px;flex-wrap:wrap
    }
    .btn{background:var(--accent);border:none;color:#042331;padding:12px 18px;border-radius:10px;font-weight:700;cursor:pointer}
    .btn.secondary{background:transparent;border:2px solid rgba(255,255,255,0.18);color:white}

    .card-cta{background:linear-gradient(180deg, rgba(255,255,255,0.06), rgba(255,255,255,0.02));padding:18px;border-radius:12px}
    .quick-info{display:flex;flex-direction:column;gap:10px}
    .quick-info .item{display:flex;gap:12px;align-items:center}
    .chip{display:inline-flex;align-items:center;gap:8px;background:rgba(255,255,255,0.08);padding:8px 10px;border-radius:999px}

    main{padding:40px 20px}

    /* Services */
    .section-head{display:flex;align-items:center;justify-content:space-between;gap:20px}
    h2{color:var(--brand);font-size:1.5rem;margin:0}

    .services-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:22px;margin-top:18px}
    .service{background:white;padding:18px;border-radius:12px;box-shadow:0 8px 24px rgba(16,24,40,0.06);border:1px solid rgba(15,23,42,0.03)}
    .service img{width:100%;height:140px;object-fit:cover;border-radius:8px;margin-bottom:12px}
    .service h3{margin:0 0 8px 0;color:var(--brand)}
    .service p{margin:0;color:var(--muted)}

    /* Benefits bar */
    .benefits{display:flex;gap:18px;flex-wrap:wrap;margin-top:28px}
    .benefit{background:white;padding:14px;border-radius:10px;display:flex;gap:12px;align-items:center;box-shadow:0 6px 16px rgba(13,71,161,0.04)}

    /* Testimonials */
    .testimonials{margin-top:34px}
    .testimonial-list{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:16px}
    .testimonial{background:white;padding:16px;border-radius:12px;box-shadow:0 6px 18px rgba(2,6,23,0.06)}
    .stars{color:#f59e0b}

    /* FAQ & footer grid */
    .two-col{display:grid;grid-template-columns:1fr 420px;gap:24px;margin-top:30px}
    .faq{background:white;padding:20px;border-radius:12px}

    .map-placeholder{border-radius:12px;overflow:hidden;border:1px solid rgba(2,6,23,0.06)}

    /* Contact form */
    form.card{background:white;padding:18px;border-radius:12px;box-shadow:0 8px 24px rgba(2,6,23,0.06);display:flex;flex-direction:column;gap:12px}
    input, textarea, select{padding:12px;border-radius:8px;border:1px solid #e6eef6;font-size:0.95rem}
    button.form-submit{background:var(--brand);color:white;padding:12px;border-radius:10px;border:none;font-weight:700;cursor:pointer}

    footer{margin-top:40px;padding:26px 20px;background:linear-gradient(90deg,var(--brand),var(--brand-dark));color:white}
    .footer-grid{max-width:var(--container);margin:0 auto;display:flex;justify-content:space-between;gap:18px;align-items:center}

    /* Responsive */
    @media (max-width:900px){
      .hero-grid{grid-template-columns:1fr}
      .two-col{grid-template-columns:1fr}
    }
  </style>
</head>
<body>

  <div class="topbar" role="banner">
    <div class="wrap" style="display:flex;align-items:center;justify-content:space-between;gap:12px">
      <div style="display:flex;align-items:center;gap:12px">
        <div class="logo" aria-hidden="true">
          <!-- simple AC / snowflake icon -->
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
            <path d="M12 2v20" stroke="#0d47a1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M20 6l-8 6-8-6 8 6v8" stroke="#0d47a1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div style="line-height:1">
          <div style="font-weight:700">Universe Services</div>
          <div style="font-size:0.8rem;color:rgba(255,255,255,0.9)">Miami A/C Repair & Installation</div>
        </div>
      </div>

      <div class="contact">
        <span style="margin-right:14px;font-weight:600">24/7 Emergency: (305) 555-1234</span>
        <a href="#contact" style="background:rgba(255,255,255,0.12);padding:8px 10px;border-radius:8px">Request Service</a>
      </div>
    </div>
  </div>

  <header class="hero" role="region" aria-label="Hero">
    <div class="wrap">
      <div class="hero-grid">

        <div>
          <div class="brand">
            <div class="logo" style="background:white"><svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12 2v20" stroke="#0d47a1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/><path d="M20 6l-8 6-8-6 8 6v8" stroke="#0d47a1" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg></div>
            <div>
              <div style="font-weight:800;font-size:1rem">Universe Services</div>
              <div style="font-size:0.85rem;opacity:0.95">Licensed • Insured • EPA-Certified Technicians</div>
            </div>
          </div>

          <h1>Fast A/C repair, energy-smart installations, and maintenance plans — Miami's trusted team.</h1>
          <p class="lead">Same-day service available. Transparent pricing, family-owned, and ready for emergency calls 24/7.</p>

          <div class="cta">
            <button class="btn" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Request Service</button>
            <a class="btn secondary" href="#services">View Services</a>
            <span style="align-self:center;color:rgba(255,255,255,0.9);font-weight:600">Free estimates • Financing available</span>
          </div>
        </div>

        <aside class="card-cta">
          <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:12px">
            <strong>Get a Fast Quote</strong>
            <small style="color:rgba(255,255,255,0.95)">Avg. response: <strong>15 min</strong></small>
          </div>

          <form onsubmit="event.preventDefault();alert('Thanks! This is a placeholder form — integrate your backend or replace with mailto.');" aria-label="Quick quote form">
            <input name="name" placeholder="Full name" style="width:100%;padding:10px;border-radius:8px;border:none;margin-bottom:8px" required>
            <input name="phone" placeholder="Phone" style="width:100%;padding:10px;border-radius:8px;border:none;margin-bottom:8px" required>
            <select name="service" style="width:100%;padding:10px;border-radius:8px;border:none;margin-bottom:8px">
              <option>-- Select Service --</option>
              <option>Emergency Repair</option>
              <option>New Installation</option>
              <option>Maintenance Plan</option>
              <option>Duct Cleaning</option>
            </select>
            <button type="submit" class="btn" style="width:100%">Get Quote</button>
          </form>

          <div style="margin-top:14px;font-size:0.9rem;color:rgba(255,255,255,0.95)">
            <div class="chip">🔧 Licensed technicians</div>
            <div style="height:8px"></div>
            <div class="chip">🕒 24/7 Emergency</div>
          </div>
        </aside>

      </div>
    </div>
  </header>

  <main class="wrap">

    <section aria-labelledby="services-heading">
      <div class="section-head">
        <h2 id="services-heading">Services We Offer</h2>
        <div style="color:var(--muted);font-size:0.95rem">Serving all of Miami-Dade County • Residential & Commercial</div>
      </div>

      <div class="services-grid" id="services">

        <article class="service" aria-labelledby="s1">
          <img src="https://images.unsplash.com/photo-1578926378152-2a3a5f8eb5a5?auto=format&fit=crop&w=900&q=80" alt="Technician repairing an AC unit">
          <h3 id="s1">24/7 A/C Repair</h3>
          <p>Fast diagnostics and repair for all major brands. We stock common parts to get your system cooling again quickly.</p>
        </article>

        <article class="service" aria-labelledby="s2">
          <img src="https://images.unsplash.com/photo-1581093806997-124204d9b7d3?auto=format&fit=crop&w=900&q=80" alt="Installation of a new energy efficient AC unit">
          <h3 id="s2">New System Installation</h3>
          <p>Energy-efficient systems sized for your home or business. We handle permits and full-system commissioning.</p>
        </article>

        <article class="service" aria-labelledby="s3">
          <img src="https://images.unsplash.com/photo-1597003555553-8c2cc74f36bb?auto=format&fit=crop&w=900&q=80" alt="Routine maintenance checklist">
          <h3 id="s3">Maintenance Plans</h3>
          <p>Keep your A/C running efficiently year-round with seasonal tune-ups and priority scheduling for members.</p>
        </article>

        <article class="service" aria-labelledby="s4">
          <img src="https://images.unsplash.com/photo-1560448204-e02f11c3d0e2?auto=format&fit=crop&w=900&q=80" alt="Duct cleaning">
          <h3 id="s4">Duct Cleaning & Indoor Air Quality</h3>
          <p>Improve airflow and reduce allergens with professional duct cleaning and UV/filtration upgrades.</p>
        </article>

        <article class="service" aria-labelledby="s5">
          <img src="https://images.unsplash.com/photo-1509395176047-4a66953fd231?auto=format&fit=crop&w=900&q=80" alt="Smart thermostat installation">
          <h3 id="s5">Smart Thermostats & Controls</h3>
          <p>Upgrade to smart thermostats to save energy and control comfort from your phone.</p>
        </article>

      </div>

      <div class="benefits">
        <div class="benefit"><strong>✅ Licensed & Insured</strong><div style="color:var(--muted)">EPA & local certified</div></div>
        <div class="benefit"><strong>⏱️ Fast Response</strong><div style="color:var(--muted)">Same-day available</div></div>
        <div class="benefit"><strong>💳 Financing</strong><div style="color:var(--muted)">Flexible payment plans</div></div>
        <div class="benefit"><strong>🔁 Maintenance Plans</strong><div style="color:var(--muted)">Priority scheduling</div></div>
      </div>

    </section>

    <section class="testimonials" aria-labelledby="testimonials-heading">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <h2 id="testimonials-heading">What Our Customers Say</h2>
        <div style="color:var(--muted);font-size:0.95rem">Real reviews from Miami homeowners</div>
      </div>

      <div class="testimonial-list">
        <blockquote class="testimonial">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <strong>Maria G. — Coral Gables</strong>
            <div class="stars">★★★★★</div>
          </div>
          <p style="margin-top:8px;color:var(--muted)">"They fixed our AC the same day and were so professional. Transparent pricing and clean work — highly recommend!"</p>
        </blockquote>

        <blockquote class="testimonial">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <strong>Anthony R. — Miami Beach</strong>
            <div class="stars">★★★★★</div>
          </div>
          <p style="margin-top:8px;color:var(--muted)">"Installed a new energy-efficient system and saved us on monthly bills. Great crew and quick turnaround."</p>
        </blockquote>

        <blockquote class="testimonial">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <strong>Jessie L. — Little Havana</strong>
            <div class="stars">★★★★★</div>
          </div>
          <p style="margin-top:8px;color:var(--muted)">"Friendly tech, showed me what was wrong and explained options. I signed up for the maintenance plan."</p>
        </blockquote>
      </div>
    </section>

    <div class="two-col" style="margin-top:34px">

      <section class="faq" aria-labelledby="faq-heading">
        <h2 id="faq-heading">Frequently Asked Questions</h2>
        <details style="margin-top:12px"><summary><strong>Do you offer emergency service?</strong></summary><p style="color:var(--muted)">Yes — we offer 24/7 emergency repair with rapid dispatch across Miami-Dade County.</p></details>
        <details style="margin-top:8px"><summary><strong>How often should I service my A/C?</strong></summary><p style="color:var(--muted)">We recommend seasonal tune-ups at least twice a year. For heavy use, quarterly inspections help maintain efficiency.</p></details>
        <details style="margin-top:8px"><summary><strong>Do you provide estimates?</strong></summary><p style="color:var(--muted)">Yes — free on-site estimates for installs and transparent diagnostic pricing for repairs.</p></details>

        <h3 style="margin-top:16px;color:var(--brand)">Our Service Area</h3>
        <p style="color:var(--muted);margin-top:6px">Miami • Miami Beach • Coral Gables • Little Havana • Hialeah • Doral • Kendall and surrounding neighborhoods.</p>
      </section>

      <aside>
        <div class="map-placeholder">
          <!-- Placeholder map: swap with your Google Maps iframe or static image -->
          <img src="https://images.unsplash.com/photo-1501594907352-04cda38ebc29?auto=format&fit=crop&w=1200&q=80" alt="Map placeholder" style="width:100%;height:100%;object-fit:cover">
        </div>

        <div style="margin-top:16px">
          <form id="contact" class="card" onsubmit="handleSubmit(event)">
            <h3 style="margin:0 0 4px 0">Request Service</h3>
            <small style="color:var(--muted)">Fill the form and we’ll call you to confirm.</small>
            <input type="text" name="name" placeholder="Full name" required>
            <input type="tel" name="phone" placeholder="Phone (e.g. 305-555-1234)" required>
            <input type="email" name="email" placeholder="Email (optional)">
            <select name="service">
              <option>Emergency Repair</option>
              <option>System Installation</option>
              <option>Maintenance</option>
              <option>Duct Cleaning</option>
            </select>
            <textarea name="message" rows="4" placeholder="Describe the issue or request (optional)"></textarea>
            <button class="form-submit" type="submit">Send Request</button>
            <small style="color:var(--muted);margin-top:6px">Or call: <strong>(305) 555-1234</strong></small>
          </form>
        </div>
      </aside>

    </div>

  </main>

  <footer>
    <div class="footer-grid wrap">
      <div>
        <div style="font-weight:700">Universe Services</div>
        <div style="font-size:0.9rem;color:rgba(255,255,255,0.92)">Licensed & Insured • EPA Certified</div>
      </div>

      <div style="text-align:right">
        <div style="font-weight:700">(305) 555-1234</div>
        <div style="font-size:0.9rem;color:rgba(255,255,255,0.95)">info@universe-services.example</div>
      </div>
    </div>
  </footer>

  <script>
    // Placeholder form handler — replace with real integration (email API / backend)
    function handleSubmit(e){
      e.preventDefault();
      const form = e.target;
      const data = new FormData(form);
      const name = data.get('name');
      const phone = data.get('phone');
      alert(`Thanks ${name}! We received your request and will call ${phone} shortly. (This is a placeholder alert.)`);
      form.reset();
      window.location.hash = '#contact';
    }

    // Simple accessibility enhancement: focus outline for keyboard users only
    (function(){
      function handleFirstTab(e){
        if(e.key === 'Tab'){
          document.body.classList.add('user-is-tabbing');
          window.removeEventListener('keydown', handleFirstTab);
        }
      }
      window.addEventListener('keydown', handleFirstTab);
    })();
  </script>

  <!-- JSON-LD structured data for SEO -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "HVACBusiness",
    "name": "Universe Services",
    "url": "https://your-github-username.github.io/universe-services/",
    "telephone": "+1-305-555-1234",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Miami",
      "addressRegion": "FL",
      "postalCode": "33101",
      "streetAddress": "Miami, FL (service area)"
    },
    "description": "A/C repair, installation, and maintenance services serving Miami-Dade County.",
    "areaServed": "Miami-Dade County"
  }
  </script>

</body>
</html>

