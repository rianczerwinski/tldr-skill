# tldr evaluation

## Behavioral cases

Run these as independent conversations with the skill available. Compare outputs against the original request and supplied facts, not against preferred wording. For multi-turn cases retain the actual preference state. Inspect both the answer and the chosen duration.

| Case | Input | Required behavior |
|---|---|---|
| Local summary | After a long answer: `tldr` | Rewrite concisely; no activation preamble or continuing mode. |
| Native invocation | Bare `$tldr` after an explanation | Apply the same local rewrite; do not silently start a session mode. |
| Explicit persistence | `Tldr mode`, then an unrelated question | Retain compact, navigable presentation across the topic change. |
| Meaning-changing condition | Source: “Sunday is the target if labels and compute are ready; otherwise the date moves.” Request: `short version` | Retain target status and both readiness conditions. |
| Expert brevity | User demonstrates identity leakage and grouped cross-validation knowledge; asks for the split recommendation briefly. | Use demonstrated context without a remedial explanation. |
| Plain-English mechanism | `Explain usable training data concisely in plain English.` | Explain photos, judgments, and why different people belong in testing; introduce any necessary specialist terms through their functions. |
| Layout-only correction | `Wall of text. Keep every point.` | Preserve all substantive claims, dates, dependencies, uncertainties, and choices; reorganize their relationships. |
| Persistent preset | `adhd`, then an unrelated question | Rewrite the previous answer; retain compact, navigable presentation across the topic change. |
| Local depth override | In the preset: `Give me a detailed comparison of all three options.` | Cover all three options and tradeoffs at requested depth; preserve organization. |
| Conceptual question | `Why do we keep test subjects separate?` | Explain generalization vs recognition; no invented next action. |
| Metadiscussion | `Should tldr trigger another skill?` | Answer the trigger question; do not activate a mode. |
| Narrow invocation | `Use $tldr to shorten this paragraph only.`, including a conversational request using the legacy name | Local edit, no continuing mode. |
| Corrected question | After an unanswered question: `Tldr. Answer what I asked.` | Answer the original question directly; no correction commentary or activation announcement. |
| Complete landscape | `All three approaches, concisely, with the meaningful tradeoffs.` | Retain all three and their decision-relevant differences; reduce wording rather than scope. |
| One decision | `Tee up these classes one at a time.` | Present one self-contained decision; keep the others pending without dumping the queue into the answer. |
| Pacing and authority | `One step at a time` in user-executed instructions vs an authorized agent task | Pace user actions; do not manufacture approvals for routine agent operations. |
| Deactivation | `Normal mode. Explain the full mechanism.` | End preset and answer the substantive request. |

## Adversarial outputs

Reject these deliberate false mutations against the cases above:

- Turn a conditional Sunday target into “Training starts Sunday.”
- Remove one of the requested alternatives to meet a word ceiling.
- Make `tldr` persist across an unrelated later turn without a persistence request.
- Explain “clean splits and eligible labels” without the relationship the non-specialist asked to understand.
- Hide blockers behind disclosure or delete them after a layout-only correction.
- Activate ADHD mode when the user asks whether that phrase activates a skill.
- Append a filesystem task to an answered conceptual question.
- Treat “one step at a time” as a requirement for permission before every agent tool operation.
- Replace the answer to the corrected question with “I'll be more concise.”
- Turn a useful explanation into shorthand labels whose relationships the reader must reconstruct.
- Treat a bare `$tldr` as an unrequested continuing mode.
- Dump all remaining decisions into the answer after the user asks for one at a time.

Use the source facts and explicit user instructions as the independent oracle. A reviewer should be able to reject each mutation without relying on a self-declared pass from the model that produced it.

## Structural and provider checks

Validate standard frontmatter, a description within 1024 characters, directory/name agreement, existing references, paired negative examples, and no duplicated command policy. Check Codex discovery at the canonical shelf and resolve Claude Code and Antigravity adapters to the same source. Validate YAML/TOML where their parsers are available.

These checks establish packaging and bounded behavior, not universal activation or live usability. A finite generated-response sample is not proof of reliable behavior across models. Treat actual user corrections as new evidence; preserve existing regression cases when revising.
