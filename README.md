<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#f8f5ee">
  <meta name="description" content="Morrow Coffee — thoughtfully sourced coffee, made fresh in your neighborhood.">
  <title>Morrow Coffee — Good coffee. Better mornings.</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@500;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --paper: #f8f5ee;
      --paper-deep: #eee8dc;
      --ink: #29241f;
      --muted: #746d63;
      --coffee: #573b2b;
      --coffee-dark: #34251d;
      --olive: #64715b;
      --accent: #d39a58;
      --line: rgba(41, 36, 31, .13);
      --serif: "Playfair Display", Georgia, serif;
      --sans: "DM Sans", Arial, sans-serif;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; scroll-padding-top: 88px; }
    body {
      margin: 0;
      color: var(--ink);
      background: var(--paper);
      font-family: var(--sans);
      -webkit-font-smoothing: antialiased;
    }
    a { color: inherit; text-decoration: none; }
    button { font: inherit; }
    img { display: block; max-width: 100%; }
    .shell { width: min(1160px, calc(100% - 48px)); margin-inline: auto; }

    .topline {
      min-height: 34px;
      display: grid;
      place-items: center;
      padding: 7px 20px;
      color: #f8f5ee;
      background: var(--coffee-dark);
      text-align: center;
      font-size: 10px;
      letter-spacing: .19em;
      text-transform: uppercase;
    }
    .site-header {
      position: sticky;
      z-index: 10;
      top: 0;
      background: rgba(248, 245, 238, .91);
      border-bottom: 1px solid var(--line);
      backdrop-filter: blur(14px);
    }
    .nav {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 28px;
    }
    .brand {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      flex-shrink: 0;
      font-family: var(--serif);
      font-size: 23px;
      font-weight: 700;
      letter-spacing: -.04em;
    }
    .brand-mark {
      width: 31px;
      height: 31px;
      display: grid;
      place-items: center;
      color: var(--paper);
      background: var(--coffee);
      border-radius: 50%;
    }
    .brand-mark svg { width: 17px; height: 17px; }
    .nav-links { display: flex; align-items: center; gap: clamp(18px, 3vw, 38px); }
    .nav-links a {
      color: #554d45;
      font-size: 12px;
      transition: color .2s ease;
    }
    .nav-links a:hover { color: var(--accent); }
    .nav-cta, .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      min-height: 45px;
      padding: 0 20px;
      color: var(--paper);
      background: var(--coffee);
      border: 1px solid var(--coffee);
      border-radius: 3px;
      font-size: 11px;
      font-weight: 600;
      letter-spacing: .08em;
      text-transform: uppercase;
      transition: background .2s ease, transform .2s ease, border-color .2s ease;
    }
    .nav-cta:hover, .button:hover { background: var(--coffee-dark); border-color: var(--coffee-dark); transform: translateY(-2px); }
    .nav-cta svg, .button svg { width: 14px; height: 14px; }

    .hero {
      position: relative;
      min-height: 600px;
      display: grid;
      grid-template-columns: 1fr .96fr;
      align-items: center;
      gap: 46px;
      padding-block: 66px 78px;
    }
    .hero-copy { position: relative; z-index: 1; padding: 16px 0 20px; }
    .eyebrow {
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 0 0 22px;
      color: var(--olive);
      font-size: 10px;
      font-weight: 700;
      letter-spacing: .2em;
      text-transform: uppercase;
    }
    .eyebrow::before { width: 26px; height: 1px; content: ""; background: currentColor; }
    h1, h2, h3, p { margin-top: 0; }
    h1 {
      max-width: 590px;
      margin-bottom: 22px;
      font-family: var(--serif);
      font-size: clamp(55px, 7.2vw, 88px);
      font-weight: 500;
      letter-spacing: -.065em;
      line-height: .99;
    }
    h1 em { color: var(--coffee); font-weight: 500; }
    .hero-copy > p:not(.eyebrow) {
      max-width: 420px;
      margin-bottom: 30px;
      color: var(--muted);
      font-size: 14px;
      line-height: 1.9;
    }
    .hero-actions { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
    .text-link {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      color: var(--ink);
      font-size: 11px;
      font-weight: 600;
      letter-spacing: .04em;
    }
    .text-link svg { width: 15px; height: 15px; transition: transform .2s ease; }
    .text-link:hover svg { transform: translateX(4px); }
    .hero-note {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-top: 56px;
      color: var(--muted);
      font-size: 10px;
      letter-spacing: .03em;
    }
    .avatar-stack { display: flex; padding-left: 6px; }
    .avatar-stack span {
      width: 26px;
      height: 26px;
      display: grid;
      place-items: center;
      margin-left: -6px;
      color: #fff;
      background: var(--olive);
      border: 2px solid var(--paper);
      border-radius: 50%;
      font-family: var(--serif);
      font-size: 10px;
    }
    .avatar-stack span:nth-child(2) { background: #b56f4d; }
    .avatar-stack span:nth-child(3) { background: #bd9a64; }

    .hero-visual {
      position: relative;
      min-height: 465px;
      animation: float-in .9s .12s both cubic-bezier(.2,.7,.2,1);
    }
    .hero-photo {
      position: absolute;
      inset: 0 24px 14px 0;
      overflow: hidden;
      background: #cbbba7;
      border-radius: 48% 48% 3px 3px / 39% 39% 3px 3px;
    }
    .hero-photo img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: 52% center;
      animation: photo-drift 18s ease-in-out infinite alternate;
    }
    .hero-photo::after {
      position: absolute;
      inset: 30% 0 0;
      content: "";
      background: linear-gradient(transparent, rgba(32, 22, 15, .42));
    }
    .photo-caption {
      position: absolute;
      z-index: 1;
      right: 35px;
      bottom: 37px;
      left: 30px;
      color: #fffaf2;
    }
    .photo-caption small { display: block; margin-bottom: 6px; font-size: 9px; letter-spacing: .17em; text-transform: uppercase; }
    .photo-caption strong { font-family: var(--serif); font-size: 24px; font-weight: 500; }
    .floating-stamp {
      position: absolute;
      z-index: 2;
      top: 45px;
      right: -3px;
      width: 102px;
      height: 102px;
      display: grid;
      place-items: center;
      color: var(--paper);
      background: var(--olive);
      border: 6px solid var(--paper);
      border-radius: 50%;
      text-align: center;
      transform: rotate(9deg);
      animation: stamp-in .7s .65s both cubic-bezier(.2,.8,.2,1.3);
    }
    .floating-stamp span { max-width: 65px; font-family: var(--serif); font-size: 12px; line-height: 1.2; }
    .floating-stamp b { display: block; margin-top: 3px; font-family: var(--sans); font-size: 8px; font-weight: 500; letter-spacing: .16em; text-transform: uppercase; }
    .hero-visual::before {
      position: absolute;
      z-index: -1;
      right: -14px;
      bottom: -2px;
      width: 75%;
      height: 70%;
      content: "";
      border: 1px solid rgba(100, 113, 91, .36);
      border-radius: 48% 48% 3px 3px / 39% 39% 3px 3px;
    }

    .ticker {
      overflow: hidden;
      padding-block: 16px;
      color: var(--paper);
      background: var(--olive);
    }
    .ticker-track {
      width: max-content;
      display: flex;
      align-items: center;
      gap: 27px;
      animation: ticker 34s linear infinite;
    }
    .ticker span { font-family: var(--serif); font-size: 16px; font-style: italic; }
    .ticker i { color: #e5c69d; font-size: 12px; font-style: normal; }

    .section { padding-block: 104px; }
    .section-heading {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 28px;
      margin-bottom: 37px;
    }
    .section-heading .eyebrow { margin-bottom: 12px; }
    h2 {
      margin-bottom: 0;
      font-family: var(--serif);
      font-size: clamp(39px, 5vw, 57px);
      font-weight: 500;
      letter-spacing: -.05em;
      line-height: 1.08;
    }
    .section-heading > p {
      max-width: 290px;
      margin-bottom: 3px;
      color: var(--muted);
      font-size: 12px;
      line-height: 1.8;
    }
    .menu-section { padding-top: 92px; }
    .menu-controls { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 24px; }
    .filter {
      min-height: 34px;
      padding: 0 14px;
      color: var(--muted);
      background: transparent;
      border: 1px solid var(--line);
      border-radius: 99px;
      cursor: pointer;
      font-size: 10px;
      transition: color .2s ease, background .2s ease, border-color .2s ease;
    }
    .filter:hover, .filter[aria-pressed="true"] { color: #fff; background: var(--coffee); border-color: var(--coffee); }
    .menu-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; }
    .menu-card {
      position: relative;
      min-height: 230px;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding: 22px 20px 20px;
      background: rgba(255, 255, 255, .52);
      border: 1px solid var(--line);
      transition: transform .25s ease, background .25s ease, box-shadow .25s ease;
    }
    .menu-card:hover { z-index: 1; background: #fffdf9; box-shadow: 0 18px 38px rgba(55, 41, 30, .08); transform: translateY(-5px); }
    .menu-card[hidden] { display: none; }
    .card-top { width: 100%; display: flex; align-items: center; justify-content: space-between; margin-bottom: 25px; }
    .cup-art {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      color: var(--coffee);
      background: #efe8db;
      border-radius: 50%;
    }
    .cup-art svg { width: 21px; height: 21px; }
    .tag { color: var(--olive); font-size: 8px; font-weight: 700; letter-spacing: .14em; text-transform: uppercase; }
    .menu-card h3 { margin-bottom: 7px; font-family: var(--serif); font-size: 19px; font-weight: 600; letter-spacing: -.02em; }
    .menu-card p { min-height: 36px; margin-bottom: 15px; color: var(--muted); font-size: 10px; line-height: 1.7; }
    .card-bottom { width: 100%; display: flex; align-items: center; justify-content: space-between; margin-top: auto; padding-top: 12px; border-top: 1px solid var(--line); }
    .price { font-family: var(--serif); font-size: 20px; font-weight: 600; }
    .size { color: var(--muted); font-size: 9px; letter-spacing: .08em; text-transform: uppercase; }
    .menu-footnote { margin: 19px 0 0; color: var(--muted); font-size: 10px; }

    .story {
      position: relative;
      overflow: hidden;
      color: var(--paper);
      background: var(--coffee-dark);
    }
    .story::after {
      position: absolute;
      top: -150px;
      right: -85px;
      width: 450px;
      height: 450px;
      content: "";
      border: 1px solid rgba(248, 245, 238, .13);
      border-radius: 50%;
      box-shadow: 0 0 0 35px rgba(248,245,238,.025), 0 0 0 70px rgba(248,245,238,.025);
      pointer-events: none;
    }
    .story-inner { position: relative; z-index: 1; display: grid; grid-template-columns: .92fr 1fr; align-items: center; gap: 90px; }
    .story-photo {
      position: relative;
      min-height: 415px;
      overflow: hidden;
      background: #594638;
    }
    .story-photo img { width: 100%; height: 100%; position: absolute; inset: 0; object-fit: cover; }
    .story-photo::after { position: absolute; inset: 0; content: ""; background: linear-gradient(30deg, rgba(32, 22, 15, .23), transparent 60%); }
    .story .eyebrow { color: #cbb48e; }
    .story h2 { max-width: 470px; margin-bottom: 20px; }
    .story-copy > p:not(.eyebrow) { max-width: 420px; color: rgba(248, 245, 238, .68); font-size: 12px; line-height: 2; }
    .story-points { display: grid; grid-template-columns: 1fr 1fr; gap: 18px; margin: 29px 0 30px; }
    .story-point { padding-top: 14px; border-top: 1px solid rgba(248,245,238,.2); }
    .story-point strong { display: block; margin-bottom: 5px; font-family: var(--serif); font-size: 17px; font-weight: 500; }
    .story-point span { color: rgba(248, 245, 238, .55); font-size: 9px; letter-spacing: .06em; }
    .button-light { color: var(--coffee-dark); background: var(--paper); border-color: var(--paper); }
    .button-light:hover { color: var(--paper); background: transparent; border-color: rgba(248,245,238,.65); }

    .visit-section { padding-block: 92px; }
    .visit-grid { display: grid; grid-template-columns: 1fr 280px; align-items: stretch; gap: 50px; }
    .visit-copy { padding-block: 10px; }
    .visit-copy h2 { max-width: 520px; margin-bottom: 14px; }
    .visit-copy > p:not(.eyebrow) { max-width: 410px; margin-bottom: 27px; color: var(--muted); font-size: 12px; line-height: 1.85; }
    .visit-details { display: flex; gap: 38px; flex-wrap: wrap; }
    .visit-detail small { display: block; margin-bottom: 8px; color: var(--olive); font-size: 9px; font-weight: 700; letter-spacing: .15em; text-transform: uppercase; }
    .visit-detail span { color: var(--ink); font-size: 11px; line-height: 1.8; }
    .qr-card {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 23px;
      background: #eee8dc;
      text-align: center;
    }
    .qr-frame { width: 148px; height: 148px; display: grid; place-items: center; margin-bottom: 16px; background: #fff; }
    .qr-frame img { width: 136px; height: 136px; image-rendering: pixelated; }
    .qr-card strong { margin-bottom: 6px; font-family: var(--serif); font-size: 17px; font-weight: 600; }
    .qr-card p { max-width: 180px; margin: 0; color: var(--muted); font-size: 9px; line-height: 1.7; }

    .site-footer { padding-block: 24px; color: rgba(248,245,238,.72); background: #251b16; }
    .footer-inner { display: flex; align-items: center; justify-content: space-between; gap: 20px; }
    .footer-brand { color: var(--paper); font-family: var(--serif); font-size: 18px; font-weight: 600; }
    .footer-inner p { margin: 0; font-size: 9px; letter-spacing: .04em; }
    .footer-links { display: flex; gap: 19px; font-size: 10px; }
    .footer-links a:hover { color: #e5c69d; }

    .reveal { opacity: 0; transform: translateY(18px); transition: opacity .65s ease, transform .65s cubic-bezier(.2,.7,.2,1); }
    .reveal.is-visible { opacity: 1; transform: translateY(0); }
    .menu-card.reveal:nth-child(2) { transition-delay: .06s; }
    .menu-card.reveal:nth-child(3) { transition-delay: .12s; }
    .menu-card.reveal:nth-child(4) { transition-delay: .18s; }
    @keyframes float-in { from { opacity: 0; transform: translateY(25px) scale(.985); } to { opacity: 1; transform: translateY(0) scale(1); } }
    @keyframes stamp-in { from { opacity: 0; transform: scale(.6) rotate(-12deg); } to { opacity: 1; transform: scale(1) rotate(9deg); } }
    @keyframes photo-drift { from { transform: scale(1.01); } to { transform: scale(1.08); } }
    @keyframes ticker { to { transform: translateX(-50%); } }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { scroll-behavior: auto !important; animation-duration: .01ms !important; animation-iteration-count: 1 !important; transition-duration: .01ms !important; }
      .reveal { opacity: 1; transform: none; }
    }
    @media (max-width: 860px) {
      .hero { min-height: 530px; grid-template-columns: 1fr .88fr; gap: 20px; }
      .hero-visual { min-height: 410px; }
      h1 { font-size: clamp(53px, 8vw, 72px); }
      .menu-grid { grid-template-columns: repeat(2, 1fr); }
      .story-inner { gap: 45px; }
      .story-photo { min-height: 380px; }
    }
    @media (max-width: 640px) {
      .shell { width: min(100% - 34px, 480px); }
      .topline { font-size: 8px; }
      .nav { min-height: 66px; gap: 14px; }
      .brand { font-size: 20px; }
      .nav-links { gap: 13px; }
      .nav-links a { font-size: 10px; }
      .nav-links a:nth-child(3) { display: none; }
      .nav-cta { min-height: 37px; padding-inline: 12px; font-size: 9px; }
      .nav-cta svg { display: none; }
      .hero { min-height: 0; grid-template-columns: 1fr; gap: 33px; padding-block: 55px 52px; }
      h1 { max-width: 470px; font-size: clamp(55px, 15vw, 76px); }
      .hero-copy > p:not(.eyebrow) { max-width: 360px; font-size: 13px; }
      .hero-note { margin-top: 32px; }
      .hero-visual { min-height: 390px; margin-inline: 15px 3px; }
      .floating-stamp { top: 28px; right: -9px; width: 88px; height: 88px; }
      .section { padding-block: 70px; }
      .menu-section { padding-top: 72px; }
      .section-heading { align-items: flex-start; flex-direction: column; gap: 14px; margin-bottom: 26px; }
      .section-heading > p { max-width: 360px; }
      h2 { font-size: 43px; }
      .menu-grid { gap: 9px; }
      .menu-card { min-height: 218px; padding: 17px 14px 15px; }
      .card-top { margin-bottom: 19px; }
      .menu-card h3 { font-size: 17px; }
      .story-inner { grid-template-columns: 1fr; gap: 35px; }
      .story-photo { min-height: 310px; }
      .story-copy { padding-bottom: 5px; }
      .story-points { margin-block: 22px; }
      .visit-grid { grid-template-columns: 1fr; gap: 27px; }
      .visit-section { padding-block: 70px; }
      .qr-card { min-height: 255px; }
      .footer-inner { align-items: flex-start; flex-wrap: wrap; }
      .footer-inner p { order: 3; width: 100%; }
    }
    @media (max-width: 380px) {
      .nav-links { gap: 9px; }
      .nav-links a:nth-child(2) { display: none; }
      .menu-card { padding-inline: 11px; }
      .menu-controls { gap: 6px; }
      .filter { padding-inline: 11px; }
    }
  </style>
</head>
<body>
  <div class="topline">Thoughtfully sourced · freshly brewed · always local</div>
  <header class="site-header">
    <nav class="nav shell" aria-label="Main navigation">
      <a class="brand" href="#top" aria-label="Morrow Coffee home">
        <span class="brand-mark" aria-hidden="true">
          <svg viewBox="0 0 24 24" fill="none"><path d="M5 9h12v7a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4V9Z" stroke="currentColor" stroke-width="1.7"/><path d="M17 11h1.3a2.7 2.7 0 1 1 0 5.4H17M8 5c0-1 1-1.2 1-2.2M12 5c0-1 1-1.2 1-2.2" stroke="currentColor" stroke-width="1.7" stroke-linecap="round"/></svg>
        </span>
        Morrow
      </a>
      <div class="nav-links">
        <a href="#menu">Menu</a>
        <a href="#story">Our story</a>
        <a href="#visit">Visit</a>
      </div>
      <a class="nav-cta" href="#menu">Find your favorite
        <svg viewBox="0 0 20 20" fill="none" aria-hidden="true"><path d="M4 10h12m-5-5 5 5-5 5" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
      </a>
    </nav>
  </header>

  <main id="top">
    <section class="hero shell">
      <div class="hero-copy">
        <p class="eyebrow">Your neighborhood coffee house</p>
        <h1>Good coffee.<br><em>Better mornings.</em></h1>
        <p>A little pause in a busy day. We pour carefully sourced coffee, make everything fresh, and save you a seat.</p>
        <div class="hero-actions">
          <a class="button" href="#menu">Explore the menu
            <svg viewBox="0 0 20 20" fill="none" aria-hidden="true"><path d="M4 10h12m-5-5 5 5-5 5" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </a>
          <a class="text-link" href="#story">A little about us
            <svg viewBox="0 0 20 20" fill="none" aria-hidden="true"><path d="M4 10h12m-5-5 5 5-5 5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </a>
        </div>
        <div class="hero-note">
          <span class="avatar-stack" aria-hidden="true"><span>M</span><span>J</span><span>A</span></span>
          <span>Made with care, shared with neighbors.</span>
        </div>
      </div>
      <div class="hero-visual" aria-label="A freshly made cup of coffee">
        <div class="hero-photo">
          <img src="https://images.unsplash.com/photo-1442512595331-e89e73853f31?auto=format&fit=crop&w=1300&q=85" alt="Barista preparing freshly brewed coffee" fetchpriority="high">
          <div class="photo-caption"><small>Good things take a moment</small><strong>Made fresh, every day.</strong></div>
        </div>
        <div class="floating-stamp"><span>Good beans<br>good people<b>since 2018</b></span></div>
      </div>
    </section>

    <div class="ticker" aria-hidden="true">
      <div class="ticker-track">
        <span>Small batch, big heart</span><i>✳</i><span>Good coffee for good days</span><i>✳</i><span>Stay for one more sip</span><i>✳</i><span>Small batch, big heart</span><i>✳</i><span>Good coffee for good days</span><i>✳</i><span>Stay for one more sip</span><i>✳</i>
      </div>
    </div>

    <section class="section menu-section shell" id="menu">
      <div class="section-heading reveal">
        <div>
          <p class="eyebrow">The good stuff</p>
          <h2>Made for your<br>kind of morning.</h2>
        </div>
        <p>Thoughtful classics and house favorites, made to order with beans we love.</p>
      </div>
      <div class="menu-controls reveal" role="group" aria-label="Filter menu items">
        <button class="filter" type="button" data-filter="all" aria-pressed="true">All drinks</button>
        <button class="filter" type="button" data-filter="espresso" aria-pressed="false">Espresso</button>
        <button class="filter" type="button" data-filter="signature" aria-pressed="false">House favorites</button>
        <button class="filter" type="button" data-filter="iced" aria-pressed="false">Iced</button>
        <button class="filter" type="button" data-filter="tea" aria-pressed="false">Tea</button>
      </div>
      <div class="menu-grid">
        <article class="menu-card reveal" data-category="espresso">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="M5 10h12v6a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4v-6Zm12 2h1a2 2 0 1 1 0 4h-1M8 6c0-.8.8-1 .8-1.8M12 6c0-.8.8-1 .8-1.8" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">Espresso</span></div>
          <h3>Double Espresso</h3><p>Rich, balanced, and beautifully simple.</p>
          <div class="card-bottom"><span class="price">$3</span><span class="size">2 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="espresso">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="M5 10h12v6a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4v-6Zm12 2h1a2 2 0 1 1 0 4h-1M8 6c0-.8.8-1 .8-1.8M12 6c0-.8.8-1 .8-1.8" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">Espresso</span></div>
          <h3>Honey Cappuccino</h3><p>Velvety milk with a touch of local honey.</p>
          <div class="card-bottom"><span class="price">$5</span><span class="size">8 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="signature">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="M5 9h12v7a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4V9Zm12 2h1a2.7 2.7 0 1 1 0 5.4H17M8 5c0-1 1-1.2 1-2.2M12 5c0-1 1-1.2 1-2.2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">House favorite</span></div>
          <h3>Honey Oat Latte</h3><p>Double espresso, oat milk, and wildflower honey.</p>
          <div class="card-bottom"><span class="price">$6</span><span class="size">12 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="signature">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="M5 9h12v7a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4V9Zm12 2h1a2.7 2.7 0 1 1 0 5.4H17M8 5c0-1 1-1.2 1-2.2M12 5c0-1 1-1.2 1-2.2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">House favorite</span></div>
          <h3>Brown Butter Mocha</h3><p>Dark chocolate, espresso, and a little sea salt.</p>
          <div class="card-bottom"><span class="price">$7</span><span class="size">12 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="iced">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="m7 4 2 16h6l2-16M6.5 8h11M9 12h7M9 16h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">Iced</span></div>
          <h3>Slow Steep Cold Brew</h3><p>Silky, chocolatey, steeped for 18 hours.</p>
          <div class="card-bottom"><span class="price">$5</span><span class="size">12 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="iced">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="m7 4 2 16h6l2-16M6.5 8h11M9 12h7M9 16h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">Iced</span></div>
          <h3>Iced Vanilla Latte</h3><p>Our espresso over ice with real vanilla.</p>
          <div class="card-bottom"><span class="price">$6</span><span class="size">16 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="tea">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="M5 10h12v6a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4v-6Zm12 2h1a2 2 0 1 1 0 4h-1M8 6c0-.8.8-1 .8-1.8M12 6c0-.8.8-1 .8-1.8" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">Tea</span></div>
          <h3>Cloud Matcha</h3><p>Bright ceremonial matcha whisked to order.</p>
          <div class="card-bottom"><span class="price">$7</span><span class="size">12 oz</span></div>
        </article>
        <article class="menu-card reveal" data-category="espresso">
          <div class="card-top"><span class="cup-art" aria-hidden="true"><svg viewBox="0 0 24 24" fill="none"><path d="M5 9h12v7a4 4 0 0 1-4 4H9a4 4 0 0 1-4-4V9Zm12 2h1a2.7 2.7 0 1 1 0 5.4H17M8 5c0-1 1-1.2 1-2.2M12 5c0-1 1-1.2 1-2.2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg></span><span class="tag">Espresso</span></div>
          <h3>Flat White</h3><p>Silky microfoam over a smooth double shot.</p>
          <div class="card-bottom"><span class="price">$5</span><span class="size">8 oz</span></div>
        </article>
      </div>
      <p class="menu-footnote">Prices in USD. Oat and almond milk available.</p>
    </section>

    <section class="story section" id="story">
      <div class="story-inner shell">
        <div class="story-photo reveal">
          <img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?auto=format&fit=crop&w=1200&q=85" alt="Coffee beans and a freshly brewed cup on the counter" loading="lazy">
        </div>
        <div class="story-copy reveal">
          <p class="eyebrow">A good cup starts somewhere</p>
          <h2>Rooted in good things.</h2>
          <p>We believe coffee tastes better when you know where it comes from and who made it. We partner with small farms, roast in thoughtful batches, and make room for the everyday rituals that bring us together.</p>
          <div class="story-points">
            <div class="story-point"><strong>Good by nature</strong><span>Responsible, traceable beans</span></div>
            <div class="story-point"><strong>Made with care</strong><span>Freshly prepared, always</span></div>
          </div>
          <a class="button button-light" href="#visit">Come say hello
            <svg viewBox="0 0 20 20" fill="none" aria-hidden="true"><path d="M4 10h12m-5-5 5 5-5 5" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </a>
        </div>
      </div>
    </section>

    <section class="visit-section shell" id="visit">
      <div class="visit-grid">
        <div class="visit-copy reveal">
          <p class="eyebrow">Your seat is waiting</p>
          <h2>Make yourself<br>at home.</h2>
          <p>Drop by for your morning coffee, bring a friend, or stay a while. There is always a fresh pot and a warm welcome.</p>
          <div class="visit-details">
            <div class="visit-detail"><small>Come by</small><span>Your neighborhood<br>coffee house</span></div>
            <div class="visit-detail"><small>Open daily</small><span>Monday – Sunday<br>7:00 am – 6:00 pm</span></div>
          </div>
        </div>
        <aside class="qr-card reveal" aria-label="Scan to open the digital menu">
          <div class="qr-frame"><img id="menu-qr" alt="QR code for the Morrow Coffee digital menu" loading="lazy"></div>
          <strong>Menu, in a scan</strong>
          <p>Point your camera here to open our menu on your phone.</p>
        </aside>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="footer-inner shell">
      <a class="footer-brand" href="#top">Morrow Coffee</a>
      <p>© <span id="year"></span> Morrow Coffee. Made for good mornings.</p>
      <div class="footer-links"><a href="#menu">Menu</a><a href="#story">Our story</a><a href="#visit">Visit</a></div>
    </div>
  </footer>

  <script>
    const filters = document.querySelectorAll('.filter');
    const menuCards = document.querySelectorAll('.menu-card');

    filters.forEach((button) => {
      button.addEventListener('click', () => {
        const filter = button.dataset.filter;
        filters.forEach((item) => item.setAttribute('aria-pressed', String(item === button)));
        menuCards.forEach((card) => {
          card.hidden = filter !== 'all' && card.dataset.category !== filter;
        });
      });
    });

    const revealObserver = new IntersectionObserver((entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.12 });
    document.querySelectorAll('.reveal').forEach((element) => revealObserver.observe(element));

    const menuUrl = new URL(window.location.href);
    menuUrl.hash = 'menu';
    document.getElementById('menu-qr').src =
      'https://api.qrserver.com/v1/create-qr-code/?size=240x240&format=svg&margin=8&color=2C241F&bgcolor=FFFFFF&data=' +
      encodeURIComponent(menuUrl.href);
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
# project-one
