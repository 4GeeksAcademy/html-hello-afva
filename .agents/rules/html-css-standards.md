
# HTML and CSS Development Standards

## Scope

Apply this rule whenever creating, modifying, or reviewing HTML or CSS files.

## Technology Restrictions

- Use HTML5 and CSS3 for the website.
- Do not introduce application-authored JavaScript or TypeScript. The Tailwind CSS v4 Browser CDN script documented in `README.md` is the only permitted executable JavaScript.
- Do not introduce frontend frameworks, external component libraries, backend application services, or build tools.
- The optional Tailwind CSS v4 Browser CDN and Flask local preview server are permitted only as documented in `README.md`; Flask is not part of the website.
- JSON-LD is permitted for Schema.org structured metadata.
- Keep HTML and CSS in separate files.

## HTML Standards

- Use valid HTML5 syntax and consistent indentation.
- Prefer semantic elements such as `header`, `nav`, `main`, `section`, `article`, and `footer`.
- Use one primary `h1` representing the page's main topic.
- Maintain a logical heading hierarchy without skipping levels unnecessarily.
- Use `a` for navigation and `button` for actions.
- Use `div` and `span` only when no more appropriate semantic element exists.
- Assign unique IDs to elements requiring identification.
- Use descriptive class names and meaningful content.

## CSS Standards

- Use external stylesheets.
- Prefer reusable classes over ID selectors for styling.
- Use CSS custom properties for repeated colors, spacing, and typography values.
- Use Flexbox for one-dimensional layouts and Grid for two-dimensional layouts.
- Prefer relative units such as `rem`, `%`, and `fr` where appropriate.
- Avoid unnecessary `!important`, excessive selector specificity, and duplicated declarations.
- Organize CSS by logical components or page sections.
- Do not introduce unnecessary animations or visual effects.

## Responsive Design

- Follow a mobile-first approach.
- Use media queries when the layout requires them.
- Prefer `min-height: 100svh` over fixed viewport heights for full-screen sections.
- Ensure content can expand without clipping or overflowing.
- Avoid unnecessary horizontal scrolling.
- Verify layouts at mobile, tablet, and desktop widths.

## Maintainability

- Follow existing naming conventions.
- Avoid unnecessary abstractions and premature optimization.
- Preserve existing functionality unless modifications are requested.
- Keep changes limited to the current task.
- Add comments only when they clarify non-obvious implementation decisions.

## Validation

Before reporting completion:

1. Check HTML syntax and nesting.
2. Verify semantic structure and heading hierarchy.
3. Check CSS syntax and selector consistency.
4. Verify internal links and asset paths.
5. Review responsive behavior.
6. Confirm that no prohibited technologies were introduced.

Report any checks that could not be performed.
