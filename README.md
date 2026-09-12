<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>অন্তর্জগৎ · Rajia Sultana</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;500;600;700&family=Noto+Serif+Bengali:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<style>
* { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --bg: #fbf7f0;
  --bg-warm: #f5ede0;
  --paper: #fffdf9;
  --ink: #2b1d1a;
  --ink-soft: #6b5550;
  --maroon: #7b2d3b;
  --maroon-deep: #5a1e2a;
  --gold: #c9a24a;
  --gold-soft: #e6cf9a;
  --rose: #d98a94;
  --border: #e8dcc9;
  --shadow-sm: 0 4px 16px rgba(90, 30, 42, 0.06);
  --shadow-md: 0 12px 32px rgba(90, 30, 42, 0.10);
  --shadow-lg: 0 24px 48px rgba(90, 30, 42, 0.14);
}

html { scroll-behavior: smooth; }

body {
  font-family: 'Hind Siliguri', 'Inter', sans-serif;
  background: var(--bg);
  color: var(--ink);
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
  background-image:
    radial-gradient(circle at 10% 0%, rgba(201,162,74,0.05) 0%, transparent 40%),
    radial-gradient(circle at 90% 100%, rgba(123,45,59,0.05) 0%, transparent 40%);
  background-attachment: fixed;
}

img { max-width: 100%; display: block; }
a { text-decoration: none; color: inherit; }
ul { list-style: none; }
button { font-family: inherit; cursor: pointer; border: none; background: none; }

.container { max-width: 1180px; margin: 0 auto; padding: 0 24px; }

.lang-en [data-lang="bn"] { display: none !important; }
.lang-bn [data-lang="en"] { display: none !important; }

/* ============ HEADER ============ */
header {
  position: sticky; top: 0; z-index: 100;
  background: rgba(251, 247, 240, 0.92);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid var(--border);
}

.header-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 14px 0;
  gap: 20px;
}

.logo {
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.7rem;
  font-weight: 700;
  color: var(--maroon);
  display: flex;
  align-items: center;
  gap: 10px;
  white-space: nowrap;
}

.logo i { color: var(--gold); font-size: 1.3rem; }

.search-wrap {
  flex: 1;
  max-width: 420px;
  position: relative;
}

.search-wrap i {
  position: absolute;
  left: 18px;
  top: 50%;
  transform: translateY(-50%);
  color: var(--ink-soft);
  font-size: 0.95rem;
}

.search-input {
  width: 100%;
  padding: 12px 18px 12px 46px;
  border: 1.5px solid var(--border);
  border-radius: 40px;
  background: var(--paper);
  font-size: 0.95rem;
  font-family: inherit;
  color: var(--ink);
  transition: all 0.2s;
}

.search-input:focus {
  outline: none;
  border-color: var(--maroon);
  box-shadow: 0 0 0 4px rgba(123,45,59,0.08);
}

