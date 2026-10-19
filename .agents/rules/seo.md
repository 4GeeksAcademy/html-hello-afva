
# SEO and Structured Data Standards

## Scope

Apply this rule whenever creating, modifying, or reviewing page content, HTML structure, metadata, or Schema.org structured data.

## SEO Objectives

- Make the website understandable to search engines.
- Improve content discoverability and clarity.
- Use accurate, relevant, and descriptive metadata.
- Avoid manipulative or misleading optimization techniques.

## HTML Metadata

- Include a descriptive and unique `title` element.
- Include a relevant `meta name="description"` element.
- Declare the document language.
- Use UTF-8 character encoding.
- Include an appropriate viewport declaration.
- Keep metadata consistent with the visible page content.

## Semantic Structure

- Use semantic HTML5 elements.
- Maintain one clear primary `h1`.
- Organize content using logically nested headings.
- Use descriptive anchor text.
- Ensure important content is present in the HTML.
- Avoid unnecessary duplication of content.

## Content Quality

- Write clear, useful, and accurate content.
- Describe the artist's identity, work, and professional history.
- Use relevant terminology naturally.
- Avoid keyword stuffing.
- Do not invent artist biographies or professional achievements.
- Use clearly identified placeholders when factual information is unavailable.
- Keep published information consistent with the artist's actual details.

## Images

- Use descriptive filenames where practical.
- Provide appropriate alternative text based on image purpose.
- Specify image dimensions when available to reduce layout shifts.
- Optimize image file sizes without unnecessary quality loss.
- Avoid using images as the only source of important textual information.

## Schema.org Structured Data

- Use Schema.org vocabulary to describe relevant entities.
- Prefer JSON-LD for structured data.
- Include JSON-LD using `script type="application/ld+json"`.
- Do not include executable JavaScript.
- Select the most accurate Schema.org type for the artist.
- Use `Person` for an individual artist when appropriate.
- Ensure structured data accurately reflects the visible content.
- Do not fabricate names, URLs, or professional achievements.
- Avoid unsupported or irrelevant properties.

## Indexability

- Ensure any navigation or internal links required by `CONTEXT.md` use valid HTML anchors. The current project scope excludes a primary section-navigation menu.
- Verify that internal links reference existing section IDs.
- Avoid broken resource paths.
- Do not accidentally introduce `noindex` directives.
- Ensure essential content is accessible without JavaScript.
- Do not assume that valid metadata guarantees search engine indexing or ranking.

## Validation

Before reporting completion:

1. Verify the page title and meta description.
2. Review heading hierarchy.
3. Check internal links and resource paths.
4. Validate JSON-LD syntax.
5. Check Schema.org types and properties.
6. Verify consistency between structured data and visible content.
7. Confirm that no unsupported factual information was introduced.

When possible, use appropriate HTML and structured-data validation tools.

Report validation limitations and unresolved SEO issues.
