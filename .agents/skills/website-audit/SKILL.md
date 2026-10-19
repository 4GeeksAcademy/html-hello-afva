
---
name: website-audit
description: Audits a static HTML and CSS website for code quality, accessibility, responsiveness, SEO, Schema.org structured data, and compliance with project requirements. Use after significant changes or before delivery.
---

# Website Audit

## Objective

Perform a systematic quality assurance review of the website to identify technical errors, accessibility issues, SEO problems, and deviations from project requirements.

Produce an actionable audit report without modifying the website unless explicitly authorized.

## When to Use

Use this skill when:

- Reviewing the complete website before delivery.
- Validating a significant implementation milestone.
- Checking compliance with the project acceptance criteria.
- Investigating accessibility, responsiveness, or SEO issues.
- Performing a comprehensive quality review after major changes.

Do not use this skill for routine development or minor CSS changes.

## Prerequisites

Before starting:

1. Read `AGENTS.md` and `CONTEXT.md`.
2. Review the existing project structure.
3. Read the relevant source files, including `index.html` and `styles.css`.
4. Apply the relevant rules:
   - `.agents/rules/html-css-standards.md`
   - `.agents/rules/accessibility.md`
   - `.agents/rules/seo.md`
5. Identify the project's acceptance criteria and technology restrictions.

## Workflow

### Step 1: Validate Project Requirements

Compare the implementation against `CONTEXT.md`.

Verify:

- All required website sections exist.
- No primary navigation menu is present, as required; the skip-to-content link targets the main content.
- The hero section introduces the artist.
- About Me and Career are implemented.
- Main sections occupy approximately one viewport height on desktop.
- The design is visually consistent.
- Missing artist information is clearly identified as placeholder content.
- No functionality outside the approved scope has been introduced.

### Step 2: Audit HTML

Check:

- Valid HTML5 syntax and element nesting.
- Correct document structure.
- Appropriate semantic elements.
- Logical heading hierarchy.
- One primary `h1`.
- Unique element IDs.
- Descriptive links.
- Correct internal anchor references required by `CONTEXT.md` and the approved specification, including skip-to-content; do not expect section-navigation links.
- Valid image and stylesheet paths.
- Appropriate document language.

Use an HTML validator when available.

### Step 3: Audit CSS and Responsiveness

Check:

- Valid CSS syntax.
- Consistent naming conventions.
- Reusable styles and design tokens.
- Absence of unnecessary duplicated declarations.
- Appropriate use of Flexbox and Grid.
- Mobile-first responsive behavior.
- Readability at mobile, tablet, and desktop widths.
- No unintended horizontal scrolling.
- No clipped or overlapping content.
- Full-screen sections allow content to expand naturally.
- No unnecessary `!important` declarations.

Use browser inspection or automated tools when available.

### Step 4: Audit Accessibility

Evaluate applicable WCAG 2.2 Level AA requirements.

Check:

- Semantic landmarks and reading order.
- Logical heading hierarchy.
- Meaningful alternative text.
- Accessible names for interactive elements.
- Keyboard navigation.
- Visible focus indicators.
- Skip-to-content functionality.
- Sufficient text and interface contrast.
- Readability under zoom and text resizing.
- Appropriate ARIA usage.
- No essential functionality dependent exclusively on hover.
- No information conveyed exclusively through color.

Use automated accessibility tools when available.

Perform manual keyboard and screen-reader testing when the environment supports it.

Do not claim full WCAG compliance based solely on automated checks.

### Step 5: Audit SEO

Check:

- Descriptive page title.
- Relevant meta description.
- Correct document language.
- Appropriate heading hierarchy.
- Semantic HTML.
- Descriptive internal links.
- Meaningful image alternative text.
- Valid internal links, including the skip-to-content target.
- Absence of accidental `noindex` directives.
- Availability of essential content without JavaScript.

Do not make unsupported claims about search engine rankings or indexing.

### Step 6: Audit Schema.org

Check:

- JSON-LD is syntactically valid JSON.
- Schema.org types and properties are appropriate.
- Structured data accurately represents the artist.
- Structured data is consistent with visible page content.
- No fabricated information is included.
- JSON-LD contains no executable JavaScript.

Use a structured-data validator when available.

### Step 7: Verify Technology Restrictions

Confirm that:

- The delivered site is a static HTML5 and CSS3 single page.
- No application-authored JavaScript or TypeScript is present. The optional Tailwind CSS v4 Browser CDN script documented in `README.md` is permitted.
- No frontend frameworks or CSS frameworks other than the optional Tailwind CSS v4 Browser CDN documented in `README.md` are used.
- No external component libraries are introduced.
- No backend application services, databases, or APIs are used. Flask is limited to the README's local preview server.
- No package managers or build tools are used, except the README's `pip3 install flask` command for local preview.
- HTML and CSS remain in separate files.

JSON-LD is permitted for structured metadata.

### Step 8: Classify Findings

Classify each finding using the following severity levels:

- **Critical:** Prevents essential functionality or violates a mandatory project constraint.
- **High:** Significant accessibility, functionality, or usability problem.
- **Medium:** Important quality, responsiveness, SEO, or maintainability issue.
- **Low:** Minor inconsistency or improvement opportunity.

For each finding, record:

- Severity.
- Affected file and location.
- Description of the issue.
- Requirement or rule affected.
- Recommended corrective action.

Avoid reporting subjective design preferences as technical failures.

### Step 9: Produce Audit Report

Provide a concise report containing:

#### Executive Summary

- Overall assessment.
- Number of findings by severity.
- Most important issues.
- Readiness for delivery.

#### Validation Results

For each audit category, report one of:

- **PASS:** Checks were performed successfully.
- **FAIL:** One or more verified issues were identified.
- **NOT VERIFIED:** Required validation could not be performed.

#### Findings

Present issues in descending order of severity.

#### Recommended Actions

Prioritize corrections that affect mandatory requirements, functionality, accessibility, and usability.

#### Validation Limitations

Explicitly identify checks that were not performed and explain why.

## Acceptance Criteria

The audit is complete when:

- [ ] Project requirements have been reviewed.
- [ ] HTML structure and semantics have been assessed.
- [ ] CSS quality and responsiveness have been assessed.
- [ ] Accessibility requirements have been reviewed.
- [ ] SEO metadata has been checked.
- [ ] Schema.org structured data has been reviewed.
- [ ] Technology restrictions have been verified.
- [ ] Findings have been classified by severity.
- [ ] Actionable recommendations have been provided.
- [ ] Validation limitations have been documented.
- [ ] No source files have been modified without authorization.

## Constraints

- Operate in read-only mode by default.
- Do not automatically fix identified issues.
- Do not modify project requirements.
- Do not introduce dependencies or frameworks.
- Do not invent test results.
- Do not claim visual, browser, or screen-reader testing without performing it.
- Do not mark untested requirements as passed.
- Do not create commits unless explicitly requested.

## Guiding Principle

Provide an evidence-based, reproducible, and actionable assessment of website quality.

Prioritize verified problems over speculative improvements.