.search-input::placeholder { color: #a89a94; }

.lang-switch {
  display: flex;
  background: var(--paper);
  border: 1px solid var(--border);
  border-radius: 30px;
  padding: 3px;
  font-size: 0.85rem;
  font-weight: 600;
  flex-shrink: 0;
}

.lang-switch button {
  padding: 6px 14px;
  border-radius: 30px;
  color: var(--ink-soft);
  transition: all 0.2s;
}

.lang-switch button.active { background: var(--maroon); color: #fff; }

.header-nav {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  padding: 10px 0;
  border-top: 1px solid var(--border);
  flex-wrap: wrap;
}

.header-nav a {
  padding: 8px 18px;
  border-radius: 30px;
  font-size: 0.94rem;
  font-weight: 500;
  color: var(--ink-soft);
  transition: all 0.2s;
}

.header-nav a:hover { background: rgba(123,45,59,0.08); color: var(--maroon); }
.header-nav a.active { background: var(--maroon); color: #fff; }

/* ============ HERO ============ */
.hero { padding: 70px 0 50px; }

.hero-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 60px;
  align-items: center;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(201,162,74,0.15);
  color: #8a6a1e;
  font-size: 0.82rem;
  font-weight: 600;
  padding: 8px 16px;
  border-radius: 30px;
  margin-bottom: 22px;
}

.hero h1 {
  font-family: 'Noto Serif Bengali', 'Playfair Display', serif;
  font-size: 3.2rem;
  font-weight: 700;
  line-height: 1.25;
  color: var(--ink);
  margin-bottom: 20px;
  letter-spacing: -0.5px;
}

.hero h1 .accent { color: var(--maroon); font-style: italic; }

.hero p.lead {
  font-size: 1.12rem;
  color: var(--ink-soft);
  max-width: 90%;
  margin-bottom: 30px;
}

.hero-actions { display: flex; gap: 12px; flex-wrap: wrap; }

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  padding: 13px 28px;
  border-radius: 40px;
  font-weight: 600;
  font-size: 0.97rem;
  transition: all 0.25s ease;
}

.btn-primary {
  background: var(--maroon);
  color: #fff;
  box-shadow: 0 8px 20px rgba(123,45,59,0.25);
}

.btn-primary:hover { background: var(--maroon-deep); transform: translateY(-2px); }

.btn-outline {
  background: transparent;
  border: 1.5px solid var(--maroon);
  color: var(--maroon);
}

.btn-outline:hover { background: rgba(123,45,59,0.06); }

/* Hero visual */
.hero-visual { display: flex; justify-content: center; }

.book-stack { position: relative; width: 300px; height: 400px; }

.book {
  position: absolute; inset: 0;
  border-radius: 6px 14px 14px 6px;
  box-shadow: var(--shadow-lg);
  transition: transform 0.5s ease;
}

.book-1 {
  background: linear-gradient(135deg, #7b2d3b, #5a1e2a);
  transform: rotate(-8deg) translateX(-18px) translateY(10px);
}

.book-2 {
  background: linear-gradient(135deg, #c9a24a, #a8822e);
  transform: rotate(4deg) translateX(28px) translateY(-15px);
}

.book-3 {
  background: var(--paper);
  border: 1px solid var(--border);
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  padding: 40px 30px; text-align: center;
}

.book-title {
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--maroon);
  margin-bottom: 12px;
}

.book-author {
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 0.95rem;
  color: var(--gold);
  margin-bottom: 12px;
}

.book-divider { width: 40px; height: 2px; background: var(--gold); margin: 16px auto; }

.book-sub { font-size: 0.82rem; color: var(--ink-soft); font-style: italic; }

.hero:hover .book-1 { transform: rotate(-12deg) translateX(-28px) translateY(15px); }
.hero:hover .book-2 { transform: rotate(8deg) translateX(38px) translateY(-20px); }

/* ============ SECTION ============ */
.section { padding: 60px 0; }

.section-head { text-align: center; margin-bottom: 40px; }

.section-head .kicker {
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 12px;
}

.section-head h2 {
  font-family: 'Noto Serif Bengali', 'Playfair Display', serif;
  font-size: 2.2rem;
  font-weight: 700;
  margin-bottom: 14px;
}

.section-head p {
  color: var(--ink-soft);
  font-size: 1.05rem;
  max-width: 600px;
  margin: 0 auto;
}

/* ============ FILTER ============ */
.filter-bar {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  justify-content: center;
  margin-bottom: 36px;
}

.chip {
  padding: 8px 20px;
  border-radius: 30px;
  border: 1.5px solid var(--border);
  background: var(--paper);
  color: var(--ink-soft);
  font-size: 0.9rem;
  font-weight: 600;
  transition: all 0.2s;
}

.chip:hover { border-color: var(--maroon); color: var(--maroon); }
.chip.active { background: var(--maroon); color: #fff; border-color: var(--maroon); }

/* ============ WRITING CARDS ============ */
.writings-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 26px;
}

.writing-card {
  background: var(--paper);
  border-radius: 18px;
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  border: 1px solid var(--border);
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
  cursor: pointer;
}

.writing-card:hover {
  transform: translateY(-8px);
  box-shadow: var(--shadow-md);
  border-color: var(--gold-soft);
}

.writing-card.hidden { display: none; }

.writing-visual { height: 180px; position: relative; overflow: hidden; }

.placeholder-img {
  position: absolute; inset: 0;
  background-size: cover;
  background-position: center;
  transition: transform 0.5s;
}

.writing-card:hover .placeholder-img { transform: scale(1.06); }

.writing-visual::after {
  content: '';
  position: absolute; inset: 0;
  background: linear-gradient(to top, rgba(43,29,26,0.55), transparent 60%);
}

.unit-label {
  position: absolute; top: 14px; left: 14px;
  background: rgba(255,253,249,0.95);
  color: var(--maroon);
  font-size: 0.75rem;
  font-weight: 700;
  padding: 5px 12px;
  border-radius: 20px;
  z-index: 2;
}

.category-tag {
  position: absolute; bottom: 14px; left: 14px;
  background: var(--gold);
  color: #fff;
  font-size: 0.72rem;
  font-weight: 700;
  padding: 4px 12px;
  border-radius: 20px;
  z-index: 2;
}

.writing-body {
  padding: 22px 22px 24px;
  flex: 1;
  display: flex;
  flex-direction: column;
}

.writing-body h3 {
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--ink);
  margin-bottom: 10px;
  line-height: 1.45;
}

.writing-body p {
  color: var(--ink-soft);
  font-size: 0.93rem;
  flex: 1;
  margin-bottom: 18px;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.writing-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 16px;
  border-top: 1px dashed var(--border);
}

.writing-footer .date {
  font-size: 0.8rem;
  color: var(--ink-soft);
  font-weight: 500;
}

.read-link {
  color: var(--maroon);
  font-weight: 600;
  font-size: 0.9rem;
  display: inline-flex;
  align-items: center;
  gap: 6px;
  transition: gap 0.2s;
}

.writing-card:hover .read-link { gap: 10px; }

.no-results {
  text-align: center;
  padding: 60px 20px;
  color: var(--ink-soft);
  display: none;
}

.no-results.show { display: block; }
.no-results i { font-size: 3rem; color: var(--gold-soft); margin-bottom: 16px; }

.no-results h3 {
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.4rem;
  color: var(--ink);
  margin-bottom: 8px;
}

/* ============ ABOUT ============ */
.about-wrap {
  display: grid;
  grid-template-columns: 0.8fr 1.2fr;
  gap: 50px;
  align-items: center;
  background: var(--paper);
  border-radius: 24px;
  padding: 50px;
  border: 1px solid var(--border);
  box-shadow: var(--shadow-sm);
}

.about-photo {
  aspect-ratio: 1;
  border-radius: 50%;
  background: linear-gradient(135deg, var(--gold-soft), var(--rose));
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 4.5rem;
  color: #fff;
  box-shadow: var(--shadow-md);
  position: relative;
}

.about-photo::before {
  content: '';
  position: absolute;
  inset: -12px;
  border: 2px dashed var(--gold);
  border-radius: 50%;
  opacity: 0.5;
}

.about-text h2 {
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.9rem;
  color: var(--maroon);
  margin-bottom: 18px;
}

.about-text .author-name-en {
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 1.15rem;
  color: var(--gold);
  display: block;
  margin-top: -10px;
  margin-bottom: 18px;
}

.about-text p {
  color: var(--ink-soft);
  font-size: 1.02rem;
  margin-bottom: 14px;
}

.about-signature {
  font-family: 'Playfair Display', serif;
  font-style: italic;
  font-size: 1.5rem;
  color: var(--gold);
  margin-top: 20px;
}

/* ============ CTA ============ */
.cta-strip {
  background: linear-gradient(135deg, var(--maroon), var(--maroon-deep));
  border-radius: 24px;
  padding: 55px 45px;
  text-align: center;
  color: #fff;
  box-shadow: var(--shadow-md);
}

.cta-strip h2 {
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.9rem;
  margin-bottom: 12px;
}

.cta-strip p {
  color: rgba(255,255,255,0.85);
  max-width: 520px;
  margin: 0 auto 26px;
}

.cta-strip .btn { background: var(--gold); color: var(--ink); }
.cta-strip .btn:hover { background: #d9b055; }

/* ============ FOOTER ============ */
footer {
  background: #2b1d1a;
  color: #b8a89f;
  padding: 55px 0 28px;
  margin-top: 70px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.6fr 1fr 1fr;
  gap: 45px;
  margin-bottom: 45px;
}

.footer-brand .logo { color: #fff; margin-bottom: 16px; }

.footer-brand p {
  font-size: 0.93rem;
  max-width: 320px;
  line-height: 1.7;
  margin-bottom: 20px;
}

.socials { display: flex; gap: 12px; }

.socials a {
  width: 40px; height: 40px;
  background: rgba(255,255,255,0.08);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  transition: all 0.2s;
}

.socials a:hover { background: var(--gold); color: var(--ink); transform: translateY(-3px); }

.footer-col h4 {
  color: #fff;
  font-family: 'Noto Serif Bengali', serif;
  font-size: 1.02rem;
  margin-bottom: 18px;
}

.footer-col ul li { margin-bottom: 10px; }
.footer-col ul a { transition: color 0.2s; font-size: 0.93rem; }
.footer-col ul a:hover { color: var(--gold); }

.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.08);
  padding-top: 24px;
  text-align: center;
  font-size: 0.87rem;
}

.footer-bottom i { color: var(--rose); }

#backTop {
  position: fixed;
  bottom: 28px;
  right: 28px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: var(--maroon);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.1rem;
  box-shadow: var(--shadow-md);
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s;
  z-index: 90;
}

