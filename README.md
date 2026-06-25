# Grenzphilosophie

A journal of philosophy at the frontier of science.
*Where measurement guides the exploration of purpose.*

Live site: **[grenzphilosophie.com](https://grenzphilosophie.com)**

## Design

A literary "dark academia" template — parchment ground, oxblood accent, Libre
Caslon throughout — built as a single hand-written stylesheet. No framework, no
build step, no JavaScript dependencies.

| Token        | Value     | Role                         |
| ------------ | --------- | ---------------------------- |
| Parchment    | `#F9EFE6` | Background                   |
| Ink          | `#21121E` | Body text (dark aubergine)  |
| Oxblood      | `#9F3732` | Accent — links, rules, marks |
| Display font | Libre Caslon Display | Titles, drop caps |
| Text font    | Libre Caslon Text    | Body, italics     |

Reading column is held to a single ~41rem measure; a faint SVG paper grain,
staggered fade-ups, a drop cap, centred pull-quotes, and a reading-progress
hairline carry the editorial feel. Everything degrades gracefully and respects
`prefers-reduced-motion`.

## Structure

```
.
├── index.html          # Masthead + recent essays
├── archive.html        # Complete archive, by year
├── css/
│   └── style.css       # The entire design system
├── posts/              # One file per essay (shared article template)
│   ├── epistemology-neural.html
│   ├── quantum-measurement.html
│   └── … (12 essays)
├── images/
│   ├── hero-book.webp   # Frontispiece (optimized)
│   └── hero-book.png    # Frontispiece (fallback)
├── CNAME               # Custom domain for GitHub Pages
└── .nojekyll           # Serve files as-is (skip Jekyll)
```

## Deployment (GitHub Pages + custom domain)

The repository is configured to publish from the `main` branch root.

1. **Pages settings** — Settings → Pages → Source: *Deploy from a branch*,
   Branch: `main` / `(root)`.
2. **Custom domain** — the `CNAME` file already declares `grenzphilosophie.com`.
3. **DNS** — at your registrar, point the domain at GitHub Pages:
   - Apex `A` records → `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`
   - (and/or apex `AAAA` records → `2606:50c0:8000::153` … `8003::153`)
   - `www` `CNAME` → `jonashertner.github.io`
4. Once DNS resolves, enable **Enforce HTTPS** in Pages settings.

## Adding an essay

1. Copy any file in `posts/` as a template.
2. Replace the `<title>`, meta description, `article__meta`, `article__title`,
   `article__standfirst`, and the `.prose` body (paragraphs, `h2` sections, one
   `blockquote` pull-quote).
3. Add the entry to `index.html` (if recent) and to `archive.html`.
4. Update the `← Newer` / `Older →` links on the neighbouring posts.

## License

Content and design © 2026 Grenzphilosophie. All rights reserved.
