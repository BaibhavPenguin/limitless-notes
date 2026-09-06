<div>

![LOGO](/LOGO-NO-BG.png)

> A free and open platform for accessing notes and academic resources without any data logging and pay walls. 
---


</div>

## Overview

Limitless is an open academic archive built by students, for students. It puts syllabus-aligned degree notes, clear diagrams, and practical solutions directly on the web, ready to read the moment you open the page.

There are no accounts, paywalls, tracking scripts, or intrusive ads. Everything renders natively in the browser, so you never have to download massive, blurry scanned PDFs just to check a single concept or formula before an exam.

Alongside regular theory, we also provide reference lab manuals, step-by-step experiment procedures, verified code, and embedded video guides showing exactly how to set up tools and run your practicals without getting stuck. Every page is lightweight and edge-cached to load instantly.



<style>
/* Responsive Button Container */
.btn-grid {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  gap: 14px;
  margin: 28px auto;
  max-width: 100%;
}

/* Compact Rounded Square Button */
.animated-btn {
  position: relative;
  display: inline-flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 105px;
  height: 105px;
  border-radius: 18px;
  color: #ffffff !important;
  text-decoration: none !important;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  box-shadow: 0 6px 18px rgba(0, 0, 0, 0.18);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  overflow: hidden;
  z-index: 1;
  flex-shrink: 0;
  background: #000;
}

.animated-btn:hover {
  transform: translateY(-3px) scale(1.04);
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.28);
}

/* Base Scene Layer */
.btn-bg {
  position: absolute;
  inset: 0;
  z-index: -1;
  overflow: hidden;
}

.btn-fy-bg {
  animation: skyCycle 10s infinite ease-in-out;
}

.fy-celestial {
  position: absolute;
  width: 22px;
  height: 22px;
  border-radius: 50%;
  left: 15px;
  top: 15px;
  animation: celestialOrbit 10s infinite ease-in-out;
}

.fy-mountains {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 48px;
}

.fy-mountains::before,
.fy-mountains::after {
  content: "";
  position: absolute;
  bottom: 0;
  border-style: solid;
}

.fy-mountains::before {
  left: -15px;
  border-width: 0 45px 44px 45px;
  border-color: transparent transparent #162436 transparent;
  animation: mountainShub 10s infinite ease-in-out;
}

.fy-mountains::after {
  right: -20px;
  border-width: 0 55px 36px 55px;
  border-color: transparent transparent #0d1722 transparent;
  animation: mountainFront 10s infinite ease-in-out;
}

