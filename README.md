<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BMS Fitness — Ghazipur</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&family=Barlow:ital,wght@0,300;0,400;0,500;0,600;1,300&family=Bebas+Neue&display=swap" rel="stylesheet">
<style>
/* ===== RESET & BASE ===== */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; font-size: 16px; }
body {
  font-family: 'Barlow', sans-serif;
  background: #0a0a0a;
  color: #ffffff;
  overflow-x: hidden;
  line-height: 1.6;
}

/* ===== VARIABLES ===== */
:root {
  --y: #F5C518;
  --yd: #C9A010;
  --yl: rgba(245,197,24,0.12);
  --blk: #0a0a0a;
  --d1: #111111;
  --d2: #181818;
  --d3: #222222;
  --d4: #2a2a2a;
  --gray: #777777;
  --lgray: #aaaaaa;
  --white: #ffffff;
  --font-display: 'Oswald', sans-serif;
  --font-hero: 'Bebas Neue', sans-serif;
  --font-body: 'Barlow', sans-serif;
}

/* ===== SCROLLBAR ===== */
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: var(--d1); }
::-webkit-scrollbar-thumb { background: var(--y); border-radius: 3px; }

/* ===== NAVBAR ===== */
#navbar {
  position: fixed; top: 0; left: 0; right: 0; z-index: 999;
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 6%;
  height: 72px;
  background: rgba(10,10,10,0.97);
  border-bottom: 1px solid rgba(245,197,24,0.18);
  backdrop-filter: blur(12px);
}
.nav-logo {
  font-family: var(--font-hero);
  font-size: 2.1rem;
  letter-spacing: 4px;
  color: var(--y);
  text-decoration: none;
}
.nav-logo span { color: #fff; }
.nav-links {
  display: flex; gap: 2.5rem; list-style: none;
}
.nav-links a {
  font-family: var(--font-display);
  font-size: 0.82rem;
  font-weight: 500;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.65);
  text-decoration: none;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--y); }
.nav-btn {
  font-family: var(--font-display);
  font-size: 0.8rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  background: var(--y);
  color: var(--blk);
  padding: 10px 22px;
  border-radius: 3px;
  text-decoration: none;
  transition: background 0.2s, transform 0.2s;
}
.nav-btn:hover { background: var(--yd); transform: translateY(-1px); }

/* ===== HERO ===== */
#hero {
  min-height: 100vh;
  display: flex; align-items: center;
  padding: 100px 6% 60px;
  position: relative;
  overflow: hidden;
}
.hero-bg {
  position: absolute; inset: 0;
  background: #0a0a0a;
}
.hero-pattern {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(245,197,24,0.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(245,197,24,0.05) 1px, transparent 1px);
  background-size: 70px 70px;
}
.hero-glow {
  position: absolute;
  right: 5%; top: 50%; transform: translateY(-50%);
  width: 600px; height: 600px; border-radius: 50%;
  background: radial-gradient(circle at center, rgba(245,197,24,0.1) 0%, transparent 65%);
  pointer-events: none;
}
.hero-line {
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 4px;
  background: linear-gradient(to bottom, transparent, var(--y), transparent);
}
.hero-content { position: relative; z-index: 2; max-width: 750px; }
.hero-eyebrow {
  display: inline-flex; align-items: center; gap: 10px;
  margin-bottom: 1.5rem;
  font-family: var(--font-display);
  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: var(--y);
  border: 1px solid rgba(245,197,24,0.3);
  padding: 7px 18px;
  border-radius: 2px;
  background: rgba(245,197,24,0.06);
}
.hero-eyebrow::before {
  content: '';
  width: 8px; height: 8px;
  background: var(--y);
  border-radius: 50%;
  display: inline-block;
  animation: pulse 2s infinite;
}
@keyframes pulse {
  0%, 100% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.4; transform: scale(0.7); }
}
.hero-h1 {
  font-family: var(--font-hero);
  font-size: clamp(4.5rem, 10vw, 9rem);
  line-height: 0.9;
  letter-spacing: 3px;
  margin-bottom: 1.5rem;
  color: #fff;
}
.hero-h1 .y { color: var(--y); }
.hero-h1 .stroke {
  -webkit-text-stroke: 2px var(--y);
  color: transparent;
}
.hero-tagline {
  font-family: var(--font-display);
  font-size: 1.25rem;
  font-weight: 400;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.5);
  margin-bottom: 1rem;
}
.hero-desc {
  font-size: 1rem;
  color: rgba(255,255,255,0.55);
  line-height: 1.8;
  max-width: 500px;
  margin-bottom: 2.5rem;
  font-weight: 300;
}
.hero-btns { display: flex; gap: 1rem; flex-wrap: wrap; margin-bottom: 3.5rem; }
.btn-y {
  font-family: var(--font-display);
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  background: var(--y);
  color: var(--blk);
  padding: 14px 32px;
  border-radius: 3px;
  text-decoration: none;
  transition: all 0.2s;
  display: inline-block;
}
.btn-y:hover { background: var(--yd); transform: translateY(-3px); box-shadow: 0 8px 30px rgba(245,197,24,0.25); }
.btn-outline {
  font-family: var(--font-display);
  font-size: 0.85rem;
  font-weight: 500;
  letter-spacing: 2px;
  text-transform: uppercase;
  border: 1px solid rgba(255,255,255,0.2);
  color: rgba(255,255,255,0.8);
  padding: 14px 32px;
  border-radius: 3px;
  text-decoration: none;
  transition: all 0.2s;
  display: inline-block;
}
.btn-outline:hover { border-color: var(--y); color: var(--y); transform: translateY(-3px); }
.hero-stats {
  display: flex; gap: 3rem;
  padding-top: 2.5rem;
  border-top: 1px solid rgba(255,255,255,0.07);
}
.stat-num {
  font-family: var(--font-hero);
  font-size: 3rem;
  color: var(--y);
  letter-spacing: 2px;
  line-height: 1;
}
.stat-lbl {
  font-family: var(--font-display);
  font-size: 0.68rem;
  font-weight: 500;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.35);
  margin-top: 5px;
}