#backTop.show { opacity: 1; visibility: visible; }
#backTop:hover { background: var(--maroon-deep); transform: translateY(-4px); }

/* ============ RESPONSIVE ============ */
@media (max-width: 980px) {
  .hero-grid { grid-template-columns: 1fr; gap: 40px; }
  .hero-visual { order: -1; }
  .book-stack { width: 240px; height: 320px; }
  .writings-grid { grid-template-columns: repeat(2, 1fr); }
  .about-wrap { grid-template-columns: 1fr; padding: 36px; }
  .about-photo { max-width: 180px; margin: 0 auto; }
  .search-wrap { max-width: 100%; }
}

@media (max-width: 700px) {
  .header-top { flex-wrap: wrap; }
  .search-wrap { order: 3; flex-basis: 100%; max-width: 100%; }
  .hero h1 { font-size: 2.1rem; }
  .hero p.lead { max-width: 100%; }
  .writings-grid { grid-template-columns: 1fr; }
  .section { padding: 45px 0; }
  .section-head h2 { font-size: 1.7rem; }
  .cta-strip { padding: 40px 24px; }
  .cta-strip h2 { font-size: 1.4rem; }
  .footer-grid { grid-template-columns: 1fr; gap: 32px; }
  .logo { font-size: 1.4rem; }
  .header-nav a { padding: 6px 12px; font-size: 0.86rem; }
}
</style>
</head>

