# Portfolio design specification

Version: 0.3 — published placeholder implementation, October 8, 2026

Status: placeholder implementation authorized for immediate GitHub Pages publication. The design remains open for refinement.

The owner requested a live dummy site using placeholder projects. This supersedes the earlier requirement to finish the specification before implementation. Fictional projects are explicitly labeled; biography, employment history, resume, and contact details remain unfilled until supplied.

## 1. Purpose

Showcase engineering projects and software development through a bold, expressive portfolio aimed at developer roles. Help hiring managers, engineers, and recruiters understand the problems I solve, inspect evidence of my work, review my experience, and contact me.

The details labeled **proposed** below are starting points for discussion, not approved design decisions. No biography, employment history, credentials, project results, or contact details should be invented. Fictional project concepts are permitted in the dummy site when clearly labeled.

## 2. Confirmed requirements

| Area | Requirement |
| --- | --- |
| About | An about me section |
| Work | A dedicated projects page |
| Background | Past experience and resume |
| Contact | A clear way to contact me |
| Stack | Plain HTML, CSS, and JavaScript |
| Architecture | Static site; no backend |
| Hosting | GitHub Pages |
| Process | Publish a dummy site now; continue refining design and content afterward |
| Purpose | Showcase creative work |
| Featured work | Engineering projects and software development |
| Audience and goal | Hiring teams considering me for developer roles |
| Visual character | Bold and expressive |
| Visual direction | Dark gallery: immersive imagery, dark background, luminous accents |

## 3. Proposed information architecture

Use three pages with shared navigation and a footer. Keep About and Contact on the home page so visitors can find the essential information quickly.

| Destination | Proposed location | Contents |
| --- | --- | --- |
| Home | `index.html` | Introduction, selected projects, about me, contact |
| About | Home page, `#about` | Background, interests, working style |
| Projects | `projects.html` | Curated project summaries and useful links |
| Experience | `experience.html` | Work history, relevant education, resume link |
| Contact | Home page, `#contact` | Email and selected professional profiles |

Navigation: name/home link, About, Projects, Experience, Contact. Cross-page section links must lead to the appropriate home-page anchor.

Separate project detail pages are optional. Add them only when the available material supports a meaningful case study. Separate About or Contact pages remain an open choice.

## 4. Proposed page layouts and content

### Home

1. **Header:** name or simple wordmark and navigation.
2. **Introduction:** an oversized statement about my engineering and software focus, my name, and a brief supporting line. Primary action: View projects. Secondary action: View experience, with a resume link when supplied. Keep Contact visible in the navigation. Final wording depends on the supplied content.
3. **Selected projects:** two or three representative projects with large imagery, each paired with a title, short description, my contribution, and a link. Give the strongest project the most visual space.
4. **About me:** two or three short paragraphs covering background, current interests, and what I enjoy working on. A portrait is optional.
5. **Contact:** a short invitation, a visible email link, and selected professional profiles. Availability statements appear only if supplied.
6. **Footer:** name and a small set of useful links.

### Projects

- Begin with a short introduction explaining what the collection represents.
- Show a curated set of projects, ordered by relevance to the intended audience.
- For each project, include title, problem or purpose, my role, approach or technologies, and outcome when supported by evidence.
- Add repository, live demo, publication, or case-study links when available. Omit missing links instead of using empty buttons.
- Use concise technology labels as supporting information, not the main story.
- Start with a visually varied grid: a prominent lead project followed by paired or full-width entries, based on the available assets. Preserve a clear reading order; filtering is unnecessary unless the collection becomes large enough to justify it.
- Only include work and assets selected for public presentation by the owner.

For developer-role applications, each project should make the following evidence easy to scan:

| Field | Content to collect |
| --- | --- |
| Problem | What needed to work, and for whom? |
| Contribution | What did I personally design, implement, or test? Distinguish individual work from team work. |
| Technical decisions | One or two meaningful architecture choices, constraints, or tradeoffs |
| Evidence | A working demo, repository, screenshot, hardware photo, architecture diagram, or test result |
| Outcome | What works now, what was learned, and any measured improvement supported by data |
| Stack | A short list of technologies actually used |

Keep the home-page summary to a title, a short problem-and-contribution statement, and one or two useful links. Put deeper technical context on the Projects page or an optional case-study page. For hardware or engineering work, show the actual system and explain how the software interacts with it. For software-only work, prefer a real interface, a clear architecture diagram, or a concise demonstration over a decorative code screenshot.

