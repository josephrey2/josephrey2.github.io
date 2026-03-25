diff --git a/index.html b/index.html
index e17054743f1fe591c43a3d93859987d0274dc950..def8ef1df58f9da3e293603164889a3d5ee742b9 100644
--- a/index.html
+++ b/index.html
@@ -20,50 +20,64 @@
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
 
+    .skip-link {
+      position: absolute;
+      left: -999px;
+      top: 0;
+      z-index: 100;
+      background: #fff;
+      color: var(--blue-dark);
+      padding: .6rem .9rem;
+      border-radius: 0 0 8px 8px;
+      font-weight: 600;
+    }
+
+    .skip-link:focus { left: 1rem; }
+
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
@@ -1236,197 +1250,144 @@
       .process-grid {
         grid-template-columns: repeat(2, 1fr);
         gap: 2rem;
       }
 
       .process-grid::before { display: none; }
     }
 
     @media (max-width: 768px) {
       /* ── Navbar ── */
       .nav-links, .nav-right { display: none; }
       .nav-toggle { display: inline-flex; }
       .navbar-inner { height: 56px; }
       .logo-img { height: 50px !important; }
 
       /* Scroll anchor offset matches new navbar height */
       html { scroll-padding-top: 72px; }
 
       .hero-inner {
         padding-top: 130px;
         padding-bottom: 60px;
       }
       .hero-headline { font-size: 2.2rem; }
       .hero-grid { gap: 2rem; }
 
-      /* Hide thermostat on mobile */
-      #thermostat { display: none !important; }
-
       /* Glance panel */
       .glance-panel { max-width: 100%; padding: 1.4rem 1.2rem; }
       .glance-stats > div { padding: .65rem .75rem; }
 
       /* Trust bar — vertical stack, clean and readable */
       .hero-trust {
         width: 100%;
         border-radius: 12px;
         flex-direction: column;
       }
       .hero-trust-item {
         flex: none;
         justify-content: flex-start;
         padding: .7rem 1rem;
         border-right: none;
         border-bottom: 1px solid rgba(255,255,255,.12);
         font-size: .84rem;
         gap: .5rem;
       }
       .hero-trust-item:last-child { border-bottom: none; }
 
       /* Services */
       .services-grid { grid-template-columns: 1fr; }
 
       /* Process */
       .process-grid { grid-template-columns: 1fr; gap: 1.8rem; }
 
       /* About */
       .about-layout { grid-template-columns: 1fr; }
 
       /* Contact */
       .field-row { flex-direction: column; }
       .contact-layout { grid-template-columns: 1fr; }
 
       /* General spacing */
       section, #about, #services, #contact { padding: 60px 0; }
       .process-strip { padding: 60px 0; }
       .container { padding: 0 1.2rem; }
     }
 
     @media (max-width: 480px) {
       .hero-headline { font-size: 1.85rem; }
       .glance-stats { grid-template-columns: 1fr 1fr; }
     }
   </style>
 </head>
 <body>
+  <a href="#home" class="skip-link">Skip to content</a>
 
   <!-- ─── NAVBAR ──────────────────────────────── -->
   <header class="navbar" id="navbar">
     <div class="container navbar-inner">
       <a href="#home" class="nav-logo">
         <img src="Universe Services Logo White.png" alt="Universe Services logo" class="logo-img" style="height:145px;" />
       </a>
 
-      <nav class="nav-links">
+      <nav class="nav-links" aria-label="Primary">
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
 
-      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation">
+      <button class="nav-toggle" id="navToggle" aria-label="Toggle navigation" aria-expanded="false" aria-controls="navMobile">
         <div class="hamburger">
           <span></span><span></span><span></span>
         </div>
       </button>
     </div>
   </header>
 
   <!-- Mobile nav dropdown — sits outside header to avoid any clipping -->
