# Resume Site

My personal resume and portfolio site, built with vanilla HTML, CSS, and JavaScript.

**Live site:** https://work-sand-psi.vercel.app/

## Features

- **Project table** with live demo and source links for each project
- **Copy-to-clipboard** buttons for contact info, using the Clipboard API with a fallback for older browsers
- **Contact form** with required-field validation that composes a pre-filled email via `mailto:`
- **Draft saving** — form input is saved to `localStorage` so a half-written message survives a page reload
- **Accessible status messages** using an `aria-live` region

## Project Structure

```
├── index.html   # Page markup: header, summary, skills, projects, contact form
├── styles.css   # Layout and styling
├── scriptCV.js  # Copy buttons, contact form validation, draft saving, mailto
└── image.png    # Profile photo
```

## Running Locally

No build step or dependencies. Open `index.html` in a browser, or serve the folder:

```bash
git clone https://github.com/zykia-j/resume-site.git
cd resume-site
npx serve .
```

The copy buttons use the modern Clipboard API on `https://` or `localhost`, and fall back to `document.execCommand("copy")` elsewhere.

## Deployment

Deployed on Vercel as a static site.