/* ===== SECTION COMMON ===== */
section { padding: 90px 6%; }
.s-label {
  font-family: var(--font-display);
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: var(--y);
  margin-bottom: 10px;
}
.s-title {
  font-family: var(--font-hero);
  font-size: clamp(2.5rem, 5vw, 4rem);
  letter-spacing: 2px;
  line-height: 0.95;
  color: #fff;
  margin-bottom: 14px;
}
.s-sub {
  font-size: 1rem;
  color: rgba(255,255,255,0.45);
  line-height: 1.8;
  max-width: 540px;
  font-weight: 300;
}
.y-line {
  width: 50px; height: 3px;
  background: var(--y);
  margin: 16px 0 40px;
}

/* ===== ABOUT ===== */
#about { background: var(--d1); }
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 5rem;
  align-items: center;
}
.about-img-wrap { position: relative; }
.about-img {
  width: 100%;
  aspect-ratio: 4/3;
  border-radius: 4px;
  overflow: hidden;
  border: 1px solid rgba(245,197,24,0.12);
}
.about-img img { width: 100%; height: 100%; object-fit: cover; display: block; }
.about-tag {
  position: absolute;
  bottom: -20px; right: -20px;
  background: var(--y);
  color: var(--blk);
  padding: 20px 24px;
  border-radius: 3px;
}
.about-tag-num {
  font-family: var(--font-hero);
  font-size: 2.8rem;
  line-height: 1;
  letter-spacing: 2px;
}
.about-tag-txt {
  font-family: var(--font-display);
  font-size: 0.65rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-top: 3px;
}
.features-list { display: grid; gap: 14px; margin-top: 28px; }
.feat {
  display: flex; align-items: flex-start; gap: 14px;
  padding: 16px 18px;
  background: var(--d3);
  border-radius: 4px;
  border-left: 3px solid var(--y);
  transition: background 0.2s;
}
.feat:hover { background: var(--d4); }
.feat-icon { color: var(--y); font-size: 1.1rem; flex-shrink: 0; margin-top: 2px; }
.feat-title {
  font-family: var(--font-display);
  font-size: 0.88rem;
  font-weight: 600;
  letter-spacing: 1px;
  color: #fff;
  margin-bottom: 3px;
}
.feat-desc { font-size: 0.82rem; color: rgba(255,255,255,0.5); font-weight: 300; }

/* ===== TIMING ===== */
#timing { background: var(--blk); }
.timing-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
  margin-top: 10px;
}
.t-card {
  background: var(--d2);
  border: 1px solid rgba(245,197,24,0.1);
  border-radius: 4px;
  padding: 2rem 1.5rem;
  text-align: center;
  transition: border-color 0.25s, transform 0.25s;
  position: relative;
  overflow: hidden;
}
.t-card::before {
  content: '';
  position: absolute;
  bottom: 0; left: 0; right: 0;
  height: 2px;
  background: var(--y);
  transform: scaleX(0);
  transition: transform 0.25s;
}
.t-card:hover { border-color: rgba(245,197,24,0.35); transform: translateY(-5px); }
.t-card:hover::before { transform: scaleX(1); }
.t-emoji { font-size: 2rem; margin-bottom: 1rem; }
.t-lbl {
  font-family: var(--font-display);
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--y);
  margin-bottom: 10px;
}
.t-time {
  font-family: var(--font-hero);
  font-size: 2rem;
  letter-spacing: 2px;
  color: #fff;
  line-height: 1;
  margin-bottom: 6px;
}
.t-sub { font-size: 0.75rem; color: var(--gray); font-weight: 300; }
.t-closed { color: rgba(255,255,255,0.25); }

