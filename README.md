# Nguyen Duy Cuong — Online CV (Resume)

Standalone, print-ready **1-page A4** online CV built with semantic HTML & CSS, featuring clickable project links and instant browser **Save PDF** export.

- **Live CV (GitHub Pages):** https://duycuongdev.github.io/curriculum-vitae/
- **Portfolio Site:** https://duycuongdev.github.io/portfolio/ ([Repository](https://github.com/duycuongdev/portfolio))
- **GitHub:** https://github.com/duycuongdev

## Features

- **1-Page A4 Print Layout:** Precisely tuned `@media print` and `@page` rules (`size: A4 portrait; margin: 0`) so exported PDFs stay crisp on one single page with selectable text and working hyperlinks.
- **Screen-Only PDF Toolbar:** Built-in **Save PDF** (`window.print()`) button that automatically hides when printing or exporting.
- **Structured Project Table:** Clean single-column tech CV format highlighting architecture, real-time Socket.IO features, Dual-Auth security, MongoDB pipelines, CI/CD, and links to live demos and repositories.
- **Responsive Mobile View:** Adapts smoothly into a stacked single-column layout on screens narrower than `820px`.

## Export to PDF

1. Open [the live CV](https://duycuongdev.github.io/curriculum-vitae/) (or `index.html` locally).
2. Click **Save PDF** in the top-right toolbar (or press `Ctrl+P` / `Cmd+P`).
3. Recommended browser print settings:
   - **Destination:** Save as PDF
   - **Paper size:** A4
   - **Margins:** None
   - **Options:** Background graphics **On** (Headers and footers **Off**)

## Project Structure

```text
curriculum-vitae/
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions -> GitHub Pages deployment
├── assets/
│   ├── ico/logo.jpg        # Browser favicon
│   └── img/avatar.jpg      # Portrait photo
├── css/
│   └── style.css           # Screen, responsive & A4 print stylesheet
├── index.html              # Semantic CV document
└── README.md
```

## Run Locally

Open `index.html` directly in your browser, or run a lightweight static server:

```bash
# Using Python
python -m http.server 5500

# Or using Node.js
npx serve .
```

## Automated Deployment

Every push to `main` triggers [`.github/workflows/deploy.yml`](./.github/workflows/deploy.yml) to verify assets and deploy the static bundle to **GitHub Pages**.

> First-time GitHub setup: Open repository **Settings -> Pages -> Build and deployment -> Source**, and select **GitHub Actions**.
