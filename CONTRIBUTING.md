# Contributing

Thank you for helping improve GitHub Developer Assessor.

## What to contribute

Useful contributions include:

- Clearer evidence-collection guidance.
- Better scoring anchors that reduce subjective interpretation.
- Role-specific assessment criteria.
- Report-template improvements.
- Corrections that strengthen privacy, fairness, or attribution safeguards.

Keep the skill tool-agnostic and focused on publicly demonstrated engineering capability. Do not add instructions for accessing private data or inferring sensitive personal characteristics.

## Before submitting a change

1. Read `SKILL.md` and the files under `references/`.
2. Keep procedural instructions concise and imperative.
3. Put detailed scoring guidance in `references/rubric.md` and output structure in `references/report-template.md` instead of duplicating them in `SKILL.md`.
4. Preserve the distinction between missing evidence and negative evidence.
5. Ensure every new assessment claim can be supported by a public URL or is explicitly marked as unknown.
6. Update `CHANGELOG.md` for user-visible changes.

## Validation

Before proposing a change:

- Confirm that the YAML frontmatter in `SKILL.md` contains only `name` and `description`.
- Check that every referenced file exists and that relative links are correct.
- Review the full workflow for contradictions with the rubric and report template.
- Test the instructions against a public GitHub account when the change affects assessment behavior; do not publish personal or sensitive information in test artifacts.

If the Codex skill-creator utilities are available, run:

```text
quick_validate.py path/to/github-developer-assessor
```

## Change guidelines

- Make focused changes with a clear rationale.
- Avoid popularity metrics as proxies for engineering skill.
- Do not weaken the public-evidence, identity-uncertainty, or confidence requirements.
- Use neutral, evidence-first language.
- Do not commit generated reports containing unnecessary personal data.

By contributing, you agree that your contribution is licensed under the MIT License included in this repository.
