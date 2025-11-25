<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Universe Mechanical & Air Conditioning, Inc. — Miami HVAC Contractors</title>
  <meta name="description" content="Universe Mechanical & Air Conditioning, Inc. - Commercial & residential HVAC: new construction, installations, repairs, maintenance, and indoor air quality in Miami." />

  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{--brand:#0d47a1;--brand-dark:#09367c;--accent:#00bcd4;--muted:#6b7280;--radius:12px;--max:1200px}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter,system-ui,Arial;background:#f6fbfc;color:#0b1220}
    a{color:var(--brand);text-decoration:none}

    /* Header / Nav */
    .site-wrap{max-width:var(--max);margin:0 auto;padding:0 18px}
    header.top{display:flex;align-items:center;justify-content:space-between;padding:18px 0}
    header .brand{display:flex;align-items:center;gap:14px}
    header .brand img{height:64px}
    nav.primary{display:flex;gap:18px;align-items:center}
    nav.primary a{padding:8px 12px;border-radius:8px;font-weight:600}
    nav.primary a:hover{background:rgba(13,71,161,0.06)}

    .cta-phone{background:var(--brand);color:white;padding:10px 14px;border-radius:10px;font-weight:700}

    /* Hero */
    .hero{background:linear-gradient(180deg,rgba(13,71,161,0.06),rgba(9,54,124,0.04));border-radius:14px;padding:36px;margin-bottom:20px;display:grid;grid-template-columns:1fr 360px;gap:24px;align-items:center}
    .hero h1{margin:0;font-size:1.9rem;color:var(--brand-dark)}
    .hero p.lead{margin:10px 0;color:#334155}
    .hero .actions{display:flex;gap:12px;margin-top:12px}
    .btn{background:var(--brand);color:white;padding:10px 14px;border-radius:10px;border:none;cursor:pointer;font-weight:700}
    .btn.ghost{background:transparent;border:2px solid var(--brand);color:var(--brand)}

    .quick-card{background:white;padding:18px;border-radius:12px;box-shadow:0 10px 30px rgba(13,71,161,0.06)}

    /* Section headings */
    section{margin-bottom:28px}
    .section-head{display:flex;justify-content:space-between;align-items:center}
    .section-head h2{margin:0;color:var(--brand)}

    /* Services grid */
    .services-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:18px;margin-top:14px}
    .service{background:white;border-radius:10px;padding:14px;box-shadow:0 8px 24px rgba(2,6,23,0.04);border:1px solid rgba(2,6,23,0.04)}
    .service img{width:100%;height:140px;object-fit:cover;border-radius:8px}
    .service h3{margin:10px 0 6px;color:var(--brand)}
    .service p{margin:0;color:var(--muted)}

    /* New construction layout */
    .new-construction{display:grid;grid-template-columns:1fr 420px;gap:18px;align-items:start}
    .proj-list{background:white;padding:18px;border-radius:10px}
    .proj-list li{margin:8px 0}

    /* Testimonials and FAQ */
    .testimonials{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:12px}
    .testimonial{background:white;padding:14px;border-radius:10px}

    /* Contact */
    form.card{background:white;padding:18px;border-radius:10px;display:flex;flex-direction:column;gap:10px}
    input,textarea,select{padding:10px;border-radius:8px;border:1px solid #e6eef6}
    button.form-submit{background:var(--brand);color:white;border:none;padding:12px;border-radius:8px;font-weight:700}

    footer{margin-top:20px;padding:18px 0;background:linear-gradient(90deg,var(--brand),var(--brand-dark));color:white;border-radius:8px}

    @media (max-width:960px){.hero{grid-template-columns:1fr}.new-construction{grid-template-columns:1fr}.site-wrap{padding:0 14px}}
  </style>
</head>
<body>
  <div class="site-wrap">
    <header class="top">
      <div class="brand">
        <img src="/mnt/data/f2dcdb57-0a81-43f4-aff1-3ff4764ccde4.png" alt="Universe Mechanical & Air Conditioning Inc. logo">
        <div>
          <div style="font-weight:800">Universe Mechanical & Air Conditioning, Inc.</div>
          <div style="font-size:0.85rem;color:var(--muted)">Commercial & Residential HVAC • Licensed & Insured</div>
        </div>
      </div>

      <nav class="primary" aria-label="Primary navigation">
        <a href="#home">Home</a>
        <a href="#new-construction">New Construction</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
        <a href="tel:+13055551234" class="cta-phone">(305) 555-1234</a>
      </nav>
    </header>

    <main>
      <!-- Hero -->
      <section id="home" class="hero">
        <div>
          <h1>Miami HVAC experts for new construction, commercial projects, and home comfort.</h1>
          <p class="lead">Universe Mechanical & Air Conditioning designs, installs, and maintains high-performance HVAC systems throughout South Florida. Fast response, transparent pricing, and code-compliant workmanship.</p>

          <div class="actions">
            <button class="btn" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Request Service</button>
            <button class="btn ghost" onclick="document.getElementById('services').scrollIntoView({behavior:'smooth'})">See Services</button>
          </div>

          <div style="display:flex;gap:10px;margin-top:16px">
            <div class="quick-card" style="flex:1">
              <strong>24/7 Emergency Service</strong>
              <div style="color:var(--muted);margin-top:6px">Rapid dispatch for emergencies across Miami-Dade County.</div>
            </div>
            <div class="quick-card" style="width:220px;text-align:center">
              <strong>Financing Available</strong>
              <div style="color:var(--muted);margin-top:6px">Flexible payment options for installations.</div>
            </div>
          </div>
        </div>

        <aside class="quick-card">
          <strong>Get a Free Estimate</strong>
          <form style="margin-top:10px" onsubmit="event.preventDefault();alert('Placeholder: integrate your backend to receive leads.');">
            <input placeholder="Name" required style="width:100%;margin-bottom:8px">
            <input placeholder="Phone" required style="width:100%;margin-bottom:8px">
            <select style="width:100%;margin-bottom:8px">
              <option>Service type</option>
              <option>New Construction</option>
              <option>Installation</option>
              <option>Repair</option>
              <option>Maintenance</option>
            </select>
            <button class="btn" style="width:100%">Request Estimate</button>
          </form>
        </aside>
      </section>

      <!-- New Construction -->
      <section id="new-construction">
        <div class="section-head">
          <h2>New Construction HVAC Services</h2>
          <div style="color:var(--muted)">Design • Install • Commission • Maintain</div>
        </div>

        <div class="new-construction" style="margin-top:14px">
          <div>
            <p style="color:var(--muted)">Universe Mechanical specializes in turnkey HVAC services for new construction and major renovations. We partner with builders, architects, and project managers to deliver systems that meet performance, efficiency, and code requirements.</p>

            <ul class="proj-list">
              <li><strong>System design & load calculation</strong> — ACCA Manual J & D compliant.</li>
              <li><strong>Commercial rooftop units & VRF systems</strong> — large-scale solutions.</li>
              <li><strong>Residential central systems</strong> — high-efficiency splits and heat pumps.</li>
              <li><strong>Controls & building automation</strong> — smart integration for energy savings.</li>
              <li><strong>Permit coordination & inspections</strong> — we handle paperwork and testing.</li>
            </ul>

            <h3 style="color:var(--brand);margin-top:14px">Sample projects</h3>
            <ol style="color:var(--muted)">
              <li>5-story mixed-use development — full HVAC design & rooftop units</li>
              <li>Custom luxury home — ducted multi-zone system with smart thermostat</li>
              <li>Retail center retrofit — system replacement and demand-control ventilation</li>
            </ol>
          </div>

          <aside>
            <img src="https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?auto=format&fit=crop&w=900&q=80" alt="New construction HVAC" style="width:100%;border-radius:10px;object-fit:cover">
            <div style="margin-top:12px;background:white;padding:12px;border-radius:10px;box-shadow:0 8px 20px rgba(2,6,23,0.04)">
              <strong>Why choose us?</strong>
              <p style="margin:8px 0;color:var(--muted)">Licensed technicians, project management experience, and a track record of on-time delivery.</p>
            </div>
          </aside>
        </div>
      </section>

      <!-- Services -->
      <section id="services">
        <div class="section-head">
          <h2>Our Services</h2>
          <div style="color:var(--muted)">Comprehensive HVAC services for homes & businesses</div>
        </div>

        <div class="services-grid" style="margin-top:14px">

          <article class="service">
            <img src="https://images.unsplash.com/photo-1578926378152-2a3a5f8eb5a5?auto=format&fit=crop&w=900&q=80" alt="AC repair">
            <h3>24/7 A/C Repair</h3>
            <p>Rapid diagnostics, transparent pricing, and fully stocked trucks to get systems cooling fast. Emergency response available.</p>
            <p style="margin-top:8px;color:var(--muted)"><strong>Typical response:</strong> same day</p>
          </article>

          <article class="service">
            <img src="https://images.unsplash.com/photo-1581093806997-124204d9b7d3?auto=format&fit=crop&w=900&q=80" alt="New installs">
            <h3>New System Installation</h3>
            <p>Proper equipment sizing (Manual J), professional installation, and system commissioning to ensure efficient operation and warranty compliance.</p>
            <p style="margin-top:8px;color:var(--muted)"><strong>Brands:</strong> Carrier, Trane, Lennox, Mitsubishi</p>
          </article>

          <article class="service">
            <img src="https://images.unsplash.com/photo-1597003555553-8c2cc74f36bb?auto=format&fit=crop&w=900&q=80" alt="maintenance">
            <h3>Maintenance Plans</h3>
            <p>Seasonal tune-ups reduce breakdowns and improve efficiency. Membership options include priority scheduling and discounts on repairs.</p>
            <p style="margin-top:8px;color:var(--muted)"><strong>Includes:</strong> coil cleaning, refrigerant check, filter change, safety inspection.</p>
          </article>

          <article class="service">
            <img src="https://images.unsplash.com/photo-1560448204-e02f11c3d0e2?auto=format&fit=crop&w=900&q=80" alt="duct cleaning">
            <h3>Duct Cleaning & IAQ</h3>
            <p>Improve indoor air quality with professional duct cleaning, UV lights, and high-efficiency filtration upgrades.</p>
            <p style="margin-top:8px;color:var(--muted)"><strong>Benefits:</strong> better airflow, fewer allergens, longer equipment life.</p>
          </article>

          <article class="service">
            <img src="https://images.unsplash.com/photo-1509395176047-4a66953fd231?auto=format&fit=crop&w=900&q=80" alt="controls">
            <h3>Controls & Smart Thermostats</h3>
            <p>Smart thermostats and building controls that reduce energy use and give you remote control over comfort settings.</p>
          </article>

        </div>

        <div style="margin-top:18px;display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px">
          <div class="quick-card">
            <strong>Licensed & Insured</strong>
            <div style="color:var(--muted);margin-top:6px">EPA-certified technicians and full liability coverage.</div>
          </div>
          <div class="quick-card">
            <strong>Transparent Pricing</strong>
            <div style="color:var(--muted);margin-top:6px">Clear estimates and no surprise fees.</div>
          </div>
          <div class="quick-card">
            <strong>Maintenance Plans</strong>
            <div style="color:var(--muted);margin-top:6px">Keep systems efficient with seasonal visits.</div>
          </div>
        </div>

      </section>

      <!-- Testimonials + FAQ + Contact -->
      <section style="display:grid;grid-template-columns:1fr 360px;gap:18px;align-items:start">
        <div>
          <div class="section-head">
            <h2>Customer Stories</h2>
            <div style="color:var(--muted)">Trusted by homeowners and contractors</div>
          </div>

          <div class="testimonials" style="margin-top:12px">
            <div class="testimonial">
              <strong>Maria G. — Coral Gables</strong>
              <div style="color:var(--muted);margin-top:6px">"They fixed our AC the same day and were so professional. Transparent pricing and clean work — highly recommend!"</div>
            </div>
            <div class="testimonial">
              <strong>Anthony R. — Miami Beach</strong>
              <div style="color:var(--muted);margin-top:6px">"Installed a new energy-efficient system and saved us on monthly bills. Great crew and quick turnaround."</div>
            </div>
            <div class="testimonial">
              <strong>Jessie L. — Little Havana</strong>
              <div style="color:var(--muted);margin-top:6px">"Friendly tech, showed me what was wrong and explained options. I signed up for the maintenance plan."</div>
            </div>
          </div>

          <div style="margin-top:18px">
            <h3 style="color:var(--brand)">FAQ</h3>
            <details style="margin-top:8px"><summary><strong>Do you offer emergency service?</strong></summary><p style="color:var(--muted)">Yes — 24/7 emergency dispatch across Miami-Dade County.</p></details>
            <details style="margin-top:6px"><summary><strong>How often should I service my A/C?</strong></summary><p style="color:var(--muted)">We recommend two seasonal tune-ups per year; heavy-use properties may need more frequent checks.</p></details>
            <details style="margin-top:6px"><summary><strong>Do you handle permits?</strong></summary><p style="color:var(--muted)">Yes — for new construction and major replacements we handle permit coordination and inspections.</p></details>
          </div>
        </div>

        <aside>
          <div class="quick-card">
            <h3 id="contact">Request Service</h3>
            <form class="card" onsubmit="handleSubmit(event)">
              <input name="name" placeholder="Full name" required>
              <input name="phone" placeholder="Phone" required>
              <input name="email" placeholder="Email (optional)">
              <select name="service">
                <option>Emergency Repair</option>
                <option>New Installation</option>
                <option>Maintenance</option>
                <option>Duct Cleaning</option>
                <option>New Construction Consultation</option>
              </select>
              <textarea name="message" rows="3" placeholder="Describe the issue or project (optional)"></textarea>
              <button class="form-submit" type="submit">Send Request</button>
              <div style="color:var(--muted);margin-top:8px">Or call <strong>(305) 555-1234</strong></div>
            </form>
          </div>

          <div style="margin-top:12px;background:white;padding:12px;border-radius:10px;box-shadow:0 8px 20px rgba(2,6,23,0.04)">
            <strong>Service Area</strong>
            <div style="color:var(--muted);margin-top:6px">Miami • Miami Beach • Coral Gables • Hialeah • Doral • Kendall</div>
          </div>
        </aside>
      </section>

    </main>

    <footer>
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;max-width:var(--max);margin:0 auto">
        <div>
          <div style="font-weight:700">Universe Mechanical & Air Conditioning, Inc.</div>
          <div style="color:rgba(255,255,255,0.92)">Licensed & Insured • EPA Certified</div>
        </div>
        <div style="text-align:right">
          <div style="font-weight:700">(305) 555-1234</div>
          <div style="color:rgba(255,255,255,0.92)">info@universe-mech.example</div>
        </div>
      </div>
    </footer>

  </div>

  <script>
    function handleSubmit(e){
      e.preventDefault();
      const form = e.target;
      const fd = new FormData(form);
      const name = fd.get('name');
      const phone = fd.get('phone');
      alert(`Thanks ${name}! We received your request and will call ${phone} shortly. (Placeholder)`);
      form.reset();
      location.hash = '#contact';
    }
  </script>

  <script type="application/ld+json">
  {
    "@context":"https://schema.org",
    "@type":"HVACBusiness",
    "name":"Universe Mechanical & Air Conditioning, Inc.",
    "telephone":"+1-305-555-1234",
    "address":{ "@type":"PostalAddress", "addressLocality":"Miami", "addressRegion":"FL" },
    "description":"Commercial and residential HVAC services including new construction, installs, repairs, and maintenance in Miami-Dade County."
  }
  </script>

</body>
</html>

