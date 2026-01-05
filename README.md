# LuisFMCuriel.github.io

Personal portfolio website for **Luis Felipe Morales Curiel**, showcasing selected research publications, industry projects, and applied machine learning work.

This site is built with **GitHub Pages + Jekyll** and is intentionally lightweight, fast, and easy to maintain, while still supporting dynamic content (projects, featured work, confidential industry experience).

🌐 **Live site:** https://luisfmcuriel.github.io/

---

## ✨ Overview

This portfolio highlights:

- Peer‑reviewed research in **deep learning for microscopy and computational imaging**
- Applied **computer vision and ML systems** deployed under real‑time and edge constraints
- **Physics‑based simulations** (e.g. COMSOL) supporting microfluidic and thermal system design
- Selected **confidential industry projects**, described safely and professionally

The goal is to present *what I work on* and *how I think*, without exposing proprietary material.

---

## 🧱 Tech stack

- **Static site:** Jekyll (GitHub Pages)
- **Styling:** Custom CSS (no frameworks)
- **Data‑driven content:** YAML (`_data/projects.yml`)
- **Languages:** Markdown, HTML, CSS, Liquid
- **Hosting:** GitHub Pages

No JavaScript frameworks, build steps, or backend services are required.

---

## 📁 Repository structure

```
.
├── index.md                # Homepage
├── projects.md             # Projects page (cards + filters)
├── cv.md                   # Embedded CV page
├── _data/
│   └── projects.yml        # All projects (research + industry)
├── assets/
│   ├── css/
│   │   └── style.css       # Custom styling
│   ├── img/
│   │   ├── profile.jpg
│   │   └── projects/       # Project images / GIFs
│   └── projects/           # (optional) alternate project media
└── README.md
```

---

## 📌 Projects

Projects are defined in `_data/projects.yml` and rendered automatically.

Each entry can include:
- `title`
- `year`
- `tags`
- `description`
- `link` (optional)
- `image` (optional PNG/GIF)
- `featured` (true/false)

This allows easy reordering, filtering, and homepage highlighting without touching page layouts.

### Confidential / industry projects
Industry work is included without links or sensitive details, and is clearly marked as confidential.  
Descriptions focus on **methods, systems, and impact**, not IP.

---

## 🚀 Local development (optional)

To preview locally:

```bash
bundle install
bundle exec jekyll serve
```

Then open:
```
http://localhost:4000
```

---

## 📄 License

Content is © Luis Felipe Morales Curiel.  
Code structure and configuration may be reused with attribution.

---

## 📫 Contact

- Email: felipemoralescuriel@gmail.com  
- LinkedIn: see CV or website

Thanks for visiting!
