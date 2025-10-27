---
layout: archive
title: "Research"
permalink: /research/
excerpt: "Current cognitive neuroscience research projects by Javier Gonzalez-Castillo"
author_profile: false
toc: false
sidebar:
    nav: "sidebar_research"
---

{: .text-justify}
The brain works in mysterious ways, and my research aims to uncover—or at least help explain—some of these mysteries through the combination of state-of-the-art neuroimaging, artificial intelligence, machine learning, and advanced computational modeling.

{: .text-justify}
Over the past 20 years, I’ve contributed to more than 60 research projects spanning a wide range of topics—from technical questions like how to optimize scanning parameters to improve data fidelity, to complex biological questions such as how spontaneous brain activity relates to conscious experience.

{: .text-justify}
There are many ways to organize such a broad research portfolio, but for the purpose of this website, I’ve divided the “Research” section into four main areas:

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Research Portfolio Infographic</title>
  <style>
    :root{
      --navy: #001f3f; /* navy */
      --black: #000000;
      --bg: #ffffff;
      --gap: 28px;
      --radius: 12px;
      --card-padding: 28px;
      --title-size: 18px;
    }
    html,body{height:100%;}
    body{
      margin:0;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background:var(--bg);
      color:var(--black);
      display:flex;
      align-items:center;
      justify-content:center;
      padding:36px;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
    }

    .infographic{
      width:min(980px, 96vw);
      aspect-ratio: 1 / 1; /* keeps a square layout */
      display:grid;
      grid-template-columns:1fr 1fr;
      grid-template-rows:1fr 1fr;
      gap:var(--gap);
      align-items:stretch;
    }

    .card{
      background:transparent;
      border:1px solid rgba(0,0,0,0.08);
      border-radius:var(--radius);
      padding:var(--card-padding);
      display:flex;
      flex-direction:column;
      align-items:center;
      justify-content:center;
      text-align:center;
      transition:transform .18s ease, box-shadow .18s ease;
      box-shadow: 0 6px 18px rgba(0,0,0,0.03);
    }
    .card:focus-within, .card:hover{
      transform:translateY(-6px);
      box-shadow:0 18px 36px rgba(0,0,0,0.08);
    }

    .icon-wrap{
      width:140px;
      height:140px;
      display:flex;
      align-items:center;
      justify-content:center;
      margin-bottom:18px;
    }
    svg, img{width:100%;height:100%;object-fit:contain;}

    .title{
      font-weight:600;
      font-size:var(--title-size);
      color:var(--navy);
      letter-spacing:0.2px;
    }

    /* Responsive tweaks */
    @media (max-width:700px){
      .infographic{aspect-ratio: auto; grid-template-columns:1fr; grid-template-rows:repeat(4, auto);} 
      .icon-wrap{width:120px;height:120px}
    }
  </style>
</head>
<body>
  <main class="infographic" role="img" aria-label="Research portfolio infographic with four quadrants">

    <!-- Experimental Design / Acquisition -->
    <section class="card" aria-labelledby="exp-title">
      <div class="icon-wrap" aria-hidden="true">
        <img src="assets/icons/Scanner_Icon.png" alt="MRI scanner icon representing experimental design and acquisition" />
      </div>
      <div id="exp-title" class="title">Experimental Design / Acquisition</div>
    </section>

    <!-- Analytical Methods -->
    <section class="card" aria-labelledby="anal-title">
      <div class="icon-wrap" aria-hidden="true">
        <!-- Neural network icon -->
        <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" role="img">
          <g stroke="var(--navy)" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round" fill="none">
            <circle cx="12" cy="20" r="4"/>
            <circle cx="52" cy="20" r="4"/>
            <circle cx="32" cy="12" r="4"/>
            <circle cx="20" cy="44" r="4"/>
            <circle cx="44" cy="44" r="4"/>
            <path d="M16 22c6 6 12 6 16 0"/>
            <path d="M36 22c6 6 12 6 16 0"/>
            <path d="M22 24c8 6 18 6 20 20"/>
            <path d="M42 24c-8 6-18 6-20 20"/>
          </g>
        </svg>
      </div>
      <div id="anal-title" class="title">Analytical Methods</div>
    </section>

    <!-- Cognitive Neuroscience -->
    <section class="card" aria-labelledby="cog-title">
      <div class="icon-wrap" aria-hidden="true">
        <!-- Brain icon -->
        <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" role="img">
          <g stroke="var(--navy)" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round" fill="none">
            <path d="M20 18c-4 0-6 4-6 8s2 8 6 8v10c0 3 3 6 6 6h12c3 0 6-3 6-6V34c4 0 6-4 6-8s-2-8-6-8c0-6-6-8-12-8s-12 2-12 8z"/>
            <path d="M32 12v40" stroke-dasharray="2 4"/>
          </g>
        </svg>
      </div>
      <div id="cog-title" class="title">Cognitive Neuroscience</div>
    </section>

    <!-- Clinical Research -->
    <section class="card" aria-labelledby="clin-title">
      <div class="icon-wrap" aria-hidden="true">
        <!-- Medical cross icon -->
        <svg viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" role="img">
          <g stroke="var(--navy)" stroke-width="2.6" stroke-linecap="round" stroke-linejoin="round" fill="none">
            <rect x="18" y="12" width="28" height="40" rx="6"/>
            <path d="M32 20v24M44 32H20" stroke="var(--navy)" stroke-width="3"/>
          </g>
        </svg>
      </div>
      <div id="clin-title" class="title">Clinical</div>
    </section>

  </main>
</body>
</html>


Click on any of the sections above—or use the menu to your left—to explore the questions I’ve sought to answer in each area and how I (with the invaluable help of many colleagues) went about it. I hope you find it engaging, and maybe even learn something new along the way.

