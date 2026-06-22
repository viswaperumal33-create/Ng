<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>InAmigos Foundation — Together, We Rise</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,300;9..144,500;9..144,600;9..144,700&family=Work+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@500&display=swap" rel="stylesheet">
<style>

  /* ============ TOKENS ============ */
  :root{
    --paper:#FBF6EE;
    --paper-dim:#F2EAD8;
    --ink:#1C2541;
    --ink-soft:#3A4566;
    --marigold:#E8871E;
    --marigold-light:#F4C95D;
    --terracotta:#C8553D;
    --sage:#4F7965;
    --line:rgba(28,37,65,0.12);
  }

  *{ box-sizing:border-box; margin:0; padding:0; }

  html{ scroll-behavior:smooth; }
  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ animation:none !important; transition:none !important; }
  }

  body{
    background:var(--paper);
    color:var(--ink);
    font-family:'Work Sans', sans-serif;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }

  h1,h2,h3{
    font-family:'Fraunces', serif;
    color:var(--ink);
    line-height:1.08;
    letter-spacing:-0.01em;
  }

  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.72rem;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--terracotta);
    font-weight:500;
  }

  a{ color:inherit; }
  img,svg{ display:block; max-width:100%; }
  ul{ list-style:none; }

  .wrap{
    max-width:1120px;
    margin:0 auto;
    padding:0 32px;
  }

  /* ============ GARLAND DIVIDER — signature element ============ */
  .garland{
    display:flex;
    justify-content:center;
    align-items:center;
    gap:14px;
    padding:36px 0;
  }
  .garland span{
    width:9px; height:9px;
    border-radius:50%;
    background:var(--marigold);
    opacity:0.55;
  }
  .garland span:nth-child(3n){ background:var(--terracotta); width:12px; height:12px; opacity:0.9; }
  .garland span:nth-child(4n){ background:var(--sage); opacity:0.5; }

  /* ============ HEADER ============ */
  header{
    position:sticky; top:0; z-index:50;
    background:rgba(251,246,238,0.92);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  .nav{
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 32px;
    max-width:1120px; margin:0 auto;
  }
  .wordmark{
    font-family:'Fraunces', serif;
    font-weight:600;
    font-size:1.25rem;
    display:flex; align-items:center; gap:10px;
  }
  .wordmark .dot{
    width:10px;height:10px;border-radius:50%;
    background:linear-gradient(135deg,var(--marigold),var(--terracotta));
  }
  .nav-links{
    display:flex; gap:32px; align-items:center;
    font-size:0.92rem; font-weight:500;
  }
  .nav-links a{ text-decoration:none; color:var(--ink-soft); }
  .nav-links a:hover{ color:var(--terracotta); }
  .btn{
    display:inline-block;
    font-family:'Work Sans', sans-serif;
    font-weight:600;
    font-size:0.92rem;
    padding:12px 24px;
    border-radius:100px;
    text-decoration:none;
    border:1.5px solid transparent;
    transition:transform 0.15s ease, box-shadow 0.15s ease;
  }
  .btn:hover{ transform:translateY(-2px); }
  .btn-primary{
    background:var(--terracotta);
    color:var(--paper);
    box-shadow:0 6px 18px rgba(200,85,61,0.28);
  }
  .btn-primary:hover{ box-shadow:0 10px 22px rgba(200,85,61,0.35); }
  .btn-ghost{
    border-color:var(--ink);
    color:var(--ink);
  }
  .btn-ghost:hover{ background:var(--ink); color:var(--paper); }
  .btn-light{
    background:var(--paper);
    color:var(--ink);
  }
  .nav .btn{ padding:10px 20px; font-size:0.85rem; }

  /* ============ HERO ============ */
  .hero{
    padding:80px 0 20px;
  }
  .hero-grid{
    display:grid;
    grid-template-columns:1.05fr 0.95fr;
    gap:48px;
    align-items:center;
  }
  .hero h1{
    font-size:clamp(2.4rem, 5vw, 3.6rem);
    font-weight:600;
    margin:18px 0 22px;
  }
  .hero h1 em{
    font-style:italic;
    color:var(--terracotta);
  }
  .hero p.lead{
    font-size:1.08rem;
    color:var(--ink-soft);
    max-width:46ch;
    margin-bottom:30px;
  }
  .hero-ctas{ display:flex; gap:14px; flex-wrap:wrap; }
  .hero-meta{
    display:flex; gap:28px; margin-top:38px;
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem; color:var(--ink-soft);
  }
  .hero-meta b{ display:block; font-family:'Fraunces',serif; font-size:1.4rem; color:var(--ink); font-weight:600; }

  /* Marigold mandala — signature illustration */
  .mandala-wrap{
    display:flex; align-items:center; justify-content:center;
  }
  .mandala{ width:100%; max-width:380px; animation:spin-slow 50s linear infinite; }
  @keyframes spin-slow{ from{ transform:rotate(0deg);} to{ transform:rotate(360deg);} }

  /* ============ SECTION HEADINGS ============ */
  .section{ padding:30px 0 70px; }
  .section-head{ max-width:640px; margin-bottom:48px; }
  .section-head h2{
    font-size:clamp(1.8rem,3.4vw,2.4rem);
    font-weight:600;
    margin-top:10px;
  }
  .section-head p{ color:var(--ink-soft); margin-top:14px; font-size:1.02rem; }

  /* ============ ABOUT ============ */
  .about-grid{
    display:grid;
    grid-template-columns:1.2fr 0.8fr;
    gap:56px;
    align-items:start;
  }
  .about-grid p{ color:var(--ink-soft); margin-bottom:16px; font-size:1.02rem; }
  .badges{
    display:grid; grid-template-columns:1fr 1fr; gap:12px;
  }
  .badge{
    background:var(--paper-dim);
    border:1px solid var(--line);
    border-radius:14px;
    padding:16px 16px;
    font-size:0.84rem;
    font-weight:600;
    color:var(--ink);
  }
  .badge span{
    display:block;
    font-family:'IBM Plex Mono', monospace;
    font-weight:500;
    font-size:0.68rem;
    color:var(--sage);
    text-transform:uppercase;
    letter-spacing:0.08em;
    margin-bottom:6px;
  }

  /* ============ PROJECTS ============ */
  .project-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:22px;
  }
  .card{
    background:#fff;
    border:1px solid var(--line);
    border-radius:18px;
    padding:30px 26px;
    transition:transform 0.2s ease, box-shadow 0.2s ease;
  }
  .card:hover{
    transform:translateY(-5px);
    box-shadow:0 16px 30px rgba(28,37,65,0.08);
  }
  .icon-circle{
    width:52px; height:52px;
    border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    background:var(--paper-dim);
    margin-bottom:18px;
  }
  .card h3{
    font-size:1.2rem;
    font-weight:600;
    margin-bottom:6px;
  }
  .card .tag{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.68rem;
    text-transform:uppercase;
    letter-spacing:0.08em;
    color:var(--marigold);
    font-weight:500;
    display:block;
    margin-bottom:10px;
  }
  .card p{ color:var(--ink-soft); font-size:0.94rem; }

  /* ============ IMPACT ============ */
  .impact{
    background:var(--ink);
    color:var(--paper);
    border-radius:28px;
    padding:64px 48px;
  }
  .impact .eyebrow{ color:var(--marigold-light); }
  .impact h2{ color:var(--paper); }
  .impact-grid{
    display:grid;
    grid-template-columns:repeat(4, 1fr);
    gap:30px;
    margin:44px 0 40px;
  }
  .stat b{
    display:block;
    font-family:'Fraunces', serif;
    font-size:2.4rem;
    font-weight:600;
    color:var(--marigold-light);
  }
  .stat span{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.74rem;
    text-transform:uppercase;
    letter-spacing:0.07em;
    color:rgba(251,246,238,0.65);
  }
  .impact-text{
    max-width:62ch;
    color:rgba(251,246,238,0.82);
    font-size:1.02rem;
    border-top:1px solid rgba(251,246,238,0.18);
    padding-top:32px;
  }

  /* ============ CTA ============ */
  .cta{
    background:linear-gradient(135deg, var(--marigold) 0%, var(--terracotta) 100%);
    border-radius:28px;
    padding:64px 48px;
    color:var(--paper);
    text-align:center;
  }
  .cta h2{ color:var(--paper); font-size:clamp(2rem,4vw,2.8rem); }
  .cta p{
    max-width:50ch; margin:18px auto 32px;
    color:rgba(251,246,238,0.92);
    font-size:1.05rem;
  }
  .cta-ctas{ display:flex; gap:14px; justify-content:center; flex-wrap:wrap; }
  .cta .btn-ghost{ border-color:var(--paper); color:var(--paper); }
  .cta .btn-ghost:hover{ background:var(--paper); color:var(--terracotta); }

  /* ============ FOOTER ============ */
  footer{
    background:var(--ink);
    color:rgba(251,246,238,0.75);
    padding:56px 0 28px;
    margin-top:60px;
  }
  .footer-grid{
    display:grid;
    grid-template-columns:1.3fr 1fr 1fr;
    gap:40px;
    padding-bottom:36px;
    border-bottom:1px solid rgba(251,246,238,0.15);
  }
  footer h4{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.72rem;
    text-transform:uppercase;
    letter-spacing:0.1em;
    color:var(--marigold-light);
    margin-bottom:16px;
  }
  footer .wordmark{ color:var(--paper); margin-bottom:14px; }
  footer p{ font-size:0.9rem; max-width:34ch; }
  footer ul li{ margin-bottom:9px; font-size:0.9rem; }
  footer a{ text-decoration:none; }
  footer a:hover{ color:var(--marigold-light); }
  .cert-row{ display:flex; flex-wrap:wrap; gap:8px; }
  .cert-pill{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.68rem;
    border:1px solid rgba(251,246,238,0.25);
    padding:6px 12px;
    border-radius:100px;
  }
  .bottom-row{
    display:flex; justify-content:space-between; align-items:center;
    padding-top:24px;
    font-size:0.8rem;
    color:rgba(251,246,238,0.5);
    flex-wrap:wrap; gap:10px;
  }

  /* ============ RESPONSIVE ============ */
  @media (max-width: 860px){
    .nav-links{ display:none; }
    .hero-grid{ grid-template-columns:1fr; }
    .mandala-wrap{ order:-1; }
    .mandala{ max-width:230px; }
    .about-grid{ grid-template-columns:1fr; gap:32px; }
    .project-grid{ grid-template-columns:1fr 1fr; }
    .impact-grid{ grid-template-columns:1fr 1fr; }
    .footer-grid{ grid-template-columns:1fr; gap:28px; }
    .impact, .cta{ padding:44px 26px; border-radius:20px; }
  }
  @media (max-width: 540px){
    .wrap{ padding:0 20px; }
    .project-grid{ grid-template-columns:1fr; }
    .impact-grid{ grid-template-columns:1fr 1fr; gap:22px; }
    .hero{ padding:50px 0 10px; }
    .hero-ctas .btn, .cta-ctas .btn{ width:100%; text-align:center; }
    .bottom-row{ flex-direction:column; align-items:flex-start; }
  }
