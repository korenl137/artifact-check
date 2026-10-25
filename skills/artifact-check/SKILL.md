---
name: artifact-check
description: >-
  Checks and fixes a user-facing artifact against the original request and applicable
  instructions, then verifies the changes and reports the outcome. Use for
  "결과물 점검해줘", "요청대로 만들어졌는지 확인하고 고쳐줘", or equivalent
  artifact refinement requests. Formats are open; code correctness review alone
  belongs to the existing code review workflow.
metadata:
  version: "0.1.0"
---

# Artifact Check

Treat invocation as a request to inspect and fix the artifact, then report the result.
Do not stop at a list of issues when corrections are possible within the authorized scope.

An artifact is a deliverable the user directly reads, views, interacts with or uses.
Documents, slides, images, tables and webpages are examples, not a supported-format whitelist.
For an interactive artifact, implementation changes may be needed to correct its visible behavior.
Code correctness or architecture review alone uses the appropriate existing workflow.

## Tools

Use the available reader, renderer, viewer or execution tool appropriate to the artifact.
Use relevant format-specific skills for inspection and editing when available; their files are not dependencies of this skill.
Inspect the actual deliverable, including rendered appearance or interactions where relevant.
If a required modality or tool is unavailable, do the supported checks and name the remaining inspection or correction blocker.
Source text, a generation prompt or an earlier success claim does not prove the rendered result is correct.

## Select the target and criteria

Use the artifact the user identifies; otherwise use the unambiguous artifact just created or edited in the current conversation.
Inspect accessible conversation context and artifact locations before asking the user to repeat them.
If several targets remain plausible, ask which one rather than reviewing everything.

Recover the original request, later accepted changes and applicable instructions.
Turn them into a short internal checklist focused on content, presentation and intended use.
Respect the approved direction and preserve unrelated user work.
Distinguish a requirement failure or usability problem from an optional taste preference.
Do not invent requirements or reopen settled design choices.

## Inspect, correct and recheck

Use the current agent for the review by default.
Inspect the target against the checklist and fix supported problems within the requested artifact scope.
Use the appropriate editing tool rather than giving the user instructions to make the correction themselves.
An independent reviewer is optional when the user requests one; invocation alone does not request extra agents.

Recheck the changed content and any affected appearance or interaction, using the actual output where accessible.
If a focused recheck reveals a remaining defect from the correction, resolve it when practical.
Stop when the requested requirements and relevant use checks are satisfied, or when a concrete blocker prevents further progress.
Do not keep redesigning, expanding scope or repeating broad reviews for marginal polish.

The request authorizes artifact corrections, not additional publication, sending, deployment,
destructive replacement, or separately cost-incurring operations outside existing authorization.
Ask only when such an operation is needed or an unresolved choice would change the intended direction.
Continue independent permitted corrections while a separate decision is pending.

## Report

Briefly state what was corrected, what was actually checked, and any unresolved issue or verification limit.
Link the updated artifact when applicable.
If no correction was needed, say which relevant checks passed rather than inventing improvements.
Keep optional redesign ideas separate from defects, and omit them when they do not help the user.
