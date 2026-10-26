# PROMPT MASTER: OPENAI EDITION

An adaptation of [nidhinjs/prompt-master](https://github.com/nidhinjs/prompt-master) for ChatGPT, ChatGPT Work, Codex and OpenAI API applications.

**I made this adaptation using AI.** AI helped research the guidance, revise the skill, write the documentation and run model-based checks. The original Prompt Master was created by nidhinjs. This repository is my adaptation of that work, with the original MIT licence and credit retained.

## What it does

- Turns rough ideas into prompts that preserve the intended task and constraints
- Separates guidance for ChatGPT conversations, Codex agents and API applications
- Proactively produces a better prompt when an action request is materially unclear, even without an explicit prompt-writing request
- Leaves clear requests, factual questions, minor typos and contextual follow-ups alone
- Uses evidence requirements, realistic tool access and proportionate verification

In automatic mode it returns a usable improved prompt rather than executing a materially unclear task. Supply the missing detail or tell the assistant to proceed to continue with the clarified work. A direct instruction to skip rewriting takes precedence. This feature depends on the host loading the skill and allowing automatic selection; it cannot change a separate ChatGPT account or guarantee selection in every environment.

## Based on the original

The base is Prompt Master version 1.8.2 at [commit 49b3a724](https://github.com/nidhinjs/prompt-master/tree/49b3a72469b1e7287d66387004ccfcca90e5968a). It retains the nine intent dimensions, diagnostic patterns 1 to 37, memory handovers, prompt decompilation and templates A to N. Other providers' profiles remain as legacy material and have not been independently validated by this adaptation.

The OpenAI changes remove rigid formatting requirements, invented file boundaries, unnecessary approval requests and guarantees of perfect first-attempt results. References distinguish current official guidance from historical research and authored recommendations.

## Use in Codex

Install this repository's skill folder in a user or project skill directory supported by your Codex host. Keep SKILL.md, agents and references together. Do not overwrite an existing customised copy without reviewing the changes.

For example, from a shell with Git:

```sh
git clone https://github.com/alban260112/prompt-master-openai.git ~/.agents/skills/prompt-master-openai
```

Codex also supports project skills under `.agents/skills`. This local adaptation was installed in the creating environment's existing Codex skill directory. Host versions can differ; consult [OpenAI's skill documentation](https://learn.chatgpt.com/docs/build-skills) for current locations.

Invoke it explicitly with `$prompt-master-openai`, or let the host select it for a matching request. `agents/openai.yaml` enables implicit invocation. No server, API key or additional executable is included.

## Use in ChatGPT

Use a compatible skill host, or paste the self-contained [ChatGPT instructions](ChatGPT-instructions.txt) into a conversation and then provide the idea or prompt to improve. Local Codex installation does not automatically install anything into an unrelated ChatGPT web or mobile session.

## Evidence and validation

The initial review consulted eleven official OpenAI documents and twelve research papers, plus the original repository. Read the [evidence register](references/evidence.md), [research report](docs/research.html) and [evaluation protocol](references/evaluation.md).

For edition 1.8.2-openai.1, two agents generated responses to twelve synthetic cases. A third reviewer, without version labels and with balanced A/B order, preferred the revision seven times and recorded five ties. These were qualitative judgements about generated prompts, not downstream ChatGPT task-success measurements. The sample was small, development-authored and judged by a model. No percentage quality gain, token saving or cost reduction is established.

Edition 1.8.2-openai.2 adds the requested automatic trigger. The earlier comparison does not establish its performance. The validation record identifies the scope of each check. Source selection, AI-authored documentation and remaining legacy claims should be reviewed critically.

Eight additional synthetic trigger checks selected the skill for two materially vague requests and one explicit prompt-writing request. They left a factual question, a contextual follow-up, a clear edit, a misspelt translation request and an explicit opt-out alone. No underlying task was executed during these checks. This checks the intended selection boundaries, not selection reliability across every host or conversation.

## Licence and attribution

The original [MIT licence](LICENSE) is preserved. See [NOTICE.md](NOTICE.md) for provenance and the AI disclosure. This is an unofficial derivative, with no endorsement from OpenAI or the original author.