</style>
</head>
<body>

<header>
  <nav class="nav">
    <div class="wordmark"><span class="dot"></span> InAmigos Foundation</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#impact">Impact</a></li>
      <li><a href="#join">Join Us</a></li>
    </ul>
    <a href="#join" class="btn btn-primary">Donate</a>
  </nav>
</header>

<main>

  <!-- ============ HERO ============ -->
  <section class="hero wrap">
    <div class="hero-grid">
      <div>
        <p class="eyebrow">Grassroots NGO · Bilaspur, Chhattisgarh</p>
        <h1>Compassion, <em>turned</em><br>into action.</h1>
        <p class="lead">InAmigos Foundation is a community of volunteers feeding the hungry, educating children, empowering women, protecting animals, and healing the environment — across 28 states and counting.</p>
        <div class="hero-ctas">
          <a href="#join" class="btn btn-primary">Volunteer With Us</a>
          <a href="#projects" class="btn btn-ghost">See Our Projects</a>
        </div>
        <div class="hero-meta">
          <div><b>2020</b> Founded</div>
          <div><b>28</b> States Reached</div>
          <div><b>6</b> Active Projects</div>
        </div>
      </div>

      <div class="mandala-wrap">
        <svg class="mandala" viewBox="0 0 400 400" fill="none">
          <circle cx="200" cy="200" r="190" stroke="#E8871E" stroke-opacity="0.25" stroke-width="1"/>
          <g>
            <!-- 12 marigold petals -->
            <g fill="#F4C95D">
              <ellipse cx="200" cy="70" rx="20" ry="42"/>
            </g>
          </g>
          <!-- generate petal ring via repeated rotated groups -->
          <g>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#F4C95D" transform="rotate(0 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#EFA63A" transform="rotate(30 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#F4C95D" transform="rotate(60 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#EFA63A" transform="rotate(90 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#F4C95D" transform="rotate(120 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#EFA63A" transform="rotate(150 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#F4C95D" transform="rotate(180 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#EFA63A" transform="rotate(210 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#F4C95D" transform="rotate(240 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#EFA63A" transform="rotate(270 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#F4C95D" transform="rotate(300 200 200)"/>
            <ellipse cx="200" cy="70" rx="18" ry="40" fill="#EFA63A" transform="rotate(330 200 200)"/>
          </g>
          <circle cx="200" cy="200" r="58" fill="#C8553D"/>
          <circle cx="200" cy="200" r="58" fill="none" stroke="#1C2541" stroke-opacity="0.06" stroke-width="10"/>
          <text x="200" y="195" text-anchor="middle" fill="#FBF6EE" font-family="Fraunces, serif" font-size="15" font-weight="600">TOGETHER</text>
          <text x="200" y="216" text-anchor="middle" fill="#FBF6EE" font-family="Fraunces, serif" font-size="15" font-weight="600">WE RISE</text>
        </svg>
      </div>
    </div>
  </section>

  <div class="garland">
    <span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span>
  </div>

  <!-- ============ ABOUT ============ -->
  <section class="section wrap" id="about">
    <div class="about-grid">
      <div>
        <p class="eyebrow">Who We Are</p>
        <h2 style="margin-bottom:20px;">A small circle of volunteers, grown into a movement.</h2>
        <p>InAmigos Foundation was founded on 23 September 2020 by Govind Shukla, who set out to prove that a handful of committed people could make a measurable dent in hunger, illiteracy, and inequality. Headquartered in Bilaspur, Chhattisgarh, the foundation is registered as a Section 8 non-profit under the Central Government.</p>
        <p>What started locally has since reached communities across 28 states, powered by a growing network of volunteers, content creators, designers, and interns who believe that consistency — not scale — is what changes lives.</p>
        <p>We exist because dignity shouldn't depend on circumstance. Every project we run is built around one question: what does this community need to stand a little taller today?</p>
      </div>
      <div class="badges">
        <div class="badge"><span>Certification</span>80G &amp; 12A Certified</div>
        <div class="badge"><span>Registration</span>CSR-1 Registered</div>
        <div class="badge"><span>Government</span>NITI Aayog Listed</div>
        <div class="badge"><span>Quality</span>ISO 9001:2015</div>
        <div class="badge"><span>Transparency</span>NGO Darpan Registered</div>
        <div class="badge"><span>Reach</span>28 States Across India</div>
      </div>
    </div>
  </section>

  <div class="garland">
    <span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span><span></span>
  </div>

  <!-- ============ PROJECTS ============ -->
  <section class="section wrap" id="projects">
    <div class="section-head">
      <p class="eyebrow">Where Your Support Goes</p>
      <h2>Six causes, one mission.</h2>
      <p>Each project closes a specific gap. Together, they form a complete circle of care — from a meal on the table to a tree in the ground.</p>
    </div>

    <div class="project-grid">

      <div class="card">
        <div class="icon-circle">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#C8553D" stroke-width="1.6">
            <path d="M5 3v8a3 3 0 0 0 3 3v7" stroke-linecap="round"/>
            <path d="M9 3v6M5 3v6" stroke-linecap="round"/>
            <path d="M16 3c-2 1-3 3.5-3 6 0 2 1 3 1 3v9" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <span class="tag">Project SEVA</span>
        <h3>Food &amp; Clothing</h3>
        <p>Hunger doesn't wait. SEVA has delivered 50,000+ meals and essential clothing to underserved families — restoring nutrition, and dignity, in the same hand.</p>
      </div>

      <div class="card">
        <div class="icon-circle">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#C8553D" stroke-width="1.6">
            <path d="M4 19V6a2 2 0 0 1 2-2h5v16H6a2 2 0 0 1-2-2Z" stroke-linejoin="round"/>
            <path d="M20 19V6a2 2 0 0 0-2-2h-5v16h5a2 2 0 0 0 2-2Z" stroke-linejoin="round"/>
          </svg>
        </div>
        <span class="tag">Project Bachpanshala</span>
        <h3>Education</h3>
        <p>Every child deserves a fair shot. Bachpanshala delivers digital literacy, life skills, and school support to underprivileged children.</p>
      </div>

      <div class="card">
        <div class="icon-circle">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#C8553D" stroke-width="1.6">
            <circle cx="12" cy="7" r="3.5"/>
            <path d="M5 21c0-4 3-7 7-7s7 3 7 7" stroke-linecap="round"/>
          </svg>
        </div>
        <span class="tag">Project Udaan</span>
        <h3>Women Empowerment</h3>
        <p>Independence starts with a skill. Udaan trains women in livelihood skills and financial literacy so they can build income on their own terms.</p>
      </div>

      <div class="card">
        <div class="icon-circle">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#4F7965" stroke-width="1.6">
            <path d="M12 22s7-5.5 7-12a7 7 0 0 0-14 0c0 6.5 7 12 7 12Z" stroke-linejoin="round"/>
            <path d="M12 6v8M9 9l3-3 3 3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <span class="tag">Project Prakriti</span>
        <h3>Environment</h3>
        <p>The planet is everyone's responsibility. Prakriti runs plantations, clean-up drives, and sustainability awareness for the generations after us.</p>
      </div>

      <div class="card">
        <div class="icon-circle">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#C8553D" stroke-width="1.6">
            <rect x="3" y="8" width="18" height="12" rx="2"/>
            <path d="M9 8V6a3 3 0 0 1 6 0v2" stroke-linecap="round"/>
          </svg>
        </div>
        <span class="tag">Project Vikas</span>
        <h3>Skill Development</h3>
        <p>A skill is a door to employment. Vikas equips youth with practical, job-ready training to build careers, not just resumes.</p>
      </div>

      <div class="card">
        <div class="icon-circle">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none" stroke="#4F7965" stroke-width="1.6">
            <circle cx="7" cy="6" r="1.6"/><circle cx="12" cy="4.5" r="1.6"/><circle cx="17" cy="6" r="1.6"/>
            <path d="M9 13c0-2 1.5-3.5 3-3.5s3 1.5 3 3.5c0 2.5-2 3-2 5.5a1 1 0 0 1-2 0c0-2.5-2-3-2-5.5Z" stroke-linejoin="round"/>
          </svg>
        </div>
        <span class="tag">Project Jeev</span>
        <h3>Animal Welfare</h3>
        <p>Compassion includes every living being. Jeev supports feeding drives, rescue efforts, and awareness for stray and injured animals.</p>
      </div>

    </div>
  </section>

  <!-- ============ IMPACT ============ -->
  <section class="section wrap" id="impact">
    <div class="impact">
      <p class="eyebrow">Why It Matters</p>
      <h2>Impact, measured in lives — not likes.</h2>

      <div class="impact-grid">
        <div class="stat"><b>50,000+</b><span>Meals &amp; clothing distributed</span></div>
        <div class="stat"><b>28</b><span>States reached across India</span></div>
        <div class="stat"><b>28+</b><span>Active on-ground volunteers</span></div>
        <div class="stat"><b>6</b><span>Flagship projects running</span></div>
      </div>

      <p class="impact-text">We don't measure success by donations collected — we measure it in meals eaten, classes attended, skills learned, trees planted, and animals cared for. Every project is built to close one specific gap in society, and together they form a complete ecosystem of care: from a child's first lesson to a woman's first paycheck to a stray's first proper meal.</p>
    </div>
  </section>

  <!-- ============ CTA / JOIN US ============ -->
  <section class="section wrap" id="join">
    <div class="cta">
      <p class="eyebrow" style="color:rgba(251,246,238,0.85)">Be Part of the Circle</p>
      <h2>Your time, skill, or ₹200 — all of it counts.</h2>
      <p>Whether you volunteer on the ground, lend your skills online, or give what you can, you become part of a movement rebuilding dignity one act of kindness at a time.</p>
      <div class="cta-ctas">
        <a href="https://inamigosfoundation.org.in/" class="btn btn-light">Donate Now</a>
        <a href="https://inamigosfoundation.org.in/" class="btn btn-ghost">Volunteer With Us</a>
        <a href="https://www.instagram.com/inamigos/" class="btn btn-ghost">Follow Our Work</a>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">
    <div class="footer-grid">
      <div>
        <div class="wordmark"><span class="dot"></span> InAmigos Foundation</div>
        <p>A Section 8 registered non-profit based in Bilaspur, Chhattisgarh, working across education, food security, women's empowerment, animal welfare, and the environment.</p>
      </div>
      <div>
        <h4>Explore</h4>
        <ul>
          <li><a href="#about">About Us</a></li>
          <li><a href="#projects">Our Projects</a></li>
          <li><a href="#impact">Our Impact</a></li>
          <li><a href="#join">Get Involved</a></li>
        </ul>
      </div>
      <div>
        <h4>Connect</h4>
        <ul>
          <li><a href="https://inamigosfoundation.org.in/" target="_blank" rel="noopener">Official Website</a></li>
          <li><a href="https://www.instagram.com/inamigos/" target="_blank" rel="noopener">Instagram</a></li>
          <li><a href="https://www.facebook.com/InAmigos/" target="_blank" rel="noopener">Facebook</a></li>
          <li><a href="https://in.linkedin.com/company/inamigos-foundation" target="_blank" rel="noopener">LinkedIn</a></li>
        </ul>
      </div>
    </div>

    <div class="cert-row" style="margin-top:28px;">
      <span class="cert-pill">80G &amp; 12A</span>
      <span class="cert-pill">CSR-1 Registered</span>
      <span class="cert-pill">NITI Aayog Listed</span>
      <span class="cert-pill">ISO 9001:2015</span>
      <span class="cert-pill">NGO Darpan</span>
    </div>

    <div class="bottom-row">
      <span>© 2026 InAmigos Foundation · Bilaspur, Chhattisgarh, India</span>
      <span>Awareness webpage by Viswa Permal · InAmigos Foundation Internship Program</span>
    </div>
  </div>
</footer>

</body>
</html>
