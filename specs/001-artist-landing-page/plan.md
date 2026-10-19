# Implementation Plan 001: Artist Landing Page

## 1. Architecture

Implement a static, single-page website using HTML5 and CSS3.

No build process, dependencies, or backend services are required.

## 2. Files

- `index.html`: Semantic page structure, content, metadata, and Schema.org JSON-LD.
- `styles.css`: Visual design, layout, responsiveness, and focus styles.

## 3. HTML Structure

Use the following document structure:

- `header`: Artist identity, without a primary navigation menu.
- `main`: Main website content.
  - Hero section.
  - About Me section.
  - Career section.

Use a native anchor link for skip-to-content; do not add a primary navigation menu or links to content sections.

## 4. CSS Strategy

- Mobile-first styling.
- CSS custom properties for colors, typography, and spacing.
- Flexbox and CSS Grid for layouts.
- Responsive media queries.
- `min-height: 100svh` for major sections where appropriate.
- Visible `:focus-visible` states.
- Respect reduced-motion preferences for optional animations.

## 5. Accessibility Strategy

- Semantic HTML before ARIA.
- Skip-to-content navigation.
- Logical reading order and heading hierarchy.
- Meaningful image alternatives.
- Keyboard-accessible skip-to-content link.
- Sufficient contrast and responsive text.

## 6. SEO Strategy

- HTML metadata in the document head.
- Appropriate heading structure.
- Descriptive section content.
- Schema.org JSON-LD using an appropriate artist entity type.
- No invented artist information or professional achievements.

## 7. Validation Strategy

Use the `website-audit` skill to review:

1. Project requirements.
2. HTML validity and semantics.
3. CSS validity and responsiveness.
4. Accessibility.
5. SEO metadata.
6. Schema.org JSON-LD.
7. Technology restrictions.

Document checks that could not be performed.

## 8. Implementation Constraints

Follow `AGENTS.md`, `CONTEXT.md`, and all applicable rules.

Use `create-web-section` for section implementation.

Do not introduce additional technologies or directories without approval.