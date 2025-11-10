---
layout: home
title: "Dr. Domenico Marco Stillitano"
description: "Chirurgia vascolare ed endovascolare – Monza e Milano"
---

<html lang="it">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />

<title>{{ page.title }}</title>
<meta name="description" content="{{ page.description }}">

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Merriweather:wght@400;700&display=swap" rel="stylesheet">

<style>
:root{
  --accent:#0ea5e9;
  --accent-2:#10b981;
  --ink:#1e293b;
  --ink-2:#0f172a;
  --muted:#637287;
  --card:#f8fafc;
  --line:#e5e7eb;
  --radius:1rem;
  --shadow:0 10px 30px rgba(0,0,0,.08);
}

/* Global */
body{
  margin:0;
  font-family:Inter,ui-sans-serif,system-ui;
  color:var(--ink);
  background:#fff;
  line-height:1.55;
}
.container{
  width:min(1100px, 90%);
  margin-inline:auto;
}

/* Header (ghost sticky) */
.site-header{
  position:fixed;
  inset:0 0 auto 0;
  height:64px;
  display:flex;
  align-items:center;
  z-index:60;
  padding-inline: clamp(1rem, 2vw, 2rem);
  background:rgba(255,255,255,.6);
  backdrop-filter: blur(10px);
  border-bottom:1px solid rgba(15,23,42,.08);
  transform:translateY(-100%);
  transition: transform .45s ease;
}
.site-header.is-stuck{
  transform:translateY(0);
}
.site-header .brand{
  font-weight:800;
  color:var(--ink-2);
}
.site-header nav{
  margin-left:auto;
  display:flex;
  gap:.9rem;
}
.site-header nav a{
  text-decoration:none;
  color:var(--ink);
  padding:.45rem .75rem;
  border-radius:999px;
  border:1px solid transparent;
  font-weight:600;
}
.site-header nav a:hover{
  border-color:rgba(14,165,233,.35);
  background:rgba(255,255,255,.7);
}

