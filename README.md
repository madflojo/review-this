# review-this

An agent skill for producing structured reviews of code or documentation with
clear scores, concise rationale, and actionable improvement suggestions.

The canonical skill identifier is `review-this`. The repository is structured
so it can be installed directly with GitHub CLI or copied manually into an
agent skill directory.

## What the skill does

The `review-this` skill helps an agent:

- review code or docs with a consistent scorecard
- separate category ratings from overall judgment
- summarize strengths and weaknesses without hedging
- provide a quick checklist for scanability
- give concrete follow-up suggestions instead of vague advice

## Repository layout

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

The main prompt lives at `skills/review-this/SKILL.md`.
Supporting docs live under `references/`, and the structured review template
lives under `assets/`.

## Installing the skill

Primary path: install from GitHub CLI with `gh skill install`.

```bash
gh skill install madflojo/review-this
```

Optional: pin to a tag or commit for reproducible installs:

```bash
gh skill install madflojo/review-this@v1.0.0
gh skill install madflojo/review-this@<commit-sha>
```

Fallback path: manually copy `skills/review-this/` into either:

- `.agents/skills/` in a repository
- `~/.agents/skills/` for a user-level install

## Example output

This is the kind of review output the skill should generate:

```text
Category Ratings
- Code quality: 8/10
  Clear structure and naming, but a few branches still do too much at once.
- Maintainability: 6/10
  The code is workable, though tests and docs are thinner than they should be.

Overall Rating
- 7/10 🙂
  Solid foundation, but it still has a couple of sharp edges where future work
  could trip over its own shoelaces.

Checklist Summary
- ✅ Clear public API
- ⚠️ Test coverage is uneven
- ❌ No release or contribution docs

Suggestions for Improvement
- Split the larger functions into smaller reviewable units.
- Add tests for the failure paths the current code already hints at.
- Document the expected setup and contribution flow.
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution and release guidance.

## License

Licensed under [Apache-2.0](LICENSE).
