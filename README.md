<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tamweel Ltd – Accounting & Tax Systems | Outsourcing Solutions</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --navy:    #1A3A6B;
    --navy-dk: #0D2347;
    --sky:     #4A90C4;
    --sky-lt:  #A8D4EE;
    --white:   #FFFFFF;
    --ivory:   #F4F8FC;
    --mid:     #D6E6F2;
    --ink:     #0D1B2A;
    --muted:   #5A6E82;
    --accent:  #2563A8;
  }

  html { scroll-behavior: smooth; }
  body { font-family: 'Inter', sans-serif; background: var(--white); color: var(--ink); line-height: 1.6; }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; height: 70px;
    background: rgba(10, 28, 60, 0.97);
    backdrop-filter: blur(8px);
    border-bottom: 2px solid var(--sky);
  }
  .nav-logo {
    display: flex; align-items: center; gap: 12px;
    text-decoration: none;
  }
  .logo-box {
    width: 44px; height: 44px;
    background: var(--white);
    border: 2px solid var(--sky);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Playfair Display', serif;
    font-size: 0.75rem;
    color: var(--navy);
    font-weight: 700;
    line-height: 1;
    text-align: center;
    padding: 2px;
    letter-spacing: -0.5px;
  }
  .logo-text {
    display: flex; flex-direction: column;
  }
  .logo-main {
    font-family: 'Inter', sans-serif;
    font-weight: 700;
    font-size: 1.35rem;
    color: var(--white);
    letter-spacing: 0.06em;
    line-height: 1;
  }
  .logo-sub {
    font-size: 0.6rem;
    color: var(--sky-lt);
    letter-spacing: 0.05em;
    margin-top: 3px;
  }
  .nav-links { display: flex; gap: 32px; list-style: none; }
  .nav-links a {
    color: rgba(255,255,255,0.72);
    text-decoration: none;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-weight: 500;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--sky-lt); }
  .nav-cta {
    background: var(--sky) !important;
    color: var(--white) !important;
    padding: 8px 22px;
    font-weight: 600 !important;
  }
  .nav-cta:hover { background: #5BA3D4 !important; }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background: linear-gradient(145deg, var(--navy-dk) 0%, var(--navy) 50%, #1E4E8C 100%);
    display: flex; align-items: center;
    padding: 120px 5% 80px;
    position: relative; overflow: hidden;
  }
  .hero-wave {
    position: absolute; bottom: 0; left: 0; right: 0;
    height: 120px; overflow: hidden;
  }
  .hero-wave svg { width: 100%; height: 100%; }
  .hero-circles {
    position: absolute; top: 0; right: 0; bottom: 0;
    width: 50%; pointer-events: none;
    display: flex; align-items: center; justify-content: center;
  }
  .circle-bg {
    position: absolute;
    border-radius: 50%;
    border: 1px solid rgba(74,144,196,0.15);
  }
  .c1 { width: 500px; height: 500px; right: -100px; top: 50%; transform: translateY(-50%); }
  .c2 { width: 360px; height: 360px; right: -30px; top: 50%; transform: translateY(-50%); }
  .c3 { width: 220px; height: 220px; right: 40px; top: 50%; transform: translateY(-50%); background: rgba(74,144,196,0.05); }

  .hero-content { position: relative; z-index: 2; max-width: 640px; }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 10px;
    border: 1px solid rgba(74,144,196,0.5);
    padding: 6px 16px;
    margin-bottom: 28px;
    font-size: 0.7rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--sky-lt);
    font-weight: 600;
  }
  .badge-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--sky); }
  .hero h1 {
    font-family: 'Inter', sans-serif;
    font-size: clamp(2.4rem, 4.5vw, 3.6rem);
    color: var(--white);
    line-height: 1.1;
    font-weight: 700;
    letter-spacing: -0.02em;
    margin-bottom: 10px;
  }
  .hero h1 .ltd { color: var(--sky-lt); font-weight: 300; }
  .hero-tagline {
    font-size: 0.95rem;
    color: var(--sky-lt);
    font-weight: 400;
    letter-spacing: 0.06em;
    margin-bottom: 24px;
    padding-bottom: 24px;
    border-bottom: 1px solid rgba(74,144,196,0.3);
  }
  .hero-desc {
    font-size: 1rem;
    color: rgba(255,255,255,0.68);
    line-height: 1.8;
    margin-bottom: 14px;
    font-weight: 300;
  }
  .hero-italic {
    font-style: italic;
    color: var(--sky-lt);
    font-size: 1.05rem;
    margin-bottom: 40px;
    font-weight: 400;
  }
  .hero-values {
    display: flex; gap: 20px; flex-wrap: wrap; margin-bottom: 40px;
  }
  .val-chip {
    display: flex; align-items: center; gap: 7px;
    font-size: 0.78rem;
    color: rgba(255,255,255,0.7);
    font-weight: 500;
  }
  .val-chip::before {
    content: '•';
    color: var(--sky);
    font-size: 1.1rem;
    line-height: 1;
  }
  .hero-btns { display: flex; gap: 14px; flex-wrap: wrap; }
  .btn-primary {
    background: var(--sky);
    color: var(--white);
    padding: 14px 32px;
    font-weight: 600;
    font-size: 0.82rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
    border: none; cursor: pointer;
  }
  .btn-primary:hover { background: #5BA3D4; transform: translateY(-1px); }
  .btn-outline {
    border: 1.5px solid rgba(255,255,255,0.35);
    color: rgba(255,255,255,0.85);
    padding: 14px 32px;
    font-size: 0.82rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    transition: border-color 0.2s, color 0.2s;
    display: inline-block;
  }
  .btn-outline:hover { border-color: var(--sky-lt); color: var(--sky-lt); }

  /* ── BLUE DIVIDER WAVE ── */
  .wave-divider { line-height: 0; background: var(--navy-dk); }
  .wave-divider svg { display: block; }

  /* ── SERVICES ── */
  .services {
    padding: 90px 5%;
    background: var(--ivory);
  }
  .section-label {
    font-size: 0.68rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--sky);
    font-weight: 700;
    margin-bottom: 12px;
  }
  .section-h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.7rem, 3vw, 2.5rem);
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 14px;
    color: var(--navy-dk);
  }
  .section-sub {
    font-size: 0.93rem;
    color: var(--muted);
    margin-bottom: 56px;
    max-width: 500px;
  }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }
  .svc-card {
    background: var(--white);
    border-top: 3px solid var(--sky);
    padding: 36px 28px 32px;
    transition: box-shadow 0.25s, transform 0.2s;
    position: relative;
  }
  .svc-card:hover { box-shadow: 0 12px 36px rgba(26,58,107,0.12); transform: translateY(-3px); }
  .svc-tag {
    display: inline-block;
    background: var(--navy);
    color: var(--white);
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 5px 14px;
    margin-bottom: 18px;
  }
  .svc-title {
    font-size: 1.05rem;
    font-weight: 700;
    color: var(--navy-dk);
    margin-bottom: 10px;
    line-height: 1.3;
  }
  .svc-desc {
    font-size: 0.87rem;
    color: var(--muted);
    line-height: 1.75;
  }
  .svc-icon {
    position: absolute; top: 32px; right: 28px;
    font-size: 1.6rem; opacity: 0.15;
  }

  /* ── ABOUT BANNER ── */
  .about-banner {
    background: var(--navy);
    padding: 80px 5%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }
  .about-left .section-h2 { color: var(--white); }
  .about-left .section-sub { color: rgba(255,255,255,0.55); max-width: 100%; }
  .about-italic {
    font-style: italic;
    color: var(--sky-lt);
    font-size: 1.15rem;
    line-height: 1.6;
    font-weight: 400;
    margin-bottom: 28px;
  }
  .values-list { list-style: none; }
  .values-list li {
    display: flex; align-items: center; gap: 14px;
    padding: 13px 0;
    border-bottom: 1px solid rgba(255,255,255,0.08);
    color: rgba(255,255,255,0.8);
    font-size: 0.92rem;
    font-weight: 500;
  }
  .values-list li:last-child { border-bottom: none; }
  .val-num {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem;
    color: var(--sky);
    font-weight: 700;
    opacity: 0.5;
    min-width: 28px;
  }
  .about-right {
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(74,144,196,0.2);
    padding: 40px 36px;
  }
  .stat-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 2px; background: rgba(74,144,196,0.15); }
  .stat-cell {
    background: rgba(10,28,60,0.6);
    padding: 28px 24px;
    text-align: center;
  }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.2rem;
    color: var(--sky-lt);
    font-weight: 700;
    display: block;
    line-height: 1;
    margin-bottom: 8px;
  }
  .stat-lbl {
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.4);
  }
  .core-values-box {
    margin-top: 24px;
    padding-top: 24px;
    border-top: 1px solid rgba(74,144,196,0.2);
  }
  .cv-title {
    font-size: 0.7rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--sky);
    font-weight: 700;
    margin-bottom: 16px;
  }
  .cv-chips { display: flex; flex-wrap: wrap; gap: 8px; }
  .cv-chip {
    border: 1px solid rgba(74,144,196,0.35);
    color: rgba(255,255,255,0.7);
    padding: 5px 14px;
    font-size: 0.78rem;
    font-weight: 500;
    letter-spacing: 0.06em;
  }

  /* ── CONTACT ── */
  .contact {
    padding: 90px 5%;
    background: var(--ivory);
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 72px;
    align-items: start;
  }
  .contact-info .section-h2 { color: var(--navy-dk); }
  .contact-info .section-sub { max-width: 100%; margin-bottom: 40px; }
  .cdet {
    display: flex; align-items: flex-start; gap: 16px;
    margin-bottom: 22px;
  }
  .cdet-icon {
    width: 42px; height: 42px; flex-shrink: 0;
    background: var(--navy);
    display: flex; align-items: center; justify-content: center;
    font-size: 1rem;
    color: var(--sky-lt);
  }
  .cdet-body strong {
    display: block;
    font-size: 0.7rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 4px;
  }
  .cdet-body span { font-size: 0.92rem; color: var(--ink); line-height: 1.55; }
  .map-link {
    display: inline-flex; align-items: center; gap: 8px;
    font-size: 0.8rem;
    color: var(--sky);
    text-decoration: none;
    margin-top: 28px;
    font-weight: 600;
    letter-spacing: 0.06em;
    transition: color 0.2s;
  }
  .map-link:hover { color: var(--navy); }

  .contact-form {
    background: var(--white);
    border-top: 3px solid var(--sky);
    padding: 44px 38px;
    box-shadow: 0 4px 24px rgba(26,58,107,0.07);
  }
  .form-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    font-weight: 700;
    color: var(--navy-dk);
    margin-bottom: 28px;
  }
  .form-group { margin-bottom: 18px; }
  .form-group label {
    display: block;
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 7px;
    font-weight: 600;
  }
  .form-group input,
  .form-group select,
  .form-group textarea {
    width: 100%;
    padding: 11px 15px;
    border: 1px solid var(--mid);
    background: var(--ivory);
    font-family: 'Inter', sans-serif;
    font-size: 0.9rem;
    color: var(--ink);
    outline: none;
    transition: border-color 0.2s;
    appearance: none;
  }
  .form-group input:focus,
  .form-group select:focus,
  .form-group textarea:focus { border-color: var(--sky); background: var(--white); }
  .form-group textarea { resize: vertical; min-height: 100px; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  .submit-btn {
    width: 100%;
    background: var(--navy);
    color: var(--white);
    border: none;
    padding: 14px;
    font-family: 'Inter', sans-serif;
    font-size: 0.8rem;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    font-weight: 700;
    cursor: pointer;
    transition: background 0.2s;
    margin-top: 6px;
  }
  .submit-btn:hover { background: var(--sky); }

  /* ── FOOTER ── */
  footer {
    background: var(--navy-dk);
    padding: 56px 5% 28px;
    border-top: 3px solid var(--sky);
  }
  .footer-top {
    display: grid;
    grid-template-columns: 1.6fr 1fr 1fr;
    gap: 48px;
    padding-bottom: 40px;
    border-bottom: 1px solid rgba(255,255,255,0.07);
    margin-bottom: 28px;
  }
  .footer-brand-name {
    font-weight: 700;
    font-size: 1.2rem;
    color: var(--white);
    letter-spacing: 0.06em;
    margin-bottom: 6px;
  }
  .footer-brand-sub {
    font-size: 0.72rem;
    color: var(--sky-lt);
    letter-spacing: 0.05em;
    margin-bottom: 16px;
  }
  .footer-brand p {
    font-size: 0.83rem;
    color: rgba(255,255,255,0.38);
    line-height: 1.75;
  }
  .footer-col-title {
    font-size: 0.68rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--sky);
    font-weight: 700;
    margin-bottom: 18px;
  }
  .footer-col ul { list-style: none; }
  .footer-col ul li { margin-bottom: 10px; }
  .footer-col ul li a {
    color: rgba(255,255,255,0.42);
    text-decoration: none;
    font-size: 0.84rem;
    transition: color 0.2s;
  }
  .footer-col ul li a:hover { color: var(--sky-lt); }
  .footer-bottom {
    display: flex; justify-content: space-between; align-items: center;
    font-size: 0.75rem;
    color: rgba(255,255,255,0.22);
  }
  .footer-bottom a { color: rgba(255,255,255,0.3); text-decoration: none; }
  .footer-bottom a:hover { color: var(--sky-lt); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .nav-links { display: none; }
    .about-banner { grid-template-columns: 1fr; gap: 40px; }
    .services-grid { grid-template-columns: 1fr 1fr; }
    .contact { grid-template-columns: 1fr; gap: 40px; }
    .footer-top { grid-template-columns: 1fr 1fr; }
  }
  @media (max-width: 560px) {
    .services-grid { grid-template-columns: 1fr; }
    .form-row { grid-template-columns: 1fr; }
    .footer-top { grid-template-columns: 1fr; }
    .footer-bottom { flex-direction: column; gap: 8px; text-align: center; }
    .stat-grid { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">
    <div class="logo-box">tam<br>weel</div>
    <div class="logo-text">
      <span class="logo-main">TAMWEEL LTD</span>
      <span class="logo-sub">Accounting & Tax Systems | Outsourcing Solutions</span>
    </div>
  </a>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="mailto:info@tamweelltd.com" class="nav-cta">Email Us</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="circle-bg c1"></div>
  <div class="circle-bg c2"></div>
  <div class="circle-bg c3"></div>

  <div class="hero-content">
    <div class="hero-badge"><span class="badge-dot"></span>Mauritius-Based Corporate Firm</div>
    <h1>TAMWEEL <span class="ltd">LTD</span></h1>
    <p class="hero-tagline">Accounting &amp; Tax Systems &nbsp;|&nbsp; Outsourcing Solutions</p>
    <p class="hero-desc">We are a team of professionals with wide experience in Practice and Industry, providing high quality services to our clients.</p>
    <p class="hero-italic">"Unmatched Tailor Made Solutions"</p>
    <div class="hero-values">
      <div class="val-chip">Professionalism</div>
      <div class="val-chip">Competency</div>
      <div class="val-chip">Integrity</div>
      <div class="val-chip">Commitment</div>
    </div>
    <div class="hero-btns">
      <a href="#services" class="btn-primary">Our Services</a>
      <a href="#contact" class="btn-outline">Get in Touch</a>
    </div>
  </div>

  <div class="hero-wave">
    <svg viewBox="0 0 1440 120" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0,80 C360,120 1080,0 1440,80 L1440,120 L0,120 Z" fill="#F4F8FC"/>
    </svg>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div class="section-label">Available Systems</div>
  <h2 class="section-h2">What We Offer</h2>
  <p class="section-sub">Comprehensive accounting, tax, advisory, and outsourcing services tailored to your business needs.</p>

  <div class="services-grid">
    <div class="svc-card">
      <div class="svc-icon">📊</div>
      <div class="svc-tag">Accounting</div>
      <div class="svc-title">Bookkeeping &amp; Financial Reporting</div>
      <p class="svc-desc">Accurate and timely bookkeeping paired with clear financial reporting to keep your business on solid footing and decision-ready at all times.</p>
    </div>
    <div class="svc-card">
      <div class="svc-icon">🧾</div>
      <div class="svc-tag">Tax</div>
      <div class="svc-title">Personal &amp; Company Tax, VAT, PAYE &amp; TDS</div>
      <p class="svc-desc">Full-spectrum tax compliance services covering personal and corporate tax returns, VAT filings, PAYE administration, and TDS obligations.</p>
    </div>
    <div class="svc-card">
      <div class="svc-icon">💼</div>
      <div class="svc-tag">Advisory</div>
      <div class="svc-title">Business Plan, Forecast, Business System &amp; Corporate Finance</div>
      <p class="svc-desc">Strategic advisory covering business planning, financial forecasting, systems design, and corporate finance solutions to drive informed growth.</p>
    </div>
    <div class="svc-card">
      <div class="svc-icon">⚙️</div>
      <div class="svc-tag">Outsourcing</div>
      <div class="svc-title">Payroll &amp; Business Process</div>
      <p class="svc-desc">Reliable payroll management and business process outsourcing services that free your team to focus on what matters most — growing your business.</p>
    </div>
    <div class="svc-card">
      <div class="svc-icon">🏛️</div>
      <div class="svc-tag">Secretarial</div>
      <div class="svc-title">Company Formation &amp; Administration</div>
      <p class="svc-desc">End-to-end company formation support and ongoing secretarial administration to ensure your corporate structure remains compliant and well-managed.</p>
    </div>
    <div class="svc-card" style="background: var(--navy); border-top-color: var(--sky-lt);">
      <div class="svc-icon" style="opacity:0.2; color:#fff;">✨</div>
      <div class="svc-tag" style="background: var(--sky);">Approach</div>
      <div class="svc-title" style="color:#fff;">Tailor-Made Solutions</div>
      <p class="svc-desc" style="color:rgba(255,255,255,0.6);">Every business is unique. We take the time to understand your specific context and design solutions that fit — not off-the-shelf packages, but bespoke service for your goals.</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about-banner" id="about">
  <div class="about-left">
    <div class="section-label">About Tamweel Ltd</div>
    <h2 class="section-h2" style="color:#fff;">Professionals With Experience in Practice and Industry</h2>
    <p class="about-italic">"We are a team of professionals with wide experience in Practice and Industry providing high quality services to our clients."</p>
    <p class="section-sub">Tamweel Ltd is a Mauritius-based firm combining deep technical expertise with a genuine commitment to client success. Our multidisciplinary team delivers accounting, tax, advisory, and outsourcing services with precision and care.</p>
    <ul class="values-list">
      <li><span class="val-num">•</span> Professionalism in every engagement</li>
      <li><span class="val-num">•</span> Competency backed by industry experience</li>
      <li><span class="val-num">•</span> Integrity as our non-negotiable foundation</li>
      <li><span class="val-num">•</span> Commitment to our clients' outcomes</li>
    </ul>
  </div>
  <div class="about-right">
    <div class="stat-grid">
      <div class="stat-cell">
        <span class="stat-num">5</span>
        <span class="stat-lbl">Service Areas</span>
      </div>
      <div class="stat-cell">
        <span class="stat-num">MU</span>
        <span class="stat-lbl">Mauritius-Based</span>
      </div>
      <div class="stat-cell">
        <span class="stat-num">100%</span>
        <span class="stat-lbl">Client Focus</span>
      </div>
      <div class="stat-cell">
        <span class="stat-num">∞</span>
        <span class="stat-lbl">Commitment</span>
      </div>
    </div>
    <div class="core-values-box">
      <div class="cv-title">Core Values</div>
      <div class="cv-chips">
        <div class="cv-chip">Professionalism</div>
        <div class="cv-chip">Competency</div>
        <div class="cv-chip">Integrity</div>
        <div class="cv-chip">Commitment</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="contact-info">
    <div class="section-label">Get In Touch</div>
    <h2 class="section-h2">We're Here to Help</h2>
    <p class="section-sub">Reach out to discuss how Tamweel Ltd can support your business. Our team responds promptly and is happy to arrange a consultation.</p>

    <div class="cdet">
      <div class="cdet-icon">📍</div>
      <div class="cdet-body">
        <strong>Address</strong>
        <span>Crn. Trianon No. 1 &amp; Ave. Tulipes<br>Quatre Bornes, Mauritius</span>
      </div>
    </div>
    <div class="cdet">
      <div class="cdet-icon">📞</div>
      <div class="cdet-body">
        <strong>Telephone</strong>
        <span>(230) 5449 0217</span>
      </div>
    </div>
    <div class="cdet">
      <div class="cdet-icon">📠</div>
      <div class="cdet-body">
        <strong>Fax</strong>
        <span>(230) 465 56 20</span>
      </div>
    </div>
    <div class="cdet">
      <div class="cdet-icon">📱</div>
      <div class="cdet-body">
        <strong>Mobile</strong>
        <span>(230) 5499 1117</span>
      </div>
    </div>
    <div class="cdet">
      <div class="cdet-icon">✉</div>
      <div class="cdet-body">
        <strong>Email</strong>
        <span><a href="mailto:info@tamweelltd.com" style="color:var(--sky);text-decoration:none;">info@tamweelltd.com</a></span>
      </div>
    </div>
    <a href="https://www.facebook.com/TamweelCorporateServicesLTD" target="_blank" class="map-link">
      ↗ Visit our Facebook Page
    </a>
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
        <option>Accounting – Bookkeeping & Financial Reporting</option>
        <option>Tax – Personal & Company Tax, VAT, PAYE & TDS</option>
        <option>Advisory – Business Plan, Forecast & Corporate Finance</option>
        <option>Outsourcing – Payroll & Business Process</option>
        <option>Secretarial – Company Formation & Administration</option>
        <option>Other / General Enquiry</option>
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
      <div class="footer-brand-name">TAMWEEL LTD</div>
      <div class="footer-brand-sub">Accounting &amp; Tax Systems | Outsourcing Solutions</div>
      <p>Unmatched Tailor Made Solutions for businesses across Mauritius. Professionalism, Competency, Integrity, and Commitment — in everything we do.</p>
    </div>
    <div class="footer-col">
      <div class="footer-col-title">Our Services</div>
      <ul>
        <li><a href="#services">Accounting</a></li>
        <li><a href="#services">Tax Services</a></li>
        <li><a href="#services">Advisory</a></li>
        <li><a href="#services">Outsourcing</a></li>
        <li><a href="#services">Secretarial</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <div class="footer-col-title">Contact</div>
      <ul>
        <li><a href="tel:+23054490217">(230) 5449 0217</a></li>
        <li><a href="tel:+23054991117">(230) 5499 1117</a></li>
        <li><a href="mailto:info@tamweelltd.com">info@tamweelltd.com</a></li>
        <li><a href="https://www.facebook.com/TamweelCorporateServicesLTD" target="_blank">Facebook</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <span>&copy; 2025 Tamweel Ltd. All rights reserved. &nbsp;|&nbsp; Quatre Bornes, Mauritius</span>
    <span><a href="#">Privacy Policy</a></span>
  </div>
</footer>

</body>
</html>
