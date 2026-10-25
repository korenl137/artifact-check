# Contributing

Keep this repository focused on inspecting and correcting user-facing deliverables.
The skill's executable instructions belong in `skills/artifact-check/SKILL.md`; user-facing usage belongs in README.md.
Do not add format-specific engines, mandatory sibling skills, hooks or a shared runtime without a demonstrated need.

## Preserve the contract

- Keep formats open and the selected artifact scope explicit.
- Treat invocation as permission to correct within the user's existing authorization.
- Preserve accepted design decisions and unrelated user work.
- Inspect the actual output and distinguish verified results from unavailable checks.
- Use the current agent by default and stop after relevant corrections and focused rechecks.
- Keep code-only review, task closeout and guidance improvement with their existing workflows.

Keep each skill self-contained and write its instructions in English, including concise Korean invocation examples.
Update the version and affected scenario expectations before changing behavior; retain at least three realistic cases.
Add scripts or references only when they remove concrete repeated work or improve reliability.

## Validate

Use the current agent product's available skill-authoring validator on `skills/artifact-check`.
Check that the JSON scenarios parse and inspect all local Markdown links.
Run `git diff --check` and `git diff --cached --check` when staging.
Review untracked files separately because normal diffs omit them.

Exercise a representative artifact when behavior changes warrant it, using disposable fixtures rather than private user data.
Record the request, observed defect, correction, recheck and limits in the change's validation report.
Separate manual scenario review, current-agent execution and independent model evaluation.
Do not run additional paid model evaluations without authorization.

## Publish

Keep changes scoped, preserve existing authorship, and disclose AI assistance where applicable.
Use short imperative commit subjects.
Commits, publication, catalog registration and installation are separate actions governed by the user's authorization.