<body class="lang-bn">

<!-- ============ HEADER ============ -->
<header>
  <div class="container">
    <div class="header-top">
      <a href="#" class="logo">
        <i class="fas fa-feather-alt"></i>
        <span data-lang="bn">অন্তর্জগৎ</span>
        <span data-lang="en">Antorjogot</span>
      </a>

      <div class="search-wrap">
        <i class="fas fa-search"></i>
        <input type="text" class="search-input" id="searchInput"
               placeholder="লেখা খুঁজুন..." data-ph-bn="লেখা খুঁজুন..." data-ph-en="Search writings...">
      </div>

      <div class="lang-switch">
        <button id="btn-bn" class="active" onclick="setLang('bn')">বাং</button>
        <button id="btn-en" onclick="setLang('en')">EN</button>
      </div>
    </div>

    <!-- NAVIGATION — নাম আপডেটেড -->
    <nav class="header-nav">
      <a href="#" class="active" data-lang="bn">🏠 হোম</a>
      <a href="#" class="active" data-lang="en">🏠 Home</a>

      <a href="#writings" data-lang="bn">📖 সব লেখা</a>
      <a href="#writings" data-lang="en">📖 All Writings</a>

      <a href="#about" data-lang="bn">✍️ Rajia Sultana</a>
      <a href="#about" data-lang="en">✍️ Rajia Sultana</a>

      <a href="#contact" data-lang="bn">💌 যোগাযোগ</a>
      <a href="#contact" data-lang="en">💌 Contact</a>
    </nav>
  </div>
</header>

<!-- ============ HERO ============ -->
<section class="hero">
  <div class="container hero-grid">
    <div class="hero-content">
      <span class="hero-badge">
        <i class="fas fa-heart"></i>
        <span data-lang="bn">Rajia Sultana · হৃদয় থেকে লেখা</span>
        <span data-lang="en">Rajia Sultana · Written from the heart</span>
      </span>

      <h1 data-lang="bn">
        প্রতিটি লেখা <span class="accent">একটি অনুভূতি</span>,<br>
        প্রতিটি শব্দ একটি গল্প।
      </h1>
      <h1 data-lang="en">
        Every writing is <span class="accent">a feeling</span>,<br>
        every word a story.
      </h1>

      <p class="lead" data-lang="bn">
        আমার ডায়েরির পাতা থেকে ছোট ছোট ক্যাপশন, ভালোবাসার গল্প, আর মনের গভীরে লুকানো আবেগ — সব এক জায়গায়।
      </p>
      <p class="lead" data-lang="en">
        Short captions, love stories, and emotions hidden deep within — all from the pages of my diary.
      </p>

      <div class="hero-actions">
        <a href="#writings" class="btn btn-primary">
          <i class="fas fa-book-open"></i>
          <span data-lang="bn">পড়া শুরু করুন</span>
          <span data-lang="en">Start reading</span>
        </a>
        <a href="#about" class="btn btn-outline">
          <i class="fas fa-user-pen"></i>
          <span data-lang="bn">Rajia সম্পর্কে</span>
          <span data-lang="en">About Rajia</span>
        </a>
      </div>
    </div>

    <div class="hero-visual">
      <div class="book-stack">
        <div class="book book-1"></div>
        <div class="book book-2"></div>
        <div class="book book-3">
          <div class="book-title" data-lang="bn">অন্তর্জগৎ</div>
          <div class="book-title" data-lang="en" style="font-family:'Playfair Display',serif; font-style:italic;">Antorjogot</div>
          <div class="book-author">Rajia Sultana</div>
          <div class="book-divider"></div>
          <div class="book-sub" data-lang="bn">একটি ডায়েরির গল্প</div>
          <div class="book-sub" data-lang="en">A diary's tale</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ============ WRITINGS ============ -->