-  <div class="nav-mobile" id="navMobile">
+  <div class="nav-mobile" id="navMobile" aria-label="Mobile">
     <div class="nav-mobile-inner container">
       <a href="#home">Home</a>
       <a href="#about">About</a>
       <a href="#services">Services</a>
       <a href="#contact">Contact</a>
       <a href="tel:+13055550123" style="color:#7dd3fc;font-weight:600;">📞 (305) 555-0123</a>
     </div>
   </div>
 
   <main id="home">
 
     <!-- ─── HERO ─────────────────────────────── -->
     <section class="hero">
       <div class="hero-overlay"></div>
-      <canvas id="snowCanvas" style="position:absolute;top:0;left:0;width:100%;height:100%;z-index:3;pointer-events:none;display:block;"></canvas>
-      <!-- Thermostat widget -->
-      <div id="thermostat" style="
-        position:absolute;
-        bottom:2.5rem;
-        right:2.5rem;
-        z-index:6;
-        width:110px;
-        background:rgba(10,30,80,.35);
-        border:1px solid rgba(255,255,255,.22);
-        border-radius:20px;
-        padding:1rem .85rem 1.1rem;
-        backdrop-filter:blur(16px);
-        -webkit-backdrop-filter:blur(16px);
-        text-align:center;
-        pointer-events:none;
-        box-shadow:0 8px 32px rgba(0,10,40,.4), inset 0 1px 0 rgba(255,255,255,.15);
-      ">
-        <div style="font-size:.6rem;letter-spacing:.18em;text-transform:uppercase;color:rgba(255,255,255,.6);margin-bottom:.5rem;">TEMPERATURE</div>
-        <svg viewBox="0 0 60 105" width="50" style="display:block;margin:0 auto .7rem;overflow:visible;" id="thermoSvg">
-          <defs>
-            <clipPath id="tubeClip">
-              <rect x="24" y="10" width="12" height="68" rx="6"/>
-            </clipPath>
-          </defs>
-          <!-- Tube background (empty) -->
-          <rect x="24" y="10" width="12" height="68" rx="6"
-                fill="rgba(255,255,255,.1)" stroke="rgba(255,255,255,.4)" stroke-width="1.5"/>
-          <!-- Mercury fill — clipped to tube, grows/shrinks via JS -->
-          <rect id="mercury" x="24" y="20" width="12" height="58" rx="4"
-                fill="#7dd3fc" clip-path="url(#tubeClip)"/>
-          <!-- Tick marks on right -->
-          <line x1="36" y1="18" x2="42" y2="18" stroke="rgba(255,255,255,.5)" stroke-width="1.2"/>
-          <line x1="36" y1="29" x2="40" y2="29" stroke="rgba(255,255,255,.35)" stroke-width="1"/>
-          <line x1="36" y1="40" x2="42" y2="40" stroke="rgba(255,255,255,.5)" stroke-width="1.2"/>
-          <line x1="36" y1="51" x2="40" y2="51" stroke="rgba(255,255,255,.35)" stroke-width="1"/>
-          <line x1="36" y1="62" x2="42" y2="62" stroke="rgba(255,255,255,.5)" stroke-width="1.2"/>
-          <line x1="36" y1="73" x2="40" y2="73" stroke="rgba(255,255,255,.35)" stroke-width="1"/>
-          <!-- Tube glass shine -->
-          <rect x="26" y="13" width="3" height="58" rx="2" fill="rgba(255,255,255,.18)"/>
-          <!-- Bulb outer -->
-          <circle id="thermoBulb" cx="30" cy="89" r="11"
-                  fill="#7dd3fc" stroke="rgba(255,255,255,.4)" stroke-width="1.5"/>
-          <!-- Bulb inner shine -->
-          <circle cx="26" cy="85" r="3" fill="rgba(255,255,255,.35)"/>
-        </svg>
-        <div id="thermoTemp" style="font-family:'DM Serif Display',Georgia,serif;font-size:1.6rem;color:#fff;line-height:1;margin-bottom:.15rem;">78°</div>
-        <div style="font-size:.58rem;letter-spacing:.1em;text-transform:uppercase;color:rgba(255,255,255,.55);">Cooling down</div>
-        <!-- Snowflake accents -->
-        <div style="font-size:.9rem;margin-top:.5rem;letter-spacing:.2rem;color:rgba(255,255,255,.5);">❄ ❄ ❄</div>
-      </div>
 
       <div class="container hero-inner">
         <div class="hero-grid">
           <div>
             <div class="hero-tag">Mechanical Contractor</div>
 
             <h1 class="hero-headline">
               Air Conditioning
               <em>Done Right.</em>
             </h1>
 
             <p class="hero-sub">
               South Florida's family-owned HVAC company. We show up, communicate clearly, and get the job done right.
             </p>
 
             <div class="hero-actions">
               <a href="#contact" class="btn btn-primary">Request Service</a>
               <a href="tel:+13055550123" class="btn btn-ghost">📞 Call Us Now</a>
             </div>
 
 
           </div>
 
           <aside class="glance-panel">
             <div class="glance-title">Universe at a Glance</div>
