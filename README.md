# Yulianto, S.Kom., M.Kom — Personal Portfolio

A vibrant, fully responsive single-page portfolio built to maximize personal branding, visibility, and credibility. Includes a real profile photo, academic profiles, professional links, and a filterable project showcase.

Built with **HTML5**, **CSS3**, **Tailwind CSS**, and **vanilla JavaScript** — no build step required.

## What's inside
- **Hero** — headline, availability badge, CTAs, portrait, and quick domain badges
- **About / Spotlight** — background, achievement cards, and an animated "Core expertise" panel
- **Selected Work** — filterable grid (All / IoT & AI / Development / Creative)
- **Research & Profiles** — credibility links to Google Scholar, Scopus, Sinta, ORCID, Shutterstock, and the Keylens blog
- **Contact & Socials** — validated form, WhatsApp/email/location cards, and social links
- **Footer** — quick navigation and back-to-top

## Built-in features
- Sticky glass navbar with active-section highlighting and a mobile menu
- Scroll-reveal animations with a reduced-motion fallback and a visibility safety net
- Animated gradient borders, floating ambient blobs, gradient text, and a marquee
- Client-side form validation with accessible errors and a success toast
- Responsive across mobile, tablet, and desktop
- Accessible: skip link, focus states, ARIA labels, semantic landmarks

## Project structure
```
.
├── index.html          # the entire site (HTML + CSS + JS)
├── assets/
│   ├── portrait.jpg    # optimized profile photo (1000×1777, ~213 KB)
│   ├── dsc6223-2.jpg   # slideshow photo
│   ├── dsc4419-2.jpg   # slideshow photo
│   ├── LAB09675.JPG
│   ├── DSC05728.JPG
│   ├── DSC05649~2.JPG
│   ├── DSC05438~2.JPG
│   └── DSC02898.JPG
├── _DSC9415.JPG        # original photo (keep or delete)
├── New Text Document.txt   # original profile notes
└── README.md
```

## Preview locally
Open `index.html` directly, or serve the folder:

```bash
python -m http.server 8000
# visit http://localhost:8000
```

## Deploy to GitHub Pages
1. Create a repository (e.g. `portfolio`).
2. Push these files to the repo root:
   ```bash
   git init
   git add .
   git commit -m "Add portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
3. Go to **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Live at `https://<your-username>.github.io/<repo>/`.

> Naming the repo `<your-username>.github.io` serves it at the root domain.

## Customize
| What | Where |
| --- | --- |
| Name / initials | Search `Yulianto` and the `Y` logo badge |
| Headline & intro | Hero `<section id="home">` |
| About copy & achievement cards | `<section id="about">` |
| Expertise bars | `#skills` panel (`data-width` attributes) |
| Projects | `.project-card` articles; `data-category` drives filtering |
| Profile links | `<section id="profiles">` |
| Social links | Contact section icon row |
| Email / location | Contact cards (`hello@yulianto.dev` is a placeholder) |
| Photo | Replace `assets/portrait.jpg` (keep the same filename) |

### Replace the placeholder project links
The six project cards describe representative work across your expertise areas. Update each card's title, description, tags, and `href="#"` links with your real case studies, repositories, or publications.

### Make the contact form live
A ready-to-use [Formspree](https://formspree.io) action is already wired up:
```html
<form id="contactForm" action="https://formspree.io/f/your-id" method="POST" novalidate>
```
Replace `your-id` with your Formspree form ID. Once it no longer contains `your-id`, the script lets the browser POST the form natively after client-side validation. (You can also use Getform or Web3Forms — update the `action`.)

Until then, the form runs in demo mode: it validates, shows a success toast, and resets.

## Notes
- Fonts load from **Google Fonts** and utilities from the **Tailwind Play CDN**, so the page needs internet on first load. For a fully self-contained or production build, compile Tailwind with the CLI and self-host the fonts:
  ```bash
  npx tailwindcss -i input.css -o styles.css --minify
  ```
- `_DSC9415.JPG` is the original 11 MB photo. `assets/portrait.jpg` is the optimized version used by the site; you can delete the original to keep the repo small.
- GitHub Pages uses Jekyll by default, which excludes files whose names start with `_`. Slideshow images therefore use names without a leading underscore so they are published correctly.
- All decorative visuals are CSS/SVG only, so there are no extra image dependencies.

## License
Free to use and adapt for your own portfolio.
