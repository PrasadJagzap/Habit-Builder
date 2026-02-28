# 🧠 Habit-Builder

> *"You do not rise to the level of your goals. You fall to the level of your systems."* — James Clear

[![Status](https://img.shields.io/badge/Status-Active%20Development-brightgreen)]()
[![Version](https://img.shields.io/badge/Version-1.0.0-blue)]()
[![License](https://img.shields.io/badge/License-MIT-yellow)]()
[![Stack](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JS-orange)]()

A portfolio-grade, frontend-only habit tracking web app inspired by *Atomic Habits*. No frameworks. No backend. No dependencies. Pure HTML, CSS, and Vanilla JavaScript — structured at production level.

🔗 **[Live Demo](#)** &nbsp;|&nbsp; 📁 **[Blueprint Doc](docs/blueprint.md)** &nbsp;|&nbsp; 🗺 **[Roadmap](docs/roadmap.md)**

---

## ⚡ What It Does

| Feature | Detail |
|---|---|
| Daily Check-in | Mark habits complete each day |
| Streak Tracking | Flame-based streak counter with milestone alerts |
| Habit Manager | Create, edit, archive habits with icon, color, category |
| Progress Heatmap | GitHub-style monthly completion grid |
| Analytics | Per-habit stats, best/worst day, completion rate |
| Motivation Hub | 100+ quotes with save, share, and daily rotation |
| Onboarding | 5-step first-time setup wizard |
| Themes | Light / dark mode via CSS custom properties |
| Reminders | Browser push notification system |
| Data Export | Export all habit data to CSV |

---

## 📄 Pages

| Page | File | Role |
|---|---|---|
| Landing | `index.html` | Marketing, intro, CTA |
| Dashboard | `pages/dashboard.html` | Daily hub, today's habits |
| Habit Manager | `pages/habits.html` | CRUD for all habits |
| Progress | `pages/progress.html` | Streaks, heatmap, completion |
| Analytics | `pages/analytics.html` | Charts, trends, records |
| Motivation | `pages/motivation.html` | Quotes, challenges, tips |
| Onboarding | `pages/onboarding.html` | First-time setup wizard |
| Settings | `pages/settings.html` | Theme, reminders, data |
| Login / Register | `pages/login.html` · `register.html` | Auth UI |
| About | `pages/about.html` | Project + developer info |

---

## 📁 Folder Structure

```
habit-builder/
│
├── index.html
├── pages/
│   ├── dashboard.html
│   ├── habits.html
│   ├── progress.html
│   ├── analytics.html
│   ├── motivation.html
│   ├── onboarding.html
│   ├── settings.html
│   ├── login.html
│   ├── register.html
│   ├── forgot-password.html
│   └── about.html
│
├── components/
│   ├── navbar.html
│   ├── sidebar.html
│   ├── footer.html
│   ├── habit-card.html
│   ├── streak-badge.html
│   ├── modal.html
│   ├── progress-bar.html
│   ├── toast.html
│   ├── quote-card.html
│   └── empty-state.html
│
├── styles/
│   ├── main.css            ← variables, reset, base
│   ├── layout.css          ← grid, containers, spacing
│   ├── components.css      ← buttons, cards, inputs
│   ├── animations.css      ← all keyframes
│   ├── themes.css          ← light/dark overrides
│   ├── dashboard.css
│   ├── habits.css
│   ├── progress.css
│   ├── analytics.css
│   ├── motivation.css
│   ├── settings.css
│   ├── auth.css
│   └── onboarding.css
│
├── scripts/
│   ├── app.js              ← boot, global listeners
│   ├── router.js           ← navigation, active links
│   ├── storage.js          ← localStorage abstraction
│   ├── auth.js             ← login, register, session
│   ├── habits.js           ← create, edit, delete, archive
│   ├── tracker.js          ← check-in, streak engine
│   ├── analytics.js        ← aggregation, calculations
│   ├── charts.js           ← bar, heatmap, pie renderers
│   ├── quotes.js           ← load, rotate, save, filter
│   ├── notifications.js    ← reminders, milestone alerts
│   ├── settings.js         ← preferences, theme toggle
│   ├── onboarding.js       ← step manager, validation
│   └── utils.js            ← dates, math, string helpers
│
├── assets/
│   ├── images/             ← logo, hero, OG preview
│   ├── icons/              ← habit, UI, social SVGs
│   └── fonts/              ← Inter woff2 files
│
├── data/
│   ├── quotes.json         ← { id, text, author, category }
│   ├── habit-templates.json
│   └── categories.json     ← { id, name, icon, color }
│
└── docs/
    ├── blueprint.md
    ├── roadmap.md
    └── changelog.md
```

---

## 🛠 Tech Stack

| Layer | Choice | Why |
|---|---|---|
| Markup | HTML5 | Semantic, accessible |
| Styling | CSS3 + Custom Properties | Scalable theming, zero deps |
| Logic | Vanilla JS (ES6+) | No framework overhead |
| Storage | `localStorage` | Zero-backend persistence |
| Charts | Canvas API | Lightweight, no library |
| Fonts | Inter (self-hosted) | Clean, highly legible |
| Hosting | GitHub Pages / Netlify | Free, instant deploy |

---

## 🗃 Data Schema

```
localStorage keys
──────────────────────────────────────────────────────────────────
habitbuilder_user       → { name, email, avatar }
habitbuilder_habits     → [{ id, name, category, icon, color,
                             frequency[], createdAt, isArchived }]
habitbuilder_checkins   → [{ id, habitId, date, completedAt }]
habitbuilder_settings   → { theme, reminderTime, defaultView }
habitbuilder_quotes     → [ savedQuoteIds ]
habitbuilder_onboarded  → boolean
```

---

## 🎨 CSS Token System

All visual values are CSS custom properties. Dark mode switches via `data-theme="dark"` on `<html>`.

```
Color   →  --color-primary  --color-surface  --color-text
Type    →  --font-size-sm/base/lg/xl  --font-weight-bold
Space   →  --space-xs / sm / md / lg / xl
Shape   →  --radius-sm / md / lg / full
Shadow  →  --shadow-card  --shadow-modal
Motion  →  --transition-fast  --transition-base
```

---

## 📱 Breakpoints

| Range | Target |
|---|---|
| `< 480px` | Small phones |
| `480–768px` | Large phones |
| `768–1024px` | Tablets |
| `1024–1280px` | Laptops |
| `> 1280px` | Desktops |

---

## 🚀 Getting Started

```bash
# 1. Clone
git clone https://github.com/prasadjagzap/habit-builder.git
cd habit-builder

# 2. Run — zero install required
# Open index.html in browser  OR  use VS Code Live Server
```

No `npm install`. No build step. No config. Open and run.

---

## 🗺 Roadmap

**Phase 1 — Core** *(active)*
- [x] Full project structure
- [x] CSS design system
- [ ] Auth pages logic
- [ ] Habit CRUD + localStorage
- [ ] Daily check-in + streak engine
- [ ] Dashboard complete

**Phase 2 — Depth**
- [ ] Progress heatmap + analytics charts
- [ ] Quotes hub + push notifications
- [ ] CSV data export

**Phase 3 — Polish**
- [ ] PWA + Service Worker (offline support)
- [ ] Skeleton loaders + page transitions
- [ ] WCAG 2.1 AA accessibility audit
- [ ] Lighthouse score 90+

**Phase 4 — Backend** *(future)*
- [ ] Node.js + Express REST API
- [ ] JWT auth + PostgreSQL
- [ ] Cloud sync + email reminders

---

## 🤝 Contributing

```bash
git checkout -b feature/your-feature-name
# make changes
git commit -m "feat: describe your change"
git push origin feature/your-feature-name
# open a Pull Request
```

| Prefix | Use for |
|---|---|
| `feat:` | New feature |
| `fix:` | Bug fix |
| `style:` | CSS / visual only |
| `refactor:` | Code restructure |
| `docs:` | Documentation update |

---

## 📋 Changelog

**v1.0.0** *(in progress)*
- All pages, components, styles, and scripts scaffolded
- CSS design system and theming complete
- Data schema and localStorage architecture defined
- Full documentation written

> See [`docs/changelog.md`](docs/changelog.md) for full history

---

## 📄 License

MIT License — free to use, modify, and distribute with attribution.
See [`LICENSE`](LICENSE) for details.

---

## 👤 Author

**Your Name** — Frontend Developer

[![Portfolio](https://img.shields.io/badge/Portfolio-yoursite.com-blue)]()
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5)]()
[![GitHub](https://img.shields.io/badge/GitHub-prasadjagzap-181717)]()

---

## 🙏 Acknowledgements

- **James Clear** — *Atomic Habits*, the philosophical core of this project
- **Inter Font** — Rasmus Andersson
- **Undraw** — open-source SVG illustrations
- **Shields.io** — README badges

---

<div align="center">

**Small habits. Consistent systems. Extraordinary results.**

⭐ Star this repo if it helped you ⭐

</div>