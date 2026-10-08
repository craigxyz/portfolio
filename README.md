# Personal portfolio

A bold dark gallery for engineering and software projects, built with plain HTML, CSS, and JavaScript.

**Live preview:** https://craigxyz.github.io/portfolio/

The current site uses three clearly labeled fictional projects. About, experience, and resume content are placeholders. GitHub is the current contact destination. No backend or build step is required.

## Pages

- `index.html`: introduction, selected work, About, and Contact
- `projects.html`: sample projects with expandable briefs
- `experience.html`: experience and resume placeholders
- `404.html`: custom not-found page

Shared styles, the mobile-navigation script, and original SVG concept illustrations live in `assets/`. The site loads Space Grotesk and DM Sans from Google Fonts, with local system-font fallbacks.

## Edit and preview

Open `index.html` in a browser, or serve this directory locally:

```sh
python3 -m http.server 8000
```

Content is written directly in the HTML files. Update the shared navigation and footer in each page when changing them. Keep relative links compatible with the `/portfolio/` deployment path; the 404 page uses project-root paths for nested missing URLs.

## Deployment

GitHub Pages publishes the root of `main`. `.nojekyll` keeps the site as plain static files. Changes to `main` trigger publication.

The preview contains `noindex` metadata while the content is fictional. Remove it from the HTML pages when the real portfolio is ready. Add the actual biography, projects, experience, resume, and chosen contact details before treating this as a finished portfolio.

See [DESIGN_SPEC.md](DESIGN_SPEC.md) for the design direction and remaining decisions.