/* HERO */
.hero{
  min-height:90vh;
  display:grid;
  align-items:center;
  padding-top:64px;
  background:
    radial-gradient(900px 600px at 82% 8%, rgba(16,185,129,.10), transparent 70%),
    linear-gradient(#ffffff, #f8fbff);
}
.hero .grid{
  display:grid;
  gap:2rem;
}
@media(min-width:900px){
  .hero .grid{
    grid-template-columns:1fr 1fr;
    gap:3rem;
  }
}

.kicker{
  text-transform:uppercase;
  letter-spacing:.12em;
  font-size:.8rem;
  font-weight:700;
  color:var(--accent-2);
}
.hero h1{
  font-family:Merriweather,serif;
  font-size:clamp(2.2rem,4vw,3.2rem);
  margin:.5rem 0 .9rem;
  color:var(--ink-2);
}
.hero .sub{
  font-size:1.15rem;
  color:#2b3553;
  opacity:.95;
}

.cta{
  display:flex;
  gap:.75rem;
  flex-wrap:wrap;
  margin-top:1.2rem;
}
.btn{
  display:inline-flex;
  gap:.45rem;
  align-items:center;
  justify-content:center;
  text-decoration:none;
  padding:.9rem 1.2rem;
  font-weight:700;
  border-radius:1rem;
  border:2px solid transparent;
  box-shadow:var(--shadow);
  transition:.15s ease;
}
.btn-primary{
  background:linear-gradient(135deg, var(--accent), #22d3ee);
  color:#001018;
}
.btn-secondary{
  background:linear-gradient(135deg, var(--accent-2), #34d399);
  color:#001812;
}
.btn:hover{
  transform:translateY(-1px);
  box-shadow:0 12px 28px rgba(0,0,0,.12);
}

/* Portrait circolare */
.hero-visual{
  margin-inline:auto;
  max-width:420px;
  aspect-ratio:1/1;
  border-radius:50%;
  overflow:hidden;
  box-shadow:0 30px 60px rgba(0,0,0,.12);
}
.hero-visual img{
  width:100%;
  height:100%;
  object-fit:cover;
}

/* Pill nav */
.pill-menu-wrapper{
  position:sticky;
  top:0;
  z-index:50;
  background:rgba(255,255,255,.82);
  backdrop-filter:blur(10px);
  border-bottom:1px solid rgba(15,23,42,.1);
  padding:.85rem 0;
}
.pill-menu{
  display:flex;
  gap:.5rem;
  flex-wrap:wrap;
  justify-content:center;
}
.pill{
  font-weight:700;
  color:#0f172a;
  padding:.6rem .95rem;
  border-radius:999px;
  text-decoration:none;
  background:rgba(255,255,255,.9);
  border:1px solid rgba(15,23,42,.15);
}
.pill:hover{
  border-color:rgba(14,165,233,.4);
  box-shadow:0 0 0 2px rgba(14,165,233,.18);
}

/* Content */
.section{
  padding:clamp(2.2rem,6vw,4rem) 0;
}
.lead{
  color:var(--muted);
  font-size:1rem;
}

/* Cards */
.cards{
  display:grid;
  grid-template-columns:repeat(12,1fr);
  gap:1rem;
  margin-top:1.5rem;
}
.card{
  grid-column:span 12;
  background:var(--card);
  border:1px solid var(--line);
  border-radius:var(--radius);
  box-shadow:var(--shadow);
  padding:1.25rem;
}
.card h3{
  margin-top:.25rem;
  font-size:1.2rem;
  color:var(--ink-2);
}
.card p{
  color:var(--muted)
}
@media(min-width:740px){
  .card{ grid-column:span 4 }
}

/* Contact */
.contact{
  background:linear-gradient(#f8fbff,#ffffff);
}
.contact .grid{
  display:grid;
  gap:1rem;
}
@media(min-width:840px){
  .contact .grid{
    grid-template-columns:1.1fr .9fr;
  }
}
.box{
  background:#fff;
  border:1px solid var(--line);
  border-radius:var(--radius);
  box-shadow:var(--shadow);
  padding:1.25rem;
}

/* Reveal */
.reveal{
  opacity:0;
  transform:translateY(12px);
  transition:.55s ease;
}
.reveal.is-in{
  opacity:1;
  transform:none;
}
</style>

</head>
<body>

<header class="site-header" id="siteHeader">
  <div class="brand">Dr. Stillitano</div>
  <nav>
    <a href="/aree-di-competenza/">Aree</a>
    <a href="#servizi">Servizi</a>
    <a href="#contatti">Contatti</a>
    <a href="#prenota">Prenota</a>
  </nav>
</header>

<section class="hero">
  <div class="container">
    <div class="grid">
      <div class="copy reveal">
        <div class="kicker">Chirurgia vascolare</div>
        <h1>{{ page.title }}</h1>
        <p class="sub">{{ page.subtitle }}</p>

        <div class="cta">
          <a class="btn btn-primary" href="#prenota">Prenota online</a>
          <a class="btn btn-secondary" href="https://wa.me/393758707109" target="_blank" rel="noopener">WhatsApp</a>
        </div>
      </div>

      <figure class="hero-visual reveal">
        <img src="/assets/images/hero.jpg" alt="Foto Dr. Stillitano">
      </figure>
    </div>
  </div>
</section>

<div class="pill-menu-wrapper">
  <div class="container pill-menu">
    <a class="pill" href="/aree-di-competenza/">Aree di competenza</a>
    <a class="pill" href="#servizi">Servizi</a>
    <a class="pill" href="#contatti">Contatti</a>
    <a class="pill" href="#prenota">Prenota</a>
  </div>
</div>

<section class="section" id="servizi">
  <div class="container">
    <h2 class="reveal">Prenditi cura della tua salute</h2>
    <p class="lead reveal">Consulenze e visite specialistiche di <strong>chirurgia vascolare</strong>…</p>

    <div class="cards">
      <article class="card reveal">
        <h3>Consulenza e valutazione referti online</h3>
        <p>Interpretazione esami e referti…</p>
        <a class="btn btn-primary" href="/aree/referti-online/">Approfondisci</a>
      </article>

      <article class="card reveal">
        <h3>Visita e consulto in videochiamata</h3>
        <p>Ideale per pazienti con difficoltà…</p>
        <a class="btn btn-primary" href="/prenota/#video">Approfondisci</a>
      </article>

      <article class="card reveal">
        <h3>Piano terapeutico personalizzato</h3>
        <p>Strategia medico-chirurgica…</p>
        <a class="btn btn-primary" href="/aree/piano-terapeutico/">Approfondisci</a>
      </article>
    </div>
  </div>
</section>

<section class="section contact" id="contatti">
  <div class="container grid">
    <div class="box reveal">
      <h2>Contatta il Dr. Stillitano</h2>
      <div>
        <strong>Politerapico di Monza</strong><br>Via Gerolamo Borgazzi, 87B — 20900 Monza (MB)
      </div>
      <div><strong>Tel:</strong> <a href="tel:+393758707109">+39 375 870 7109</a></div>
      <div><strong>Email:</strong> <a href="mailto:domenicomarco.stillitano@gmail.com">domenicomarco.stillitano@gmail.com</a></div>
    </div>

    <div class="box reveal" id="prenota">
      <h2>Prenota</h2>
      <p class="lead">Chiama o WhatsApp per disponibilità.</p>

      <div class="cta">
        <a class="btn btn-primary" href="tel:+393758707109">Chiama ora</a>
        <a class="btn btn-secondary" href="https://wa.me/393758707109" target="_blank" rel="noopener">WhatsApp</a>
      </div>
    </div>
  </div>
</section>

<script>
(function(){
  const header = document.getElementById('siteHeader');
  const onScroll = ()=>{
    header.classList.toggle('is-stuck', (window.scrollY || window.pageYOffset) > 50);
  };
  onScroll();
  window.addEventListener('scroll', onScroll, {passive:true});

  const reveals = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window) {
    const io = new IntersectionObserver(entries=>{
      entries.forEach(e=>{
        if(e.isIntersecting){
          e.target.classList.add('is-in');
          io.unobserve(e.target);
        }
      })
    },{ threshold: .1 });
    reveals.forEach(el=> io.observe(el));
  } else {
    reveals.forEach(el=> el.classList.add('is-in'));
  }
})();
</script>

</body>
</html>
