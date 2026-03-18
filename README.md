# Evangelia Antonopoulou — Personal CV Website

A clean, minimal, and professional CV website built with HTML, CSS, and vanilla JavaScript.

**Live Site:** `https://evaantonopoulou.github.io/`

---

## Features

* 🌙 Dark / Light mode toggle
* ⬇️ Download as PDF (print-optimized styles)
* 🔗 Share button (native share on mobile, copy link on desktop)
* 📷 Profile photo embedded as base64 (no external dependencies)
* 🔤 Century Gothic font via system fonts (no external dependencies)
* 📱 Responsive design (mobile, tablet, desktop)
* 🖨️ Print-optimized styles (compact, black & white friendly)
* ✅ Single-file architecture — everything in one `index.html`

---

## Project Structure

```
cv/
├── index.html      # Everything: HTML, CSS, JS, and embedded photo
└── README.md       # This file
```

> This project is intentionally **single-file**. The photo is embedded as base64, styles are inline, and JavaScript is included at the bottom — making it zero-dependency and trivial to deploy.

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

All content lives inside `index.html`. To update:

1. **Name / Title:** Edit the `<h1>` and `.title` inside `.header`
2. **Contact links:** Edit the `<div class="contacts">` links
3. **About:** Edit the `<p class="about-text">` paragraph
4. **Experience:** Add or edit `<div class="entry">` blocks
5. **Tech Stack:** Add or remove `<span class="skill-tag">` elements
6. **Education & Certifications:** Add or remove `<span class="skill-tag">` elements inside the Education section
7. **Volunteering:** Edit the last `<div class="entry">` block

### Adding a New Job Entry

```html
<div class="entry">
  <div class="entry-left">
    <div class="entry-title">Job Title</div>
    <div class="entry-company">Company Name</div>
    <ul class="entry-details">
      <li>Achievement or responsibility</li>
      <li>Another bullet point</li>
    </ul>
  </div>
  <div class="entry-date">Month YYYY — Month YYYY</div>
</div>
<hr class="divider">
```

---

## Styling Customization

CSS variables are defined in `:root` at the top of the `<style>` block:

```css
:root {
  --bg: #ffffff;           /* Page background */
  --surface: #f8f9fa;      /* Surface background */
  --border: #e2e8f0;       /* Borders and dividers */
  --text: #1a1a2e;         /* Main text color */
  --muted: #64748b;        /* Secondary text */
  --accent: #6d28d9;       /* Primary accent (dark purple) */
  --accent-light: #f3f0ff; /* Light purple for tags */
  --accent2: #4c1d95;      /* Secondary accent */
}
```

Dark mode overrides these inside `body.dark { ... }`.

---

## Buttons

| Button | Action |
|--------|--------|
| 🌙 Moon icon | Toggles dark / light mode |
| ⬇️ Download icon | Opens print dialog → Save as PDF |
| 🔗 Share icon | Native share on mobile · Copies URL on desktop |

> **PDF Tip:** In the print dialog, go to **More settings** and disable **"Headers and footers"** for a cleaner PDF.

---

## Deployment

The site is deployed via **GitHub Pages** from the `main` branch.

Any push to `main` will trigger a rebuild (takes ~1–2 minutes).

To deploy:
1. Upload `index.html` to a GitHub repository
2. Go to **Settings → Pages → Deploy from branch → main**
3. Your site will be live at `https://[your-username].github.io/[repo-name]`

---

## Tech Stack

* **HTML5** — Semantic markup
* **CSS3** — Custom properties, Flexbox, animations, print styles
* **JavaScript** — Vanilla JS, no frameworks
* **GitHub Pages** — Hosting

---

## License

This is a personal CV website. Feel free to use the structure as a template for your own CV.
