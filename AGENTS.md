
# Agent Guidance

**All AI agents working on this repository must follow these instructions before starting any task.**

## 1. Project Context

- Read `./README.md` and `./CONTEXT.md` to understand the repository's starter instructions and project requirements.
- Review the existing repository structure before proposing changes.
- Follow this source-of-truth order when documents conflict: `README.md`, then `CONTEXT.md`, then approved feature specifications, then these agent instructions, rules, and skills. Apply lower-level documents only where they do not conflict with higher-level requirements.
- Treat approved feature specifications as the source of feature-specific detail only when consistent with `README.md` and `CONTEXT.md`.
- Follow existing architectural conventions and naming conventions.
- Do not introduce functionality outside the approved project scope.

## 2. Technology Constraints

This project is a static, single-page artist portfolio website. Tooling documented in `README.md` permits optional Tailwind CSS v4 Browser CDN for presentation and Flask for local preview; neither adds website functionality.

### Allowed Technologies

- HTML5 for structure and content.
- CSS3 for styling, layout, and responsiveness.
- Schema.org JSON-LD for structured metadata.
- Optional Tailwind CSS v4 Browser CDN, as documented in `README.md`.
- Optional Flask local preview server, using the command documented in `README.md`; it is not part of the website.

### Prohibited Technologies

- Application JavaScript or TypeScript. The Tailwind CSS v4 Browser CDN script shown in `README.md` is the only permitted executable JavaScript.
- Frontend frameworks such as React, Vue, or Angular.
- CSS frameworks other than the optional Tailwind CSS v4 Browser CDN documented in `README.md`.
- Backend application services, databases, or APIs.
- External component libraries.
- Package managers or build systems, except the `pip3 install flask` command documented in `README.md` for optional local preview.

**Agents must not introduce prohibited technologies without explicit approval and an approved change to the project requirements. The optional README tooling does not add website functionality.**

## 3. Development Rules

Before modifying code:

1. Review `./.agents/rules/`.
2. Identify and apply all rules relevant to the task.
3. Follow existing project conventions.
4. Read the relevant directory's `README.md`, if present.
5. Review existing code before creating new implementations.

### Available Rules

- `./.agents/rules/html-css-standards.md`
  - HTML5 structure, CSS3 standards, responsiveness, and maintainability.

- `./.agents/rules/accessibility.md`
  - Accessibility, semantic HTML, keyboard navigation, and WCAG principles.

- `./.agents/rules/seo.md`
  - SEO metadata, semantic structure, and Schema.org structured data.

Rules define mandatory development standards.

Do not duplicate their detailed instructions in other files.

## 4. Agent Skills

Before executing a task:

1. Review `./.agents/skills/`.
2. Identify skills relevant to the requested work.
3. Follow their documented workflows.
4. Verify their acceptance criteria.

### Available Skills

#### create-web-section

Location:

`./.agents/skills/create-web-section/SKILL.md`

Purpose:

Create or modify website sections using semantic HTML5 and responsive CSS3 while preserving design consistency, accessibility, and SEO.

Use during website section development or significant modifications.

#### website-audit

Location:

`./.agents/skills/website-audit/SKILL.md`

Purpose:

Perform comprehensive quality assurance covering HTML, CSS, accessibility, responsiveness, SEO, Schema.org, and project requirements.

Use after significant changes or before final delivery.

The audit operates in read-only mode unless modifications are explicitly authorized.

## 5. Spec-Driven Development

All new features and significant functional or architectural changes must follow Spec-Driven Development (SDD).

Minor corrections that do not change functionality or architecture do not require a new specification.

### 5.1 Specification Structure

Store feature specifications under:

`./specs/<feature-id>/`

Each feature directory must contain:

- `spec.md`: Functional requirements, constraints, and acceptance criteria.
- `plan.md`: Technical approach, architecture, and implementation decisions.
- `tasks.md`: Ordered, verifiable implementation tasks.

Use descriptive feature identifiers.

Example:

`./specs/001-artist-landing-page/`

### 5.2 Specification Workflow

Follow this sequence:

1. **Specify**
   - Read project context and applicable rules.
   - Define functional and non-functional requirements.
   - Establish measurable acceptance criteria.
   - Identify missing information and assumptions.
   - Request approval of `spec.md`.

2. **Plan**
   - Define the technical implementation approach.
   - Identify files and components affected.
   - Document relevant architectural decisions.
   - Verify compatibility with project constraints.
   - Request approval of `plan.md`.

3. **Tasks**
   - Break the approved plan into small, actionable tasks.
   - Define verifiable completion criteria.
   - Order tasks according to dependencies.
   - Record them in `tasks.md`.

4. **Implement**
   - Execute approved tasks in order.
   - Apply relevant rules and skills.
   - Keep changes focused on the approved specification.
   - Mark tasks complete only after verification.

5. **Validate**
   - Perform relevant technical checks.
   - Run the `website-audit` skill before final delivery.
   - Compare results against specification acceptance criteria.
   - Document unresolved issues and validation limitations.

### 5.3 SDD Restrictions

- Do not begin feature implementation before `spec.md` and `plan.md` have been approved.
- Do not modify approved specifications without explicit authorization.
- Do not introduce functionality outside the approved specification.
- Do not treat assumptions as approved requirements.
- Do not mark tasks complete without verification.
- Do not create unnecessary specification documents.
- Stop and request clarification when requirements conflict or materially affect implementation.

