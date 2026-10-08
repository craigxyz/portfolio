# Portfolio design specification

Version: 0.1 — initial draft, October 8, 2026  
Status: open for discussion; implementation has not started.

## 1. Purpose

Showcase my creative work through a bold, expressive portfolio. Help visitors explore the work first, then understand who I am, review my experience, and contact me. The precise audience still needs to be chosen; the confirmed priority is presenting creative work.

The details labeled **proposed** below are starting points for discussion, not approved design decisions. No biography, employment history, credentials, project results, or contact details should be invented.

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
| Process | Refine the design specification before building |
| Purpose | Showcase creative work |
| Visual character | Bold and expressive |

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
2. **Introduction:** an oversized typographic statement about my creative focus, my name, and a brief supporting line. Primary action: Explore my work. Secondary action: Get in touch. Final wording depends on the supplied content.
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

Confirmed direction: bold and expressive, with creative work as the centerpiece. Proposed execution: an oversized typographic opening, high-contrast color, generous negative space, and large project imagery. Use varied composition to create personality while keeping the work easy to browse.

| Element | Starting proposal |
| --- | --- |
| Palette | Warm off-white and near-black with a vivid electric-violet accent; occasional large color fields |
| Typography | Oversized, tightly composed display headings with a readable sans-serif body; consider one self-hosted, licensed display font |
| Content width | Approximately 1,280 px overall for imagery; long text limited to about 65–75 characters per line |
| Spacing | Consistent 8 px-based spacing scale; generous separation and deliberate changes in visual density |
| Project presentation | Large images, prominent titles, and an asymmetric desktop composition that becomes a clear single column on phones |
| Imagery | Real project screenshots, artwork, or diagrams; preserve original aspect ratios or approve crops individually; optional portrait |
| Motion | Subtle image and link transitions; optional short entrance effects that never hide content or delay reading; respect reduced motion |
| Theme | One cohesive theme initially, with selective inverted sections; a theme switch remains optional |

Final colors, type choices, image treatment, and density should be agreed on before implementation. Any color combination must be checked for readable contrast.

Two variations to compare during refinement: an expressive editorial treatment with oversized type and an off-white canvas, or a darker gallery treatment with luminous accents and immersive imagery. The editorial treatment is the initial proposal. Reference sites and actual project assets will help make this choice concrete.

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
- Configure GitHub Pages only after implementation and review. The repository is being published now solely to collaborate on this specification.
- A custom domain is optional and outside the initial setup.

## 9. Content needed from the owner

| Content | Needed for |
| --- | --- |
| Preferred public name and headline | Header, introduction, metadata |
| Main audience and desired visitor action | Tone, project order, calls to action |
| Short biography and interests | About section |
| Selected projects, role, outcomes, links, and assets | Projects page and home-page highlights |
| Employment history and relevant education | Experience page |
| Current resume PDF, if desired | Resume link |
| Public email and selected profile links | Contact section |
| Optional portrait and visual references | Final visual direction |

## 10. Decisions to resolve before building

1. Within the creative-work focus, who is the primary audience: hiring teams, potential clients, collaborators, or another group?
2. Is exploring projects the right primary action, with contact as the secondary action?
3. Within the confirmed bold, expressive direction, should the visual treatment feel like an editorial portfolio or a darker gallery? Are there reference sites to learn from?
4. Does the proposed three-page structure work, including About and Contact on the home page?
5. Which projects and experiences should be featured, and how much detail should each receive?
6. Should the first version include a portrait, downloadable resume, or dark mode?

We can refine this document incrementally. Implementation begins after the owner agrees that the specification is ready.

## 11. Future completion criteria

These are acceptance criteria for the later build, not claims about the current repository.

- The approved visual direction and all four requested content areas are present.
- Final content comes from the owner; no placeholder biography, projects, or achievements remain.
- Pages work on small and large screens, with keyboard navigation and browser zoom.
- Core content and navigation work with JavaScript disabled.
- Project, contact, resume, and cross-page anchor links work.
- Assets and direct page URLs work under the actual GitHub Pages project path.
- Images are appropriately sized, and pages avoid unnecessary dependencies.
- The owner reviews the finished site before deployment.