@@ -1586,306 +1547,181 @@
             <div class="process-num">3</div>
             <div class="process-step-title">Repair or Replace</div>
             <p class="process-step-text">We complete the work cleanly and efficiently, respecting your home and your schedule.</p>
           </div>
           <div class="process-step">
             <div class="process-num">4</div>
             <div class="process-step-title">Stay Supported</div>
             <p class="process-step-text">We're available after the job is done. Call us anytime if something comes up.</p>
           </div>
         </div>
       </div>
     </div>
 
     <!-- ─── CONTACT ───────────────────────────── -->
     <section id="contact">
       <div class="container">
         <div class="eyebrow">Contact</div>
         <h2 class="section-title" style="margin-bottom:.5rem;">Tell us what you need.</h2>
         <p class="section-sub" style="margin-bottom:2.5rem;">Fill out the form and someone from our team will follow up shortly.</p>
 
         <div class="contact-layout">
           <div class="contact-form-card">
             <div class="form-title">Request Service</div>
             <p class="form-sub">For urgent no-cool calls, please call <strong>(305) 555-0123</strong> directly.</p>
 
-            <form>
+            <form action="mailto:info@universeservicesfl.com" method="post" enctype="text/plain">
               <div class="field-row">
                 <div class="field">
                   <label for="name">Full Name</label>
-                  <input id="name" type="text" placeholder="Your name" />
+                  <input id="name" name="name" type="text" placeholder="Your name" required />
                 </div>
                 <div class="field">
                   <label for="phone">Mobile Phone</label>
-                  <input id="phone" type="tel" placeholder="(305) 555-0123" />
+                  <input id="phone" name="phone" type="tel" placeholder="(305) 555-0123" required />
                 </div>
               </div>
 
               <div class="field-row">
                 <div class="field">
                   <label for="email">Email</label>
-                  <input id="email" type="email" placeholder="you@example.com" />
+                  <input id="email" name="email" type="email" placeholder="you@example.com" required />
                 </div>
                 <div class="field">
                   <label for="city">City / Neighborhood</label>
-                  <input id="city" type="text" placeholder="Miami, Doral, Kendall…" />
+                  <input id="city" name="city" type="text" placeholder="Miami, Doral, Kendall…" />
                 </div>
               </div>
 
               <div class="field-row">
                 <div class="field">
                   <label for="serviceType">I'm Reaching Out About</label>
-                  <select id="serviceType">
+                  <select id="serviceType" name="service_type">
                     <option>Service / repair</option>
                     <option>System replacement</option>
                     <option>Controls / smart thermostat</option>
                     <option>Maintenance program</option>
                     <option>Other A/C need</option>
                   </select>
                 </div>
                 <div class="field">
                   <label for="timeframe">Ideal Timeframe</label>