/* ===== PLANS ===== */
#plans { background: var(--d1); }
.plans-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin-top: 10px;
}
.plan {
  background: var(--d2);
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 5px;
  padding: 2rem 1.75rem;
  position: relative;
  transition: transform 0.25s, border-color 0.25s;
}
.plan:hover { transform: translateY(-6px); border-color: rgba(245,197,24,0.2); }
.plan.hot {
  border: 2px solid var(--y);
  background: var(--d3);
}
.plan-badge {
  display: inline-block;
  background: var(--y);
  color: var(--blk);
  font-family: var(--font-display);
  font-size: 0.65rem;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 5px 14px;
  border-radius: 2px;
  margin-bottom: 1.25rem;
}
.plan-name {
  font-family: var(--font-display);
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--y);
  margin-bottom: 10px;
}
.plan-price {
  font-family: var(--font-hero);
  font-size: 4rem;
  letter-spacing: 2px;
  color: #fff;
  line-height: 1;
  margin-bottom: 4px;
}
.plan-price sup {
  font-family: var(--font-display);
  font-size: 1.3rem;
  vertical-align: super;
  margin-right: 3px;
}
.plan-period {
  font-size: 0.78rem;
  color: var(--gray);
  font-weight: 300;
  margin-bottom: 1.75rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid rgba(255,255,255,0.06);
}
.plan-feats { list-style: none; display: grid; gap: 10px; margin-bottom: 2rem; }
.plan-feats li {
  display: flex; align-items: flex-start; gap: 10px;
  font-size: 0.85rem;
  color: rgba(255,255,255,0.6);
  font-weight: 300;
}
.plan-feats li::before {
  content: '✓';
  color: var(--y);
  font-weight: 700;
  flex-shrink: 0;
  font-family: var(--font-display);
}
.plan-cta {
  display: block;
  text-align: center;
  font-family: var(--font-display);
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  padding: 13px;
  border-radius: 3px;
  text-decoration: none;
  transition: all 0.2s;
}
.cta-ghost { border: 1px solid rgba(245,197,24,0.35); color: var(--y); }
.cta-ghost:hover { background: rgba(245,197,24,0.1); }
.cta-fill { background: var(--y); color: var(--blk); }
.cta-fill:hover { background: var(--yd); }

/* ===== TRAINER ===== */
#trainer { background: var(--blk); }
.trainer-wrap {
  display: grid;
  grid-template-columns: 320px 1fr;
  gap: 0;
  border-radius: 6px;
  overflow: hidden;
  border: 1px solid rgba(245,197,24,0.12);
  margin-top: 10px;
}
.trainer-img {
  background: var(--d2);
  display: flex; align-items: center; justify-content: center;
  flex-direction: column; gap: 12px;
  min-height: 360px;
  position: relative;
  border-right: 1px solid rgba(245,197,24,0.1);
  overflow: hidden;
}
.trainer-img img { width: 100%; height: 100%; object-fit: cover; position: absolute; inset: 0; }
.trainer-img-placeholder { position: relative; z-index: 2; text-align: center; color: rgba(255,255,255,0.15); }
.trainer-img-placeholder svg { width: 64px; height: 64px; margin-bottom: 10px; display: block; margin: 0 auto 10px; }
.trainer-img-placeholder span {
  font-family: var(--font-display);
  font-size: 0.65rem;
  letter-spacing: 2px;
  text-transform: uppercase;
}
.trainer-medal {
  position: absolute; bottom: 16px; left: 16px; z-index: 3;
  background: var(--y);
  color: var(--blk);
  font-family: var(--font-display);
  font-size: 0.65rem;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 6px 12px;
  border-radius: 2px;
}
.trainer-info { padding: 2.5rem; background: var(--d1); }
.trainer-name {
  font-family: var(--font-hero);
  font-size: 3.2rem;
  letter-spacing: 2px;
  color: #fff;
  line-height: 1;
  margin-bottom: 6px;
}
.trainer-role {
  font-family: var(--font-display);
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--y);
  margin-bottom: 1.25rem;
}
.trainer-bio {
  font-size: 0.95rem;
  color: rgba(255,255,255,0.55);
  line-height: 1.8;
  font-weight: 300;
  margin-bottom: 1.5rem;
  max-width: 520px;
}
.trainer-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 1.75rem; }
.ttag {
  font-family: var(--font-display);
  font-size: 0.7rem;
  font-weight: 500;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  background: rgba(245,197,24,0.08);
  border: 1px solid rgba(245,197,24,0.2);
  color: var(--y);
  padding: 6px 14px;
  border-radius: 2px;
}
.trainer-divider { border: none; border-top: 1px solid rgba(255,255,255,0.06); margin: 1.5rem 0; }
.workout-section-lbl {
  font-family: var(--font-display);
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.3);
  margin-bottom: 12px;
}
.workout-chips { display: flex; flex-wrap: wrap; gap: 7px; }
.wchip {
  background: var(--d3);
  color: rgba(255,255,255,0.45);
  font-size: 0.75rem;
  font-family: var(--font-display);
  font-weight: 500;
  letter-spacing: 1px;
  text-transform: uppercase;
  padding: 5px 12px;
  border-radius: 2px;
}

