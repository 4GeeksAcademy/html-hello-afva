
# Project Context: Artist Portfolio Website

## 1. Project Overview

**Project Name:** Artist Portfolio Website  
**Project Type:** Static, single-page website  
**Development Stage:** Minimum Viable Product (MVP)  
**Methodology:** Spec-Driven Development (SDD)  
**Purpose:** Educational project for the 4Geeks AI Engineering course.

The project consists of developing a professional, visually attractive, accessible, and search-engine-friendly landing page for an artist.

The website will introduce the artist and present their professional career.

The implementation must remain simple, maintainable, and understandable while following professional web development standards.

## 2. Business Objectives

The website must:

- Establish an online presence for the artist.
- Communicate the artist's identity and creative work.
- Present their professional background and achievements.
- Present the required sections in a clear reading order.
- Be accessible to users with visual impairments.
- Improve discoverability through SEO and structured data.
- Provide a consistent experience across desktop and mobile devices.

## 3. Target Audience

The website is intended for:

- People interested in the artist and their work.
- Potential collaborators.
- Visitors using assistive technologies.
- Search engines indexing information about the artist.

## 4. Functional Scope

### 4.1 Navigation

Do not include a primary navigation menu or links to content sections. Include a skip-to-content link to the main content for accessibility; this is the only permitted section-targeting link.

### 4.2 Hero Section

The initial section must:

- Introduce the artist.
- Display the artist's name and artistic discipline.
- Include a welcoming headline.
- Provide an attractive visual introduction.
- Encourage visitors to explore the website.

### 4.3 About Me

Present the artist's:

- Biography.
- Background.
- Artistic interests.
- Creative identity.

### 4.4 Career

Present relevant information about:

- Professional experience.
- Artistic achievements.
- Exhibitions or performances.
- Significant career milestones.

## 5. Technology Stack

### Allowed Technologies

- **HTML5:** Structure, semantic content, accessibility, and metadata.
- **CSS3:** Styling, layout, responsiveness, and visual presentation.
- **Schema.org JSON-LD:** Structured metadata describing the artist.
- **Tailwind CSS v4 Browser CDN:** Optional, as documented in `README.md`.
- **Flask:** Local preview server, using the command documented in `README.md`; it is not part of the website.

### Prohibited Technologies

- Application JavaScript or TypeScript. The Tailwind CSS v4 Browser CDN script shown in `README.md` is the only permitted executable JavaScript.
- Frontend frameworks such as React, Vue, or Angular.
- CSS frameworks other than the optional Tailwind CSS v4 Browser CDN documented in `README.md`.
- Backend services or functionality in the delivered website.
- Databases.
- APIs.
- External component libraries.
- Package managers or build tools, except the `pip3 install flask` command documented in `README.md` for local preview.

**Critical constraint:** The delivered website remains a static single-page site. README tooling is limited to optional Tailwind CSS for presentation and Flask for local preview; neither adds backend functionality to the delivered website.

JSON-LD is permitted for structured metadata. Do not add application-authored executable JavaScript.

## 6. Design Requirements

The website must follow these principles:

- Modern, professional, artistic visual identity.
- Consistent colors, typography, and spacing.
- Clear visual hierarchy.
- Responsive design for mobile, tablet, and desktop.
- Approximately one viewport height per main section on desktop.
- Content must remain readable when it exceeds the viewport height.
- No unnecessary visual complexity.
- No horizontal overflow.

Prefer `min-height: 100svh` over fixed heights when implementing full-screen sections.

The final color palette, typography, and visual assets will be defined during the design and implementation process.

## 7. Accessibility Requirements

The website must follow applicable WCAG 2.2 Level AA principles.

### Semantic HTML

Use appropriate HTML5 elements:

- `header`
- `main`
- `section`
- `article`, where appropriate

Maintain a logical heading hierarchy.

### Screen Reader Accessibility

- Declare the document language.
- Provide meaningful alternative text for informative images.
- Use empty alternative text for decorative images.
- Provide accessible names for interactive elements.
- Use ARIA attributes only when native HTML is insufficient.

### Keyboard Accessibility

- Ensure the skip-to-content link is keyboard accessible.
- Provide visible focus indicators.
- Include a skip-to-content link.
- Avoid keyboard traps.

### Visual Accessibility

- Maintain sufficient text contrast.
- Use readable font sizes.
- Support browser zoom.
- Avoid communicating essential information exclusively through color.
- Prevent content clipping and overlapping.

Accessibility must be considered during development, not added afterward.

## 8. SEO Requirements

Implement foundational on-page SEO.

### Metadata

Include:

- Descriptive page title.
- Relevant meta description.
- Character encoding.
- Viewport metadata.
- Document language.