### Experience and resume

- Present roles in reverse chronological order.
- Each role includes title, organization, dates, and two to four concise contributions or achievements.
- Include relevant education, certifications, or skills only when supplied.
- Offer an accessible link to a PDF resume if one is provided; clearly identify its file type.
- Keep essential experience readable in HTML so the PDF is optional for visitors.
- Avoid publishing personal addresses, phone numbers, or other resume details unless intentionally chosen for the public site.

### Contact

- Use a standard email link and display the address as text.
- Include only the professional profiles the owner chooses to publish.
- Do not include a contact form in the initial scope; no message-delivery service is planned.

## 5. Proposed visual direction

Confirmed direction: a bold, expressive dark gallery with immersive imagery and luminous accents. Creative work is the centerpiece. Proposed execution: oversized typography above a large featured image, a near-black canvas, generous negative space, and a luminous lime accent. Let the projects supply most of the color and texture.

| Element | Starting proposal |
| --- | --- |
| Palette | Near-black background, warm-white primary text, muted sage-gray secondary text, luminous lime accent |
| Typography | Oversized, tightly composed display headings with a readable sans-serif body; consider one self-hosted, licensed display font |
| Content width | Approximately 1,280 px overall for imagery; long text limited to about 65–75 characters per line |
| Spacing | Consistent 8 px-based spacing scale; generous separation and deliberate changes in visual density |
| Project presentation | One large lead image followed by an asymmetric pair; visible captions below imagery; single-column reading order on phones |
| Imagery | Real project screenshots, artwork, or diagrams; preserve original aspect ratios or approve crops individually; optional portrait |
| Motion | Subtle image and link transitions; optional short entrance effects that never hide content or delay reading; respect reduced motion |
| Theme | Dark gallery throughout; no theme switch proposed for the first version |

Final colors, type choices, image treatment, and density should be agreed on before implementation. Any color combination must be checked for readable contrast.

The owner selected the dark gallery direction over the bright editorial alternative. The exact accent, typography, and composition below remain proposals for review.

### Proposed color and typography system

| Role | Proposed value | Usage |
| --- | --- | --- |
| Canvas | `#101211` | Main page background |
| Raised surface | `#1A1F1B` | Image backing and occasional grouped content |
| Primary text | `#F4F6EF` | Headings and body text |
| Secondary text | `#B3BAB0` | Dates, captions, project metadata |
| Accent | `#C9F75B` | Main call to action, link emphasis, focus indication |

Calculated contrast on the canvas: primary text 17.26:1, secondary text 9.46:1, and accent 15.17:1. These token checks do not replace checking the actual rendered components, especially text near project imagery.

- Hero heading: approximately 96–144 px on wide screens and 48–64 px on phones, scaled fluidly to avoid overflow.
- Section headings: approximately 40–64 px on desktop and 32–40 px on phones.
- Body text: 18 px with approximately 1.6 line height; captions no smaller than 14 px.
- Keep headings compact and body copy relaxed. Use a system sans-serif for the concept; choose a licensed display font only if it adds a distinctive voice.
- Keep text on solid backgrounds. Avoid text over busy artwork and avoid glow effects on paragraphs.

### Proposed composition

**Home:** compact header; large two-line introduction; one dominant featured-project image with its caption below; two supporting projects; a quieter About section; a large closing contact invitation. Keep the first featured work close enough to the introduction to establish the site's purpose without a full screen of empty space.

**Projects:** a short title and introduction followed immediately by the work. Let the first project span the content width, then vary the size of later entries when their assets justify it. Preserve a predictable reading order and always keep project title, role, and destination visible.

**Experience:** retain the same header, palette, and typography, but use a restrained list. On wider screens, put dates in a narrow left column and role details on the right. Stack dates above each role on phones. Place the optional resume link beside the page introduction.

Use roughly 64 px desktop side padding, 24 px on phones, and 16 px at very narrow widths. Aim for 96–144 px between major desktop sections and 64–80 px on phones. Treat these as layout targets, not fixed dimensions that should cause clipping.

### Image and interaction treatment

