<div align="center">

# Limitless - The Open Academic Archive

> A free and open platform for accessing notes and academic resources without any data logging and pay walls. 

<!-- Licenses -->
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE-MIT)
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC_BY--NC_4.0-lightgrey.svg)](LICENSE-CC-BY-NC-4.0)

<!-- Collaborators -->
[![Maintainer: Baibhav Bhattacharya](https://img.shields.io/badge/Developer-Baibhav_Bhattacharya-10b981.svg)](#)
[![Maintainer: Prem Vishvakarma](https://img.shields.io/badge/Collaborator-Prem_Vishvakarma-6366f1.svg)](#)
[![Maintainer: Ankush Yadav](https://img.shields.io/badge/Maintainer-Ankush_Yadav-ec4899.svg)](#)

</div>

---
## Overview

Limitless is an open academic archive built by students, for students. It puts syllabus-aligned degree notes, clear diagrams, and practical solutions directly on the web, ready to read the moment you open the page.

There are no accounts, paywalls, tracking scripts, or intrusive ads. Everything renders natively in the browser, so you never have to download massive, blurry scanned PDFs just to check a single concept or formula before an exam.

Alongside regular theory, we also provide reference lab manuals, step-by-step experiment procedures, verified code, and embedded video guides showing exactly how to set up tools and run your practicals without getting stuck. Every page is lightweight and edge-cached to load instantly, even on spotty campus Wi-Fi.


---
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
}

.animated-btn:hover {
  transform: translateY(-3px) scale(1.04);
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.28);
}

/* Fast Multi-Layer Abstract Wave Engine */
.animated-btn::before {
  content: "";
  position: absolute;
  top: -60%;
  left: -60%;
  width: 220%;
  height: 220%;
  background-size: 200% 200%;
  animation: dynamicFluidMesh 3.2s ease-in-out infinite alternate;
  z-index: -1;
}

/* High-Contrast Dynamic Palettes */
/* FY: Electric Cyan -> Cobalt -> Vivid Magenta -> Royal Blue */
.btn-fy::before {
  background-image: 
    radial-gradient(circle at 20% 20%, #00f2fe 0%, transparent 50%),
    radial-gradient(circle at 80% 80%, #4facfe 0%, transparent 50%),
    linear-gradient(135deg, #0052d4, #4364f7, #6fb1fc, #ff0844);
}

/* SY: Neon Violet -> Hot Pink -> Electric Orange -> Deep Indigo */
.btn-sy::before {
  background-image: 
    radial-gradient(circle at 30% 30%, #f72585 0%, transparent 50%),
    radial-gradient(circle at 70% 70%, #7209b7 0%, transparent 50%),
    linear-gradient(135deg, #3a0ca3, #4361ee, #4cc9f0, #f72585);
}

/* TY: Lime Green -> Bright Emerald -> Aquamarine -> Deep Teal */
.btn-ty::before {
  background-image: 
    radial-gradient(circle at 25% 25%, #00ff87 0%, transparent 50%),
    radial-gradient(circle at 75% 75%, #60efff 0%, transparent 50%),
    linear-gradient(135deg, #0575e6, #00f260, #10b981, #047857);
}

/* Typography Hierarchy */
.btn-title {
  font-size: 18px;
  font-weight: 800;
  letter-spacing: 0.8px;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.35);
  line-height: 1;
}

.btn-sub {
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.2px;
  text-transform: uppercase;
  opacity: 0.92;
  margin-top: 5px;
  text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
}

/* Fluid Translation & Rotation */
@keyframes dynamicFluidMesh {
  0% {
    transform: translate(0, 0) rotate(0deg) scale(1);
  }
  50% {
    transform: translate(-10%, -8%) rotate(70deg) scale(1.15);
  }
  100% {
    transform: translate(8%, 10%) rotate(160deg) scale(1.05);
  }
}

/* Mobile Tuning: Fits all 3 side-by-side on 360px+ screens */
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
<div class="btn-grid">
  <a href="" class="animated-btn btn-fy">
    <span class="btn-title">FY</span>
    <span class="btn-sub">First Year</span>
  </a>

  <a href="" class="animated-btn btn-sy">
    <span class="btn-title">SY</span>
    <span class="btn-sub">Second Year</span>
  </a>

  <a href="" class="animated-btn btn-ty">
    <span class="btn-title">TY</span>
    <span class="btn-sub">Third Year</span>
  </a>
</div>

---


## Legal Notice & Terms of Use

This platform operates under a dual-licensing structure to protect open educational access while preserving maintainer attribution and intellectual property rights.

### 1. Dual-Licensing Framework

* **Academic Notes, Documentation, and Visual Media:** All written notes, module summaries, examination solutions, and watermarked diagrams are licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)](LICENSE-CC-BY-NC-4.0).
* **Source Code and Practical Scripts:** All executable software, lab code implementations, scripts, and build configurations are licensed under the [MIT License](LICENSE-MIT).

### 2. Permitted Uses

* **Academic Study:** Students and educators are permitted to read, download, print for personal revision, and share direct links for non-commercial educational purposes.
* **Open Source Collaboration:** Anyone may fork, translate, or expand upon these materials, provided full maintainer attribution is preserved and derived works remain non-commercial.
* **Code Implementation:** Source code released under the MIT License may be executed, modified, and integrated into personal, academic, or software projects pursuant to the terms of the MIT license.

### 3. Prohibited Uses & Restrictions

* **Commercial Exploitation:** Commercial entities, coaching institutes, private tutors, and ed-tech platforms are strictly prohibited from selling, sublicensing, packaging, or placing the written notes, visual guides, or diagrams behind paywalls, subscription tiers, or ad-monetized services.
* **Watermark & Attribution Removal:** Stripping, cropping, altering, or obscuring watermarks from diagrams, figures, or visual media constitutes an explicit copyright violation.
* **Plagiarism & Misrepresentation:** Claiming authorship over any portion of this repository, or republishing content without clear attribution to the maintainers, is strictly prohibited.
* **Unauthorized Bulk Scraping:** Systematic automated scraping or harvesting of content for inclusion in proprietary training sets, commercial databases, or commercial distribution channels is prohibited under CC BY-NC 4.0.

### 4. Copyright & Maintainers

All original materials are copyrighted by the project maintainers:

* Baibhav Bhattacharya
* Prem Vishvakarma
* Ankush Yadav

For inquiries regarding permissions beyond the scope of these licenses, open an issue in the official GitHub repository.

To report unauthorized commercial use or file an infringement notice, refer to our [DMCA Notice & Policy](#/DMCA).

## Credits
**Limitless** was developed by a group of college friends **Baibhav Bhattacharya**, **Ankush Yadav** and **Prem Vishvakarma** studying in **Shree L.R. Tiwari Degree College** as a way to effeiciently share notes and academic resources among all students.
