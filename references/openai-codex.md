# Codex

Use this profile for prompts aimed at a Codex agent that can inspect a workspace or use developer tools. The surface and environment determine available actions; the product name does not identify the selected model.

## Preserve the requested mode

An explanation request should produce an explanation. A review should report findings. A plan should be reviewable. An implementation request should lead to a completed change and appropriate validation. Do not turn every prompt into an instruction to edit files. Prompt Master's prompt-generation task remains separate from the task being described.

For implementation, retain Template N's goal, context, constraints, actions, completion checks and output as needed. Give a reproducible symptom or concrete before/after behaviour when supplied. Include exact paths, commands, versions and function names only when known. Otherwise direct the target to discover them from the workspace and project guidance. Do not lock it to an invented filename or to one file when the behaviour spans callers, configuration and tests.

## Provide useful context

Include observations, reproduction steps, relevant errors, expected behaviour, known failed attempts and protected behaviour. Let the target inspect applicable AGENTS.md files, existing conventions and relevant code before deciding what to change. Avoid requiring it to read the entire repository or to use a fixed tool name that may not exist.

Persisting project rules belong in project guidance; the current task prompt should add the change-specific information. Do not duplicate a whole harness prompt in every request. A screenshot or reference artifact needs an instruction about which details it defines.

## Scope and authorisation

Allow routine inspection, implementation and checks that the request authorises. Preserve existing user approval and actual permission boundaries. Do not demand another confirmation for every command, dependency or file change by default. Conversely, do not turn a broad objective into authority to publish, purchase, contact people or destroy unrelated data.

Use strict directory or file limits when the user requires them or when the task justifies them. Otherwise scope by the intended behaviour and protected interfaces. If a consequential new decision or unauthorised action is required, have the target prepare the independently authorised work first and ask about the remaining decision. A prompt cannot override the host's approval controls.

## Follow through and verify

For a fix, ask the target to establish the failure, make the relevant change and verify the result using the project's actual checks. Use proportionate evidence: a targeted regression check for a behaviour change, a build or type check when affected, a visual inspection for a visual change, or the repository's required checks. Do not demand new tests for every reversible text or styling edit.

Completion reports should distinguish changes made, checks run, checks unavailable and residual limitations. Passing a command is evidence for what that command covers, not proof of every runtime behaviour. For a review, require actionable findings with the concrete failure condition and file references, and preserve any no-edit requirement.

Continue towards the agreed outcome instead of stopping at a proposal when implementation is requested. Stop a loop when it produces no new evidence or when a concrete unresolved dependency requires the user. Use observed failure and task budgets, not a universal two-retry limit.

## Long tasks

Request progress when a finding, milestone or blocker changes what the user needs to know; follow host communication requirements. Avoid a message after every command. Do not import old API harness advice that suppresses all status updates into a different Codex surface.

Use subagents only when available, permitted and worthwhile for independent work. Define each deliverable and a practical concurrency or cost limit when necessary. Simulated personas in one answer are not independent execution. Keep one owner for the integrated outcome. Preserve user restrictions on delegation.

Keep model selection, reasoning effort and other runtime settings in setup notes when requested. Verify current controls for the selected model and host; do not infer API parameters from interface labels.

See [evidence.md](evidence.md), especially O2, O3, O5, O10 and P5. These instructions adapt Prompt Master's agent workflow; they do not replace the agent's own system instructions.