### 5.4 Specification Changes

When an approved requirement changes:

1. Identify the affected specification.
2. Explain the proposed change and its impact.
3. Request approval.
4. Update the relevant specification documents.
5. Revise implementation tasks as necessary.
6. Continue implementation only after approval.

## 6. File and Directory Restrictions

Agents must respect the following restrictions.

### Protected Files

- Do not modify files explicitly marked as protected.
- Follow additional restrictions defined in applicable project rules.

### Out-of-Scope Changes

- Do not modify unrelated files.
- Do not perform unrelated refactoring.
- Avoid unnecessary file creation.

### Sensitive Files

- Do not access, modify, or expose secrets, credentials, or sensitive configurations without explicit authorization.

### Critical Configurations

- Request approval before modifying deployment, infrastructure, or security configurations.

### Project Structure

- Do not create, rename, move, or delete top-level directories without explicit approval.
- The `./specs/` directory is explicitly approved for SDD documentation.
- Agents may create feature-specific subdirectories within `./specs/`.
- Agents may update specification documents according to the approved SDD workflow.
- Do not reorganize the repository without approval.

### Project Documentation

- Do not modify fundamental requirements in `CONTEXT.md` without approval.
- Do not modify `AGENTS.md`, agent rules, or skills unless explicitly requested.

## 7. Development Workflow

Before implementation:

1. Read `AGENTS.md` and `CONTEXT.md`.
2. Review applicable rules and skills.
3. Determine whether the task requires SDD.
4. If required, review the approved specification, plan, and tasks.
5. Inspect existing source files.
6. Identify the minimum changes necessary.

During implementation:

1. Follow the approved technical plan.
2. Implement one logical task at a time.
3. Preserve existing functionality.
4. Maintain semantic HTML, accessibility, and responsive design.
5. Avoid unnecessary complexity.
6. Update task status only after verification.

After implementation:

1. Review changes against requirements.
2. Run relevant validation checks.
3. Verify that no prohibited technologies were introduced.
4. Run the website audit when required.
5. Report validation results and unresolved issues.
6. Commit changes only when explicitly requested.

## 8. Validation and Quality Assurance

Agents must perform checks appropriate to the changes made.

### HTML

- Validate HTML syntax and nesting.
- Review semantic structure and heading hierarchy.
- Verify internal links required by `CONTEXT.md` and the approved specification, including the skip-to-content link.
- Check image and stylesheet paths.

### CSS

- Validate CSS syntax.
- Review responsive behavior.
- Check for horizontal overflow or clipped content.
- Verify consistency with existing design conventions.

### Accessibility

- Review keyboard navigation.
- Verify visible focus indicators.
- Check alternative text and accessible names.
- Review contrast and reading order.
- Test with accessibility tools when available.

### SEO

- Verify metadata.
- Review semantic headings and content.
- Validate JSON-LD syntax.
- Verify Schema.org consistency with visible content.

### Reporting

Use the following validation statuses:

- **PASS:** Successfully verified.
- **FAIL:** A verified issue exists.
- **NOT VERIFIED:** Validation could not be performed.

Never claim that a test was executed unless it was actually performed.

Automated checks do not replace manual accessibility or visual testing.

## 9. Documentation

- Keep documentation concise, accurate, and relevant.
- Avoid duplicating information across files.
- Update `tasks.md` as implementation progresses.
- Keep specifications consistent with approved requirements.
- Document significant implementation decisions when necessary.
- Do not introduce a memory bank unless project complexity justifies it.

### Documentation Responsibilities

- `CONTEXT.md`: Project objectives, scope, and constraints.
- `AGENTS.md`: Agent operating instructions.
- `.agents/rules/`: Mandatory development standards.
- `.agents/skills/`: Reusable operational workflows.
- `specs/`: Feature requirements, plans, and implementation tasks.

## 10. Git and Version Control

- Keep changes focused on the current task.
- Review modified files before committing.
- Use clear, meaningful commit messages.
- Do not commit automatically.
- Commit only when explicitly requested and after required validation.
- Never commit credentials, secrets, or temporary files.
- Do not rewrite Git history without explicit authorization.

## 11. Clarification and Escalation

Stop and request clarification when:

- Requirements are ambiguous and materially affect implementation.
- Instructions conflict.
- A significant architectural decision requires approval.
- A requested change violates technology restrictions.
- An approved specification must be modified.
- A protected file or restricted directory must be changed.
- Mandatory validation fails and cannot be resolved.
- Essential information is missing.

Do not silently make significant decisions on behalf of the user.

## 12. Core Principles

1. **Specification first:** Agree on requirements before implementation.
2. **Simplicity:** Implement the smallest solution that satisfies the requirements.
3. **Consistency:** Follow existing architecture, rules, and conventions.
4. **Accessibility:** Build accessible interfaces from the beginning.
5. **Maintainability:** Prefer readable, reusable code over unnecessary complexity.
6. **Traceability:** Link implementation work to approved requirements and tasks.
7. **Verification:** Report only checks that were actually performed.
8. **Controlled changes:** Respect scope, approval requirements, and repository restrictions.

**Build only what has been specified, validate what has been implemented, and report what remains unresolved.**
