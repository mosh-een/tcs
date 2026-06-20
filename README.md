<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tamweel Corporate Services Ltd</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --ink:      #0D1B2A;
    --navy:     #1A3356;
    --gold:     #B8913A;
    --gold-lt:  #D4AA5A;
    --ivory:    #F8F5F0;
    --mid:      #E8E2D9;
    --muted:    #6B7280;
    --white:    #FFFFFF;
  }

  html { scroll-behavior: smooth; }
  body { font-family: 'Inter', sans-serif; background: var(--white); color: var(--ink); line-height: 1.6; }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%;
    height: 72px;
    background: rgba(13, 27, 42, 0.97);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid rgba(184,145,58,0.25);
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    color: var(--white);
    font-size: 1.2rem;
    letter-spacing: 0.04em;
    text-decoration: none;
    display: flex; align-items: center; gap: 10px;
  }
  .nav-logo span { color: var(--gold); }
  .nav-emblem {
    width: 36px; height: 36px;
    border: 1.5px solid var(--gold);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    color: var(--gold);
    font-size: 1rem;
    letter-spacing: 0;
    flex-shrink: 0;
  }
  .nav-links { display: flex; gap: 36px; list-style: none; }
  .nav-links a {
    color: rgba(255,255,255,0.78);
    text-decoration: none;
    font-size: 0.82rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-weight: 500;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold-lt); }
  .nav-cta {
    background: var(--gold);
    color: var(--ink) !important;
    padding: 8px 22px;
    font-weight: 600 !important;
    transition: background 0.2s !important;
  }
  .nav-cta:hover { background: var(--gold-lt) !important; color: var(--ink) !important; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background: var(--ink);
    display: flex; align-items: center;
    padding: 120px 5% 80px;
    position: relative;
    overflow: hidden;
  }
  .hero-grid-lines {
    position: absolute; inset: 0; pointer-events: none;
    background-image:
      linear-gradient(to right, rgba(184,145,58,0.06) 1px, transparent 1px),
      linear-gradient(to bottom, rgba(184,145,58,0.06) 1px, transparent 1px);
    background-size: 80px 80px;
  }
  .hero-glow {
    position: absolute; top: -200px; right: -200px;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(184,145,58,0.12) 0%, transparent 65%);
    pointer-events: none;
  }
  .hero-content { position: relative; max-width: 680px; }
  .hero-eyebrow {
    font-size: 0.72rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 600;
    margin-bottom: 24px;
    display: flex; align-items: center; gap: 12px;
  }
  .hero-eyebrow::before {
    content: ''; display: block;
    width: 32px; height: 1px;
    background: var(--gold);
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.4rem, 5vw, 4rem);
    color: var(--white);
    line-height: 1.15;
    font-weight: 700;
    margin-bottom: 28px;
  }
  .hero h1 em { color: var(--gold); font-style: normal; }
  .hero-sub {
    font-size: 1.05rem;
    color: rgba(255,255,255,0.65);
    max-width: 520px;
    margin-bottom: 48px;
    font-weight: 300;
    line-height: 1.75;
  }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--gold);
    color: var(--ink);
    padding: 14px 32px;
    font-weight: 600;
    font-size: 0.85rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    text-decoration: none;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }
  .btn-primary:hover { background: var(--gold-lt); transform: translateY(-1px); }
  .btn-outline {
    border: 1px solid rgba(255,255,255,0.35);
    color: rgba(255,255,255,0.85);
    padding: 14px 32px;
    font-size: 0.85rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    text-decoration: none;
    transition: border-color 0.2s, color 0.2s;
    display: inline-block;
  }
  .btn-outline:hover { border-color: var(--gold); color: var(--gold); }
  .hero-stats {
    position: absolute; bottom: 60px; right: 5%;
    display: flex; gap: 48px;
  }
  .stat { text-align: right; }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    color: var(--gold);
    font-weight: 700;
    display: block;
  }
  .stat-lbl {
    font-size: 0.72rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.45);
  }

  /* ── DIVIDER ── */
  .gold-rule { height: 3px; background: linear-gradient(to right, var(--gold), var(--gold-lt), transparent); }

  /* ── ABOUT ── */
  .about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0;
  }
  .about-text {
    background: var(--ivory);
    padding: 100px 5% 100px 10%;
  }
  .about-visual {
    background: var(--navy);
    padding: 100px 10% 100px 5%;
    display: flex; flex-direction: column; justify-content: center;
  }
  .section-label {
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 600;
    margin-bottom: 18px;
  }
  .section-h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3vw, 2.6rem);
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 24px;
  }
  .about-text .section-h2 { color: var(--ink); }
  .about-visual .section-h2 { color: var(--white); }
  .body-text {
    font-size: 0.95rem;
    line-height: 1.85;
    color: var(--muted);
    margin-bottom: 20px;
  }
  .about-visual .body-text { color: rgba(255,255,255,0.6); }
  .value-list { list-style: none; margin-top: 32px; }
  .value-list li {
    display: flex; align-items: flex-start; gap: 14px;
    padding: 12px 0;
    border-top: 1px solid var(--mid);
    font-size: 0.9rem;
    color: var(--ink);
  }
  .value-list li::before {
    content: '▸';
    color: var(--gold);
    font-size: 0.75rem;
    margin-top: 3px;
    flex-shrink: 0;
  }

  /* ── SERVICES ── */
  .services {
    padding: 100px 5%;
    background: var(--white);
  }
  .services-header {
    text-align: center;
    margin-bottom: 60px;
  }
  .services-header .section-h2 { color: var(--ink); }
  .services-header .body-text { max-width: 520px; margin: 0 auto; }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    background: var(--mid);
  }
  .service-card {
    background: var(--white);
    padding: 48px 36px;
    transition: background 0.25s;
    cursor: default;
  }
  .service-card:hover { background: var(--navy); }
  .service-card:hover .service-title { color: var(--white); }
  .service-card:hover .service-desc { color: rgba(255,255,255,0.6); }
  .service-card:hover .service-icon { border-color: var(--gold); color: var(--gold); }
  .service-icon {
    width: 52px; height: 52px;
    border: 1.5px solid var(--mid);
    display: flex; align-items: center; justify-content: center;
    font-size: 1.4rem;
    margin-bottom: 28px;
    transition: border-color 0.25s, color 0.25s;
    color: var(--navy);
  }
  .service-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 14px;
    transition: color 0.25s;
  }
  .service-desc {
    font-size: 0.87rem;
    color: var(--muted);
    line-height: 1.75;
    transition: color 0.25s;
  }

  /* ── WHY US ── */
  .why {
    background: var(--ink);
    padding: 100px 5%;
    display: grid;
    grid-template-columns: 1fr 1.4fr;
    gap: 80px;
    align-items: center;
  }
  .why-left .section-h2 { color: var(--white); }
  .why-left .body-text { color: rgba(255,255,255,0.55); }
  .pillars { display: grid; grid-template-columns: 1fr 1fr; gap: 24px; }
  .pillar {
    border: 1px solid rgba(184,145,58,0.2);
    padding: 28px 24px;
    transition: border-color 0.2s;
  }
  .pillar:hover { border-color: var(--gold); }
  .pillar-num {
    font-family: 'Playfair Display', serif;
    font-size: 2rem;
    color: var(--gold);
    font-weight: 700;
    opacity: 0.5;
    line-height: 1;
    margin-bottom: 12px;
  }
  .pillar-title {
    color: var(--white);
    font-size: 0.9rem;
    font-weight: 600;
    margin-bottom: 8px;
    letter-spacing: 0.02em;
  }
  .pillar-body { font-size: 0.82rem; color: rgba(255,255,255,0.45); line-height: 1.65; }

  /* ── PROCESS ── */
  .process {
    padding: 100px 5%;
    background: var(--ivory);
  }
  .process-header { text-align: center; margin-bottom: 64px; }
  .process-header .section-h2 { color: var(--ink); }
  .steps {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0;
    position: relative;
  }
  .steps::after {
    content: '';
    position: absolute;
    top: 36px; left: calc(12.5% + 36px); right: calc(12.5% + 36px);
    height: 1px;
    background: linear-gradient(to right, var(--gold), var(--gold-lt), var(--gold));
  }
  .step { padding: 0 20px; text-align: center; }
  .step-circle {
    width: 72px; height: 72px;
    border: 2px solid var(--gold);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 28px;
    background: var(--ivory);
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    color: var(--gold);
    font-weight: 700;
    position: relative; z-index: 1;
  }
  .step-title {
    font-weight: 600;
    font-size: 0.9rem;
    color: var(--ink);
    margin-bottom: 10px;
  }
  .step-desc { font-size: 0.82rem; color: var(--muted); line-height: 1.7; }

  /* ── CONTACT ── */
  .contact {
    padding: 100px 5%;
    background: var(--white);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }
  .contact-info .section-h2 { color: var(--ink); margin-bottom: 20px; }
  .contact-info .body-text { margin-bottom: 40px; }
  .contact-detail {
    display: flex; align-items: flex-start; gap: 16px;
    margin-bottom: 24px;
  }
  .detail-icon {
    width: 40px; height: 40px;
    background: var(--navy);
    display: flex; align-items: center; justify-content: center;
    color: var(--gold);
    font-size: 0.9rem;
    flex-shrink: 0;
  }
  .detail-text strong { display: block; font-size: 0.78rem; letter-spacing: 0.1em; text-transform: uppercase; color: var(--muted); margin-bottom: 4px; }
  .detail-text span { font-size: 0.92rem; color: var(--ink); }

  .contact-form { padding: 48px 40px; background: var(--ivory); }
  .form-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 32px;
  }
  .form-group { margin-bottom: 20px; }
  .form-group label {
    display: block;
    font-size: 0.75rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 8px;
    font-weight: 500;
  }
  .form-group input,
  .form-group select,
  .form-group textarea {
    width: 100%;
    padding: 12px 16px;
    border: 1px solid var(--mid);
    background: var(--white);
    font-family: 'Inter', sans-serif;
    font-size: 0.9rem;
    color: var(--ink);
    outline: none;
    transition: border-color 0.2s;
    appearance: none;
  }
  .form-group input:focus,
  .form-group select:focus,
  .form-group textarea:focus { border-color: var(--gold); }
  .form-group textarea { resize: vertical; min-height: 110px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .submit-btn {
    width: 100%;
    background: var(--navy);
    color: var(--white);
    border: none;
    padding: 15px;
    font-family: 'Inter', sans-serif;
    font-size: 0.82rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    font-weight: 600;
    cursor: pointer;
    transition: background 0.2s;
    margin-top: 8px;
  }
  .submit-btn:hover { background: var(--gold); color: var(--ink); }

  /* ── FOOTER ── */
  footer {
    background: var(--ink);
    padding: 60px 5% 32px;
    border-top: 1px solid rgba(184,145,58,0.2);
  }
  .footer-top {
    display: grid;
    grid-template-columns: 1.5fr 1fr 1fr 1fr;
    gap: 48px;
    padding-bottom: 48px;
    border-bottom: 1px solid rgba(255,255,255,0.06);
    margin-bottom: 32px;
  }
  .footer-brand p {
    font-size: 0.85rem;
    color: rgba(255,255,255,0.4);
    line-height: 1.75;
    margin-top: 16px;
  }
  .footer-col-title {
    font-size: 0.7rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 600;
    margin-bottom: 20px;
  }
  .footer-col ul { list-style: none; }
  .footer-col ul li { margin-bottom: 10px; }
  .footer-col ul li a {
    color: rgba(255,255,255,0.45);
    text-decoration: none;
    font-size: 0.85rem;
    transition: color 0.2s;
  }
  .footer-col ul li a:hover { color: var(--gold-lt); }
  .footer-bottom {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 0.78rem;
    color: rgba(255,255,255,0.25);
  }
  .footer-bottom a { color: rgba(255,255,255,0.35); text-decoration: none; }
  .footer-bottom a:hover { color: var(--gold); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .nav-links { display: none; }
    .about { grid-template-columns: 1fr; }
    .about-text { padding: 60px 6%; }
    .about-visual { padding: 60px 6%; }
    .services-grid { grid-template-columns: 1fr; }
    .why { grid-template-columns: 1fr; gap: 40px; padding: 60px 5%; }
    .steps { grid-template-columns: 1fr 1fr; }
    .steps::after { display: none; }
    .step { margin-bottom: 40px; }
    .contact { grid-template-columns: 1fr; gap: 40px; padding: 60px 5%; }
    .footer-top { grid-template-columns: 1fr 1fr; }
    .hero-stats { position: static; margin-top: 60px; justify-content: flex-start; }
    .hero { flex-direction: column; }
  }
  @media (max-width: 560px) {
    .pillars { grid-template-columns: 1fr; }
    .form-row { grid-template-columns: 1fr; }
    .footer-top { grid-template-columns: 1fr; }
    .footer-bottom { flex-direction: column; gap: 10px; text-align: center; }
    .steps { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">
    <div class="nav-emblem">T</div>
    Tamweel <span>&nbsp;Corporate Services</span>
  </a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#why">Why Us</a></li>
    <li><a href="#process">Process</a></li>
    <li><a href="#contact" class="nav-cta">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-grid-lines"></div>
  <div class="hero-glow"></div>
  <div class="hero-content">
    <div class="hero-eyebrow">Tamweel Corporate Services Ltd</div>
    <h1>Trusted <em>Corporate Solutions</em> for a Changing World</h1>
    <p class="hero-sub">We partner with businesses to deliver strategic corporate services — from company formation and compliance to financial advisory — with integrity, precision, and lasting value.</p>
    <div class="hero-btns">
      <a href="#services" class="btn-primary">Our Services</a>
      <a href="#contact" class="btn-outline">Get in Touch</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat">
      <span class="stat-num">15+</span>
      <span class="stat-lbl">Years of Experience</span>
    </div>
    <div class="stat">
      <span class="stat-num">500+</span>
      <span class="stat-lbl">Clients Served</span>
    </div>
    <div class="stat">
      <span class="stat-num">98%</span>
      <span class="stat-lbl">Client Retention</span>
    </div>
  </div>
</section>

<div class="gold-rule"></div>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-text">
    <div class="section-label">About Us</div>
    <h2 class="section-h2">A Partner You Can Build Your Business On</h2>
    <p class="body-text">Tamweel Corporate Services Ltd is a full-service corporate solutions firm dedicated to helping businesses navigate complexity with confidence. We combine deep industry knowledge with a client-first approach to deliver services that are timely, accurate, and impactful.</p>
    <p class="body-text">Whether you are launching a new venture, scaling operations, or managing ongoing compliance obligations, our team of experienced professionals is here to support every stage of your business journey.</p>
    <ul class="value-list">
      <li>Proven track record of corporate excellence</li>
      <li>Multidisciplinary team of legal, financial, and business experts</li>
      <li>Transparent processes and clear communication</li>
      <li>Tailored solutions — no one-size-fits-all approach</li>
    </ul>
  </div>
  <div class="about-visual">
    <div class="section-label">Our Mission</div>
    <h2 class="section-h2">Empowering Businesses Through Expert Guidance</h2>
    <p class="body-text">We believe that sound corporate infrastructure is the foundation of every successful enterprise. Our mission is to remove the administrative and regulatory burden from your plate, so you can focus on growth and opportunity.</p>
    <p class="body-text">Our vision is to be the most trusted corporate services partner — recognised for our reliability, integrity, and the genuine value we add to every client relationship.</p>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div class="services-header">
    <div class="section-label">What We Offer</div>
    <h2 class="section-h2">Comprehensive Corporate Services</h2>
    <p class="body-text">From incorporation to ongoing compliance, we cover every aspect of your corporate needs under one roof.</p>
  </div>
  <div class="services-grid">
    <div class="service-card">
      <div class="service-icon">⚖</div>
      <div class="service-title">Company Formation</div>
      <p class="service-desc">End-to-end business registration and incorporation services. We handle the paperwork, statutory filings, and regulatory requirements so your business launches without delay.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📋</div>
      <div class="service-title">Corporate Compliance</div>
      <p class="service-desc">Stay fully compliant with local and international regulations. We manage annual returns, statutory records, and regulatory reporting on your behalf.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">💼</div>
      <div class="service-title">Business Advisory</div>
      <p class="service-desc">Strategic advice across corporate governance, restructuring, and business development. We help you make informed decisions that drive long-term success.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">📊</div>
      <div class="service-title">Financial Services</div>
      <p class="service-desc">Accounting, bookkeeping, payroll management, and financial planning. Our financial experts ensure your business remains healthy and reporting-ready.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🏛</div>
      <div class="service-title">Legal Support</div>
      <p class="service-desc">Contract drafting, review, and legal documentation. We provide practical legal support for day-to-day corporate operations and complex transactions.</p>
    </div>
    <div class="service-card">
      <div class="service-icon">🌐</div>
      <div class="service-title">International Structuring</div>
      <p class="service-desc">Cross-border corporate structures, nominee services, and international expansion support. We help businesses operate across multiple jurisdictions efficiently.</p>
    </div>
  </div>
</section>

<!-- WHY US -->
<section class="why" id="why">
  <div class="why-left">
    <div class="section-label">Why Choose Us</div>
    <h2 class="section-h2">The Tamweel Difference</h2>
    <p class="body-text">We don't just process paperwork — we become an extension of your team. Our commitment to excellence, discretion, and responsiveness has made us the preferred corporate services partner for businesses of all sizes.</p>
    <p class="body-text">Our multidisciplinary expertise means you benefit from a holistic approach: legal, financial, and strategic considerations are always weighed together, giving you complete and coherent guidance.</p>
  </div>
  <div class="pillars">
    <div class="pillar">
      <div class="pillar-num">01</div>
      <div class="pillar-title">Expertise & Experience</div>
      <p class="pillar-body">Our seasoned professionals bring years of hands-on experience across corporate law, finance, and compliance.</p>
    </div>
    <div class="pillar">
      <div class="pillar-num">02</div>
      <div class="pillar-title">Speed & Reliability</div>
      <p class="pillar-body">We understand that time is critical in business. Our processes are built for accuracy and efficiency without compromise.</p>
    </div>
    <div class="pillar">
      <div class="pillar-num">03</div>
      <div class="pillar-title">Full Confidentiality</div>
      <p class="pillar-body">Your business information is handled with the highest level of discretion and professional confidentiality.</p>
    </div>
    <div class="pillar">
      <div class="pillar-num">04</div>
      <div class="pillar-title">Tailored Solutions</div>
      <p class="pillar-body">We take time to understand your unique context and deliver solutions specifically built for your situation.</p>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process" id="process">
  <div class="process-header">
    <div class="section-label">How We Work</div>
    <h2 class="section-h2">A Clear, Structured Process</h2>
  </div>
  <div class="steps">
    <div class="step">
      <div class="step-circle">1</div>
      <div class="step-title">Initial Consultation</div>
      <p class="step-desc">We begin with a thorough discussion to understand your business needs, goals, and challenges.</p>
    </div>
    <div class="step">
      <div class="step-circle">2</div>
      <div class="step-title">Tailored Proposal</div>
      <p class="step-desc">We design a customised service plan with clear scope, timelines, and transparent pricing.</p>
    </div>
    <div class="step">
      <div class="step-circle">3</div>
      <div class="step-title">Expert Execution</div>
      <p class="step-desc">Our team delivers with precision, keeping you informed at every stage of the engagement.</p>
    </div>
    <div class="step">
      <div class="step-circle">4</div>
      <div class="step-title">Ongoing Support</div>
      <p class="step-desc">We stay by your side beyond delivery — adapting to your evolving needs and providing continued guidance.</p>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="contact-info">
    <div class="section-label">Get In Touch</div>
    <h2 class="section-h2">Let's Start a Conversation</h2>
    <p class="body-text">Whether you have a specific requirement or simply want to explore how we can support your business, we'd love to hear from you. Our team typically responds within one business day.</p>

    <div class="contact-detail">
      <div class="detail-icon">📍</div>
      <div class="detail-text">
        <strong>Address</strong>
        <span>Tamweel Corporate Services Ltd<br>Port Louis, Mauritius</span>
      </div>
    </div>
    <div class="contact-detail">
      <div class="detail-icon">✉</div>
      <div class="detail-text">
        <strong>Email</strong>
        <span>info@tamweelcorporate.com</span>
      </div>
    </div>
    <div class="contact-detail">
      <div class="detail-icon">📞</div>
      <div class="detail-text">
        <strong>Phone</strong>
        <span>+230 000 0000</span>
      </div>
    </div>
    <div class="contact-detail">
      <div class="detail-icon">🕐</div>
      <div class="detail-text">
        <strong>Business Hours</strong>
        <span>Monday – Friday, 9:00 AM – 5:00 PM</span>
      </div>
    </div>
  </div>

  <div class="contact-form">
    <div class="form-title">Send Us a Message</div>
    <div class="form-row">
      <div class="form-group">
        <label>First Name</label>
        <input type="text" placeholder="John">
      </div>
      <div class="form-group">
        <label>Last Name</label>
        <input type="text" placeholder="Smith">
      </div>
    </div>
    <div class="form-group">
      <label>Email Address</label>
      <input type="email" placeholder="john@company.com">
    </div>
    <div class="form-group">
      <label>Service of Interest</label>
      <select>
        <option value="">— Select a service —</option>
        <option>Company Formation</option>
        <option>Corporate Compliance</option>
        <option>Business Advisory</option>
        <option>Financial Services</option>
        <option>Legal Support</option>
        <option>International Structuring</option>
        <option>Other</option>
      </select>
    </div>
    <div class="form-group">
      <label>Message</label>
      <textarea placeholder="Tell us about your requirements…"></textarea>
    </div>
    <button class="submit-btn">Submit Enquiry</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div class="footer-brand">
      <div class="nav-logo" style="color:#fff;font-family:'Playfair Display',serif;font-size:1.1rem;letter-spacing:0.04em;display:flex;align-items:center;gap:10px;text-decoration:none;">
        <div class="nav-emblem">T</div>
        Tamweel <span style="color:#B8913A;">&nbsp;Corporate Services</span>
      </div>
      <p>Your trusted partner for comprehensive corporate solutions. Built on integrity, driven by excellence.</p>
    </div>
    <div class="footer-col">
      <div class="footer-col-title">Services</div>
      <ul>
        <li><a href="#services">Company Formation</a></li>
        <li><a href="#services">Corporate Compliance</a></li>
        <li><a href="#services">Business Advisory</a></li>
        <li><a href="#services">Financial Services</a></li>
        <li><a href="#services">Legal Support</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <div class="footer-col-title">Company</div>
      <ul>
        <li><a href="#about">About Us</a></li>
        <li><a href="#why">Why Choose Us</a></li>
        <li><a href="#process">Our Process</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <div class="footer-col-title">Connect</div>
      <ul>
        <li><a href="https://www.facebook.com/TamweelCorporateServicesLTD" target="_blank">Facebook</a></li>
        <li><a href="#contact">LinkedIn</a></li>
        <li><a href="#contact">Email Us</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <span>&copy; 2025 Tamweel Corporate Services Ltd. All rights reserved.</span>
    <span>
      <a href="#">Privacy Policy</a> &nbsp;·&nbsp;
      <a href="#">Terms of Service</a>
    </span>
  </div>
</footer>

</body>
</html>