/* ===== GALLERY ===== */
#gallery { background: var(--d1); }
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 240px 240px;
  gap: 12px;
  margin-top: 10px;
}
.gitem {
  border-radius: 4px;
  overflow: hidden;
  background: var(--d3);
  position: relative;
  border: 1px solid rgba(255,255,255,0.04);
}
.gitem img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform 0.4s; }
.gitem:hover img { transform: scale(1.06); }
.gitem.span2 { grid-column: span 2; }
.gitem-label {
  position: absolute; bottom: 12px; left: 12px;
  font-family: var(--font-display);
  font-size: 0.68rem;
  font-weight: 600;
  letter-spacing: 2px;
  text-transform: uppercase;
  background: rgba(0,0,0,0.6);
  color: var(--y);
  padding: 5px 10px;
  border-radius: 2px;
  backdrop-filter: blur(4px);
}
.g-placeholder {
  width: 100%; height: 100%;
  display: flex; align-items: center; justify-content: center;
  flex-direction: column; gap: 10px;
  color: rgba(255,255,255,0.12);
}
.g-placeholder svg { width: 32px; height: 32px; }
.g-placeholder span {
  font-family: var(--font-display);
  font-size: 0.65rem;
  letter-spacing: 2px;
  text-transform: uppercase;
}

/* ===== REVIEWS ===== */
#reviews { background: var(--blk); }
.reviews-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin-top: 10px;
}
.rcard {
  background: var(--d2);
  border: 1px solid rgba(255,255,255,0.05);
  border-radius: 5px;
  padding: 2rem;
  position: relative;
  transition: border-color 0.2s;
}
.rcard:hover { border-color: rgba(245,197,24,0.18); }
.rcard::before {
  content: '"';
  position: absolute;
  top: 12px; right: 20px;
  font-family: var(--font-hero);
  font-size: 5rem;
  color: rgba(245,197,24,0.08);
  line-height: 1;
}
.r-stars { color: var(--y); font-size: 0.9rem; letter-spacing: 3px; margin-bottom: 1rem; }
.r-text {
  font-size: 0.92rem;
  color: rgba(255,255,255,0.6);
  line-height: 1.8;
  font-style: italic;
  font-weight: 300;
  margin-bottom: 1.5rem;
}
.r-author { display: flex; align-items: center; gap: 12px; }
.r-av {
  width: 38px; height: 38px; border-radius: 50%;
  background: rgba(245,197,24,0.12);
  border: 1px solid rgba(245,197,24,0.25);
  display: flex; align-items: center; justify-content: center;
  font-family: var(--font-display);
  font-size: 0.8rem;
  font-weight: 700;
  color: var(--y);
  flex-shrink: 0;
}
.r-name {
  font-family: var(--font-display);
  font-size: 0.9rem;
  font-weight: 600;
  letter-spacing: 1px;
  color: #fff;
}
.r-sub { font-size: 0.72rem; color: var(--gray); font-weight: 300; margin-top: 2px; }

/* ===== CONTACT ===== */
#contact { background: var(--d1); }
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
  margin-top: 10px;
}
.contact-items { display: grid; gap: 14px; }
.ci {
  display: flex; align-items: flex-start; gap: 16px;
  padding: 18px 20px;
  background: var(--d2);
  border-radius: 4px;
  border: 1px solid rgba(245,197,24,0.07);
  transition: border-color 0.2s;
}
.ci:hover { border-color: rgba(245,197,24,0.2); }
.ci-icon {
  width: 42px; height: 42px;
  background: rgba(245,197,24,0.1);
  border-radius: 3px;
  display: flex; align-items: center; justify-content: center;
  flex-shrink: 0;
}
.ci-icon svg { width: 20px; height: 20px; fill: var(--y); }
.ci-lbl {
  font-family: var(--font-display);
  font-size: 0.65rem;
  font-weight: 600;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  color: rgba(255,255,255,0.3);
  margin-bottom: 5px;
}
.ci-val {
  font-size: 0.92rem;
  color: #fff;
  line-height: 1.6;
  font-weight: 400;
}
.ci-val a { color: var(--y); text-decoration: none; }
.contact-map {
  border-radius: 5px;
  overflow: hidden;
  border: 1px solid rgba(245,197,24,0.1);
  height: 100%;
  min-height: 380px;
}
.contact-map iframe {
  width: 100%; height: 100%; min-height: 380px; border: none;
  filter: grayscale(50%) brightness(0.85) contrast(1.1) invert(0.05);
}