<section class="section" id="writings">
  <div class="container">
    <div class="section-head">
      <div class="kicker" data-lang="bn">আমার লেখা</div>
      <div class="kicker" data-lang="en">My writings</div>

      <h2 data-lang="bn">ক্যাপশন থেকে বইয়ের পাতা</h2>
      <h2 data-lang="en">From captions to book pages</h2>

      <p data-lang="bn">প্রতিটি লেখা ছোট ছোট ইউনিটে সাজানো। ক্যাটাগরি বেছে নিন বা সার্চ করুন।</p>
      <p data-lang="en">Each piece is arranged in small units. Pick a category or search.</p>
    </div>

    <div class="filter-bar" id="filterBar">
      <button class="chip active" data-filter="all" data-lang="bn">সব</button>
      <button class="chip active" data-filter="all" data-lang="en">All</button>

      <button class="chip" data-filter="love" data-lang="bn">ভালোবাসা</button>
      <button class="chip" data-filter="love" data-lang="en">Love</button>

      <button class="chip" data-filter="longing" data-lang="bn">বিরহ</button>
      <button class="chip" data-filter="longing" data-lang="en">Longing</button>

      <button class="chip" data-filter="hope" data-lang="bn">আশা</button>
      <button class="chip" data-filter="hope" data-lang="en">Hope</button>

      <button class="chip" data-filter="memory" data-lang="bn">স্মৃতি</button>
      <button class="chip" data-filter="memory" data-lang="en">Memory</button>
    </div>

    <div class="writings-grid" id="writingsGrid">

      <article class="writing-card" data-category="love"
               data-search-bn="প্রথম দেখা love ভালোবাসা চোখ" data-search-en="first meeting love eyes">
        <div class="writing-visual">
          <div class="placeholder-img" style="background: linear-gradient(135deg, #d98a94, #7b2d3b);"></div>
          <span class="unit-label" data-lang="bn">ইউনিট ০১</span>
          <span class="unit-label" data-lang="en">Unit 01</span>
          <span class="category-tag" data-lang="bn">ভালোবাসা</span>
          <span class="category-tag" data-lang="en">Love</span>
        </div>
        <div class="writing-body">
          <h3 data-lang="bn">প্রথম দেখা</h3>
          <h3 data-lang="en">The First Meeting</h3>
          <p data-lang="bn">যেদিন প্রথম দেখা, সেদিন মনে হয়েছিল সময় থেমে গেছে। তোমার চোখে আমি খুঁজে পেয়েছিলাম আমার সব উত্তর।</p>
          <p data-lang="en">The day we first met, time itself seemed to pause. In your eyes, I found every answer.</p>
          <div class="writing-footer">
            <span class="date"><i class="far fa-calendar"></i> 12 মে ২০২৫</span>
            <a href="#" class="read-link">
              <span data-lang="bn">পড়ুন</span><span data-lang="en">Read</span>
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </article>

      <article class="writing-card" data-category="longing"
               data-search-bn="বৃষ্টিভেজা সন্ধ্যা বিরহ বৃষ্টি" data-search-en="rain evening longing">
        <div class="writing-visual">
          <div class="placeholder-img" style="background: linear-gradient(135deg, #c9a24a, #8a6a1e);"></div>
          <span class="unit-label" data-lang="bn">ইউনিট ০২</span>
          <span class="unit-label" data-lang="en">Unit 02</span>
          <span class="category-tag" data-lang="bn">বিরহ</span>
          <span class="category-tag" data-lang="en">Longing</span>
        </div>
        <div class="writing-body">
          <h3 data-lang="bn">বৃষ্টিভেজা সন্ধ্যা</h3>
          <h3 data-lang="en">A Rain-Soaked Evening</h3>
          <p data-lang="bn">বৃষ্টির শব্দে তোমার নাম ভেসে আসে। জানালার কাচে জমে থাকা জলফোঁটায় দেখি তোমার হাসি।</p>
          <p data-lang="en">Your name drifts in with the sound of rain. In the droplets, I see your smile.</p>
          <div class="writing-footer">
            <span class="date"><i class="far fa-calendar"></i> 28 জুন ২০২৫</span>
            <a href="#" class="read-link">
              <span data-lang="bn">পড়ুন</span><span data-lang="en">Read</span>
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </article>

      <article class="writing-card" data-category="memory"
               data-search-bn="চিঠি পাঠাইনি স্মৃতি" data-search-en="letter unsent memory">
        <div class="writing-visual">
          <div class="placeholder-img" style="background: linear-gradient(135deg, #a87a94, #5a1e2a);"></div>
          <span class="unit-label" data-lang="bn">ইউনিট ০৩</span>
          <span class="unit-label" data-lang="en">Unit 03</span>
          <span class="category-tag" data-lang="bn">স্মৃতি</span>
          <span class="category-tag" data-lang="en">Memory</span>
        </div>
        <div class="writing-body">
          <h3 data-lang="bn">চিঠি যা কখনো পাঠাইনি</h3>
          <h3 data-lang="en">The Letter I Never Sent</h3>
          <p data-lang="bn">লিখেছিলাম অনেক কিছু, কিন্তু পাঠানো হয়নি। কারণ কিছু কথা চুপচাপ বুকে রাখাই ভালো।</p>
          <p data-lang="en">I wrote so much, but never sent it. Some words are better kept quietly in the heart.</p>
          <div class="writing-footer">
            <span class="date"><i class="far fa-calendar"></i> 05 জুলাই ২০২৫</span>
            <a href="#" class="read-link">
              <span data-lang="bn">পড়ুন</span><span data-lang="en">Read</span>
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </article>

      <article class="writing-card" data-category="longing"
               data-search-bn="শেষ দেখা বিদায় বিরহ" data-search-en="last goodbye farewell">
        <div class="writing-visual">
          <div class="placeholder-img" style="background: linear-gradient(135deg, #b76e79, #4a1f28);"></div>
          <span class="unit-label" data-lang="bn">ইউনিট ০৪</span>
          <span class="unit-label" data-lang="en">Unit 04</span>
          <span class="category-tag" data-lang="bn">বিরহ</span>
          <span class="category-tag" data-lang="en">Longing</span>
        </div>
        <div class="writing-body">
          <h3 data-lang="bn">শেষ দেখা</h3>
          <h3 data-lang="en">The Last Goodbye</h3>
          <p data-lang="bn">বিদায়ের সময় কেউ কিছু বলে না, শুধু চোখ দুটো সব বলে দেয়। ভালোবাসা মানে ছেড়ে দেয়াও।</p>
          <p data-lang="en">At goodbye, no one says anything — only the eyes speak. Love can also mean letting go.</p>
          <div class="writing-footer">
            <span class="date"><i class="far fa-calendar"></i> 19 আগস্ট ২০২৫</span>
            <a href="#" class="read-link">
              <span data-lang="bn">পড়ুন</span><span data-lang="en">Read</span>
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </article>

      <article class="writing-card" data-category="love"
               data-search-bn="তোমার নাম ভালোবাসা প্রার্থনা" data-search-en="your name love prayer">
        <div class="writing-visual">
          <div class="placeholder-img" style="background: linear-gradient(135deg, #c9a24a, #7b2d3b);"></div>
          <span class="unit-label" data-lang="bn">ইউনিট ০৫</span>
          <span class="unit-label" data-lang="en">Unit 05</span>
          <span class="category-tag" data-lang="bn">ভালোবাসা</span>
          <span class="category-tag" data-lang="en">Love</span>
        </div>
        <div class="writing-body">
          <h3 data-lang="bn">তোমার নাম</h3>
          <h3 data-lang="en">Your Name</h3>
          <p data-lang="bn">তোমার নামটা আমার কাছে একটা প্রার্থনার মতো। প্রতিবার উচ্চারণ করলে মনে হয় পৃথিবীটা একটু থেমে যায়।</p>
          <p data-lang="en">Your name is like a prayer to me. Every time I say it, the world seems to pause.</p>
          <div class="writing-footer">
            <span class="date"><i class="far fa-calendar"></i> 02 সেপ্টেম্বর ২০২৫</span>
            <a href="#" class="read-link">
              <span data-lang="bn">পড়ুন</span><span data-lang="en">Read</span>
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </article>

      <article class="writing-card" data-category="hope"
               data-search-bn="নীরবতা আশা অনুভূতি" data-search-en="silence hope feeling">
        <div class="writing-visual">
          <div class="placeholder-img" style="background: linear-gradient(135deg, #8a6a1e, #2b1d1a);"></div>
          <span class="unit-label" data-lang="bn">ইউনিট ০৬</span>
          <span class="unit-label" data-lang="en">Unit 06</span>
          <span class="category-tag" data-lang="bn">আশা</span>
          <span class="category-tag" data-lang="en">Hope</span>
        </div>
        <div class="writing-body">
          <h3 data-lang="bn">নীরবতা</h3>
          <h3 data-lang="en">Silence</h3>
          <p data-lang="bn">কিছু কথা বলা যায় না, শুধু অনুভব করা যায়। নীরবতাও এক ধরনের ভাষা — যদি কেউ বুঝতে পারে।</p>
          <p data-lang="en">Some things cannot be said — only felt. Silence is also a language, if only someone understands.</p>
          <div class="writing-footer">
            <span class="date"><i class="far fa-calendar"></i> 10 সেপ্টেম্বর ২০২৫</span>
            <a href="#" class="read-link">
              <span data-lang="bn">পড়ুন</span><span data-lang="en">Read</span>
              <i class="fas fa-arrow-right"></i>
            </a>
          </div>
        </div>
      </article>

    </div>

    <div class="no-results" id="noResults">
      <i class="fas fa-feather"></i>
      <h3 data-lang="bn">কিছু পাওয়া যায়নি</h3>
      <h3 data-lang="en">Nothing found</h3>
      <p data-lang="bn">অন্য কিছু দিয়ে খুঁজে দেখুন।</p>
      <p data-lang="en">Try searching something else.</p>
    </div>
  </div>
