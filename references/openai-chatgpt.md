# ChatGPT and ChatGPT Work

Use this profile when the generated prompt will be used in ChatGPT. Preserve Prompt Master's intent extraction and relevant template, but adapt it to the conversation and tools actually available.

## Choose the right amount of detail

A straightforward request often needs only the task, supplied input and one important constraint. For larger work, add the audience, relevant sources, decision criteria and what a usable result looks like. Template N is a menu, not a form. Do not invent a role, a numerical word limit or extra deliverables merely to fill it.

Infer ChatGPT as the target when the user says so or the conversation establishes it. Do not require the model name for a normal writing, explanation or analysis prompt. Preserve a named model; ask about the surface only when tools or output requirements make the distinction consequential.

## Match the task

- Writing: preserve meaning, facts, commitments and the requested voice. Include a supplied example when it defines the voice better than adjectives. State audience or length only when useful
- Learning: state the learner's level and desired explanation. Worked calculations, proofs and teaching steps are legitimate outputs; do not confuse them with private model reasoning
- Decisions: name the options, constraints, criteria and evidence needed. Ask for a recommendation with the decisive trade-off, not a predetermined endorsement
- Research: specify the question, relevant period and geographical scope when they affect the answer. Ask for accessible primary sources, supporting links and an explicit distinction between findings and interpretation
- Source-only analysis: identify the supplied documents and require source locations for material claims. Keep external knowledge out when the user restricts the evidence base. Missing evidence is a gap, not permission to fill it
- Images and files: describe the required output and the parts of an attachment that matter. For edits, specify the change and the features to preserve. Do not invent attachment content or assume an unsupported editing tool

## Tools and evidence

A prompt cannot create browsing, file access, an image tool, a connection or a background task. If access is established, state the goal and the evidence expected. If access is unknown, use a conditional instruction only where needed: use available retrieval; otherwise identify what cannot be checked and ask for the necessary source. Do not make completed-search claims in a prompt that has not been executed.

For research, citations must support the adjacent claim. Prefer direct source links, publication dates and relevant sections to an arbitrary citation quota. A source being quoted is not proof that its claim is sound. Do not replace verification with a request for high confidence or suppress material uncertainty to make the answer sound decisive.

ChatGPT Work may use tools and produce finished files. Define the intended artifact, sources, review criteria and any actual restrictions on actions. Let it perform authorised work. Distinguish preparing a draft from sending or publishing it. Preserve approvals already given and the environment's permission rules.

## Conversation and handovers

Use existing context that remains relevant. A new message can correct or narrow the earlier request; update the prompt accordingly. Do not preserve a superseded constraint in a memory block. For a new chat or tool, include a short handover of confirmed facts, active decisions, failed attempts that matter and unresolved questions. Do not reconstruct unavailable history or promise permanent retention.

Follow-up prompts should state the requested change and what needs to remain. Rebuild a consolidated brief when repeated corrections reveal drift. Do not prescribe a new chat or a fixed compaction threshold for every task.

## Output

Return the requested prompt ready to use. If the user asks to diagnose a prompt, explain the specific weakness and the proposed correction. Give alternatives only when requested or when they represent a useful choice. Do not execute the generated task unless the user also requests execution.

The principles are supported by the source register in [evidence.md](evidence.md), particularly O1, O3, O4, O9, P1 and P10. The profile is a design recommendation, not a tested guarantee.
