# Artifact Check

An agent skill that checks a user-facing deliverable against the original request and applicable instructions, fixes problems, and verifies the result.
Invoking it is a correction request: the agent makes supported fixes and reports the outcome rather than stopping at an issue list.

## Use

Ask your agent:

- "Check the slides you just made against my request and fix any issues."
- "결과물 점검해줘."
- "이 페이지가 요청대로 만들어졌는지 확인하고 고쳐줘."

An artifact is a deliverable the user directly reads, views, interacts with or uses.
Documents, slides, images, tables and webpages are examples, not a format whitelist.
The agent uses the artifact you identify, or the clear recent deliverable in the conversation.
It asks only when the target or an outcome-changing decision remains ambiguous.

The review focuses on requested content, presentation and intended use.
It preserves the approved direction, corrects problems, and rechecks the affected result.
It does not turn into an unsolicited redesign or an endless polishing loop.
Code correctness and architecture review alone belong to existing code review workflows; implementation edits needed to fix a webpage remain in scope.

## Install

The standalone skill package is [skills/artifact-check](skills/artifact-check/SKILL.md).
Use your agent's supported skill installation method, or ask it to read that file directly from a checkout.
For an AEM catalog, declare a Git source and the skill subdirectory:

```toml
[sources.artifact-check]
type = "git"
repository = "https://github.com/korenl137/artifact-check.git"

[skills.artifact-check]
source = "artifact-check"
subdir = "skills/artifact-check"
```

AEM is optional; the skill contains no installer, daemon, model client or credential store.
File inspection and editing use the agent's available tools and relevant format-specific skills.
When a required tool is unavailable, the agent reports what could and could not be checked or corrected.

## Cost and permissions

The current agent performs the review by default; independent reviewers require a user request.
There is no automatic hook or scheduled review.
Model and tool usage remain subject to their normal costs and limits.
Artifact correction does not itself authorize publication, sending, deployment or additional separately charged operations.

## Validation and contribution

[CONTRIBUTING.md](CONTRIBUTING.md) describes the boundaries and validation workflow.
[Scenarios](skills/artifact-check/evals/scenarios.json) cover correction, ambiguous targets, unavailable inspection and the code-review boundary.
Scenario definitions and structural checks do not establish effectiveness across models or formats.

## License and AI assistance

[MIT](LICENSE).
Developed with OpenAI Codex assistance.