</section>

<!-- ============ ABOUT ============ -->
<section class="section" id="about">
  <div class="container">
    <div class="about-wrap">
      <div class="about-photo"><i class="fas fa-pen-fancy"></i></div>
      <div class="about-text">
        <h2 data-lang="bn">Rajia Sultana সম্পর্কে</h2>
        <h2 data-lang="en">About Rajia Sultana</h2>
        <span class="author-name-en">Rajia Sultana</span>

        <p data-lang="bn">আমি রাজিয়া সুলতানা, একজন সাধারণ মানুষ — যার সবচেয়ে বড় সম্পদ তার ডায়েরি। ছোটবেলা থেকেই মনের কথা লিখে রাখতাম, কখনো কাগজে, কখনো মোবাইলের নোটে।</p>
        <p data-lang="en">I am Rajia Sultana, an ordinary person whose greatest treasure is a diary. From a young age, I have written what my heart feels.</p>

        <p data-lang="bn">এই ওয়েবসাইট আমার সেই লেখাগুলোর ঠিকানা। ভালোবাসা, বিরহ, আশা আর অনুভূতির ছোট ছোট টুকরো — যাতে কেউ পড়ে নিজের গল্প খুঁজে পায়।</p>
        <p data-lang="en">This website is the home of those writings. Fragments of love, longing, hope and emotion — so someone may find their own story.</p>

        <div class="about-signature">— Rajia Sultana</div>
      </div>
    </div>
  </div>
