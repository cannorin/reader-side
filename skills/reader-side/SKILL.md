---
name: reader-side
description: Write and revise text from the actual reader's side, excluding author-side process, implementation, and local context that does not help the reader understand, decide, or act. Use for PR descriptions, review comments, issues, release notes, UI copy, errors, notifications, documentation, handoffs, reports, and email. Preserve material risks, constraints, uncertainty, evidence, and required actions.
---

# Reader Side

Keep maker-side facts on the maker side unless they change what the reader needs to understand, decide, or do.

The reader may be an end user, reviewer, maintainer, investigator, auditor, or the requester. Technical detail is not inherently maker-side; its relevance depends on the reader and purpose.

## Choose the information

1. Identify the actual reader, surface, and purpose. Infer them when the context makes them clear. Ask only when the ambiguity would materially change the result.
2. Establish what that reader can reasonably know. Do not assume access to the request conversation, development history, local setup, internal labels, or temporary implementation state.
3. Gate each detail:
   - Would removing it impair the reader's understanding, decision, action, verification, or safety?
   - Does it explain the final artifact, or merely prove that the maker followed instructions or did work?
   - Is this the right surface for it?
4. Organize around the final state: the relevant problem, resulting behavior, supporting evidence, remaining limits, and any action the reader must take. Do not transcribe the work chronology.
5. Express internal causes in terms of their reader-visible effect or useful response. Keep mechanisms when the reader needs them to verify, troubleshoot, maintain, or audit the result.
6. Put diagnostics, audit history, and requester-facing work reports in their appropriate outputs instead of forcing them into user-facing copy. Do not save or publish them without the required authorization.

Do not optimize for brevity by itself. A necessary explanation can be long; an unnecessary sentence is still unnecessary when short.

## Preserve what matters

Never remove information that could change the reader's judgment or action, including:

- unresolved defects, failed checks, unverified scope, or meaningful uncertainty;
- data-loss, security, privacy, compatibility, migration, or availability risks;
- prerequisites, limitations, recovery steps, or unavailable functionality;
- technical evidence needed by reviewers, maintainers, investigators, or auditors.

Distinguish observed facts, inferences, and unknowns. Do not invent a cause, feature, guarantee, result, or remedy to make the text feel complete. A failure reproduced before the change is still a relevant failure, not proof that its cause is known or that it is harmless.

## Deliver the result

- For drafting or rewriting, return the clean audience-facing text without a note announcing that this skill was followed.
- For a requested review, identify the reader-impacting problems and give concise reasons. Rewrite only when requested or clearly part of the task.
- Preserve the requested format, factual meaning, and unrelated content unless a broader rewrite is authorized.

Read [references/evaluation-cases.md](references/evaluation-cases.md) only when changing or evaluating this skill, not during ordinary writing tasks.
