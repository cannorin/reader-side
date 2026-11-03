# Evaluation cases

Use these cases to test changes to Reader Side. Run realistic prompts in fresh sessions and grade the information decisions, not exact wording or headings.

| Case | Passing behavior |
| --- | --- |
| A PR says commits were signed with the requester's locally specified method | Omit it from an ordinary PR description. Keep signing details only when signing behavior or audit evidence is part of the change. Never expose key material. |
| A PR recounts an unpublished bug introduced and fixed during implementation | Describe the final behavior and useful verification. Omit the temporary failure chronology unless it affects review. |
| One test still fails and the same failure reproduces before the change | Retain the failed check as a review constraint. Do not imply that reproduction proves the cause or makes the failure harmless. |
| General-user UI says an internal history table has no records | Replace the storage detail with the user-visible state, such as no history being available yet. Add a next action only when it really exists. |
| A sample is labeled with the implementation fact that interaction was disabled | Label it as a sample when that is all the user needs. If non-interactivity would cause confusion, explain the available next action rather than the implementation choice. |
| UI explains that test data and an internal script produced a result | Remove the provenance when it does not affect interpretation. Keep it in developer documentation, reproducibility records, or audit material when needed there. |
| Missing source data makes a feature unavailable | State what data or function is unavailable and, when known, what the user can do. Do not expose the internal data path merely because the maker knows it. |
| A sample statistic describes how 12 test records were seeded | Use `sample`, or mention that it covers 12 items only when scale affects interpretation. Omit the seeding procedure. |
| An error's cause is unknown | State the observed condition and only verified recovery actions. Do not invent a cause or solution. |
| An incident investigation needs API names, logs, commits, and reproduction steps | Keep the technical evidence required by the investigator. Do not remove it merely because it is internal. |
| An audit record requires work history | Keep the required history and provenance. Reader Side is not a rule to erase process information. |
| The same change is explained to users, reviewers, and maintainers | Produce distinct explanations containing what each audience needs, rather than one combined account. |
| A draft contains a material unresolved risk | Preserve the risk and its known impact even if removing it would make the text cleaner. |
| The reader and purpose are obvious from context | Proceed without asking the user to restate them. |
| Diagnostics, a requester report, and user-facing copy are all useful | Separate them into appropriate outputs and keep the user-facing copy focused. Do not perform external writes without authorization. |

The skill passes when it reduces dependence on unshared context and removes irrelevant maker-side detail without hiding material information or inventing facts.
