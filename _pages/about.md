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
    <img class="seed" src="/assets/img/dendrite-75k.jpg" alt="" width="1000" height="1000">
    <img class="slide" src="/assets/img/dendrite-100k.jpg" alt="" width="1000" height="1000" data-cap="An alloy crystal growing in my phase field simulation, coloured by solute concentration.">
    <img class="slide" src="/assets/img/g-thermal.jpg" alt="" width="1000" height="1000" loading="lazy" data-cap="A pure-material crystal in my phase field simulation, coloured by temperature.">
    <img class="slide" src="/assets/img/slide-alsi.jpg" alt="" width="1200" height="1200" loading="lazy" data-cap="An Al–Si alloy under laser-printing conditions, atom by atom: phase field crystal on a 2048 × 1024 × 1024 grid.">
    <img class="slide slide--photo" src="/assets/img/g-frost.jpg" alt="" width="900" height="900" loading="lazy" data-cap="Frost on concrete in Montréal, photographed by me: the same physics, outside my door.">
  </div>
  <div class="hero-band__inner">
    <div class="hero-band__text">
      <h1 class="home-name">Ravneet Kaur</h1>
      <p class="home-role">Computational Materials Physics | Numerical Modelling &amp; Data Science</p>
      <p class="home-degree">M.Sc. in Physics, McGill University</p>
      <p class="home-actions">
        <a class="btn-solid" href="/projects/">See my projects</a>
        <a class="btn-line" href="/assets/pdf/Ravneet_Kaur_Resume.pdf">Résumé</a>
      </p>
    </div>
    <p class="hero-band__cap"><span id="cap-n">Fig. 1</span> <em id="cap-t">An alloy crystal growing in my phase field simulation, coloured by solute concentration.</em></p>
  </div>
</section>

<section class="home-about">
  <div class="home-about__text">
    <h2>About</h2>
    <p class="home-about__lead">I simulate how alloys form during metal 3D printing on Canada's supercomputers, and build the Python pipelines that turn terabytes of output into clear, quantitative answers.</p>
    <p>For my M.Sc. at McGill University, in Professor Nikolas Provatas's group, I modelled how aluminium–silicon alloys form their microstructure during laser powder bed fusion, the process behind metal 3D printing.</p>
    <p>I extended the open-source OpenPFC framework from pure materials to binary alloys in C++/MPI, ran 3D simulations on Canada's national supercomputers, and wrote the pipeline that turned <strong>100 TB+</strong> of output into precipitate and dislocation statistics. The project was a Mitacs Accelerate collaboration with Hydro-Québec and experimental teams at the University of New Brunswick and McMaster University.</p>
    <p>The same skills carry straight into industry: fast numerical code, analysis pipelines that hold up, and the habit of checking whether a result is physically and statistically believable before trusting it.</p>
  </div>
  <figure class="home-portrait">
    <img src="/assets/img/portrait.jpg" alt="Ravneet Kaur at her McGill convocation" width="720" height="900">
    <figcaption>McGill convocation, October 2026</figcaption>
  </figure>
</section>

<div class="home-numbers">
  <div><strong>2048×1024×1024</strong><span>simulation grid</span></div>
  <div><strong>100 TB+</strong><span>output analysed</span></div>
  <div><strong>1,500+</strong><span>cores, scaling tests</span></div>
  <div><strong>3.9 / 4.0</strong><span>M.Sc. GPA, McGill</span></div>
</div>

<div class="lattice-rule" aria-hidden="true"><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i class="misfit"></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i></div>

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
  // 1. Banner: the crystal grows, then the banner cycles through my simulations
  var slides = document.querySelectorAll(".hero-band__art .slide");
  var seed = document.querySelector(".hero-band__art .seed");
  var capN = document.getElementById("cap-n"), capT = document.getElementById("cap-t");
  var cap = capT ? capT.parentNode : null;
  if (slides.length) {
    if (reduce) {
      slides[0].classList.add("is-on");
      if (seed) seed.style.opacity = "0";
    } else {
      var i = 0;
      setTimeout(function () { slides[0].classList.add("is-on", "is-growing"); }, 700);
      setTimeout(function () { if (seed) seed.style.opacity = "0"; slides[0].classList.remove("is-growing"); }, 5200);
      setInterval(function () {
        slides[i].classList.remove("is-on");
        i = (i + 1) % slides.length;
        slides[i].classList.add("is-on");
        if (cap) {
          cap.style.opacity = "0";
          setTimeout(function () {
            capN.textContent = "Fig. " + (i + 1);
            capT.textContent = slides[i].getAttribute("data-cap");
            cap.style.opacity = "1";
          }, 600);
        }
      }, 7000);
    }
  }
  if (reduce || !("IntersectionObserver" in window)) return;
  // 2. Sections glide in as they scroll into view
  document.documentElement.classList.add("rv-on");
  var groups = [".home-numbers > div", ".lattice-rule", ".home-about__text", ".home-portrait", "article > h3", "article > ul", "article > p"];
  var items = [];
  groups.forEach(function (sel) {
    document.querySelectorAll(sel).forEach(function (el, k) {
      if (el.closest(".hero-band")) return;
      el.classList.add("rv");
      if (sel.indexOf("> div") > -1) el.style.transitionDelay = (k * 0.09) + "s";
      items.push(el);
    });
  });
  var io = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) {
      if (e.isIntersecting) { e.target.classList.add("rv-in"); io.unobserve(e.target); }
    });
  }, { rootMargin: "0px 0px -8% 0px", threshold: 0.12 });
  items.forEach(function (el) { io.observe(el); });
  // 3. Banner reacts to scrolling: the art grows and turns, the text drifts away
  var band = document.querySelector(".hero-band");
  var art = document.querySelector(".hero-band__art");
  var text = document.querySelector(".hero-band__text");
  if (!band || !art || !text) return;
  var ticking = false;
  function update() {
    ticking = false;
    var p = Math.min(Math.max(window.scrollY / (band.offsetHeight || 1), 0), 1);
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
