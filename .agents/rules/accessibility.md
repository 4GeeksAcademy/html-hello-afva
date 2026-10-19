
# Web Accessibility Standards

## Scope

Apply this rule whenever creating, modifying, or reviewing HTML, CSS, navigation, images, or interactive elements.

## Accessibility Objective

Follow WCAG 2.2 Level AA principles where applicable.

Prioritize accessibility through native HTML semantics before introducing ARIA attributes.

## Semantic Structure

- Declare the document language using the `lang` attribute.
- Use appropriate HTML5 semantic elements.
- Maintain a logical heading hierarchy.
- Ensure page content follows a meaningful reading order.
- Provide a clearly identifiable main content region.
- Include a skip-to-content link.

## Images and Multimedia

- Provide meaningful `alt` text for informative images.
- Use `alt=""` for purely decorative images.
- Avoid redundant descriptions such as "image of" unless necessary.
- Provide appropriate text alternatives for meaningful non-text content.
- Ensure essential information is not communicated exclusively through images.

## Keyboard Accessibility

- All interactive elements must be keyboard accessible.
- Preserve a logical tab order.
- Provide visible keyboard focus indicators using `:focus-visible`.
- Do not remove focus outlines without providing an accessible replacement.
- Avoid keyboard traps.
- Do not rely exclusively on hover interactions.
- Prefer native HTML controls.

## ARIA Usage

- Use ARIA only when native HTML cannot express the required semantics.
- Do not duplicate native HTML roles unnecessarily.
- Use `aria-label` when an interactive element lacks an appropriate accessible name.
- Prefer visible text labels whenever possible.
- Ensure ARIA attributes accurately represent the element's purpose and state.
- Do not use ARIA to compensate for incorrect HTML structure.
- Do not introduce ARIA-based custom interactions that require prohibited JavaScript.

## Visual Accessibility

- Maintain a minimum contrast ratio of 4.5:1 for normal text.
- Maintain a minimum contrast ratio of 3:1 for large text.
- Ensure relevant interface components and focus indicators have sufficient contrast.
- Do not rely on color alone to communicate meaning.
- Use readable typography and appropriate spacing.
- Support browser zoom and text resizing.
- Avoid content clipping or overlapping at narrow viewport widths.

## Navigation and Content

- Use descriptive link text.
- Make navigation labels understandable without surrounding context.
- Ensure internal anchor links lead to existing sections.
- Avoid unnecessary or confusing navigation patterns.
- Keep content understandable and logically organized.

## Validation

When applicable:

1. Test keyboard navigation using Tab and Shift+Tab.
2. Verify focus visibility.
3. Review heading hierarchy and semantic landmarks.
4. Check alternative text.
5. Verify color contrast.
6. Review the page at different viewport sizes and zoom levels.
7. Test with a screen reader when available.
8. Use automated accessibility tools when available.

Automated accessibility checks do not replace manual testing.

Never claim WCAG compliance solely because automated checks pass.

Report untested requirements and unresolved accessibility issues.
