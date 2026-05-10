<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Gelato Cielo – Taste of Heaven</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=Dancing+Script:wght@500;700&family=Josefin+Sans:wght@200;300;400;600&family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300;1,400&display=swap" rel="stylesheet">
<style>
:root {
  --pink: #e8a0b4;
  --soft-pink: #f2c4d4;
  --blush: #fceef4;
  --lavender: #c9a8d4;
  --mint: #a8d4c4;
  --green: #7bbf9e;
  --dark-grape: #3d2052;
  --plum: #7a3b72;
  --cream: #fdf6f0;
  --gold: #d4a843;
  --warm-white: #fff9f5;
  --text-body: #4a3050;
}
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{background:var(--warm-white);color:var(--dark-grape);font-family:'Cormorant Garamond',serif;overflow-x:hidden;}

/* ── VIOLET TOP STRIP ── */
.violet-strip{background:linear-gradient(135deg,var(--plum),var(--lavender));padding:1rem 3rem;display:flex;align-items:center;justify-content:center;gap:2rem;flex-wrap:wrap;color:#fff;font-family:'Josefin Sans',sans-serif;font-size:.75rem;letter-spacing:.15em;text-transform:uppercase;}
.violet-strip-item{display:flex;align-items:center;gap:.5rem;}

/* ── NAV ── */
nav{position:relative;top:0;left:0;right:0;z-index:200;display:flex;align-items:center;justify-content:space-between;padding:.9rem 3.5rem;background:rgba(253,246,240,0.92);backdrop-filter:blur(18px);border-bottom:1px solid rgba(232,160,180,.2);}
.nav-logo{font-family:'Dancing Script',cursive;font-size:1.6rem;background:linear-gradient(135deg,var(--plum),var(--pink));-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
nav ul{list-style:none;display:flex;gap:2.5rem;}
nav ul a{font-family:'Josefin Sans',sans-serif;font-size:.7rem;letter-spacing:.2em;text-transform:uppercase;color:var(--dark-grape);text-decoration:none;transition:color .25s;}
nav ul a:hover{color:var(--plum);}
.nav-order{font-family:'Josefin Sans',sans-serif;font-size:.7rem;letter-spacing:.15em;text-transform:uppercase;padding:.55rem 1.5rem;background:linear-gradient(135deg,var(--plum),var(--pink));color:#fff;border:none;border-radius:99px;cursor:pointer;transition:transform .25s,box-shadow .25s;}
.nav-order:hover{transform:translateY(-2px);box-shadow:0 8px 24px rgba(122,59,114,.35);}

/* ── HERO ── */
.hero{min-height:100vh;display:grid;grid-template-columns:1fr 1fr;gap:0;position:relative;overflow:hidden;}
.hero-left{display:flex;flex-direction:column;justify-content:center;padding:4rem 4rem 4rem 5rem;position:relative;z-index:2;}
.hero-right{position:relative;overflow:hidden;}
.hero-right img{width:100%;height:100%;object-fit:cover;display:block;}
.hero-right::after{content:'';position:absolute;inset:0;background:linear-gradient(to right,var(--warm-white) 0%,transparent 40%);}

/* blobs */
.blob{position:absolute;border-radius:50%;filter:blur(80px);opacity:.5;animation:drift 12s ease-in-out infinite;pointer-events:none;}
.b1{width:500px;height:500px;background:var(--soft-pink);top:-120px;left:-100px;animation-delay:0s;}
.b2{width:350px;height:350px;background:var(--lavender);top:50%;left:20%;animation-delay:-4s;}
.b3{width:280px;height:280px;background:var(--mint);bottom:-60px;left:5%;animation-delay:-8s;}
@keyframes drift{0%,100%{transform:translate(0,0) scale(1);}40%{transform:translate(25px,-35px) scale(1.07);}70%{transform:translate(-15px,25px) scale(.94);}}

/* logo stack */
.logo-wrap{position:relative;margin-bottom:1.5rem;}
.logo-cloud-svg{display:block;margin-bottom:.3rem;}
.logo-name{font-family:'Dancing Script',cursive;font-size:clamp(3.5rem,7vw,6.5rem);line-height:.95;display:block;}
.logo-name .gelato{background:linear-gradient(135deg,var(--plum) 20%,var(--pink) 80%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
.logo-name .cielo{background:linear-gradient(135deg,var(--green) 10%,var(--dark-grape) 85%);-webkit-background-clip:text;-webkit-text-fill-color:transparent;}
.logo-tagline{font-family:'Josefin Sans',sans-serif;font-size:.72rem;letter-spacing:.35em;text-transform:uppercase;color:var(--plum);background:linear-gradient(90deg,var(--soft-pink),var(--lavender),var(--mint));padding:.35rem 1.4rem;border-radius:99px;display:inline-block;margin-top:.7rem;}

.hero-desc{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:1.25rem;color:var(--text-body);line-height:1.7;max-width:480px;margin-bottom:2.5rem;}
.hero-actions{display:flex;gap:1rem;flex-wrap:wrap;}
.btn-pill{font-family:'Josefin Sans',sans-serif;font-size:.72rem;letter-spacing:.18em;text-transform:uppercase;padding:.85rem 2.2rem;border-radius:99px;cursor:pointer;text-decoration:none;transition:all .3s;}
.btn-dark{background:linear-gradient(135deg,var(--dark-grape),var(--plum));color:#fff;box-shadow:0 8px 28px rgba(61,32,82,.3);}
.btn-dark:hover{transform:translateY(-3px);box-shadow:0 16px 36px rgba(61,32,82,.4);}
.btn-ghost{border:1.5px solid var(--plum);color:var(--plum);}
.btn-ghost:hover{background:var(--plum);color:#fff;}

/* stats row */
.hero-stats{display:flex;gap:2.5rem;margin-top:3rem;}
.stat .num{font-family:'Playfair Display',serif;font-size:2rem;font-weight:700;color:var(--dark-grape);}
.stat .lbl{font-family:'Josefin Sans',sans-serif;font-size:.68rem;letter-spacing:.18em;text-transform:uppercase;color:var(--plum);opacity:.8;}

/* wave divider */
.wave{display:block;width:100%;overflow:hidden;line-height:0;}
.wave svg{display:block;}

/* ── SECTION BASE ── */
section{padding:5.5rem 2rem;}
.sec-eyebrow{font-family:'Josefin Sans',sans-serif;font-size:.7rem;letter-spacing:.32em;text-transform:uppercase;color:var(--plum);text-align:center;margin-bottom:.5rem;}
.sec-title{font-family:'Playfair Display',serif;font-size:clamp(2rem,4.5vw,3rem);text-align:center;color:var(--dark-grape);margin-bottom:.5rem;}
.sec-rule{width:60px;height:3px;background:linear-gradient(90deg,var(--pink),var(--lavender),var(--mint));border-radius:99px;margin:.8rem auto 3rem;}

/* ── FEATURED STRIP ── */
.featured-strip{background:linear-gradient(135deg,var(--dark-grape),var(--plum));padding:1.5rem 3rem;display:flex;align-items:center;justify-content:center;gap:3rem;flex-wrap:wrap;}
.strip-item{font-family:'Josefin Sans',sans-serif;font-size:.72rem;letter-spacing:.2em;text-transform:uppercase;color:rgba(255,255,255,.75);display:flex;align-items:center;gap:.6rem;}
.strip-dot{width:6px;height:6px;border-radius:50%;background:var(--pink);}

/* ── SUNDAE ── */
.sundae-section{background:var(--blush);}
.sundae-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:2rem;max-width:1180px;margin:0 auto;}
.card{border-radius:28px;overflow:hidden;background:#fff;box-shadow:0 6px 40px rgba(122,59,114,.09);transition:transform .35s cubic-bezier(.34,1.56,.64,1),box-shadow .35s;}
.card:hover{transform:translateY(-10px) rotate(-0.5deg);box-shadow:0 24px 60px rgba(122,59,114,.2);}
.card-img{width:100%;height:220px;object-fit:cover;display:block;}
.card-img-wrap{position:relative;}
.card-badge{position:absolute;top:14px;right:14px;font-family:'Josefin Sans',sans-serif;font-size:.65rem;letter-spacing:.12em;text-transform:uppercase;padding:.3rem .85rem;border-radius:99px;background:rgba(61,32,82,.82);color:#fff;backdrop-filter:blur(6px);}
.card-body{padding:1.6rem 1.8rem;}
.card-title{font-family:'Playfair Display',serif;font-size:1.4rem;color:var(--dark-grape);margin-bottom:.4rem;}
.card-desc{font-size:.95rem;color:#7a6070;line-height:1.65;margin-bottom:1.2rem;}
.price-loz{display:inline-flex;align-items:center;gap:.4rem;font-family:'Josefin Sans',sans-serif;font-size:.75rem;font-weight:600;letter-spacing:.1em;background:linear-gradient(135deg,var(--plum),var(--pink));color:#fff;padding:.38rem 1.1rem;border-radius:99px;}

/* Cobbler full-width */
.cobbler-card{background:linear-gradient(135deg,var(--dark-grape) 0%,var(--plum) 60%,#8c3a85 100%);border-radius:28px;overflow:hidden;display:grid;grid-template-columns:1fr 1fr;max-width:1180px;margin:2rem auto 0;box-shadow:0 12px 60px rgba(61,32,82,.28);}
.cobbler-img{width:100%;height:320px;object-fit:cover;display:block;}
.cobbler-body{display:flex;flex-direction:column;justify-content:center;padding:2.5rem 3rem;color:#fff;}
.cobbler-eyebrow{font-family:'Josefin Sans',sans-serif;font-size:.65rem;letter-spacing:.3em;text-transform:uppercase;color:var(--soft-pink);margin-bottom:.6rem;}
.cobbler-title{font-family:'Playfair Display',serif;font-size:2.5rem;font-style:italic;margin-bottom:.8rem;}
.cobbler-desc{font-size:1rem;opacity:.82;line-height:1.7;margin-bottom:1.5rem;}
.price-gold{background:linear-gradient(135deg,var(--gold),#f0c060);color:var(--dark-grape);}

/* ── PASTRIES ── */
.pastries-section{background:var(--cream);}
.pastry-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:1.6rem;max-width:1180px;margin:0 auto;}
.pastry-card{background:#fff;border-radius:22px;overflow:hidden;box-shadow:0 4px 28px rgba(122,59,114,.08);transition:transform .3s,box-shadow .3s;}
.pastry-card:hover{transform:translateY(-7px);box-shadow:0 18px 50px rgba(122,59,114,.17);}
.pastry-card img{width:100%;height:175px;object-fit:cover;display:block;}
.pastry-card-body{padding:1.3rem 1.5rem;}
.pastry-card h4{font-family:'Playfair Display',serif;font-size:1.15rem;color:var(--dark-grape);margin-bottom:.3rem;}
.pastry-card p{font-size:.88rem;color:#8a7080;line-height:1.55;margin-bottom:.9rem;}
.flavour-row{display:flex;flex-wrap:wrap;gap:.35rem;margin-bottom:.9rem;}
.fc{font-family:'Josefin Sans',sans-serif;font-size:.6rem;letter-spacing:.08em;padding:.18rem .6rem;border-radius:99px;background:var(--blush);color:var(--plum);border:1px solid var(--soft-pink);}
.price-mint{background:linear-gradient(135deg,var(--green),var(--mint));color:var(--dark-grape);}

/* ── SNACKS ── */
.snacks-section{background:linear-gradient(160deg,#2a1040 0%,var(--plum) 55%,#7a3b72 100%);}
.snacks-section .sec-eyebrow{color:var(--soft-pink);}
.snacks-section .sec-title{color:#fff;}
.snacks-section .sec-rule{background:linear-gradient(90deg,var(--gold),#f0c060,var(--mint));}
.snack-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:1.5rem;max-width:1180px;margin:0 auto;}
.snack-card{background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.13);border-radius:22px;overflow:hidden;transition:background .3s,transform .3s;}
.snack-card:hover{background:rgba(255,255,255,.14);transform:translateY(-7px);}
.snack-card img{width:100%;height:165px;object-fit:cover;display:block;opacity:.9;}
.snack-body{padding:1.3rem 1.5rem;color:#fff;}
.snack-body h4{font-family:'Playfair Display',serif;font-size:1.1rem;margin-bottom:.3rem;}
.snack-body p{font-size:.85rem;opacity:.75;line-height:1.55;margin-bottom:.9rem;}
.price-gold-snack{background:linear-gradient(135deg,var(--gold),#f4d070);color:#2a1040;}

/* pizza wide */
.pizza-wide{grid-column:1/-1;display:grid;grid-template-columns:1fr 1fr;border-radius:22px;overflow:hidden;border:1px solid rgba(255,255,255,.13);}
.pizza-wide img{width:100%;height:230px;object-fit:cover;display:block;}
.pizza-wide-body{background:rgba(255,255,255,.07);padding:1.8rem 2rem;color:#fff;display:flex;flex-direction:column;justify-content:center;}
.pizza-wide-body h4{font-family:'Playfair Display',serif;font-size:1.6rem;font-style:italic;margin-bottom:1rem;}
.pizza-row{display:flex;justify-content:space-between;font-family:'Josefin Sans',sans-serif;font-size:.78rem;letter-spacing:.08em;border-bottom:1px solid rgba(255,255,255,.1);padding:.4rem 0;}
.pizza-row:last-child{border-bottom:none;}

/* ── GALLERY ── */
.gallery-section{background:var(--blush);overflow:hidden;}
.gallery-track{display:flex;gap:1.2rem;padding:0 2rem;animation:slideTrack 28s linear infinite;}
.gallery-track:hover{animation-play-state:paused;}
.gallery-img{width:280px;height:200px;object-fit:cover;border-radius:18px;flex-shrink:0;transition:transform .3s;}
.gallery-img:hover{transform:scale(1.04);}
@keyframes slideTrack{0%{transform:translateX(0);}100%{transform:translateX(-50%);}}

/* ── INFO ── */
.info-section{background:var(--cream);}
.info-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:2rem;max-width:960px;margin:0 auto;}
.info-card{background:#fff;border-radius:24px;padding:2rem;text-align:center;box-shadow:0 4px 28px rgba(122,59,114,.08);}
.info-icon{width:52px;height:52px;border-radius:50%;background:linear-gradient(135deg,var(--soft-pink),var(--lavender));display:flex;align-items:center;justify-content:center;margin:0 auto 1rem;font-size:1.5rem;}
.info-card h4{font-family:'Playfair Display',serif;font-size:1.2rem;color:var(--dark-grape);margin-bottom:.5rem;}
.info-card p{font-size:.92rem;color:#7a6070;line-height:1.65;}
.info-card a{color:var(--plum);text-decoration:none;font-weight:600;}

/* ── FOOTER ── */
footer{background:var(--dark-grape);color:rgba(255,255,255,.6);text-align:center;padding:3.5rem 2rem;}
.foot-logo{font-family:'Dancing Script',cursive;font-size:2.2rem;background:linear-gradient(135deg,var(--pink),var(--lavender));-webkit-background-clip:text;-webkit-text-fill-color:transparent;display:block;margin-bottom:.4rem;}
footer p{font-family:'Josefin Sans',sans-serif;font-size:.7rem;letter-spacing:.12em;margin:.3rem 0;}

/* reveal */
.reveal{opacity:0;transform:translateY(36px);transition:opacity .7s ease,transform .7s ease;}
.reveal.up{opacity:1;transform:translateY(0);}

/* responsive */
@media(max-width:900px){
  .hero{grid-template-columns:1fr;}
  .hero-right{height:340px;}
  .hero-right::after{background:linear-gradient(to bottom,var(--warm-white) 0%,transparent 40%);}
  .hero-left{padding:2rem 2rem 3rem;}
  .cobbler-card{grid-template-columns:1fr;}
  .cobbler-img{height:220px;}
  .pizza-wide{grid-template-columns:1fr;}
  nav{padding:.9rem 1.5rem;}
  nav ul{gap:1rem;}
  .violet-strip{padding:1rem 1.5rem;font-size:.65rem;gap:1.5rem;}
}
@media(max-width:600px){
  .hero-stats{gap:1.5rem;}
  nav ul{display:none;}
  .violet-strip{display:none;}
}
</style>
</head>
<body>

<!-- ── VIOLET TOP STRIP ── -->
<div class="violet-strip">
  <div class="violet-strip-item">✦ Welcome to Gelato Cielo ✦</div>
  <div class="violet-strip-item">🕒 Open Daily 11AM-11PM</div>
  <div class="violet-strip-item">📍 Mylapore, Chennai</div>
</div>

<!-- ── NAV ── -->
<nav>
  <span class="nav-logo">Gelato Cielo</span>
  <ul>
    <li><a href="#sundae">Sundae</a></li>
    <li><a href="#pastries">Pastries</a></li>
    <li><a href="#snacks">Bites</a></li>
    <li><a href="#info">Visit</a></li>
  </ul>
  <button class="nav-order" onclick="document.getElementById('info').scrollIntoView({behavior:'smooth'})">Order Now</button>
</nav>

<!-- ── HERO ── -->
<div class="hero">
  <div class="blob b1"></div>
  <div class="blob b2"></div>
  <div class="blob b3"></div>

  <div class="hero-left">
    <div class="logo-wrap reveal">
      <!-- Cloud SVG in brand pink-green palette -->
      <svg class="logo-cloud-svg" width="100" height="58" viewBox="0 0 120 68" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="28" cy="42" r="22" fill="#f2c4d4" opacity=".88"/>
        <circle cx="60" cy="32" r="28" fill="#e8a0b4" opacity=".9"/>
        <circle cx="92" cy="42" r="20" fill="#f2c4d4" opacity=".85"/>
        <ellipse cx="60" cy="52" rx="52" ry="18" fill="#f2c4d4" opacity=".7"/>
        <circle cx="44" cy="26" r="16" fill="#c9a8d4" opacity=".7"/>
        <circle cx="76" cy="24" r="14" fill="#a8d4c4" opacity=".65"/>
      </svg>
      <span class="logo-name"><span class="gelato">Gelato</span> <span class="cielo">Cielo</span></span>
      <span class="logo-tagline">✦ Taste of Heaven ✦</span>
    </div>

    <p class="hero-desc reveal" style="transition-delay:.15s">
      Artisan gelato, heavenly pastries &amp; soul-warming bites — crafted with love in the heart of Mylapore, Chennai.
    </p>

    <div class="hero-actions reveal" style="transition-delay:.28s">
      <a href="#sundae" class="btn-pill btn-dark">Explore Menu</a>
      <a href="#info" class="btn-pill btn-ghost">Find Us</a>
    </div>

    <div class="hero-stats reveal" style="transition-delay:.42s">
      <div class="stat"><div class="num">30+</div><div class="lbl">Menu items</div></div>
      <div class="stat"><div class="num">5★</div><div class="lbl">Gelato flavours</div></div>
      <div class="stat"><div class="num">🛵</div><div class="lbl">Zomato · Swiggy</div></div>
    </div>
  </div>

  <div class="hero-right">
    <img src="beauti gel.jpeg" alt="Beautiful gelato scoops" loading="eager"/>
  </div>
</div>

<!-- featured strip -->
<div class="featured-strip">
  <div class="strip-item"><div class="strip-dot"></div>Sundaes from ₹160</div>
  <div class="strip-item"><div class="strip-dot"></div>Pastries from ₹80</div>
  <div class="strip-item"><div class="strip-dot"></div>Sizzling Brownie</div>
  <div class="strip-item"><div class="strip-dot"></div>Party Orders Welcome</div>
  <div class="strip-item"><div class="strip-dot"></div>185/248 Royapettah High Rd, Mylapore</div>
</div>

<!-- ── SUNDAE ── -->
<section class="sundae-section reveal" id="sundae">
  <p class="sec-eyebrow">Our Signature Creations</p>
  <h2 class="sec-title">Ice Cream Sundaes</h2>
  <div class="sec-rule"></div>

  <div class="sundae-grid">

    <div class="card reveal" style="transition-delay:.05s">
      <div class="card-img-wrap">
        <img class="card-img" src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?w=600&q=80" alt="Choco Madness sundae"/>
        <span class="card-badge">Best Seller</span>
      </div>
      <div class="card-body">
        <div class="card-title">Choco Madness</div>
        <p class="card-desc">Chocolate cake with Chocolate gelato, topped with Chocochips &amp; rich Chocolate syrup</p>
        <span class="price-loz">₹ 160</span>
      </div>
    </div>

    <div class="card reveal" style="transition-delay:.1s">
      <div class="card-img-wrap">
        <img class="card-img" src="https://images.unsplash.com/photo-1606313564200-e75d5e30476c?w=600&q=80" alt="Brownie Vanilla sundae"/>
      </div>
      <div class="card-body">
        <div class="card-title">Brownie Vanilla</div>
        <p class="card-desc">Eggless Brownie with Vanilla gelato, topped with assorted nuts &amp; Chocolate syrup</p>
        <span class="price-loz">₹ 170</span>
      </div>
    </div>

    <div class="card reveal" style="transition-delay:.15s">
      <div class="card-img-wrap">
        <img class="card-img" src="https://images.unsplash.com/photo-1580915411954-282cb1b0d780?w=600&q=80" alt="Hazelnut sundae"/>
      </div>
      <div class="card-body">
        <div class="card-title">Hazelnut</div>
        <p class="card-desc">Chocolate cake with Hazelnut gelato, topped with assorted nuts &amp; Hazelnut sauce</p>
        <span class="price-loz">₹ 180</span>
      </div>
    </div>

    <div class="card reveal" style="transition-delay:.2s">
      <div class="card-img-wrap">
        <img class="card-img" src="https://images.unsplash.com/photo-1501443762994-82bd5dace89a?w=600&q=80" alt="Almond Delight sundae"/>
      </div>
      <div class="card-body">
        <div class="card-title">Almond Delight</div>
        <p class="card-desc">Chocolate cake with roasted Almond gelato, topped with almond nuts &amp; Chocolate syrup</p>
        <span class="price-loz">₹ 160</span>
      </div>
    </div>

    <div class="card reveal" style="transition-delay:.25s">
      <div class="card-img-wrap">
        <img class="card-img" src="https://images.unsplash.com/photo-1551024601-bec78aea704b?w=600&q=80" alt="Caramel sundae"/>
      </div>
      <div class="card-body">
        <div class="card-title">Caramel</div>
        <p class="card-desc">Chocolate cake with Caramel gelato, topped with assorted nuts &amp; Chocolate syrup</p>
        <span class="price-loz">₹ 160</span>
      </div>
    </div>

  </div>

  <!-- COBBLER -->
  <div class="cobbler-card reveal" style="transition-delay:.3s">
    <img class="cobbler-img" src="https://images.unsplash.com/photo-1488900128323-21503983a07e?w=700&q=80" alt="Cobbler warm dessert"/>
    <div class="cobbler-body">
      <p class="cobbler-eyebrow">Hot Dessert</p>
      <h3 class="cobbler-title">Cobbler</h3>
      <p class="cobbler-desc">Cooked Strawberry or Pineapple with Cake crumble, served <em>piping hot</em> with creamy Vanilla gelato. A warm-cold contrast like no other.</p>
      <div style="display:flex;align-items:center;gap:1rem;flex-wrap:wrap">
        <span class="price-loz price-gold">₹ 160</span>
        <span style="font-family:'Josefin Sans',sans-serif;font-size:.68rem;letter-spacing:.15em;text-transform:uppercase;opacity:.7">Strawberry · Pineapple</span>
      </div>
    </div>
  </div>
</section>

<!-- wave -->
<div class="wave" style="background:var(--blush)"><svg viewBox="0 0 1440 60" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none" height="60"><path d="M0,60 C240,0 480,60 720,30 C960,0 1200,60 1440,20 L1440,60 Z" fill="#fdf6f0"/></svg></div>

<!-- ── PASTRIES ── -->
<section class="pastries-section reveal" id="pastries">
  <p class="sec-eyebrow">Freshly Baked Daily</p>
  <h2 class="sec-title">Pastries &amp; Cakes</h2>
  <div class="sec-rule"></div>

  <div class="pastry-grid">

    <div class="pastry-card reveal" style="transition-delay:.05s">
      <img src="roundcheese.jpeg" alt="Round Cheesecake"/>
      <div class="pastry-card-body">
        <h4>Round Cheesecake</h4>
        <div class="flavour-row"><span class="fc">Biscoff</span><span class="fc">Strawberry</span><span class="fc">Blueberry</span><span class="fc">Nutrella</span></div>
        <span class="price-loz price-mint">₹ 190</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.08s">
      <img src="tri.jpeg" alt="Triangle Chess Cake"/>
      <div class="pastry-card-body">
        <h4>Triangle Chess Cake</h4>
        <div class="flavour-row"><span class="fc">Biscoff</span><span class="fc">Strawberry</span><span class="fc">Blueberry</span><span class="fc">Nutrella</span></div>
        <span class="price-loz price-mint">₹ 180</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.11s">
      <img src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?w=500&q=80" alt="Chocolate Cake"/>
      <div class="pastry-card-body">
        <h4>Chocolate Cake</h4>
        <p>Rich, decadent slice of pure chocolate heaven</p>
        <span class="price-loz price-mint">₹ 120</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.14s">
      <img src="https://images.unsplash.com/photo-1564355808539-22fda35bed7e?w=500&q=80" alt="Brownie"/>
      <div class="pastry-card-body">
        <h4>Brownie Cashew</h4>
        <p>Loaded cashew brownie, fudgy &amp; irresistible</p>
        <span class="price-loz price-mint">₹ 120</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.17s">
      <img src="https://images.unsplash.com/photo-1606313564200-e75d5e30476c?w=500&q=80" alt="Brownie Almond"/>
      <div class="pastry-card-body">
        <h4>Brownie Almond</h4>
        <p>Nutty almond brownie with deep chocolate base</p>
        <span class="price-loz price-mint">₹ 120</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.20s">
      <img src="fudge.jpeg" alt="Brownie Fudge"/>
      <div class="pastry-card-body">
        <h4>Brownie Fudge</h4>
        <p>Extra fudgy, gooey center — sinfully good</p>
        <span class="price-loz price-mint">₹ 140</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.23s">
      <img src="https://images.unsplash.com/photo-1559620192-032c4bc4674e?w=500&q=80" alt="Brownie Chess Swirl"/>
      <div class="pastry-card-body">
        <h4>Brownie Chess Swirl</h4>
        <p>Beautiful marble swirl, golden &amp; chewy</p>
        <span class="price-loz price-mint">₹ 150</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.26s">
      <img src="https://images.unsplash.com/photo-1587668178277-295251f900ce?w=500&q=80" alt="Carrot Almond Cupcake"/>
      <div class="pastry-card-body">
        <h4>Carrot Almond Cupcake</h4>
        <p>Wholesome carrot &amp; almond, moist inside</p>
        <span class="price-loz price-mint">₹ 130</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.29s">
      <img src="chocolava.jpeg" alt="Oreo Lava Cupcake"/>
      <div class="pastry-card-body">
        <h4>Oreo Lava Cupcake</h4>
        <p>Oozy Oreo center that melts in every bite</p>
        <span class="price-loz price-mint">₹ 80</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.32s">
      <img src="WhatsApp Image 2026-05-10 at 11.53.57 AM (1).jpeg" alt="Red Velvet Jar"/>
      <div class="pastry-card-body">
        <h4>Red Velvet Jar</h4>
        <p>Layered red velvet in a gorgeous dessert jar</p>
        <span class="price-loz price-mint">₹ 180</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.35s">
      <img src="moouse.jpeg" alt="Chocolate Mousse Jar"/>
      <div class="pastry-card-body">
        <h4>Chocolate Mousse Jar</h4>
        <p>Light, airy mousse in a take-away jar</p>
        <span class="price-loz price-mint">₹ 180</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.38s">
      <img src="https://images.unsplash.com/photo-1617305855058-336d24456869?w=500&q=80" alt="Choco Lava Cake"/>
      <div class="pastry-card-body">
        <h4>Choco Lava Cake</h4>
        <p>Molten chocolate center — magic in every spoon</p>
        <span class="price-loz price-mint">₹ 140</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.41s">
      <img src="dccc.jpeg" alt="Double Choco Cupcake"/>
      <div class="pastry-card-body">
        <h4>Double Choco Cupcake</h4>
        <p>Double the chocolate — double the delight</p>
        <span class="price-loz price-mint">Ask us</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.44s">
      <img src="cant.jpeg" alt="Cantucci Italian Almond Rusk"/>
      <div class="pastry-card-body">
        <h4>Cantucci</h4>
        <p>Authentic Italian Almond Rusk, crispy &amp; aromatic</p>
        <span class="price-loz price-mint">₹ 130</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.47s">
      <img src="bug.jpeg" alt="Buggie Pasta Ravoli"/>
      <div class="pastry-card-body">
        <h4>Buggie</h4>
        <p>Italian Pasta Ravoli dusted with Sugar — crispy sweet surprise</p>
        <span class="price-loz price-mint">₹ 130</span>
      </div>
    </div>

    <div class="pastry-card reveal" style="transition-delay:.50s">
      <img src="https://images.unsplash.com/photo-1499636136210-6f4ee915583e?w=500&q=80" alt="Choco Chips Cookie"/>
      <div class="pastry-card-body">
        <h4>Choco Chips Cookie</h4>
        <p>Classic crispy cookie loaded with chocolate chips</p>
        <span class="price-loz price-mint">₹ 50</span>
      </div>
    </div>

  </div>
</section>

<!-- wave -->
<div class="wave" style="background:var(--cream)"><svg viewBox="0 0 1440 60" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none" height="60"><path d="M0,30 C360,80 720,0 1080,40 C1260,60 1380,10 1440,30 L1440,60 L0,60 Z" fill="#2a1040"/></svg></div>

<!-- ── SNACKS ── -->
<section class="snacks-section" id="snacks">
  <p class="sec-eyebrow">Beyond Ice Cream</p>
  <h2 class="sec-title">Bites &amp; Beverages</h2>
  <div class="sec-rule"></div>

  <div class="snack-grid">

    <div class="snack-card reveal" style="transition-delay:.05s">
      <img src="kcb.jpeg" alt="Korean Cheese Bun"/>
      <div class="snack-body">
        <h4>Korean Cheese Bun</h4>
        <p>Bun with Cream Cheese mix, Garlic Butter &amp; Mozzarella</p>
        <span class="price-loz price-gold-snack">₹ 150</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.09s">
      <img src="https://images.unsplash.com/photo-1624353365286-3f8d62daad51?w=500&q=80" alt="Sizzling Brownie"/>
      <div class="snack-body">
        <h4>Sizzling Brownie</h4>
        <p>The Ultimate Hot &amp; Gold Delight with a Scoop of Creamy Gelato</p>
        <span class="price-loz price-gold-snack">₹ 220</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.13s">
      <img src="https://images.unsplash.com/photo-1517578239113-b03992dcdd25?w=500&q=80" alt="Hot Chocolate"/>
      <div class="snack-body">
        <h4>Hot Chocolate</h4>
        <p>Cup of Pure Rich Cocoa — the classic warmer</p>
        <span class="price-loz price-gold-snack">₹ 130</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.17s">
      <img src="https://images.unsplash.com/photo-1562376552-0d160a2f238d?w=500&q=80" alt="Waffles"/>
      <div class="snack-body">
        <h4>Waffles</h4>
        <p>Warm, crispy Belgian-style waffles with gelato</p>
        <span class="price-loz price-gold-snack">₹ 120</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.21s">
      <img src="vegfinger.jpeg" alt="Veg Finger Fry"/>
      <div class="snack-body">
        <h4>Veg Finger Fry</h4>
        <p>Crispy battered vegetable fingers, golden &amp; hot</p>
        <span class="price-loz price-gold-snack">₹ 120</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.25s">
      <img src="https://images.unsplash.com/photo-1496116218417-1a781b1c416c?w=500&q=80" alt="Momos"/>
      <div class="snack-body">
        <h4>Momo's</h4>
        <p>Veg · Paneer · Mushroom · Tikka · Corn &amp; Cheese</p>
        <span class="price-loz price-gold-snack">₹ 120</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.29s">
      <img src="ff.jpeg" alt="French Fries Peri Peri"/>
      <div class="snack-body">
        <h4>French Fries</h4>
        <p>Peri Peri seasoned crispy fries — perfectly spiced</p>
        <span class="price-loz price-gold-snack">₹ 120</span>
      </div>
    </div>

    <div class="snack-card reveal" style="transition-delay:.33s">
      <img src="nac.jpeg" alt="Nachos"/>
      <div class="snack-body">
        <h4>Nacho's</h4>
        <p>Salted · Spicy · Americano · Creamy — pick your flavour</p>
        <span class="price-loz price-gold-snack">₹ 120</span>
      </div>
    </div>

    <!-- PIZZA wide card -->
    <div class="pizza-wide reveal" style="transition-delay:.37s">
      <img src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=600&q=80" alt="Cielo's Pizza"/>
      <div class="pizza-wide-body">
        <h4>Cielo's Pizza</h4>
        <div class="pizza-row"><span>Veg Pizza</span><span class="price-loz price-gold-snack" style="font-size:.7rem;padding:.28rem .9rem">₹ 150</span></div>
        <div class="pizza-row"><span>Spl Cielo's Pizza</span><span class="price-loz price-gold-snack" style="font-size:.7rem;padding:.28rem .9rem">₹ 220</span></div>
        <div class="pizza-row"><span>Paneer Pizza</span><span class="price-loz price-gold-snack" style="font-size:.7rem;padding:.28rem .9rem">₹ 200</span></div>
        <div class="pizza-row"><span>Mushroom Pizza</span><span class="price-loz price-gold-snack" style="font-size:.7rem;padding:.28rem .9rem">₹ 200</span></div>
      </div>
    </div>

  </div>
</section>

<!-- wave -->
<div class="wave" style="background:#2a1040"><svg viewBox="0 0 1440 60" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none" height="60"><path d="M0,20 C360,-10 720,60 1080,20 C1260,0 1380,50 1440,30 L1440,60 L0,60 Z" fill="#fceef4"/></svg></div>

<!-- ── GALLERY MARQUEE ── -->
<section class="gallery-section" style="padding:3rem 0;">
  <p class="sec-eyebrow" style="margin-bottom:2rem">Moments of Bliss</p>
  <div style="overflow:hidden;">
    <div class="gallery-track" id="gtrack">
      <img class="gallery-img" src="gel.jpeg" alt="gelato scoops"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1488900128323-21503983a07e?w=400&q=75" alt="warm dessert"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?w=400&q=75" alt="chocolate cake"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?w=400&q=75" alt="ice cream sundae"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1551024601-bec78aea704b?w=400&q=75" alt="caramel dessert"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1562376552-0d160a2f238d?w=400&q=75" alt="waffles"/>
      <img class="gallery-img"src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=400&q=75" alt="pizza"/>

      <!-- duplicated for seamless loop -->
      <img class="gallery-img" src="gel.jpeg" alt="gelato scoops"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1488900128323-21503983a07e?w=400&q=75" alt="warm dessert"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1578985545062-69928b1d9587?w=400&q=75" alt="chocolate cake"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?w=400&q=75" alt="ice cream sundae"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1551024601-bec78aea704b?w=400&q=75" alt="caramel dessert"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1562376552-0d160a2f238d?w=400&q=75" alt="waffles"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1617305855058-336d24456869?w=400&q=75" alt="lava cake"/>
      <img class="gallery-img" src="https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=400&q=75" alt="pizza"/>
    </div>
  </div>
</section>

<!-- ── INFO ── -->
<section class="info-section" id="info">
  <p class="sec-eyebrow">Come Visit Us</p>
  <h2 class="sec-title">Find Gelato Cielo</h2>
  <div class="sec-rule"></div>

  <div class="info-grid">
    <div class="info-card reveal">
      <div class="info-icon">📍</div>
      <h4>Location</h4>
      <p>185/248, Royapettah High Road,<br>Mylapore, Chennai 600004</p>
    </div>
    <div class="info-card reveal" style="transition-delay:.1s">
      <div class="info-icon">📞</div>
      <h4>Contact</h4>
      <p>D. Dhanaraj<br><a href="https://wa.me/919841868637" target="_blank">+91 98418 68637</a><br><a href="mailto:gelatocielo@gmail.com">gelatocielo@gmail.com</a></p>
    </div>
    <div class="info-card reveal" style="transition-delay:.2s">
      <div class="info-icon">🛵</div>
      <h4>Order Online</h4>
      <p>Available on<br><strong>Zomato &amp; Swiggy</strong><br>for quick home delivery</p>
    </div>
    <div class="info-card reveal" style="transition-delay:.3s">
      <div class="info-icon">🎉</div>
      <h4>Party Orders</h4>
      <p>We undertake <strong>all party orders</strong>. Call us to create your dream celebration!</p>
    </div>
  </div>

  <!-- map embed placeholder with styled box -->
  <div style="max-width:960px;margin:3rem auto 0;border-radius:28px;overflow:hidden;box-shadow:0 8px 50px rgba(122,59,114,.12);">
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3887.3!2d80.2707!3d13.0349!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zMTPCsDAyJzA1LjYiTiA4MMKwMTYnMTQuNSJF!5e0!3m2!1sen!2sin!4v1620000000000!5m2!1sen!2sin"
      width="100%" height="300" style="border:0;display:block;" allowfullscreen="" loading="lazy"
      title="Gelato Cielo Location Map">
    </iframe>
  </div>
</section>

<!-- ── FOOTER ── -->
<footer>
  <span class="foot-logo">Gelato Cielo</span>
  <p>✦ Taste of Heaven ✦</p>
  <p style="margin-top:.8rem">185/248 Royapettah High Road, Mylapore, Chennai 600004</p>
  <p style="margin-top:.5rem"><a href="https://wa.me/919841868637" target="_blank" style="color:var(--pink);text-decoration:none">+91 98418 68637</a> &nbsp;·&nbsp; <a href="mailto:gelatocielo@gmail.com" style="color:var(--pink);text-decoration:none">gelatocielo@gmail.com</a></p>
  <p style="margin-top:1.5rem;opacity:.35;font-family:'Josefin Sans',sans-serif;font-size:.65rem;letter-spacing:.1em">© 2026 Gelato Cielo. All rights reserved.</p>
</footer>

<script>
// scroll reveal
const revealEls = document.querySelectorAll('.reveal');
const io = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('up'); });
}, { threshold: 0.1 });
revealEls.forEach(el => io.observe(el));

// gallery track width fix
const track = document.getElementById('gtrack');
const imgs  = track.querySelectorAll('img');
const half  = imgs.length / 2;
const imgW  = 280 + 19.2; // width + gap
track.style.width = (imgs.length * imgW) + 'px';
track.style.animationDuration = (imgs.length * 2.8) + 's';
</script>
</body>
</html>
