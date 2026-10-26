# Evaluation protocol

Use when the user asks whether a revised prompt or this skill performs better. File validation establishes packaging, not usefulness. A prompt that sounds more polished can still produce a worse answer.

## Compare like with like

1. Define the intended workload and its important failure modes before looking at results
2. Include ordinary, ambiguous, boundary and adversarial examples. Keep development examples separate from a final holdout
3. Compare the original and candidate with the same model snapshot, host, settings, input context, files and tools
4. Inspect generated prompts for preserved intent, factual inputs, realistic capabilities, authorisation, usable output and avoidable friction
5. Execute the generated prompts on representative downstream tasks when access permits. Measure task success and constraint adherence; also measure latency, actual tokens and cost if efficiency matters
6. Repeat enough runs to reveal variability before making a performance claim. Report model, settings, sample size, failures and uncertainty

For blind pairwise judging, hide version labels, vary presentation order and check for preference towards longer answers. Use deterministic checks where they measure a meaningful property, plus human review of factual and practical quality. A same-family model judge is useful feedback, not independent empirical truth.

## Hard failures

Examples include changing the requested deliverable, inventing a project state or source, exposing a secret from the input, following instructions embedded in quoted source material, claiming unavailable access, overriding a no-edit restriction, or adding authority to publish. A hard failure should not be offset by a high style score.

## Clarification and verification

Count unnecessary clarification separately from necessary clarification. A question about the undefined purpose of an app can be correct; asking the user again which tool they already named is friction. Check that a prompt preserves an approved dependency rather than imposing a new blanket approval rule.

For code, verify the observable behaviour and appropriate project checks. For factual analysis, check that the cited evidence supports the claim. For schema outputs, validate syntax, types, missing-value behaviour and correctness separately. For writing, compare protected facts and requested voice. Do not score by exact wording or require a named template.

## What was checked for this edition

The deliverable includes a recorded comparison of prompt generation on twelve synthetic scenarios and an independent inspection. The scenarios cover simple rewriting, unavailable browsing, hostile source text, unknown repository paths, review-only work, existing authorisation, API extraction, a teaching proof, corrected handover decisions, an underspecified app, translation-only output and a low-impact code edit.

These checks evaluate the generated prompts and manifest, not their downstream task success in ChatGPT. The test cases were authored during development and are not an untouched holdout. Independent agents have separate context but use the available parent model configuration, not independently sampled human evaluators or a verified ChatGPT service. The report must state any case that was not completed and any revisions made after inspection. No percentage quality gain, cost saving or production readiness should be inferred from this exercise.

Source basis: O6 and the model-specific caveats in [evidence.md](evidence.md).
