---
layout: about
title: About
permalink: /
subtitle: Computational Physics &amp; Data Science · M.Sc., McGill University · Montréal
selected_papers: false
social: true
announcements:
  enabled: false
latest_posts:
  enabled: false
---
<section class="hero-band">
  <div class="hero-band__art" aria-hidden="true">
    <img class="grow-a" src="/assets/img/dendrite-75k.jpg" alt="" width="1000" height="1000">
    <img class="grow-b" src="/assets/img/dendrite-100k.jpg" alt="" width="1000" height="1000">
  </div>
  <div class="hero-band__inner">
    <div class="hero-band__text">
      <p class="home-kicker">Computational physics · Data science · Montréal</p>
      <h1 class="home-name">Ravneet Kaur</h1>
      <p class="home-lede">I build physics models of how materials form, from atoms to crystals, and turn the data they produce into answers people can use.</p>
      <p class="home-actions">
        <a class="btn-solid" href="/projects/">See my projects</a>
        <a class="btn-line" href="/assets/pdf/Ravneet_Kaur_Resume.pdf">Résumé</a>
      </p>
    </div>
    <p class="hero-band__cap"><span>Fig. 1</span> An alloy crystal growing in my phase field simulation, coloured by solute concentration.</p>
  </div>
</section>

<section class="models">
  <p class="models__label">Selected models</p>
  <div class="models__grid">
    <figure><img src="/assets/img/g-alsi-3d.jpg" alt="3D phase field crystal simulation of an Al–Si alloy" width="900" height="900" loading="lazy"><figcaption><b>Al–Si alloy, atom by atom</b>Phase field crystal, 3D, laser-printing conditions</figcaption></figure>
    <figure><img src="/assets/img/g-phase.jpg" alt="Phase field simulation of an alloy dendrite, solid and liquid" width="800" height="800" loading="lazy"><figcaption><b>Alloy dendrite</b>Phase field, solid–liquid order parameter</figcaption></figure>
    <figure><img src="/assets/img/g-thermal.jpg" alt="Phase field simulation of a pure-material crystal, temperature field" width="800" height="800" loading="lazy"><figcaption><b>Pure-material crystal</b>Phase field, temperature field</figcaption></figure>
    <figure><img src="/assets/img/g-frost.jpg" alt="Photograph of frost crystals on concrete" width="900" height="900" loading="lazy"><figcaption><b>Frost on concrete</b>My photograph: the same physics, outside my door</figcaption></figure>
  </div>
</section>

<div class="home-numbers">
  <div><strong>2048×1024×1024</strong><span>simulation grid</span></div>
  <div><strong>100 TB+</strong><span>output analysed</span></div>
  <div><strong>1,500+</strong><span>cores, scaling tests</span></div>
  <div><strong>3.9 / 4.0</strong><span>M.Sc. GPA, McGill</span></div>
</div>

<div class="lattice-rule" aria-hidden="true"><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i class="misfit"></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i></div>

<section class="home-about">
  <div class="home-about__text">
    <h2>About</h2>
    <p>For my M.Sc. at McGill University, in Professor Nikolas Provatas's group, I modelled how aluminium–silicon alloys form their microstructure during laser powder bed fusion, the process behind metal 3D printing.</p>
    <p>I extended the open-source OpenPFC framework from pure materials to binary alloys in C++/MPI, ran 3D simulations on Canada's national supercomputers, and wrote the pipeline that turned <strong>100 TB+</strong> of output into precipitate and dislocation statistics. The project was a Mitacs Accelerate collaboration with Hydro-Québec and experimental teams at the University of New Brunswick and McMaster University.</p>
    <p>The same skills carry straight into industry: fast numerical code, analysis pipelines that hold up, and the habit of checking whether a result is physically and statistically believable before trusting it.</p>
  </div>
  <figure class="home-portrait">
    <img src="/assets/img/portrait.jpg" alt="Ravneet Kaur at her McGill convocation" width="720" height="900">
    <figcaption>McGill convocation, October 2026</figcaption>
  </figure>
</section>

### Hire me

I'm looking for **Data Science, Scientific Computing and R&D roles**, in Montréal or remote across Canada. I'm strongest where real-world systems are messy and careful modelling matters: energy, materials, manufacturing and simulation.

- **Data & ML:** Python, pandas, NumPy, scikit-learn, LightGBM, SQL, DuckDB, time-series features, grouped cross-validation
- **Simulation & HPC:** C++, MPI, FFT/spectral methods, numerical PDEs, Slurm on Alliance Canada clusters
- **Shipping it:** Git, Streamlit, FastAPI, OVITO, Mathematica, clear writing for technical and non-technical audiences

### Highlights

- 2nd of 47, RQMP Grand Conference poster competition (2026)
- Prize, ORU IPL Analytics Hackathon (2026)
- Invited lightning talk, CHiMaD Phase Field Workshop XXI, Northwestern University (2026)
- M.Sc. GPA 3.9 / 4.0, McGill University · first in my family to earn a Master's degree
- Teaching Assistant, McGill Department of Physics, five terms (2024–2026)

### Beyond work

I'm a photographer at heart and was Creative Head of Sparks, my college physics society in Delhi, where I ran events and digital content. In Montréal I volunteer with Khalsa Aid Canada's food distribution.

<script>
(function () {
  var reduce = window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches;
  if (reduce || !("IntersectionObserver" in window)) return;
  var root = document.documentElement;
  root.classList.add("rv-on");
  // 1. Reveal sections as they scroll into view, one after another
  var groups = [".models__grid > figure", ".home-numbers > div", ".lattice-rule", ".home-about__text", ".home-portrait", "article > h3", "article > ul", "article > p", ".models__label"];
  var items = [];
  groups.forEach(function (sel) {
    var els = document.querySelectorAll(sel);
    els.forEach(function (el, i) {
      if (el.closest(".hero-band")) return;
      el.classList.add("rv");
      if (sel.indexOf("> figure") > -1 || sel.indexOf("> div") > -1) el.style.transitionDelay = (i * 0.09) + "s";
      items.push(el);
    });
  });
  var io = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) {
      if (e.isIntersecting) { e.target.classList.add("rv-in"); io.unobserve(e.target); }
    });
  }, { rootMargin: "0px 0px -8% 0px", threshold: 0.12 });
  items.forEach(function (el) { io.observe(el); });
  // 2. Hero: as you scroll, the crystal slowly grows and the text drifts away
  var band = document.querySelector(".hero-band");
  var art = document.querySelector(".hero-band__art");
  var text = document.querySelector(".hero-band__text");
  if (!band || !art || !text) return;
  var ticking = false;
  function update() {
    ticking = false;
    var h = band.offsetHeight || 1;
    var p = Math.min(Math.max(window.scrollY / h, 0), 1);
    art.style.transform = "translateY(-50%) scale(" + (1 + 0.18 * p) + ") rotate(" + (6 * p) + "deg)";
    art.style.opacity = String(1 - 0.55 * p);
    text.style.transform = "translateY(" + (-70 * p) + "px)";
    text.style.opacity = String(1 - 1.2 * p);
  }
  window.addEventListener("scroll", function () {
    if (!ticking) { ticking = true; requestAnimationFrame(update); }
  }, { passive: true });
  update();
})();
</script>
