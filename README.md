# Aliyar PhD Portfolio Website (Static)

## What you got
- A single-page static site (index.html + app.js) that loads content from `content/projects.json`.
- CV embedded + downloadable.
- Two portfolios (Design / Research) + project detail pages.
- All assets (PDFs + rendered project pages) inside `/assets`.

## How to edit / add projects (no complex coding)
1) Open `content/projects.json`
2) Duplicate an existing project object and change:
   - `id` (unique, use kebab-case)
   - `category`: "design" or "research"
   - `title`, `subtitle`, `period`, `tags`
   - `heroImage`: put an image file in `/assets` and reference it here
   - `what`, `how`, `results` arrays
   - `links` array (label + url)
3) Save. Re-deploy the site.

### Adding images
- Put PNG/JPG in `/assets`.
- Update the project's `heroImage` to match the filename.

## How to host (fast + free)
### Option A (recommended): GitHub + Netlify
1) Create a GitHub repo and push all files.
2) Netlify: New site from Git -> select repo -> build command: (none) -> publish directory: (root)
3) Netlify will give you a URL. Add a custom domain later if you want.

### Option B: GitHub Pages
1) Push to repo
2) Settings -> Pages -> Deploy from branch -> root
3) Site will be available at https://<username>.github.io/<repo>/

## Visitor tracking (analytics)
- Easiest: Google Analytics 4 (free).
  1) Create a GA4 property, copy Measurement ID like `G-ABC123...`
  2) Open `index.html`
  3) Uncomment the analytics scripts and paste your Measurement ID.
- Alternative: Plausible (paid) or Cloudflare Web Analytics (free-ish, privacy-friendly).

## Disclaimer
Some results in the original PDFs are written as claims. For PhD reviewers, add evidence:
- test setup, assumptions, plots, standards, public patent numbers, acceptance letters, etc.