-                  <select id="timeframe">
+                  <select id="timeframe" name="timeframe">
                     <option>ASAP / emergency</option>
                     <option>This week</option>
                     <option>Within 30 days</option>
                     <option>Planning / budgeting</option>
                   </select>
                 </div>
               </div>
 
               <div class="field">
                 <label for="message">Describe the Issue or Request</label>
-                <textarea id="message" placeholder="E.g. 2nd floor not cooling, system is 15 years old, looking for a maintenance plan, etc."></textarea>
+                <textarea id="message" name="message" placeholder="E.g. 2nd floor not cooling, system is 15 years old, looking for a maintenance plan, etc." required></textarea>
               </div>
 
               <div class="form-footer">
-                <button type="button" class="btn btn-primary" style="width:100%;justify-content:center;padding:.75rem 1.5rem;font-size:.88rem;">Submit Request</button>
+                <button type="submit" class="btn btn-primary" style="width:100%;justify-content:center;padding:.75rem 1.5rem;font-size:.88rem;">Submit Request</button>
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
-                  <span class="contact-info-value"><a href="/cdn-cgi/l/email-protection#325b5c545d72475c5b445740415753511c515d5f"><span class="__cf_email__" data-cfemail="8de4e3ebe2cdf8e3e4fbe8fffee8eceea3eee2e0">[email&#160;protected]</span></a></span>
+                  <span class="contact-info-value"><a href="mailto:info@universeservicesfl.com">info@universeservicesfl.com</a></span>
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
-  <script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
+  <script>
     // Navbar scroll state
     const navbar = document.getElementById("navbar");
     window.addEventListener("scroll", () => {
       navbar.classList.toggle("scrolled", window.scrollY > 10);
     }, { passive: true });
 
     // Mobile nav
     const navToggle = document.getElementById("navToggle");
     const navMobile = document.getElementById("navMobile");
 
     function openMenu() {
       // Position dropdown flush below the navbar regardless of its current height
       const navbarHeight = document.getElementById("navbar").getBoundingClientRect().height;
       navMobile.style.top = navbarHeight + "px";
       navMobile.style.display = "block";
       navToggle.classList.add("active");
+      navToggle.setAttribute("aria-expanded", "true");
     }
 
     function closeMenu() {
       navMobile.style.display = "none";
       navToggle.classList.remove("active");
+      navToggle.setAttribute("aria-expanded", "false");
     }
 
     navToggle.addEventListener("click", () => {
       navMobile.style.display === "block" ? closeMenu() : openMenu();
     });
 
     navMobile.addEventListener("click", (e) => {
       if (e.target.tagName.toLowerCase() === "a") closeMenu();
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
 
-    // ── Snow effect ──────────────────────────────────────
-    (function initSnow() {
-      var canvas = document.getElementById('snowCanvas');
-      if (!canvas) { console.warn('No snow canvas'); return; }
-      var ctx = canvas.getContext('2d');
-      var hero = document.querySelector('.hero');
-      var flakes = [];
-      var COUNT = 150;
-
-      function setSize() {
-        var r = hero.getBoundingClientRect();
-        canvas.width  = r.width  || window.innerWidth;
-        canvas.height = r.height || window.innerHeight;
-      }
-
-      function rand(a, b) { return Math.random() * (b - a) + a; }
-
-      function newFlake(atTop) {
-        return {
-          x:       rand(0, canvas.width),
-          y:       atTop ? rand(0, canvas.height) : -rand(2, 15),
-          r:       rand(2, 5),
-          vy:      rand(0.6, 2.2),
-          vx:      rand(-0.5, 0.5),
-          alpha:   rand(0.4, 0.9),
-          wobble:  rand(0, Math.PI * 2),
-          wFreq:   rand(0.01, 0.03),
-          wAmp:    rand(0.3, 0.8)
-        };
-      }
-
-      setSize();
-      for (var i = 0; i < COUNT; i++) flakes.push(newFlake(true));
-      window.addEventListener('resize', setSize, { passive: true });
-
-      function tick() {
-        ctx.clearRect(0, 0, canvas.width, canvas.height);
-        for (var i = 0; i < flakes.length; i++) {
-          var f = flakes[i];
-          f.wobble += f.wFreq;
-          f.x += f.vx + Math.sin(f.wobble) * f.wAmp;
-          f.y += f.vy;
-          if (f.y > canvas.height + 10) {
-            flakes[i] = newFlake(false);
-            continue;
-          }
-          // Draw snowflake as circle with soft glow
-          ctx.save();
-          ctx.globalAlpha = f.alpha;
-          ctx.shadowColor = 'rgba(255,255,255,0.8)';
-          ctx.shadowBlur  = f.r * 2;
-          ctx.beginPath();
-          ctx.arc(f.x, f.y, f.r, 0, Math.PI * 2);
-          ctx.fillStyle = '#ffffff';
-          ctx.fill();
-          ctx.restore();
-        }
-        requestAnimationFrame(tick);
-      }
-      tick();
-      console.log('Snow started — flakes:', COUNT, 'canvas:', canvas.width, 'x', canvas.height);
-    })();
-
-    // ── Thermostat animation ──────────────────────────────
-    (function initThermostat() {
-      var tempEl  = document.getElementById('thermoTemp');
-      var mercury = document.getElementById('mercury');
-      var bulb    = document.getElementById('thermoBulb');
-      if (!tempEl || !mercury) { console.warn('Thermostat elements not found'); return; }
-
-      var MIN = 62, MAX = 84;
-      var TUBE_TOP    = 10;
-      var TUBE_BOTTOM = 78;  // y where tube meets bulb
-      var TUBE_HEIGHT = TUBE_BOTTOM - TUBE_TOP; // 68px
-
-      var current   = MAX;
-      var SPEED     = 0.025;  // degrees per frame
-
-      function getColor(t) {
-        if (t >= 80) {
-          // 84→80: dark red to light red (fast, 4 degrees)
-          var p = (t - 80) / (84 - 80); // 1=dark red, 0=light red
-          var r = Math.round(220 - p * 30);   // 190→220
-          var g = Math.round(p * 40);          // 40→0
-          var b = Math.round(p * 40);          // 40→0
-          return 'rgb(' + r + ',' + g + ',' + b + ')';
-        } else {
-          // 80→62: dark blue to light blue (gradual, 18 degrees)
-          var p = (t - 62) / (80 - 62); // 1=dark blue, 0=light blue
-          var r = Math.round(30  + (1 - p) * 120); // 30→150
-          var g = Math.round(80  + (1 - p) * 130); // 80→210
-          var b = Math.round(180 + (1 - p) * 72);  // 180→252
-          return 'rgb(' + r + ',' + g + ',' + b + ')';
-        }
-      }
-
-      function draw(t) {
-        t = Math.max(MIN, Math.min(MAX, t));
-
-        // Update text
-        tempEl.textContent = Math.round(t) + '°F';
-
-        // Map temperature to mercury rect
-        var pct    = (t - MIN) / (MAX - MIN);
-        var minH   = 6,  maxH = 62;
-        var h = minH + pct * (maxH - minH);
-        var y = TUBE_BOTTOM - h;  // bottom of mercury always at tube bottom
-
-        mercury.setAttribute('y', y.toFixed(2));
-        mercury.setAttribute('height', h.toFixed(2));
-
-        var col = getColor(t);
-        mercury.setAttribute('fill', col);
-        if (bulb) bulb.setAttribute('fill', col);
-      }
-
-      function frame() {
-        current -= SPEED;
-        if (current <= MIN) { current = MAX; } // instant jump back to top
-        draw(current);
-        requestAnimationFrame(frame);
-      }
-
-      draw(current);
-      requestAnimationFrame(frame);
-    })();
-
   </script>
 </body>
 </html>
