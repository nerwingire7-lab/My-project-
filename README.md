<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Portofolio pribadi Nerwin Gire, mahasiswa Rekayasa Perangkat Lunak.">
  <title>Nerwin Gire — Software Engineering Student</title>
  <style>
    :root {
      --bg: #080b16;
      --panel: rgba(17, 24, 43, .76);
      --text: #eef3ff;
      --muted: #9ba8c2;
      --cyan: #64e7f5;
      --violet: #a78bfa;
      --line: rgba(164, 190, 230, .15);
      --glow: 0 0 38px rgba(100, 231, 245, .13);
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      color: var(--text);
      background:
        radial-gradient(ellipse at 12% 8%, rgba(58, 91, 174, .22), transparent 34rem),
        radial-gradient(ellipse at 88% 34%, rgba(128, 76, 205, .16), transparent 32rem),
        var(--bg);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.65;
      overflow-x: hidden;
    }
    body::before {
      content: ""; position: fixed; inset: 0; pointer-events: none; opacity: .17; z-index: -1;
      background-image: linear-gradient(rgba(155,180,220,.08) 1px, transparent 1px),
                        linear-gradient(90deg, rgba(155,180,220,.08) 1px, transparent 1px);
      background-size: 54px 54px;
      mask-image: linear-gradient(to bottom, black, transparent 80%);
    }
    a { color: inherit; text-decoration: none; }
    .wrap { width: min(1120px, calc(100% - 44px)); margin: auto; }
    header { position: sticky; top: 0; z-index: 10; backdrop-filter: blur(18px); background: rgba(8,11,22,.78); border-bottom: 1px solid var(--line); }
    nav { min-height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 24px; }
    .brand { font-weight: 800; letter-spacing: .04em; font-size: 1.12rem; }
    .brand span { color: var(--cyan); }
    .nav-links { display: flex; align-items: center; gap: 30px; color: var(--muted); font-size: .92rem; }
    .nav-links a:hover { color: var(--cyan); }
    .menu-btn { display: none; border: 1px solid var(--line); color: var(--text); background: var(--panel); border-radius: 10px; padding: 8px 12px; }
    .hero { min-height: 690px; display: grid; grid-template-columns: 1.2fr .8fr; align-items: center; gap: 56px; padding: 86px 0 100px; }
    .eyebrow { color: var(--cyan); font-size: .78rem; font-weight: 700; letter-spacing: .2em; text-transform: uppercase; display: flex; align-items: center; gap: 12px; }
    .eyebrow::before { content: ""; width: 30px; height: 1px; background: var(--cyan); }
    h1 { font-size: clamp(3.1rem, 7vw, 6.1rem); line-height: .99; letter-spacing: -.065em; margin: 22px 0; }
    h1 span { color: transparent; background: linear-gradient(100deg, var(--cyan), #b6a0ff 75%); background-clip: text; -webkit-background-clip: text; }
    .intro { max-width: 610px; color: var(--muted); font-size: 1.08rem; }
    .hero-actions { display: flex; flex-wrap: wrap; gap: 14px; margin-top: 32px; }
    .btn { padding: 12px 20px; border-radius: 12px; font-weight: 700; font-size: .92rem; transition: .25s; display: inline-flex; align-items: center; gap: 9px; }
    .btn-primary { color: #07121a; background: linear-gradient(110deg, var(--cyan), #a6c7ff); box-shadow: 0 8px 30px rgba(100,231,245,.18); }
    .btn-primary:hover { transform: translateY(-3px); box-shadow: 0 12px 34px rgba(100,231,245,.28); }
    .btn-ghost { border: 1px solid var(--line); color: var(--text); background: rgba(255,255,255,.025); }
    .btn-ghost:hover { border-color: var(--cyan); color: var(--cyan); }
    .visual { min-height: 420px; display: grid; place-items: center; position: relative; }
    .orbit { width: min(340px, 75vw); aspect-ratio: 1; border: 1px solid rgba(100,231,245,.28); border-radius: 50%; display: grid; place-items: center; position: relative; box-shadow: var(--glow), inset 0 0 55px rgba(100,231,245,.05); }
    .orbit::before, .orbit::after { content: ""; position: absolute; border: 1px solid rgba(167,139,250,.25); border-radius: 50%; }
    .orbit::before { inset: 24px; }
    .orbit::after { inset: -24px; border-style: dashed; animation: spin 34s linear infinite; }
    .core { width: 66%; aspect-ratio: 1; border-radius: 32%; transform: rotate(45deg); background: linear-gradient(135deg, rgba(100,231,245,.18), rgba(167,139,250,.19)); border: 1px solid rgba(185,220,255,.4); display: grid; place-items: center; box-shadow: 0 0 70px rgba(100,231,245,.16); }
    .core strong { transform: rotate(-45deg); font-size: clamp(3.5rem, 8vw, 5.6rem); letter-spacing: -.1em; color: var(--text); text-shadow: 0 0 24px rgba(100,231,245,.4); }
    .orbit-label { position: absolute; padding: 8px 12px; background: #10182b; border: 1px solid var(--line); border-radius: 9px; color: var(--cyan); font: 700 .75rem ui-monospace, monospace; }
    .label-one { top: 13%; right: -8%; } .label-two { bottom: 13%; left: -9%; }
    @keyframes spin { to { transform: rotate(360deg); } }
    section { padding: 82px 0; }
    .section-head { margin-bottom: 34px; }
    .section-kicker { color: var(--cyan); font-size: .75rem; font-weight: 800; letter-spacing: .18em; text-transform: uppercase; }
    h2 { font-size: clamp(2rem, 4vw, 3rem); letter-spacing: -.045em; margin-top: 8px; }
    .section-desc { color: var(--muted); max-width: 650px; margin-top: 10px; }
    .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; }
    .card { background: var(--panel); border: 1px solid var(--line); border-radius: 20px; padding: 28px; box-shadow: 0 18px 55px rgba(0,0,0,.12); }
    .card p { color: var(--muted); }
    .fact-list { display: grid; gap: 17px; }
    .fact { display: flex; justify-content: space-between; gap: 18px; border-bottom: 1px solid var(--line); padding-bottom: 12px; }
    .fact:last-child { border: 0; padding: 0; }
    .fact span:first-child { color: var(--muted); }
    .fact span:last-child { text-align: right; font-weight: 650; }
    .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px; }
    .skill { padding: 24px; border-radius: 17px; border: 1px solid var(--line); background: linear-gradient(145deg, rgba(20,30,54,.88), rgba(13,17,32,.7)); transition: .25s; }
    .skill:hover, .project:hover { transform: translateY(-5px); border-color: rgba(100,231,245,.48); box-shadow: var(--glow); }
    .skill-icon { width: 43px; height: 43px; border-radius: 12px; display: grid; place-items: center; color: var(--cyan); background: rgba(100,231,245,.1); font-weight: 800; margin-bottom: 16px; }
    .skill h3, .project h3 { margin-bottom: 7px; font-size: 1.08rem; }
    .skill p, .project p { color: var(--muted); font-size: .92rem; }
    .projects { display: grid; grid-template-columns: repeat(2, 1fr); gap: 20px; }
    .project { background: var(--panel); border: 1px solid var(--line); border-radius: 19px; overflow: hidden; transition: .25s; }
    .project-art { min-height: 170px; padding: 24px; display: flex; align-items: center; justify-content: center; background: radial-gradient(circle at 50% 45%, rgba(100,231,245,.2), transparent 48%), linear-gradient(135deg, #111c34, #17132e); }
    .browser { width: 82%; border: 1px solid rgba(180,210,255,.35); border-radius: 10px; overflow: hidden; box-shadow: 0 12px 35px rgba(0,0,0,.25); }
    .browser-top { height: 19px; background: rgba(255,255,255,.09); display: flex; align-items: center; gap: 5px; padding: 0 9px; }
    .browser-top i { width: 5px; height: 5px; background: var(--cyan); border-radius: 50%; opacity: .8; }
    .browser-body { padding: 15px; display: grid; gap: 8px; }
    .fake-line { height: 7px; width: 70%; border-radius: 8px; background: rgba(100,231,245,.55); }
    .fake-line.short { width: 43%; background: rgba(167,139,250,.55); }
    .fake-boxes { display: flex; gap: 7px; margin-top: 5px; }
    .fake-boxes span { height: 34px; flex: 1; border: 1px solid rgba(180,210,255,.2); border-radius: 5px; }
    .project-info { padding: 23px; }
    .tag { display: inline-block; margin-top: 13px; padding: 5px 9px; border-radius: 20px; color: var(--cyan); background: rgba(100,231,245,.09); font-size: .72rem; font-weight: 700; }
    .contact-box { display: flex; justify-content: space-between; align-items: center; gap: 25px; padding: 38px; border: 1px solid rgba(100,231,245,.25); border-radius: 22px; background: linear-gradient(115deg, rgba(100,231,245,.09), rgba(167,139,250,.09)); }
    .contact-box p { color: var(--muted); max-width: 570px; margin-top: 8px; }
    footer { border-top: 1px solid var(--line); padding: 25px 0; color: var(--muted); font-size: .86rem; }
    footer .wrap { display: flex; justify-content: space-between; gap: 15px; flex-wrap: wrap; }
    .reveal { opacity: 0; transform: translateY(20px); transition: .7s ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }
    @media (max-width: 760px) {
      .hero { grid-template-columns: 1fr; gap: 20px; padding-top: 70px; text-align: center; }
      .eyebrow { justify-content: center; } .intro { margin: auto; }
      .hero-actions { justify-content: center; } .visual { min-height: 340px; }
      .about-grid, .projects { grid-template-columns: 1fr; }
      .skills-grid { grid-template-columns: 1fr 1fr; }
      .contact-box { align-items: flex-start; flex-direction: column; padding: 27px; }
      .nav-links { display: none; position: absolute; top: 76px; left: 0; right: 0; padding: 20px 22px; flex-direction: column; align-items: flex-start; background: #0c1120; border-bottom: 1px solid var(--line); }
      .nav-links.open { display: flex; } .menu-btn { display: block; }
    }
    @media (max-width: 460px) { .wrap { width: min(100% - 30px, 1120px); } .skills-grid { grid-template-columns: 1fr; } .fact { flex-direction: column; gap: 2px; } .fact span:last-child { text-align: left; } }
    @media (prefers-reduced-motion: reduce) { *, *::before, *::after { scroll-behavior: auto !important; animation: none !important; transition: none !important; } }
  </style>
</head>
<body>
  <header>
    <nav class="wrap">
      <a class="brand" href="#home">NERWIN<span>.</span></a>
      <button class="menu-btn" id="menuBtn" aria-label="Buka menu" aria-expanded="false">Menu ☰</button>
      <div class="nav-links" id="navLinks">
        <a href="#about">Tentang</a><a href="#skills">Keahlian</a><a href="#projects">Projek</a><a href="#contact">Kontak</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero wrap" id="home">
      <div class="reveal">
        <div class="eyebrow">Future software engineer</div>
        <h1>Halo, saya<br><span>Nerwin Gire.</span></h1>
        <p class="intro">Mahasiswa semester 1 Rekayasa Perangkat Lunak di Politeknik Indonusa Surakarta. Saya sedang membangun fondasi di dunia teknologi dan senang mengubah ide menjadi pengalaman web yang menarik.</p>
        <div class="hero-actions">
          <a class="btn btn-primary" href="#projects">Lihat projek <span>↗</span></a>
          <a class="btn btn-ghost" href="#about">Kenali saya</a>
        </div>
      </div>
      <div class="visual reveal" aria-label="Inisial NG dalam ilustrasi futuristik">
        <div class="orbit">
          <div class="core"><strong>NG</strong></div>
          <span class="orbit-label label-one">&lt;code /&gt;</span>
          <span class="orbit-label label-two">BUILD · LEARN</span>
        </div>
      </div>
    </section>

    <section class="wrap" id="about">
      <div class="section-head reveal"><div class="section-kicker">01 / Tentang saya</div><h2>Belajar hari ini,<br>membangun masa depan.</h2><p class="section-desc">Saya percaya kemampuan besar tumbuh dari rasa ingin tahu, latihan, dan kemauan untuk terus mencoba.</p></div>
      <div class="about-grid">
        <article class="card reveal"><p>Saya adalah mahasiswa Rekayasa Perangkat Lunak yang sedang mempelajari dasar-dasar pengembangan aplikasi dan website. Saya tertarik pada desain web yang rapi, tampilan yang nyaman digunakan, serta teknologi yang bisa membantu banyak orang.</p><br><p>Saat ini saya terus berlatih menggunakan HTML, CSS, dan JavaScript sambil mengembangkan ide-ide projek sederhana.</p></article>
        <article class="card fact-list reveal">
          <div class="fact"><span>Nama</span><span>Nerwin Gire</span></div>
          <div class="fact"><span>Kampus</span><span>Politeknik Indonusa Surakarta</span></div>
          <div class="fact"><span>Program studi</span><span>Rekayasa Perangkat Lunak</span></div>
          <div class="fact"><span>Semester</span><span>1</span></div>
          <div class="fact"><span>Fokus saat ini</span><span>Web Development</span></div>
        </article>
      </div>
    </section>

    <section class="wrap" id="skills">
      <div class="section-head reveal"><div class="section-kicker">02 / Keahlian</div><h2>Teknologi yang sedang saya pelajari.</h2><p class="section-desc">Saya terus mengasah kemampuan dasar ini melalui latihan dan projek kecil.</p></div>
      <div class="skills-grid">
        <article class="skill reveal"><div class="skill-icon">HTML</div><h3>HTML</h3><p>Menyusun struktur halaman web yang jelas dan mudah dipahami.</p></article>
        <article class="skill reveal"><div class="skill-icon">CSS</div><h3>CSS</h3><p>Mengatur tata letak, warna, tipografi, dan tampilan responsif.</p></article>
        <article class="skill reveal"><div class="skill-icon">JS</div><h3>JavaScript</h3><p>Menambahkan interaksi dan perilaku dinamis pada website.</p></article>
      </div>
    </section>

    <section class="wrap" id="projects">
      <div class="section-head reveal"><div class="section-kicker">03 / Projek pilihan</div><h2>Tempat ide mulai diwujudkan.</h2><p class="section-desc">Berikut contoh projek latihan yang bisa saya kembangkan selama proses belajar.</p></div>
      <div class="projects">
        <article class="project reveal">
          <div class="project-art"><div class="browser"><div class="browser-top"><i></i><i></i><i></i></div><div class="browser-body"><div class="fake-line"></div><div class="fake-line short"></div><div class="fake-boxes"><span></span><span></span><span></span></div></div></div></div>
          <div class="project-info"><h3>Personal Portfolio</h3><p>Website profil untuk memperkenalkan diri, kemampuan, dan perjalanan belajar di bidang teknologi.</p><span class="tag">HTML · CSS · JavaScript</span></div>
        </article>
        <article class="project reveal">
          <div class="project-art"><div class="browser"><div class="browser-top"><i></i><i></i><i></i></div><div class="browser-body"><div class="fake-line short"></div><div class="fake-boxes"><span></span><span></span></div><div class="fake-line"></div></div></div></div>
          <div class="project-info"><h3>Website Informasi</h3><p>Konsep halaman informasi sederhana dengan navigasi yang mudah dan susunan konten yang rapi.</p><span class="tag">Web Design · Responsive Layout</span></div>
        </article>
      </div>
    </section>

    <section class="wrap" id="contact">
      <div class="contact-box reveal">
        <div><div class="section-kicker">04 / Mari terhubung</div><h2>Punya ide menarik?</h2><p>Saya terbuka untuk belajar, bertukar ide, dan berkolaborasi dalam projek sederhana seputar website dan teknologi.</p></div>
        <a class="btn btn-primary" href="mailto:">Hubungi saya <span>↗</span></a>
      </div>
    </section>
  </main>

  <footer><div class="wrap"><span>© <span id="year"></span> Nerwin Gire</span><span>Dibuat dengan semangat belajar dan rasa ingin tahu.</span></div></footer>

  <script>
    const menuBtn = document.getElementById('menuBtn');
    const navLinks = document.getElementById('navLinks');
    menuBtn.addEventListener('click', () => {
      const isOpen = navLinks.classList.toggle('open');
      menuBtn.setAttribute('aria-expanded', String(isOpen));
    });
    navLinks.querySelectorAll('a').forEach(link => link.addEventListener('click', () => {
      navLinks.classList.remove('open');
      menuBtn.setAttribute('aria-expanded', 'false');
    }));
    document.getElementById('year').textContent = new Date().getFullYear();
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.12 });
    document.querySelectorAll('.reveal').forEach(item => observer.observe(item));
  </script>
</body>
</html>