### Semantic Structure

- Use semantic HTML5.
- Maintain a logical heading hierarchy.
- Use descriptive link text.
- Ensure essential content is available without JavaScript.

### Structured Data

Implement Schema.org structured data using JSON-LD.

- Use an appropriate entity type for the artist.
- Use `Person` when applicable.
- Ensure structured data matches visible page content.
- Do not fabricate names or professional achievements.

## 9. Project Architecture

The project uses a static frontend architecture.

### Source Files

- `index.html`: HTML structure, content, metadata, and JSON-LD.
- `styles.css`: Styling, responsive layout, and visual accessibility.

### Agent Configuration

- `AGENTS.md`: Agent operating instructions.
- `.agents/rules/`: Mandatory development standards.
- `.agents/skills/`: Reusable development and validation workflows.

### Specifications

- `specs/`: Feature-specific requirements, technical plans, and implementation tasks.

No backend, database, or application framework is required.

## 10. Development Methodology

The project follows Spec-Driven Development (SDD).

### Stage 1: Specification

Define:

- Functional requirements.
- Non-functional requirements.
- Technical constraints.
- Acceptance criteria.

Document them in `spec.md`.

### Stage 2: Planning

Define:

- Technical implementation approach.
- Files affected.
- Design and architectural decisions.
- Validation strategy.

Document them in `plan.md`.

### Stage 3: Task Definition

Break the implementation into ordered, verifiable tasks.

Document them in `tasks.md`.

### Stage 4: Implementation

Implement approved tasks using the applicable development rules and skills.

### Stage 5: Validation

Validate the implementation against the approved specification.

Use the `website-audit` skill before final delivery.

Approved specifications must not be modified without authorization.

## 11. Project Structure

```text
artist-portfolio/
├── AGENTS.md
├── CONTEXT.md
├── index.html
├── styles.css
├── specs/
│   └── 001-artist-landing-page/
│       ├── spec.md
│       ├── plan.md
│       └── tasks.md
└── .agents/
    ├── rules/
    │   ├── html-css-standards.md
    │   ├── accessibility.md
    │   └── seo.md
    └── skills/
        ├── create-web-section/
        │   └── SKILL.md
        └── website-audit/
            └── SKILL.md
```

This structure represents the intended project organization.

Files and directories may be created progressively as their corresponding tasks are approved.

## 12. Development Principles

1. **Simplicity:** Avoid unnecessary complexity.
2. **Maintainability:** Write readable, organized code.
3. **Separation of concerns:** HTML defines structure; CSS defines presentation.
4. **Accessibility first:** Include accessibility from the beginning.
5. **Responsive design:** Support different screen sizes.
6. **SEO by design:** Apply semantic structure and metadata.
7. **Specification first:** Implement only approved requirements.
8. **Traceability:** Link implementation tasks to specifications.
9. **Verification:** Report only checks actually performed.
10. **No invented information:** Clearly identify missing artist content.

## 13. Acceptance Criteria

The MVP is complete when:

- [ ] `index.html` exists and contains valid HTML5.
- [ ] `styles.css` exists and is correctly linked.
- [ ] The Hero section is implemented.
- [ ] The About Me section is implemented.
- [ ] The Career section is implemented.
- [ ] No primary navigation menu is included.
- [ ] The skip-to-content link works correctly.
- [ ] Semantic HTML is used appropriately.
- [ ] Heading hierarchy is logical.
- [ ] The website is responsive.
- [ ] Keyboard navigation is supported.
- [ ] Focus indicators are visible.
- [ ] Informative images have appropriate alternative text.
- [ ] SEO metadata is included.
- [ ] Schema.org structured data is implemented.
- [ ] No prohibited technologies are introduced.
- [ ] The website has been reviewed for accessibility.
- [ ] The implementation satisfies the approved specification.
- [ ] Final validation results are documented.

## 14. Out of Scope

The initial version does not include:

- User authentication.
- Backend development.
- Database integration.
- Content management systems.
- Online payments.
- Booking systems.
- Executable JavaScript interactions.
- Advanced animations requiring JavaScript.
- External APIs.

Future features require separate approval and specifications.

## 15. Current Project Status

**Phase:** Specification and planning.

**Current objective:** Define and approve the initial landing-page specification before implementation.

**Initial feature:** `001-artist-landing-page`

**Next milestone:** Approve `spec.md` and `plan.md`, then execute the implementation tasks.

## 16. Project Guiding Principle

Build the simplest professional website that satisfies the artist's requirements and the educational assignment.

Prioritize accessibility, semantic HTML, maintainable CSS, SEO, and clear specifications over unnecessary technical complexity.