/* ===== CTA BANNER ===== */
#cta {
  background: var(--y);
  padding: 70px 6%;
  text-align: center;
}
.cta-title {
  font-family: var(--font-hero);
  font-size: clamp(2.5rem, 6vw, 5rem);
  color: var(--blk);
  letter-spacing: 3px;
  margin-bottom: 10px;
}
.cta-sub {
  font-family: var(--font-display);
  font-size: 0.9rem;
  font-weight: 500;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: rgba(0,0,0,0.5);
  margin-bottom: 2rem;
}
.cta-btn {
  display: inline-block;
  font-family: var(--font-display);
  font-size: 0.9rem;
  font-weight: 700;
  letter-spacing: 2.5px;
  text-transform: uppercase;
  background: var(--blk);
  color: var(--y);
  padding: 16px 40px;
  border-radius: 3px;
  text-decoration: none;
  transition: all 0.2s;
}
.cta-btn:hover { background: #222; transform: translateY(-3px); }

/* ===== FOOTER ===== */
footer {
  background: var(--d2);
  border-top: 1px solid rgba(245,197,24,0.1);
  padding: 30px 6%;
  display: flex; align-items: center; justify-content: space-between; flex-wrap: wrap; gap: 1rem;
}
.f-logo {
  font-family: var(--font-hero);
  font-size: 1.6rem;
  letter-spacing: 3px;
  color: var(--y);
}
.f-logo span { color: #fff; }
.f-copy {
  font-family: var(--font-display);
  font-size: 0.72rem;
  letter-spacing: 1.5px;
  color: var(--gray);
  text-transform: uppercase;
}
.f-links { display: flex; gap: 2rem; }
.f-links a {
  font-family: var(--font-display);
  font-size: 0.72rem;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--gray);
  text-decoration: none;
  transition: color 0.2s;
}
.f-links a:hover { color: var(--y); }

/* ===== WHATSAPP FLOAT ===== */
.wa {
  position: fixed; bottom: 28px; right: 28px; z-index: 999;
  width: 56px; height: 56px; border-radius: 50%;
  background: #25D366;
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 4px 24px rgba(37,211,102,0.4);
  text-decoration: none;
  transition: transform 0.2s, box-shadow 0.2s;
}
.wa:hover { transform: scale(1.12); box-shadow: 0 8px 32px rgba(37,211,102,0.5); }
.wa svg { width: 30px; height: 30px; fill: white; }

/* ===== RESPONSIVE ===== */
@media (max-width: 900px) {
  .nav-links { display: none; }
  .about-grid, .contact-grid, .trainer-wrap { grid-template-columns: 1fr; }
  .timing-grid { grid-template-columns: repeat(2, 1fr); }
  .plans-grid { grid-template-columns: 1fr; }
  .reviews-grid { grid-template-columns: 1fr; }
  .gallery-grid { grid-template-columns: 1fr 1fr; grid-template-rows: auto; }
  .gitem.span2 { grid-column: span 1; }
  .trainer-img { min-height: 200px; }
  .hero-stats { gap: 1.5rem; }
  .about-tag { display: none; }
}
@media (max-width: 500px) {
  .timing-grid, .gallery-grid { grid-template-columns: 1fr; }
  .hero-h1 { font-size: 3.8rem; }
}
</style>
</head>
<body>

<!-- WhatsApp Float -->
<a href="https://wa.me/919616658809" class="wa" target="_blank" title="Chat on WhatsApp">
  <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
</a>

<!-- NAVBAR -->
<nav id="navbar">
  <a href="#hero" class="nav-logo">BMS <span>FITNESS</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#timing">Timing</a></li>
    <li><a href="#plans">Plans</a></li>
    <li><a href="#trainer">Trainer</a></li>
    <li><a href="#gallery">Gallery</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="https://wa.me/919616658809" class="nav-btn">Join Now</a>
</nav>

<!-- ===== HERO ===== -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-pattern"></div>
  <div class="hero-glow"></div>
  <div class="hero-line"></div>
  <div class="hero-content">
    <div class="hero-eyebrow">Ghazipur, Uttar Pradesh</div>
    <h1 class="hero-h1">
      TRANSFORM<br>
      YOUR <span class="y">BODY.</span><br>
      <span class="stroke">CHANGE</span><br>
      YOUR LIFE.
    </h1>
    <p class="hero-tagline">Strength · Discipline · Results</p>
    <p class="hero-desc">BMS Fitness — Ghazipur ka premier gym jahan certified trainers, modern equipment, aur dedicated community milkar aapki fitness journey ko unforgettable banate hain.</p>
    <div class="hero-btns">
      <a href="#plans" class="btn-y">View Membership Plans</a>
      <a href="https://wa.me/919616658809" class="btn-outline">WhatsApp Us</a>
    </div>
    <div class="hero-stats">
      <div>
        <div class="stat-num">60+</div>
        <div class="stat-lbl">Workout Types</div>
      </div>
      <div>
        <div class="stat-num">GOLD</div>
        <div class="stat-lbl">Medal Trainer</div>
      </div>
      <div>
        <div class="stat-num">100%</div>
        <div class="stat-lbl">Certified Staff</div>
      </div>
      <div>
        <div class="stat-num">2</div>
        <div class="stat-lbl">Separate Zones</div>
      </div>
    </div>
  </div>
</section>

<!-- ===== ABOUT ===== -->
<section id="about">
  <div class="s-label">Who We Are</div>
  <h2 class="s-title">Sirf Gym Nahi —<br>Ek Transformation Hub</h2>
  <div class="y-line"></div>
  <div class="about-grid">
    <div class="about-img-wrap">
      <div class="about-img">
        <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=700&q=80" alt="BMS Fitness Gym Interior">
      </div>
      <div class="about-tag">
        <div class="about-tag-num">BMS</div>
        <div class="about-tag-txt">Fitness Center</div>
      </div>
    </div>
    <div>
      <p class="s-sub" style="margin-bottom: 1.5rem; max-width: 100%;">BMS Fitness Ghazipur mein located ek state-of-the-art gym hai jahan har ek member ko individually dhyan diya jaata hai. Hamare Gold Medalist head coach aur certified staff aapke fitness goals ko reality mein badalne ke liye hamesha taiyaar hain.</p>
      <p class="s-sub" style="max-width: 100%; margin-bottom: 0;">Chahe aap beginner hon ya experienced athlete — BMS mein aapke liye dedicated training space, modern machines, aur ek supportive community milegi jo aapko push karti rahegi.</p>
      <div class="features-list">
        <div class="feat">
          <div class="feat-icon">⚡</div>
          <div>
            <div class="feat-title">Modern Equipment</div>
            <div class="feat-desc">Body ke har part ke liye latest aur well-maintained machines available hain.</div>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon">👥</div>
          <div>
            <div class="feat-title">Separate Sections</div>
            <div class="feat-desc">Mahilaon aur purushon ke liye alag-alag dedicated training areas.</div>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon">🏅</div>
          <div>
            <div class="feat-title">Certified Trainers</div>
            <div class="feat-desc">Professional coaches jo aapke goals ke according personalized plan banate hain.</div>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon">💧</div>
          <div>
            <div class="feat-title">Premium Facilities</div>
            <div class="feat-desc">RO drinking water, clean changing area, aur hygienic environment.</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== TIMING ===== -->
<section id="timing">
  <div class="s-label">Gym Hours</div>
  <h2 class="s-title">Kab Aayein?</h2>
  <div class="y-line"></div>
  <div class="timing-grid">
    <div class="t-card">
      <div class="t-emoji">🌅</div>
      <div class="t-lbl">Morning</div>
      <div class="t-time">5:00 AM</div>
      <div class="t-sub">to 10:00 AM — Subah</div>
    </div>
    <div class="t-card">
      <div class="t-emoji">🌇</div>
      <div class="t-lbl">Evening</div>
      <div class="t-time">4:00 PM</div>
      <div class="t-sub">to 9:30 PM — Shaam</div>
    </div>
    <div class="t-card">
      <div class="t-emoji">📅</div>
      <div class="t-lbl">Days Open</div>
      <div class="t-time" style="font-size:1.4rem;">Mon – Sat</div>
      <div class="t-sub">Somvar se Shanivar</div>
    </div>
    <div class="t-card">
      <div class="t-emoji">🔒</div>
      <div class="t-lbl">Sunday</div>
      <div class="t-time t-closed" style="font-size:1.6rem;">Closed</div>
      <div class="t-sub">Ravivar ko band</div>
    </div>
  </div>
</section>

<!-- ===== PLANS ===== -->
<section id="plans">
  <div class="s-label">Membership Plans</div>
  <h2 class="s-title">Apna Plan Chuniye</h2>
  <div class="y-line"></div>
  <p class="s-sub" style="margin-bottom: 2.5rem;">Festive offers aur seasonal discounts ke liye WhatsApp pe sampark karein. Admission par 25% tak ka special offer bhi milta hai!</p>
  <div class="plans-grid">
    <div class="plan">
      <div class="plan-name">Monthly</div>
      <div class="plan-price"><sup>₹</sup>1,000<small style="font-family:'Barlow',sans-serif; font-size:1rem; color:var(--gray)">–1,200</small></div>
      <div class="plan-period">Per Month • Flexible</div>
      <ul class="plan-feats">
        <li>Full equipment access</li>
        <li>Certified trainer guidance</li>
        <li>Separate male/female zones</li>
        <li>RO drinking water</li>
        <li>Clean changing area</li>
      </ul>
      <a href="https://wa.me/919616658809" class="plan-cta cta-ghost">Enquire Now</a>
    </div>
    <div class="plan hot">
      <div class="plan-badge">⭐ Most Popular</div>
      <div class="plan-name">Quarterly</div>
      <div class="plan-price"><sup>₹</sup>2,200</div>
      <div class="plan-period">3 Months • Best Value</div>
      <ul class="plan-feats">
        <li>Everything in Monthly</li>
        <li>Priority training slots</li>
        <li>Progress tracking</li>
        <li>Festive offer eligible</li>
        <li>Flexible batch timing</li>
      </ul>
      <a href="https://wa.me/919616658809" class="plan-cta cta-fill">Join Now</a>
    </div>
    <div class="plan">
      <div class="plan-name">Personal Training</div>
      <div class="plan-price"><sup>₹</sup>6,000</div>
      <div class="plan-period">3 Months • 1-on-1 Sessions</div>
      <ul class="plan-feats">
        <li>Dedicated personal coach</li>
        <li>Custom workout program</li>
        <li>Diet & nutrition guidance</li>
        <li>60+ workout varieties</li>
        <li>Weekly progress review</li>
      </ul>
      <a href="https://wa.me/919616658809" class="plan-cta cta-ghost">Enquire Now</a>
    </div>
  </div>
</section>

<!-- ===== TRAINER ===== -->
<section id="trainer">
  <div class="s-label">Lead Coach</div>
  <h2 class="s-title">Miliye Aapke Coach Se</h2>
  <div class="y-line"></div>
  <div class="trainer-wrap">
    <div class="trainer-img">
      <img src="https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=400&q=80" alt="Dinesh Rawat — Head Trainer BMS Fitness"
        onerror="this.style.display='none'">
      <div class="trainer-img-placeholder">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1"><circle cx="12" cy="7" r="4"/><path d="M6 21v-2a6 6 0 0112 0v2"/></svg>
        <span>Trainer Photo</span>
      </div>
      <div class="trainer-medal">🥇 Gold Medalist</div>
    </div>
    <div class="trainer-info">
      <div class="trainer-name">DINESH RAWAT</div>
      <div class="trainer-role">Head Coach & Founder — BMS Fitness</div>
      <p class="trainer-bio">Dinesh Rawat ek Gold Medalist Bodybuilder hain jinhone kai national fitness competitions mein participate aur win kiya hai. Fitness industry mein unhe unki sateek training techniques ke liye jaana jaata hai. Unka approach friendly, humble aur result-oriented hai — woh har member par personally dhyan dete hain aur unke specific goals ke according tailored strategy banate hain.</p>
      <div class="trainer-tags">
        <span class="ttag">Bodybuilding</span>
        <span class="ttag">Muscle Building</span>
        <span class="ttag">Weight Loss</span>
        <span class="ttag">General Fitness</span>
        <span class="ttag">Instagram: @dineshrawat1205</span>
      </div>
      <hr class="trainer-divider">
      <div class="workout-section-lbl">60+ Workout Areas Covered</div>
      <div class="workout-chips">
        <span class="wchip">Chest</span>
        <span class="wchip">Back</span>
        <span class="wchip">Shoulders</span>
        <span class="wchip">Biceps</span>
        <span class="wchip">Triceps</span>
        <span class="wchip">Core</span>
        <span class="wchip">Legs</span>
        <span class="wchip">Cardio</span>
        <span class="wchip">Abs</span>
        <span class="wchip">Functional</span>
      </div>
    </div>
  </div>
</section>

<!-- ===== GALLERY ===== -->
<section id="gallery">
  <div class="s-label">Gallery</div>
  <h2 class="s-title">Gym Ka Nazar</h2>
  <div class="y-line"></div>
  <div class="gallery-grid">
    <div class="gitem span2">
      <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=900&q=80" alt="BMS Fitness gym floor">
      <div class="gitem-label">Gym Floor</div>
    </div>
    <div class="gitem">
      <img src="https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?w=500&q=80" alt="Weight training area">
      <div class="gitem-label">Weight Zone</div>
    </div>
    <div class="gitem">
      <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?w=500&q=80" alt="Training session">
      <div class="gitem-label">Training</div>
    </div>
    <div class="gitem">
      <img src="https://images.unsplash.com/photo-1526506118085-60ce8714f8c5?w=500&q=80" alt="Cardio equipment">
      <div class="gitem-label">Cardio</div>
    </div>
    <div class="gitem span2">
      <img src="https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?w=900&q=80" alt="Strength training">
      <div class="gitem-label">Strength Zone</div>
    </div>
  </div>
</section>

<!-- ===== REVIEWS ===== -->
<section id="reviews">
  <div class="s-label">Testimonials</div>
  <h2 class="s-title">Members Kya Kehte Hain</h2>
  <div class="y-line"></div>
  <div class="reviews-grid">
    <div class="rcard">
      <div class="r-stars">★★★★★</div>
      <p class="r-text">"BMS mein aane ke baad mere results kaafi achhe hue hain. Dinesh sir bahut acche trainer hain — woh har exercise ko personally correct karte hain aur motivation bhi dete rehte hain. Highly recommend karta hoon!"</p>
      <div class="r-author">
        <div class="r-av">RK</div>
        <div>
          <div class="r-name">Rohit Kumar</div>
          <div class="r-sub">Member since 2023</div>
        </div>
      </div>
    </div>
    <div class="rcard">
      <div class="r-stars">★★★★★</div>
      <p class="r-text">"Ghazipur mein itna achha gym milna mushkil tha. Equipment latest hai, environment clean hai aur trainers bahut cooperative hain. Paisa wasool hai — har rupay ki value milti hai!"</p>
      <div class="r-author">
        <div class="r-av">PS</div>
        <div>
          <div class="r-name">Priya Singh</div>
          <div class="r-sub">Member since 2024</div>
        </div>
      </div>
    </div>
    <div class="rcard">
      <div class="r-stars">★★★★★</div>
      <p class="r-text">"6 mahine mein mera 12 kg weight loss hua. Dinesh sir ka personal attention aur dedication kamaal ka hai. Ladies ke liye alag section hone se bahut comfortable feel hota hai. Best gym in Ghazipur!"</p>
      <div class="r-author">
        <div class="r-av">NA</div>
        <div>
          <div class="r-name">Neha Agarwal</div>
          <div class="r-sub">Member since 2023</div>
        </div>
      </div>
    </div>
    <div class="rcard">
      <div class="r-stars">★★★★☆</div>
      <p class="r-text">"Fees bilkul reasonable hai aur gym ka environment bahut positive hai. Trainer saab friendly hain aur diet ke baare mein bhi guide karte hain. Overall ek bahut achha experience raha hai!"</p>
      <div class="r-author">
        <div class="r-av">AV</div>
        <div>
          <div class="r-name">Amit Verma</div>
          <div class="r-sub">Member since 2024</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== CTA BANNER ===== -->
<section id="cta">
  <div class="cta-title">READY TO TRANSFORM?</div>
  <p class="cta-sub">Abhi join karein — pehli step sabse mushkil hoti hai</p>
  <a href="https://wa.me/919616658809" class="cta-btn">WhatsApp Karein — Join Now</a>
</section>

<!-- ===== CONTACT ===== -->
<section id="contact">
  <div class="s-label">Find Us</div>
  <h2 class="s-title">Sampark Karein</h2>
  <div class="y-line"></div>
  <div class="contact-grid">
    <div class="contact-items">
      <div class="ci">
        <div class="ci-icon">
          <svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>
        </div>
        <div>
          <div class="ci-lbl">Address</div>
          <div class="ci-val">Rauza, Ghazipur, Chandan Baha<br>Uttar Pradesh 233002</div>
        </div>
      </div>
      <div class="ci">
        <div class="ci-icon">
          <svg viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
        </div>
        <div>
          <div class="ci-lbl">Phone / WhatsApp</div>
          <div class="ci-val"><a href="tel:+919616658809">+91 96166 58809</a></div>
        </div>
      </div>
      <div class="ci">
        <div class="ci-icon">
          <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-2 .9-2 2v12c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>
        </div>
        <div>
          <div class="ci-lbl">Email</div>
          <div class="ci-val" style="color: var(--lgray);">bmsfitness.ghazipur@gmail.com</div>
        </div>
      </div>
      <div class="ci">
        <div class="ci-icon">
          <svg viewBox="0 0 24 24"><path d="M11.99 2C6.47 2 2 6.48 2 12s4.47 10 9.99 10C17.52 22 22 17.52 22 12S17.52 2 11.99 2zM12 20c-4.42 0-8-3.58-8-8s3.58-8 8-8 8 3.58 8 8-3.58 8-8 8zm.5-13H11v6l5.25 3.15.75-1.23-4.5-2.67V7z"/></svg>
        </div>
        <div>
          <div class="ci-lbl">Timings</div>
          <div class="ci-val">Mon–Sat: 5:00–10:00 AM &amp; 4:00–9:30 PM<br><span style="color:var(--gray); font-size:0.82rem;">Sunday: Closed</span></div>
        </div>
      </div>
    </div>
    <div class="contact-map">
      <iframe
        src="https://www.google.com/maps?q=25.590541,83.570363&z=15&output=embed"
        allowfullscreen
        loading="lazy"
        title="BMS Fitness Location">
      </iframe>
    </div>
  </div>
</section>

<!-- ===== FOOTER ===== -->
<footer>
  <div class="f-logo">BMS <span>FITNESS</span></div>
  <div class="f-copy">© 2025 BMS Fitness, Ghazipur. All Rights Reserved.</div>
  <div class="f-links">
    <a href="#hero">Home</a>
    <a href="#plans">Plans</a>
    <a href="#trainer">Trainer</a>
    <a href="#contact">Contact</a>
  </div>
</footer>

</body>
</html>
