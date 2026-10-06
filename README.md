# RS Builder

**Marketing website for RS Builder, general contractors in Lahore.**
Grey structure, finishing and turnkey construction, from soil test to handover.

[![Live on GitHub Pages](https://img.shields.io/badge/live-GitHub%20Pages-1f2328?logo=github)](https://ahlamcode2150.github.io/rs-builder/)
[![Live on Netlify](https://img.shields.io/badge/live-Netlify-00ad9f?logo=netlify&logoColor=white)](https://rs-builder-710.netlify.app)
![Single file](https://img.shields.io/badge/build-none%20%C2%B7%20single%20HTML%20file-555)

| | |
|---|---|
| **GitHub Pages** | https://ahlamcode2150.github.io/rs-builder/ |
| **Netlify** | https://rs-builder-710.netlify.app |

---

## Overview

The site presents RS Builder the way an engineer would: as a set of construction drawings. Each section
is a numbered drawing sheet (A-101 Process, A-201 Services, A-301 Work, S-001 Standards, A-901 Contact).
As the visitor scrolls, a live 3D model of a building rises floor by floor, from site survey to handover.

## Features

- **Blueprint loader:** a drawing that sketches itself while the page loads.
- **Interactive 3D build model** (Three.js): the building is built as you scroll. You can drag to orbit the
  model, the crane follows your cursor, and live counters show floors cast, level and concrete poured.
- **Five-stage process:** site survey and soil test, design and approvals (LDA / DHA), grey structure,
  finishing, and handover with a 10-year structural warranty.
- **Services:** turnkey construction, grey structure, finishing and renovation, and commercial buildings
  up to G+8, each with typical project size and programme length.
- **Selected work** gallery of handed-over projects.
- **Site standards spec sheet:** concrete, steel, brickwork, curing, waterproofing and reporting, each
  with the check carried out on site.
- **Project brief builder:** visitors fill in their plot, location, scope and start date, and the page
  prepares a formatted brief they can copy and send by WhatsApp or email.
- **Sticky chapter index** that tracks the current section, and smooth scrolling.
- **Responsive** layout for phones, tablets and desktops, and it respects the **reduced-motion** setting.

## Built with

The whole site is one self-contained `index.html`: hand-written HTML, CSS and JavaScript, with no build
step and no framework. These libraries load from public CDNs:

| Library | Version | Used for |
|---|---|---|
| [Three.js](https://threejs.org) | r128 | 3D building model |
| [GSAP](https://gsap.com) + ScrollTrigger | 3.12.5 | Scroll-driven animation |
| [Lenis](https://lenis.darkroom.engineering) | 1.1.13 | Smooth scrolling |
| [Google Fonts](https://fonts.google.com) (Archivo) | — | Typography |

## Project structure

```
rs-builder/
├── index.html   # the complete website
└── README.md
```

## Run locally

No installation needed. Either open `index.html` in a browser, or serve the folder:

```bash
git clone https://github.com/AhlamCode2150/rs-builder.git
cd rs-builder
python -m http.server 8000      # then open http://localhost:8000
```

An internet connection is needed for the CDN libraries and fonts.

## Deployment

The site is static, so it can be hosted anywhere.

- **GitHub Pages:** published from the `main` branch, root folder. Every push to `main` updates the site.
- **Netlify:** deploy the folder with the [Netlify CLI](https://docs.netlify.com/cli/get-started/):
  ```bash
  netlify deploy --prod --dir .
  ```

`index.html` is kept byte-for-byte as delivered. The repo has `core.autocrlf` set to `false` so git never
changes its line endings.

## Contact

**RS Builder** · Main Boulevard, Gulberg III, Lahore
Phone / WhatsApp: +92 300 0000000 · Email: hello@rsbuilder.pk

---

© RS Builder. All rights reserved.
