# Evangelia Antonopoulou - Personal CV Website

A clean, minimal, and professional CV website built with HTML, CSS, and vanilla JavaScript.

**Live Site:** `evaantonopoulou.github.io/cv`

---

## Features

* Dark / Light mode toggle
* Download as PDF (print-optimized styles)
* Share button (native share on mobile, copy link on desktop)
* Profile photo embedded directly in HTML (no external dependencies)
* Century Gothic font via system fonts (no external dependencies)
* Responsive design (mobile, tablet, desktop)
* Print-optimized styles (buttons hidden, white background)

---

## Project Structure

```
cv/
└── index.html      # Everything in one file: HTML, CSS, JS, and embedded photo
└── README.md       # This file
```

> Unlike many CV sites, this project is intentionally **single-file**. The photo is embedded as base64, the styles are inline, and the JavaScript is included at the bottom — making it zero-dependency and trivial to deploy.

---

## How to View Locally

No build tools needed. Just open the file:

```bash
# Option 1 — Double-click index.html in your file explorer

# Option 2 — Using Python
python3 -m http.server 8000
```

Then open `http://localhost:8000`

---

## How to Update Content

All CV content lives inside `index.html`. To update:

1. **Name / Title:** Edit the `<h1>` and `.istqb-badge` inside `<header>`
2. **Contact links:** Edit the `<div class="contacts">` links
3. **About:** Edit the `<p class="summary-text">` paragraph
4. **Experience:** Add or edit `<div class="exp-item">` blocks
5. **Tech Stack:** Add or remove `<span class="tech-pill">` elements
6. **Education:** Add or edit `<div class="edu-item">` blocks
7. **Volunteering:** Edit the `<div class="vol-box">` section

### Adding a New Job Entry

```html
<div class="exp-item">
  <div class="exp-meta">
    <div class="exp-date">Month YYYY — Month YYYY</div>
    <div class="exp-company">Company Name</div>
  </div>
  <div>
    <div class="exp-role">Job Title</div>
    <ul class="exp-bullets">
      <li>Achievement or responsibility</li>
      <li>Another bullet point</li>
    </ul>
  </div>
</div>
```

---

## Styling Customization

CSS variables are defined in `:root` at the top of the `<style>` block:

```css
:root {
  --bg: #0e0e0f;         /* Page background */
  --surface: #161618;    /* Card / section background */
  --surface2: #1e1e21;   /* Pills, buttons background */
  --border: #2a2a2e;     /* Borders and dividers */
  --text: #e8e8ea;       /* Main text color */
  --muted: #888890;      /* Secondary / metadata text */
  --accent: #c8f564;     /* Primary accent (yellow-green) */
  --accent2: #b388ff;    /* Secondary accent (purple) */
  --accent3: #f5a623;    /* Tertiary accent (orange) */
}
```

Light mode overrides these inside `body.light-mode { ... }`.

---

## Buttons

| Button | Action |
|--------|--------|
| 🌙 Moon icon | Toggles dark / light mode |
| ⬇️ Download icon | Opens print dialog → Save as PDF |
| 🔗 Share icon | Native share on mobile · Copies URL on desktop |

---

## Deployment

The site is deployed via **GitHub Pages** from the `main` branch.

Any push to `main` will trigger a rebuild (takes ~1–2 minutes).

To deploy your own copy:
1. Fork or upload `index.html` to a new GitHub repository
2. Go to **Settings → Pages → Deploy from branch → main**
3. Your site will be live at `https://[your-username].github.io/[repo-name]`

---

## Tech Stack

* **HTML5** — Semantic markup
* **CSS3** — Custom properties, Flexbox, Grid, animations, print styles
* **JavaScript** — Vanilla JS, no frameworks
* **GitHub Pages** — Hosting

---

## License

This is a personal CV website. Feel free to use the structure as a template for your own CV.
