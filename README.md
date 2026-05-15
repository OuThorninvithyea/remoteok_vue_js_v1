<div align="center">
  <img src="./public/images/logo.png" alt="RemoteOK Logo" width="120" />
  <h1>RemoteOK Vue</h1>
  <p><strong>Premium Remote Job Board — Frontend Edition</strong></p>

  <p>
    <a href="https://cv-ou-thorninvithyea-fvkg.vercel.app/">
      <img src="https://img.shields.io/badge/Portfolio-Ou%20Thorninvithyea-blue?style=flat-square" alt="Portfolio" />
    </a>
    <img src="https://img.shields.io/badge/Vue-3.5-4FC08D?style=flat-square&logo=vue.js" alt="Vue 3" />
    <img src="https://img.shields.io/badge/Vite-8.0-646CFF?style=flat-square&logo=vite" alt="Vite 8" />
    <img src="https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript" alt="JavaScript" />
    <img src="https://img.shields.io/badge/Status-Development-yellow?style=flat-square" alt="Status" />
  </p>
</div>

---

## Overview

**RemoteOK Vue** is a feature-rich remote job board frontend built with Vue 3. It delivers a premium browsing experience with advanced filtering, sorting, and an integrated job posting flow. The application uses a static JSON data architecture, making it fast to deploy and easy to customize without a backend dependency.

This frontend-only edition includes the complete UI for job discovery, company browsing, and a multi-step "Post a Job" wizard.

## Key Features

- **Job Discovery** — Browse remote jobs with categories, sort options, salary ranges, and location filters
- **Advanced Filtering** — Dropdown-based benefits, location, salary, and sorting controls
- **Post a Job Flow** — Complete multi-step form with company details, job description editor, preview, and payment
- **Trust Signals** — Testimonials, trusted company logos, and statistical sidebar
- **Responsive Design** — Optimized for both desktop and mobile browsing
- **Data-Driven** — Fully powered by JSON data files for easy content management

## Tech Stack

| Technology | Purpose |
|------------|---------|
| **Vue 3** (Composition API) | Frontend framework |
| **Vite 8** | Build tool and dev server |
| **JavaScript (ES6+)** | Application logic |
| **CSS3** | Styling with modular CSS files |

## Project Structure

```
remoteok_vue_js_v1/
├── public/images          # Company logos, icons, testimonials
├── src/
│   ├── assets/            # Global styles, logo
│   ├── components/        # Vue components by feature
│   │   ├── homePage/      # Job listing, filters, header
│   │   ├── postJob/       # Post-a-job flow components
│   │   ├── login/         # Login form
│   │   └── icons/         # SVG icon components
│   ├── composables/       # Vue composables (data hooks)
│   ├── data/              # JSON data files
│   ├── layouts/           # Layout wrappers
│   ├── router/            # Vue Router configuration
│   ├── styles/            # Page-specific CSS
│   ├── views/             # Page-level view components
│   ├── App.vue
│   └── main.js
├── index.html
├── package.json
└── vite.config.js
```

## Getting Started

```bash
git clone https://github.com/OuThorninvithyea/remoteok_vue_js_v1.git
cd remoteok_vue_js_v1
npm install
npm run dev      # Dev server: http://localhost:5173
npm run build    # Production build
npm run preview  # Preview production build
```

## Screens

| Route | Description |
|-------|-------------|
| `/` | Home — Browse jobs with all filters |
| `/login` | User login form |
| `/post-job` | Multi-step job posting wizard |

## Author

**Ou Thorninvithyea**

- 🌐 [Portfolio](https://cv-ou-thorninvithyea-fvkg.vercel.app/)
- 🐙 [GitHub](https://github.com/OuThorninvithyea)
- 📧 Vithyeasa@gmail.com
- 📍 Phnom Penh, Cambodia

> Software Engineer specializing in modern UI engineering, performance optimization, and accessible web applications.

---

<div align="center">
  <sub>Built with ❤️ by Ou Thorninvithyea</sub>
</div>
