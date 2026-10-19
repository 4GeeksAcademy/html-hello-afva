# Specification 001: Artist Landing Page

## 1. Objective

Develop a professional, accessible, and search-engine-friendly single-page website for an artist.

The website must introduce the artist and present their professional career.

## 2. Functional Requirements

### FR-01: Website Structure

- The website must contain an `index.html` file.
- The website must use an external `styles.css` file.
- The HTML document must be valid HTML5.

### FR-02: Primary Navigation

Do not include a primary navigation menu or links to content sections. Include a native skip-to-content link to the main content for accessibility; this is the only permitted section-targeting link.

### FR-03: Website Sections

The page must include:

1. Welcome / Hero
2. About Me
3. Career

The Career section must present relevant professional experience, achievements, past exhibitions or performances, and significant milestones. Do not invent artist information or achievements.

Each main section should occupy approximately one desktop viewport height while allowing content to expand naturally.

### FR-04: Visual Design

- Use a coherent, modern visual design.
- Ensure responsive layouts for desktop, tablet, and mobile.
- Maintain readable typography and consistent spacing.
- Avoid horizontal overflow.

## 3. Accessibility Requirements

### AR-01: Semantic HTML

Use appropriate semantic HTML5 elements and a logical heading hierarchy.

### AR-02: Screen Reader Accessibility

- Provide meaningful alternative text for informative images.
- Provide an accessible name for the skip-to-content link.
- Declare the document language.
- Avoid unnecessary ARIA attributes.

### AR-03: Keyboard Accessibility

- Interactive elements, including the skip-to-content link, must be keyboard accessible.
- Keyboard focus must remain visible.
- Include a skip-to-content link.

### AR-04: Visual Accessibility

- Maintain sufficient text contrast.
- Support browser zoom and responsive text layouts.
- Do not communicate essential information through color alone.

## 4. SEO Requirements

### SEO-01: Metadata

Include:

- Page title.
- Meta description.
- Character encoding.
- Viewport metadata.
- Document language.

### SEO-02: Search-Friendly Structure

- Use semantic HTML.
- Maintain logical headings.
- Use descriptive link text.
- Keep important content available without JavaScript.

### SEO-03: Structured Data

- Implement Schema.org structured data using JSON-LD.
- Use an appropriate entity type for the artist.
- Ensure structured data matches the visible content.
- Do not fabricate artist information or professional achievements.

## 5. Technical Constraints

- Static single-page website implemented in HTML5 and CSS3.
- No application-authored JavaScript or TypeScript. The Tailwind CSS v4 Browser CDN script shown in `README.md` is the only permitted executable JavaScript.
- No frontend frameworks.
- No CSS frameworks other than the optional Tailwind CSS v4 Browser CDN documented in `README.md`.
- No backend application services, databases, or APIs. Flask may be used only as the local preview server documented in `README.md`.
- No external component libraries.
- No package managers or build systems, except the `pip3 install flask` command documented in `README.md` for local preview.
- JSON-LD is permitted for structured metadata.

## 6. Acceptance Criteria

- [ ] `index.html` exists and contains valid semantic HTML5.
- [ ] `styles.css` exists and is correctly linked.
- [ ] All three sections are present.
- [ ] No primary navigation menu or content-section links are present, except the required skip-to-content link.
- [ ] The skip-to-content link works.
- [ ] The layout is responsive.
- [ ] The website is usable with a keyboard.
- [ ] Informative images have appropriate alternative text.
- [ ] Heading hierarchy is logical.
- [ ] SEO metadata is included.
- [ ] Schema.org structured data is included and valid.
- [ ] No prohibited technologies are used.
- [ ] The website has been reviewed against the project accessibility requirements.

## 7. Out of Scope

- User authentication.
- Databases.
- Backend APIs.
- Application-authored JavaScript interactions.
- Content management systems.
- Online booking or payment functionality.