@keyframes skyCycle {
  0%, 100% { background-color: #38bdf8; }
  35%      { background-color: #f97316; }
  60%, 85% { background-color: #0b1120; }
}

@keyframes celestialOrbit {
  0%, 100% {
    background-color: #fde047;
    box-shadow: 0 0 12px #facc15;
    transform: translateY(0);
  }
  35% {
    background-color: #fb923c;
    box-shadow: 0 0 16px #ea580c;
    transform: translateY(18px);
  }
  50% {
    transform: translateY(70px);
    opacity: 0;
  }
  60% {
    background-color: #f8fafc;
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
    transform: translateY(10px);
    opacity: 1;
  }
  85% {
    background-color: #f8fafc;
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.8);
    transform: translateY(4px);
    opacity: 1;
  }
}

@keyframes mountainShub {
  0%, 100% { border-bottom-color: #1e3a5f; }
  35%      { border-bottom-color: #581c87; }
  60%, 85% { border-bottom-color: #0c1626; }
}

@keyframes mountainFront {
  0%, 100% { border-bottom-color: #152943; }
  35%      { border-bottom-color: #3b0764; }
  60%, 85% { border-bottom-color: #050b14; }
}

.btn-sy-bg {
  background: linear-gradient(180deg, #022036 0%, #00101c 60%, #000810 100%);
}

.sy-ocean-glow {
  position: absolute;
  width: 140px;
  height: 140px;
  left: -20px;
  top: -30px;
  background: radial-gradient(circle, rgba(14, 165, 233, 0.45) 0%, transparent 70%);
  filter: blur(12px);
  animation: oceanBreathing 6s ease-in-out infinite alternate;
}

.sy-wave {
  position: absolute;
  width: 240px;
  height: 240px;
  border-radius: 42%;
  left: -65px;
}

.sy-wave-1 {
  bottom: -175px;
  background: linear-gradient(135deg, rgba(6, 182, 212, 0.4), rgba(30, 58, 138, 0.65));
  animation: oceanRoll 7s infinite linear;
}

.sy-wave-2 {
  bottom: -185px;
  background: linear-gradient(135deg, rgba(45, 212, 191, 0.35), rgba(15, 23, 42, 0.8));
  animation: oceanRoll 9.5s infinite linear reverse;
}

.sy-wave-3 {
  bottom: -192px;
  background: rgba(3, 105, 161, 0.3);
  animation: oceanRoll 5.5s infinite linear;
}

.sy-plankton {
  position: absolute;
  width: 3px;
  height: 3px;
  border-radius: 50%;
  background: #a5f3fc;
  box-shadow: 0 0 8px #38bdf8;
  animation: planktonFloat 4s infinite ease-in-out;
}

.sy-plankton-1 { left: 24%; top: 68%; animation-delay: 0s; }
.sy-plankton-2 { left: 78%; top: 45%; animation-delay: 1.8s; }
.sy-plankton-3 { left: 45%; top: 22%; animation-delay: 3.1s; }

@keyframes oceanRoll {
  0%   { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

@keyframes oceanBreathing {
  0%   { opacity: 0.35; transform: scale(0.9); }
  100% { opacity: 0.85; transform: scale(1.15); }
}

@keyframes planktonFloat {
  0%, 100% { transform: translateY(0) scale(0.8); opacity: 0.2; }
  50%      { transform: translateY(-12px) scale(1.4); opacity: 1; }
}

.btn-ty-bg {
  background: linear-gradient(180deg, #091a18 0%, #051210 40%, #020706 100%);
}

/* Ambient canopy light filtered through branches */
.ty-canopy-glow {
  position: absolute;
  top: -15px;
  left: 50%;
  transform: translateX(-50%);
  width: 90px;
  height: 50px;
  background: radial-gradient(ellipse, rgba(45, 212, 191, 0.18) 0%, transparent 75%);
  filter: blur(10px);
}

/* Ground fog drifting between tree trunks */
.ty-mist {
  position: absolute;
  bottom: 0;
  width: 200%;
  height: 32px;
  background: radial-gradient(ellipse at center, rgba(20, 184, 166, 0.25) 0%, transparent 70%);
  filter: blur(6px);
  animation: mistDrift 8s ease-in-out infinite alternate;
}

/* Forest Layer 1: Distant Background Pines */
.ty-forest-back {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 68px;
}

.ty-forest-back::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 20px;
  border-style: solid;
  border-width: 0 11px 64px 11px;
  border-color: transparent transparent #0d2722 transparent;
}

.ty-forest-back::after {
  content: "";
  position: absolute;
  bottom: 0;
  right: 22px;
  border-style: solid;
  border-width: 0 13px 60px 13px;
  border-color: transparent transparent #0d2722 transparent;
}

/* Forest Layer 2: Mid-Depth Pines */
.ty-forest-mid {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 54px;
}

.ty-forest-mid::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 42px;
  border-style: solid;
  border-width: 0 15px 52px 15px;
  border-color: transparent transparent #091d19 transparent;
}

.ty-forest-mid::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0px;
  border-style: solid;
  border-width: 0 13px 48px 13px;
  border-color: transparent transparent #091d19 transparent;
}

/* Forest Layer 3: Foreground Dense Spruces */
.ty-forest-front {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 42px;
}

.ty-forest-front::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: -8px;
  border-style: solid;
  border-width: 0 18px 40px 18px;
  border-color: transparent transparent #040d0b transparent;
}

.ty-forest-front::after {
  content: "";
  position: absolute;
  bottom: 0;
  right: -5px;
  border-style: solid;
  border-width: 0 20px 44px 20px;
  border-color: transparent transparent #040d0b transparent;
}

/* Center filler tree silhouette */
.ty-tree-center {
  position: absolute;
  bottom: 0;
  right: 32px;
  border-style: solid;
  border-width: 0 14px 36px 14px;
  border-color: transparent transparent #040d0b transparent;
}

/* Bioluminescent fireflies wandering through trees */
.ty-firefly {
  position: absolute;
  width: 3px;
  height: 3px;
  border-radius: 50%;
  background: #fef08a;
  box-shadow: 0 0 6px #facc15, 0 0 10px #84cc16;
}

.ty-firefly-1 {
  left: 22%;
  bottom: 28px;
  animation: fireflyFloat1 5s infinite ease-in-out;
}

.ty-firefly-2 {
  left: 72%;
  bottom: 36px;
  animation: fireflyFloat2 6.5s infinite ease-in-out 1.2s;
}

.ty-firefly-3 {
  left: 48%;
  bottom: 16px;
  animation: fireflyFloat3 4.8s infinite ease-in-out 2.5s;
}

.ty-firefly-4 {
  left: 36%;
  bottom: 46px;
  animation: fireflyFloat1 5.6s infinite ease-in-out 3.4s;
}

@keyframes mistDrift {
  0%   { transform: translateX(-20%); }
  100% { transform: translateX(5%); }
}

@keyframes fireflyFloat1 {
  0%, 100% { transform: translate(0, 0); opacity: 0.15; }
  50%      { transform: translate(6px, -14px); opacity: 1; }
}

@keyframes fireflyFloat2 {
  0%, 100% { transform: translate(0, 0); opacity: 0.1; }
  50%      { transform: translate(-7px, -16px); opacity: 0.95; }
}

@keyframes fireflyFloat3 {
  0%, 100% { transform: translate(0, 0); opacity: 0.2; }
  50%      { transform: translate(5px, -10px); opacity: 1; }
}

/* Typography Hierarchy */
.btn-title {
  font-size: 18px;
  font-weight: 800;
  letter-spacing: 0.8px;
  text-shadow: 0 2px 6px rgba(0, 0, 0, 0.85);
  line-height: 1;
}

.btn-sub {
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.2px;
  text-transform: uppercase;
  opacity: 0.95;
  margin-top: 5px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.85);
}

/* Mobile Tuning */
@media (max-width: 480px) {
  .btn-grid {
    gap: 10px;
    margin: 20px auto;
  }
  .animated-btn {
    width: 94px;
    height: 94px;
    border-radius: 15px;
  }
  .btn-title {
    font-size: 16px;
  }
  .btn-sub {
    font-size: 9px;
  }
}
</style>

<h2>Getting Started</h2>
<hr>
<div class="btn-grid">
  <!-- FY: Mountain Landscape & Celestial Timelapse (Intact) -->
  <a href="#/assets/first-year/overview" class="animated-btn">
    <div class="btn-bg btn-fy-bg">
      <div class="fy-celestial"></div>
      <div class="fy-mountains"></div>
    </div>
    <span class="btn-title">FY</span>
    <span class="btn-sub">First Year</span>
  </a>

  <!-- SY: Bioluminescent Oceanic Depths (Intact) -->
  <a href="#/assets/second-year/overview.md" class="animated-btn">
    <div class="btn-bg btn-sy-bg">
      <div class="sy-ocean-glow"></div>
      <div class="sy-wave sy-wave-1"></div>
      <div class="sy-wave sy-wave-2"></div>
      <div class="sy-wave sy-wave-3"></div>
      <div class="sy-plankton sy-plankton-1"></div>
      <div class="sy-plankton sy-plankton-2"></div>
      <div class="sy-plankton sy-plankton-3"></div>
    </div>
    <span class="btn-title">SY</span>
    <span class="btn-sub">Second Year</span>
  </a>

  <!-- TY: Dense Woods, Layered Tree Canopies & Drifting Fireflies -->
  <a href="#/assets/third-year/overview.md" class="animated-btn">
    <div class="btn-bg btn-ty-bg">
      <div class="ty-canopy-glow"></div>
      <div class="ty-forest-back"></div>
      <div class="ty-forest-mid"></div>
      <div class="ty-tree-center"></div>
      <div class="ty-forest-front"></div>
      <div class="ty-mist"></div>
      <div class="ty-firefly ty-firefly-1"></div>
      <div class="ty-firefly ty-firefly-2"></div>
      <div class="ty-firefly ty-firefly-3"></div>
      <div class="ty-firefly ty-firefly-4"></div>
    </div>
    <span class="btn-title">TY</span>
    <span class="btn-sub">Third Year</span>
  </a>
</div>

## Legal Information
---
To view the Terms of use, refer to our [Terms & Conditions](/legal/TERMS-OF-USE.md)

To report unauthorized commercial use or file an infringement notice, refer to our [DMCA Notice & Policy](/legal/DMCA.md).

To view our copyright notice, refer to our [Copyright Notice](/legal/NOTICE.md)
## Credits
---
**Limitless** was developed by a group of college friends **Baibhav Bhattacharya**, **Ankush Yadav** and **Prem Vishvakarma** studying in **Shree L.R. Tiwari Degree College** as a way to effeiciently share notes and academic resources among all students.

