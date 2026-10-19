
---
name: create-web-section
description: Creates or modifies sections of the artist portfolio website using semantic HTML5 and responsive CSS3, following project requirements, accessibility standards, and SEO rules.
---

# Create Web Section

## Objective

Create or modify a website section while preserving the existing design, structure, functionality, and technical constraints.

Produce clean, accessible, responsive, and maintainable HTML and CSS without introducing unnecessary complexity.

## When to Use

Use this skill when:

- Creating a new website section.
- Modifying the structure or layout of an existing section.
- Implementing a hero, biography, or career section.
- Improving the responsive design of a section.
- Refactoring the HTML or CSS of an existing section.

Do not use this skill for documentation-only changes or full website audits.

## Prerequisites

Before implementation:

1. Read `CONTEXT.md` and `AGENTS.md`.
2. Review the existing `index.html` and `styles.css`.
3. Apply the relevant rules:
   - `.agents/rules/html-css-standards.md`
   - `.agents/rules/accessibility.md`
   - `.agents/rules/seo.md`
4. Identify the requested section and its requirements.
5. Review existing CSS variables, naming conventions, and reusable styles.

Do not modify unrelated sections.

## Workflow

### Step 1: Analyze Requirements

- Identify the section's purpose and expected content.
- Determine its position within the website.
- Identify required internal links and section IDs from `CONTEXT.md` and the approved specification. The current scope excludes a primary navigation menu.
- Check whether required content and assets are available.
- Use clearly marked placeholders for missing information.
- Request clarification when essential requirements are ambiguous.

### Step 2: Design the HTML Structure

- Select appropriate semantic HTML5 elements.
- Maintain a logical heading hierarchy.
- Use unique IDs for sections.
- Ensure meaningful reading order.
- Use descriptive link text and appropriate image alternatives.
- Prefer native HTML semantics over unnecessary ARIA attributes.

Do not introduce application-authored JavaScript. The optional Tailwind CSS v4 Browser CDN script documented in `README.md` is the only permitted executable JavaScript.

### Step 3: Implement CSS

- Reuse existing design tokens and CSS conventions.
- Follow a mobile-first approach.
- Use Flexbox or CSS Grid where appropriate.
- Maintain consistent typography, colors, and spacing.
- Use `min-height: 100svh` for full-screen sections when appropriate.
- Allow content to expand naturally.
- Avoid unnecessary animations, duplicated styles, and `!important`.

### Step 4: Integrate the Section

- Add or modify the section in `index.html`.
- Add the required styles in `styles.css`.
- Update internal links only when required by `CONTEXT.md` or the approved specification. The current page has no primary navigation menu.
- Preserve existing functionality and visual consistency.
- Update SEO metadata or structured data only when affected by the change.
- Do not introduce dependencies or frameworks beyond the optional Tailwind CSS v4 Browser CDN documented in `README.md`.

### Step 5: Validate

Perform the relevant checks:

1. Verify HTML syntax and semantic structure.
2. Check heading hierarchy and unique IDs.
3. Verify internal links and asset paths.
4. Check CSS syntax and responsive behavior.
5. Review keyboard accessibility and focus visibility.
6. Verify appropriate alternative text.
7. Check for horizontal overflow or clipped content.
8. Confirm compliance with technology restrictions.

Use available validation tools when possible.

Do not claim a check passed unless it was actually performed.

### Step 6: Report Results

Provide a concise implementation summary containing:

- Section created or modified.
- Files changed.
- Main implementation decisions.
- Validation checks performed and their results.
- Outstanding issues or checks not performed.

Do not automatically commit changes unless explicitly requested.

## Acceptance Criteria

The task is complete when:

- [ ] The section satisfies the requested requirements.
- [ ] HTML5 semantic structure is appropriate.
- [ ] CSS is organized and maintainable.
- [ ] The design is consistent with existing sections.
- [ ] The layout adapts to different viewport sizes.
- [ ] Accessibility requirements are addressed.
- [ ] Required internal links, including skip-to-content, work correctly.
- [ ] Relevant SEO requirements are preserved.
- [ ] No application-authored JavaScript or prohibited frameworks are introduced.
- [ ] Existing functionality remains intact.
- [ ] Validation results and limitations are reported.

## Constraints

- Modify only files relevant to the task.
- Do not introduce unnecessary abstractions.
- Do not invent artist information.
- Do not create new top-level directories without approval.
- Do not modify project requirements without approval.
- Do not add dependencies, build tools, or backend functionality.
- Follow existing project conventions.

## Guiding Principle

Implement the smallest professional solution that satisfies the requirements while maintaining accessibility, responsiveness, and code quality.