- Default the lead image frame to 16:10; use 4:3 for supporting images when suitable. Contain diagrams and interface screenshots that would lose meaning when cropped.
- If a project has no suitable image, use a deliberate text-led entry instead of unrelated stock art or fabricated screenshots.
- Keep image corners square or subtly rounded, with no heavy card shadows.
- Use a 160–220 ms transition for link and button states. Optional image movement should be small and disabled for reduced motion.
- Do not require carousels, custom cursors, parallax, animated backgrounds, or scroll-triggered reveals for the initial version.
- The concept preview uses labeled image and content placeholders. They communicate layout. The owner has authorized labeled fictional examples on the public dummy site; they must not be presented as completed real work.

## 6. Responsive behavior and interaction

- Design from narrow screens upward; all content must remain usable at a 320 px viewport without unintended horizontal scrolling.
- Use a single project column on phones and, where content allows, two columns on larger screens.
- Keep navigation visible when it fits; if a compact menu is needed, it must support keyboard use, expose its expanded state, and remain usable when JavaScript is unavailable.
- Use native links for navigation, projects, email, and resume access.
- Limit JavaScript to small enhancements. Reading the site and following core links must work without it.
- Avoid loading screens, scroll hijacking, autoplay media, and interaction that depends on hover alone.

## 7. Accessibility and content quality

- Aim for WCAG 2.2 AA accessibility, including sufficient contrast, visible focus, and keyboard navigation.
- Use semantic landmarks, one descriptive primary heading per page, and a logical heading hierarchy.
- Provide a skip link and indicate the current page in navigation.
- Give informative images useful alternative text; decorative images use empty alternative text.
- Use clear link labels, comfortable text sizes, and generous interaction targets.
- Respect reduced motion and browser zoom.
- Give each page a specific title and description. Add social-preview metadata after the public name, description, and image are chosen.
- Write in first person with concrete examples. Avoid unsupported impact claims and skill-rating bars.

## 8. Technical and hosting plan

- Write semantic HTML, shared CSS, and small vanilla JavaScript files. No framework, backend, or bundler is required.
- Keep content in HTML so essential information does not depend on client-side rendering.
- Use explicit HTML page links and relative asset paths compatible with a GitHub Pages project subdirectory.
- Proposed future structure: root HTML pages, `assets/css/`, `assets/js/`, `assets/images/`, and an optional `assets/documents/` for the resume.
- Optimize images for their display size, include dimensions to reduce layout movement, and defer below-the-fold images where appropriate.
- Avoid third-party scripts and analytics in the initial version.
- Publish the placeholder version to GitHub Pages from the root of the main branch. The owner explicitly authorized immediate deployment.
- A custom domain is optional and outside the initial setup.

## 9. Content needed from the owner

| Content | Needed for |
| --- | --- |
| Preferred public name and headline | Header, introduction, metadata |
| Target developer roles or specialism, if any | Project order and headline; general developer roles are already confirmed |
| Short biography and interests | About section |
| Selected projects, role, outcomes, links, and assets | Projects page and home-page highlights |
| Employment history and relevant education | Experience page |
| Current resume PDF, if desired | Resume link |
| Public email and selected profile links | Contact section |
| Optional portrait and visual references | Final visual direction |

## 10. Decisions for the next refinement

1. Are there specific developer roles to prioritize, such as frontend, backend, full-stack, embedded, or machine learning? General developer roles are confirmed.
2. Is viewing projects the right primary action, with experience/resume as the secondary action?
3. Does the proposed luminous lime accent and image-first composition fit the confirmed dark gallery direction? Are there reference sites to learn from?
4. Does the proposed three-page structure work, including About and Contact on the home page?
5. Which projects and experiences should be featured, and how much detail should each receive?
6. Should the first version include a portrait and downloadable resume? The proposed initial theme is dark only.

The dummy implementation is authorized. These decisions guide later refinement and do not block publishing the placeholder site.

## 11. Future completion criteria

These are acceptance criteria for the later build, not claims about the current repository.

- The approved visual direction and all four requested content areas are present.
- Final content comes from the owner; no placeholder biography, projects, or achievements remain.
- Pages work on small and large screens, with keyboard navigation and browser zoom.
- Core content and navigation work with JavaScript disabled.
- Project, contact, resume, and cross-page anchor links work.
- Assets and direct page URLs work under the actual GitHub Pages project path.
- Images are appropriately sized, and pages avoid unnecessary dependencies.
- The owner reviews the content and design before the placeholder version becomes the final portfolio.