</section>

<!-- ============ CTA ============ -->
<section class="section" id="contact">
  <div class="container">
    <div class="cta-strip">
      <h2 data-lang="bn">আপনার অনুভূতি শেয়ার করুন</h2>
      <h2 data-lang="en">Share your feelings</h2>

      <p data-lang="bn">কোনো লেখা আপনার মন ছুঁয়ে গেলে জানান। আপনার প্রতিটি কথা আমার কাছে গুরুত্বপূর্ণ।</p>
      <p data-lang="en">If any writing touched your heart, let me know. Every word from you matters.</p>

      <a href="mailto:hello@example.com" class="btn">
        <i class="fas fa-envelope"></i>
        <span data-lang="bn">Rajia কে লিখুন</span>
        <span data-lang="en">Write to Rajia</span>
      </a>
    </div>
  </div>
</section>

<!-- ============ FOOTER ============ -->
<footer>
  <div class="container">
    <div class="footer-grid">
      <div class="footer-brand">
        <a href="#" class="logo">
          <i class="fas fa-feather-alt"></i>
          <span data-lang="bn">অন্তর্জগৎ</span>
          <span data-lang="en">Antorjogot</span>
        </a>
        <p data-lang="bn">Rajia Sultana এর হৃদয়ের গভীর থেকে লেখা ছোট ছোট গল্প, ক্যাপশন আর অনুভূতির ঠিকানা।</p>
        <p data-lang="en">A home for short stories, captions, and emotions written by Rajia Sultana from the depths of the heart.</p>

        <div class="socials">
          <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
          <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
          <a href="#" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
          <a href="#" aria-label="Email"><i class="fas fa-envelope"></i></a>
        </div>
      </div>

      <div class="footer-col">
        <h4 data-lang="bn">দ্রুত লিংক</h4>
        <h4 data-lang="en">Quick links</h4>
        <ul>
          <li><a href="#writings" data-lang="bn">সব লেখা</a><a href="#writings" data-lang="en">All writings</a></li>
          <li><a href="#about" data-lang="bn">Rajia Sultana</a><a href="#about" data-lang="en">Rajia Sultana</a></li>
          <li><a href="#contact" data-lang="bn">যোগাযোগ</a><a href="#contact" data-lang="en">Contact</a></li>
        </ul>
      </div>

      <div class="footer-col">
        <h4 data-lang="bn">যোগাযোগ</h4>
        <h4 data-lang="en">Get in touch</h4>
        <ul>
          <li><a href="mailto:hello@example.com"><i class="fas fa-envelope"></i> hello@example.com</a></li>
          <li><a href="#"><i class="fab fa-facebook"></i> Facebook</a></li>
          <li><a href="#"><i class="fab fa-instagram"></i> Instagram</a></li>
        </ul>
      </div>
    </div>

    <div class="footer-bottom">
      <p>
        © 2025 <span data-lang="bn">অন্তর্জগৎ</span><span data-lang="en">Antorjogot</span> ·
        <span data-lang="bn">লিখেছেন <strong>Rajia Sultana</strong></span>
        <span data-lang="en">Written by <strong>Rajia Sultana</strong></span>
        <i class="fas fa-heart"></i>
      </p>
    </div>
  </div>
