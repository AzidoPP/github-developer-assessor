# GitHub Developer Assessor Skill

A tool-agnostic Agent Skill for assessing the engineering capability publicly demonstrated by a GitHub account.

It uses inspectable code, contribution history, reviews, issues, releases, and maintenance activity. It treats popularity and activity metrics as navigation signals rather than proof of skill, and it keeps evidence confidence separate from the assessment itself.

## Files

- `SKILL.md` — complete instructions and workflow.
- `references/rubric.md` — detailed scoring anchors.
- `references/report-template.md` — reusable assessment output template.
- `CONTRIBUTING.md` — contribution and validation guidance.
- `CHANGELOG.md` — release history.
- `LICENSE` — MIT License.

## Installation

Copy the `github-developer-assessor` directory into the skills directory used by your agent framework, or load `SKILL.md` as an instruction resource.

## Example invocation

> Assess `https://github.com/example` for a senior backend role. Use standard depth, focus on the last 24 months, inspect organization contributions, and cite the strongest evidence.

## Recommended capabilities

The agent works best when it can:

- Browse GitHub pages.
- Search repositories, commits, issues, pull requests, and reviews.
- Read source files and diffs.
- Optionally use the GitHub API or GitHub CLI.

It remains usable without API access, but confidence may be lower.

## Scope and privacy

The skill evaluates public GitHub evidence only. It does not attempt to access private data, infer sensitive personal characteristics, or treat missing public work as evidence of weak engineering ability.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) before proposing changes. Keep the workflow evidence-first, role-aware, and explicit about uncertainty.

## License

MIT License. Copyright (c) 2026 Minsecrus. See [LICENSE](LICENSE).
