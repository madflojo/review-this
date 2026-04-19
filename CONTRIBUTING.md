# Contributing

Thanks for contributing to `review-this`.

This repository packages a focused review skill. Contributions should improve
clarity, scoring consistency, or actionable feedback quality without turning the
skill into a generic style guide or an essay generator.

## Good Contributions

Useful changes include:

- clarifying ambiguous scoring rules
- improving code or documentation review criteria
- tightening the output format or examples
- fixing links, grammar, or formatting
- improving examples so they are sharper and more realistic

## Before Opening a PR

Open an issue or start a discussion first if the proposed change would:

- materially change the review voice or intended audience
- alter the output contract significantly
- add a large amount of reference material
- broaden the scope beyond structured review work

Small fixes and focused improvements can go straight to a pull request.

## Contribution Guidelines

1. Keep the skill opinionated and practical.
2. Prefer concrete review guidance over vague principles.
3. Keep examples generic and reusable.
4. Update related docs when the scoring or output rules change.
5. Preserve the canonical skill name: `review-this`.

## Commit Messages and Releases

This repository uses Release Please to manage release PRs, tags, and GitHub
Releases from conventional commit history.

Prefer conventional commit prefixes:

- `feat:` for new capability or materially expanded guidance
- `fix:` for corrections to behavior, instructions, or examples
- `docs:` for documentation updates worth calling out in release notes
- `refactor:` for structural cleanup without changing repository behavior
- `ci:`, `build:`, `chore:`, and `test:` for maintenance work

The `metadata.version` field in `skills/review-this/SKILL.md` is informational.
Release Please treats repository tags as the canonical release version.

## Repository Structure

```text
skills/
  review-this/
    SKILL.md
    assets/
      review-template.md
    references/
      CODE-CRITERIA.md
      DOCS-CRITERIA.md
      OUTPUT.md
```

The repository-level docs, workflows, and release configuration exist only to
make the skill easier to publish and maintain.
