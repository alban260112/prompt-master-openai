# Evidence and design decisions

Research date: 26 October 2026. This edition starts from nidhinjs/prompt-master at commit `49b3a72469b1e7287d66387004ccfcca90e5968a`, version 1.8.2. It retains the original workflow and templates. The evidence supports particular design choices, not a universal improvement claim.

## Official guidance

| ID | Source | Consequence for this edition |
|---|---|---|
| O1 | [ChatGPT prompting](https://learn.chatgpt.com/docs/prompting) | Use only relevant goal, context, output and boundaries; permit conversational refinement |
| O2 | [Codex best practices](https://learn.chatgpt.com/guides/best-practices) | Specify the intended change and completion conditions; provide relevant project context |
| O3 | [Current model prompting guidance](https://developers.openai.com/api/docs/guides/latest-model/gpt-6-astra.md#prompting-best-practices) | Calibrate clarification, autonomy and testing; audit skill instructions that cause unnecessary pauses |
| O4 | [Reasoning best practices](https://developers.openai.com/api/docs/guides/reasoning-best-practices) | Prefer direct instructions and useful delimiters; start without examples when sufficient; avoid private-reasoning requests |
| O5 | [Codex prompting guide](https://developers.openai.com/cookbook/examples/gpt-5/codex_prompting_guide) | Ground tool-based work in workspace discovery, implementation and verification; its older API harness details are not universal desktop rules |
| O6 | [Evaluation best practices](https://developers.openai.com/api/docs/guides/evaluation-best-practices) | Compare versions on representative tasks and inspect grading bias and failures |
| O7 | [Structured outputs](https://developers.openai.com/api/docs/guides/structured-outputs) | Distinguish schema enforcement from JSON instructions and semantic correctness |
| O8 | [Prompt caching](https://developers.openai.com/api/docs/guides/prompt-caching) | Put stable content before dynamic request data when API caching matters; measure actual usage |
| O9 | [Prompt engineering](https://developers.openai.com/api/docs/guides/prompt-engineering) | Distinguish message roles, context, examples and prompt versioning |
| O10 | [Codex customisation](https://learn.chatgpt.com/docs/customization/overview) | Separate durable project guidance, skills, memories and tool access |
| O11 | [Build skills](https://learn.chatgpt.com/docs/build-skills) | Retain a discoverable manifest and load specialised references only when needed |

The official Markdown pages were retrieved directly where the web reader could not render Markdown. O2 was read through the HTML page. Current model documentation changes; check the exact selected model when settings matter. No account-specific capability or plan availability is assumed.

## Research papers

| ID | Source and year | Finding relevant to this work | Limit on interpretation |
|---|---|---|---|
| P1 | [The Prompt Report](https://arxiv.org/html/2406.06608v6), 2024, revised 2025 | Techniques and example selection have many interacting design choices | A taxonomy and literature synthesis do not establish one best template for current OpenAI models |
| P2 | [Lost in the Middle](https://arxiv.org/html/2307.03172v3), 2023 | Position and irrelevant context affected retrieval in the models tested | Historical models and selected tasks do not establish a universal first-30-percent rule |
| P3 | [Large Language Models Cannot Self-Correct Reasoning Yet](https://arxiv.org/html/2310.01798v2), 2023, revised 2024 | Intrinsic critique without external feedback can fail or degrade reasoning; external checks differ | Results concern tested reasoning settings, not every form of editing or every later model |
| P4 | [The Unreasonable Effectiveness of Eccentric Automatic Prompts](https://arxiv.org/abs/2402.10949), 2024 | Prompt effects did not transfer uniformly between the tested models | Small open-model mathematics experiments cannot validate motivational phrases for ChatGPT |
| P5 | [ReAct](https://arxiv.org/abs/2210.03629), 2022, revised 2023 | Interaction with external sources can improve a task-solving workflow | Tool-enabled experiments are not evidence that plain text creates tools or requires visible private reasoning |
| P6 | [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903), 2022, revised 2023 | Intermediate-step demonstrations helped the tested earlier models | The result does not override current guidance for models that already reason internally |
| P7 | [Self-Consistency](https://arxiv.org/abs/2203.11171), 2022, revised 2023 | Sampling multiple solution paths and aggregating can improve selected tasks | One answer role-playing several experts is not the evaluated sampling procedure |
| P8 | [Sensitivity to spurious prompt features](https://arxiv.org/abs/2310.11324), 2023, revised 2024 | Few-shot formatting choices produced model-dependent variation | The largest reported effects were on older open models; do not transfer their magnitude to this skill |
| P9 | [Does Prompt Formatting Have Any Impact?](https://arxiv.org/html/2411.10541v1), 2024 | Tested GPT models differed in sensitivity to plain text, Markdown, JSON and YAML | It did not test XML or current models, so cannot rank all delimiters today |
| P10 | [LLMs Get Lost In Multi-Turn Conversation](https://arxiv.org/html/2505.06120v1), 2025 | Gradually revealed instructions caused unreliable outcomes in simulated conversations | Simulated analytical tasks differ from natural dialogue and creative work |
| P11 | [Prompt Repetition Improves Non-Reasoning LLMs](https://arxiv.org/html/2512.14982v1), 2025 | Repetition helped tested non-reasoning configurations; reasoning results were much less decisive | This challenges an absolute anti-repetition rule, but does not justify doubling every current reasoning prompt |
| P12 | [Improving factuality and reasoning through multiagent debate](https://arxiv.org/abs/2305.14325), 2023 | Several separate model instances helped selected tasks | Additional calls and cost matter; results do not establish universal benefits or independent agents inside a single response |

Review depth: official guidance was read at the relevant sections; P1, P2, P3, P9, P10 and P11 were checked in full-text HTML for relevant methods, conclusions or limitations. Other papers were screened through their abstracts for the narrow points above. This is an applied literature review, not an exhaustive systematic review or a reproduction of those studies.

## How evidence changes the original

1. Retain nine-dimension intent extraction, but use it to identify relevant information rather than demand nine populated fields
2. Retain tool routing, adding separate ChatGPT, Codex and API references while preserving other profiles as legacy material
3. Retain diagnostics, replacing invented paths, default format locks and confidence-based factual rules with grounded task-specific checks
4. Retain memory blocks for useful handovers, without assuming all history is available or still valid
5. Retain the template library, correcting universal example claims and expanding Template N's practical OpenAI use
6. Retain checks for private reasoning requests, prompt injection and credentials; allow normal teaching explanations and concise public justifications
7. Replace generic agent warnings and repeated confirmation with actual authorisation boundaries
8. Replace first-try and zero-waste promises with evaluation of observable outcomes and resource use

These are authored implementation choices informed by the sources. Remaining legacy non-OpenAI guidance, including exact image parameters and model-specific assertions, needs independent verification before use. It was kept to preserve the requested original base, not certified as current.
