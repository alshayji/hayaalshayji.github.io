# Personal Website — Haya Alshayji

Single-page academic site. Static HTML + CSS, no build step, no JS framework. Designed to deploy to GitHub Pages in about 10 minutes.

## Files

- `index.html` — the page content
- `style.css` — the styling
- `cv.pdf` — drop your CV PDF here so the "CV (PDF)" link in the header works
- `README.md` — this file

## Deploy to GitHub Pages (recommended, free)

1. Make a GitHub account if you don't have one: <https://github.com/signup>
2. Create a new public repository named exactly **`hayaalshayji.github.io`** (or `<yourGithubUsername>.github.io`). The site URL will end up as `https://hayaalshayji.github.io/` (or your username equivalent).
3. Upload three files to the repository root: `index.html`, `style.css`, and your CV PDF named `cv.pdf`.
   - Easiest path: in the GitHub web UI, click "Add file" → "Upload files" → drag the three files in.
4. Wait 1–3 minutes after the upload finishes. The site goes live automatically at `https://<yourusername>.github.io/`.
5. Add the URL to your CV (already drafted as a placeholder line — see below).
6. To update later, replace `index.html` or `style.css` in the same repository.

### Custom domain (optional)

If you want a domain like `hayaalshayji.com` instead of `.github.io`:

1. Buy the domain (Namecheap, Cloudflare, Google Domains — usually $10–$15/yr).
2. In the GitHub repo Settings → Pages, set the custom domain to `hayaalshayji.com`.
3. In the domain registrar, point a `CNAME` record to `<yourusername>.github.io`.
4. GitHub will issue a free HTTPS certificate automatically.

## Add the URL to your CV

In the CV header (right under your name), the contact line currently reads:

> 301 Leonhard Building, University Park, PA 16802 | hka5222@psu.edu | 

Once the site is live, swap to:

> 301 Leonhard Building, University Park, PA 16802 | hka5222@psu.edu | hayaalshayji.github.io

(or use your custom domain).

## How to edit

Open `index.html` in any editor (VS Code, BBEdit, even TextEdit). The structure follows the visible page top-to-bottom: hero header → nav → six sections (About, Research, Publications, Talks, Teaching, Contact) → footer.

To add a new publication, paste a new `<li>...</li>` inside the appropriate `<ol class="pubs">` block. Same pattern for talks.

To change colors, edit the CSS variables at the top of `style.css`:

```css
:root {
  --navy: #0e2a4f;
  --teal: #1c7293;
  --gold: #e1b43b;
  ...
}
```

## What's already inside

- Hero header with name, role, the equity tagline, and primary links (email, Scholar, LinkedIn, CV).
- Sticky top nav for the six sections.
- About section.
- Research section with three cards (Paper 1 / Paper 2 / Paper 3) using your real numbers — 513,070 adults, 876 ZIP-3 areas, ICC 4.0%, 47.1% / 15.0% variance decomposition, Medicaid aOR = 2.31.
- Research interests pill list.
- Publications + Manuscripts + Grants (CHERISH).
- Selected talks (IISE 2026, PA Public Health 2026, INFORMS, ICDS, AI4Health Bowl).
- Teaching & Mentoring (Summer Bridge, DAIR3, society memberships).
- Contact.

## Things you should personalize before deploying

1. Replace the Google Scholar URL placeholder (`https://scholar.google.com/`) with your actual profile once it exists.
2. Replace the LinkedIn URL placeholder with your actual profile.
3. Drop your `cv.pdf` in the same folder so the "CV (PDF)" link works.
4. If you want a photo, add `<img src="profile.jpg" alt="Haya Alshayji" class="hero-photo">` inside `.hero-inner` and add a `.hero-photo { border-radius: 50%; width: 110px; ... }` rule to the CSS.
