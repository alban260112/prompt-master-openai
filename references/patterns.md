# Credit-Killing Patterns Reference

The original 37-pattern diagnostic, revised for the OpenAI edition. These are possible failure causes, not 37 mandatory additions to every prompt. Read this file when the user pastes a bad prompt and asks you to fix it, or when diagnosing why a prompt is underperforming.

---

## Task Patterns

| # | Pattern | Bad Example | Fixed |
|---|---------|------------|-------|
| 1 | **Vague task verb** | "help me with my code" | "Refactor `getUserData()` to use async/await and handle null returns" |
| 2 | **Unrelated tasks in one prompt** | "fix login and write a sales email" | Split unrelated outcomes; combine related work with shared acceptance criteria |
| 3 | **No success criteria** | "make it better" | "Done when the function passes existing unit tests and handles null input without throwing" |
| 4 | **Over-permissive agent** | "do whatever it takes" | Explicit allowed actions list + explicit forbidden actions list |
| 5 | **Emotional task description** | "it's totally broken, fix everything" | "State the observed error if supplied; otherwise inspect and reproduce the failure instead of inventing it" |
| 6 | **Build-the-whole-thing** | "build my entire app" | Keep a coherent deliverable; use milestones or separate prompts only when dependencies, context or review decisions justify them |
| 7 | **Implicit reference** | "now add the other thing we discussed" | Use available context; consolidate only what the target lacks or needs to recover from drift |

---

## Context Patterns

| # | Pattern | Bad Example | Fixed |
|---|---------|------------|-------|
| 8 | **Assumed prior knowledge** | "continue where we left off" | Carry forward relevant confirmed decisions only when transferring or recovering context |
| 9 | **No project context** | "write a cover letter" | "PM role at B2B fintech, 2yr SWE experience transitioning to product, shipped 3 features as tech lead" |
| 10 | **Forgotten stack** | New prompt contradicts prior tech choice | Preserve the established stack without duplicating a history block in every turn |
| 11 | **Hallucination invite** | "what do experts say about X?" | "Use accessible evidence; cite sources that support the claim and identify anything that cannot be verified." |
| 12 | **Undefined audience** | "write something for users" | "Non-technical B2B buyers, no coding knowledge, decision-maker level" |
| 13 | **No mention of prior failures** | (blank) | "I already tried X and it didn't work because Y. Do not suggest X." |

---

## Format Patterns

| # | Pattern | Bad Example | Fixed |
|---|---------|------------|-------|
| 14 | **Missing output format** | "explain this concept" | Choose a useful form; impose a specific structure only when the task requires it |
| 15 | **Implicit length** | "write a summary" | Preserve requested brevity without inventing a sentence or word count |
| 16 | **Missing domain perspective** | Specialized task without domain context | Add an expert role only when it changes the result |
| 17 | **Vague aesthetic adjectives** | "make it look professional" | "Monochrome palette, 16px base font, 24px line height, no decorative elements" |
| 18 | **No negative prompts for image AI** | "a portrait of a woman" | Add: "no watermark, no blur, no extra fingers, no distortion, no text overlay" |
| 19 | **Prose prompt for Midjourney** | Full descriptive sentence | "subject, style, mood, lighting, composition, --ar 16:9 --v 6" |

---

## Scope Patterns

| # | Pattern | Bad Example | Fixed |
|---|---------|------------|-------|
| 20 | **No scope boundary** | "fix my app" | Fix the stated login behaviour and protect unrelated behaviour; identify the relevant files from the actual project |
| 21 | **No stack constraints** | "build a React component" | "React 18, TypeScript strict, no external libraries, Tailwind only" |
| 22 | **No stop condition for agents** | "build the whole feature" | Explicit stop conditions + meaningful milestones and verification evidence |
| 23 | **No file path for IDE AI** | "update the login function" | Locate the relevant implementation and callers; include exact paths only when known |
| 24 | **Wrong template for tool** | GPT-style prose prompt used in Cursor | Use the selected product's actual context and tools; Template N is optional for complex OpenAI work |
| 25 | **Pasting entire codebase** | Full repo context every prompt | Keep relevant dependencies and evidence; use targeted repository discovery rather than a full dump |

---

## Reasoning Patterns

| # | Pattern | Bad Example | Fixed |
|---|---------|------------|-------|
| 26 | **No audit contract for logic task** | "which approach is better?" | Request the recommendation, assumptions, decision criteria, evidence, and verification checks |
| 27 | **Requesting hidden reasoning** | "show your chain of thought" | Remove it: ask for a concise rationale, evidence, and checks instead |
| 28 | **Expecting inter-session memory** | "you already know my project" | Provide a factual handover when the target lacks the required context; do not promise permanent memory |
| 29 | **Contradicting prior work** | New prompt ignores earlier architecture | Reconcile the active decisions, including later corrections; do not preserve superseded constraints |
| 30 | **No grounding rule for factual tasks** | "summarize what experts say about X" | "Ground claims in the specified evidence and disclose verification gaps." |

---

## Agentic Patterns

| # | Pattern | Bad Example | Fixed |
|---|---------|------------|-------|
| 31 | **No starting state** | "build me a REST API" | Include the supplied project state or request inspection; do not invent a stack or existing files |
| 32 | **No target state** | "add authentication" | Describe the required observable authentication behaviour; use paths or architecture only if established |
| 33 | **Silent agent** | No progress output | "Report meaningful milestones, blockers, and final verification results" |
| 34 | **Unlocked filesystem** | No file restrictions | Protect the specified interfaces, secrets and unrelated changes; use strict file restrictions only when justified |
| 35 | **No human review trigger** | Agent decides everything autonomously | Honour existing authorisation and host controls; ask only about necessary consequential actions that remain unauthorised |
| 36 | **Vague first turn for an agentic model** | "fix the auth bug" with no scope, files, or criteria | Use Template M for Claude or Template N for OpenAI tasks. Front-load the outcome, relevant context, file scope, constraints, action boundaries, and acceptance criteria. |
| 37 | **Context rot on long sessions** | Repeats corrections while stale assumptions remain in context | Start a new session for unrelated work; otherwise compact around current decisions, constraints, failures, and target state. Delegate only independent, sizeable investigation. |