</footer>

<button id="backTop" aria-label="Back to top">
  <i class="fas fa-chevron-up"></i>
</button>

<script>
function setLang(lang) {
  document.body.className = 'lang-' + lang;
  document.documentElement.lang = lang;
  document.getElementById('btn-bn').classList.toggle('active', lang === 'bn');
  document.getElementById('btn-en').classList.toggle('active', lang === 'en');
  const si = document.getElementById('searchInput');
  si.placeholder = lang === 'bn' ? si.dataset.phBn : si.dataset.phEn;
  try { localStorage.setItem('siteLang', lang); } catch(e) {}
}

const searchInput = document.getElementById('searchInput');
const cards = document.querySelectorAll('.writing-card');
const noResults = document.getElementById('noResults');
const chips = document.querySelectorAll('.chip');
let currentFilter = 'all';

function applyFilters() {
  const q = searchInput.value.trim().toLowerCase();
  const lang = document.body.classList.contains('lang-en') ? 'en' : 'bn';
  let visibleCount = 0;

  cards.forEach(card => {
    const cat = card.dataset.category;
    const searchText = (lang === 'bn' ? card.dataset.searchBn : card.dataset.searchEn) || '';
    const title = card.querySelector('h3[data-lang="' + lang + '"]')?.textContent.toLowerCase() || '';
    const body = card.querySelector('p[data-lang="' + lang + '"]')?.textContent.toLowerCase() || '';

    const catMatch = (currentFilter === 'all') || (cat === currentFilter);
    const searchMatch = q === '' || searchText.includes(q) || title.includes(q) || body.includes(q);

    if (catMatch && searchMatch) {
      card.classList.remove('hidden');
      visibleCount++;
    } else {
      card.classList.add('hidden');
    }
  });

  noResults.classList.toggle('show', visibleCount === 0);
}

searchInput.addEventListener('input', applyFilters);

chips.forEach(chip => {
  chip.addEventListener('click', () => {
    chips.forEach(c => c.classList.remove('active'));
    chips.forEach(c => {
      if (c.dataset.filter === chip.dataset.filter) c.classList.add('active');
    });
    currentFilter = chip.dataset.filter;
    applyFilters();
  });
});

const backTop = document.getElementById('backTop');
window.addEventListener('scroll', () => {
  backTop.classList.toggle('show', window.scrollY > 400);
});
backTop.addEventListener('click', () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
});

(function() {
  try {
    const saved = localStorage.getItem('siteLang');
    if (saved === 'en') setLang('en');
    else setLang('bn');
  } catch(e) {}
})();
</script>

</body>
</html>
