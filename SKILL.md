---
name: tldr
description: 'Reduce reading effort while preserving the substance and reasoning the user needs. Use for "tldr", "tl;dr", "short version", "just the essentials", "be concise", readability corrections such as "wall of text" or "make this easier to scan", and pacing requests such as "one step at a time". Keep brevity, organization, and pacing independent. A bare tldr or explicit $tldr invocation rewrites the preceding answer locally; "tldr mode" or "keep replies short" sets a continuing preference. Retain standalone "adhd", "i have adhd", and the legacy i-have-adhd invocation as continuing-preset aliases. Compose with domain-attunement for plain English and tee-up for decisions. Questions about these phrases or the skill do not activate it.'
license: MIT
metadata:
  tags: "Concision, Readability, Summarization, Pacing"
  category: "communication"
---

# tldr

Reduce the work of reading without making the user reconstruct what was omitted. Lead with the answer, retain the reasoning and distinctions that make it useful, and stop when the request is satisfied. Judge success by effort removed, not word count alone. Keep the language adult and the tone conversational.

## Interpret the request

Select and combine only the operations requested or supported by the conversation. A presentation correction changes presentation; preserve the underlying question, task, and authority. Mentioning or asking about a trigger is not invoking it: answer that question normally.

| Signal | Operation | Scope |
|---|---|---|
| `tldr`, `tl;dr`, `short version`, `just the essentials`, `be concise` | Summarize or compose a concise answer | Current answer or named material |
| `wall of text`, `make this easier to scan`, readability correction | Reorganize information while preserving requested substance | Current answer or named artifact |
| `one step at a time` | Pace the user-facing instructions or choices | Requested sequence |
| Bare `$tldr` or an explicit invocation without a narrower request | Rewrite the preceding answer concisely | Current answer; no new continuing mode |
| `tldr mode`, `keep replies short`, `from now on`, `always in this conversation` | Retain the named presentation preference | User-specified duration; otherwise this session |
| Standalone `adhd` / `i have adhd`, or legacy `i-have-adhd` invocation without a narrower request | Apply the continuing concise, navigable preset | Rewrite the preceding answer, then retain for the session |
| `plain English`, `what does that mean?` | Ground unfamiliar concepts through `domain-attunement` | Current explanation; this alone requests no length change |

Recognize standalone legacy triggers case-insensitively with surrounding punctuation ignored. With a substantive request, apply shaping to that request. With no preceding answer, apply it to the next substantive answer. A narrower invocation such as “use $tldr to shorten this paragraph only” stays local, including when the legacy name is used. The old name is a conversational alias; native skill selection uses the installed `tldr` handle.

On a reply correction, immediately deliver the corrected answer. Keep the original question or task live; spend the response on answering it rather than announcing the mode, apologizing, or discussing the correction. A local `tldr` neither creates a persistent mode nor erases an existing preference. Retain continuing preferences across topic changes until revised or revoked; `stop tldr mode`, `stop adhd mode`, `normal mode`, and equivalent ordinary language end the preset. A request for detail controls depth for that answer while retaining helpful organization. If deactivation is the entire request, acknowledge it briefly; otherwise answer its substantive content.

## Shape the answer

**Summarize.** Answer the actual question first, then give the smallest complete explanation. Preserve the causal mechanism, facts needed to act, uncertainty, attribution, and conditions that change the conclusion. When the task is a comparison or a landscape, retain its meaningful alternatives and tradeoffs. Cut preambles, repeated conclusions, routine process narration, and background the conversation has already established. Keep required substance until the user narrows scope; a fixed word or bullet quota cannot make that judgment. A dense pile of labels is not a concise explanation: use connected sentences that carry the relationship.

**Reorganize.** Make relationships legible: sequence as steps, alternatives as a comparison, dependencies as a flow, and related facts as coherent groups. Prefer short connected paragraphs for an explanation; use lists, headings, tables, or diagrams when the material benefits from them. Scannability does not require fragmenting every sentence into a bullet or adding a heading for every thought. A readability request alone calls for restructuring while preserving substance. Keep conclusions, blockers, and meaning-changing conditions visible. Preserve requested depth even if a complete overview needs more screen space.

**Pace.** Present one coherent unit the user can understand, decide, or act on, with the context it needs in the same response. When asked to serve choices one at a time, prepare the current decision fully and retain the remaining queue for later; stop at the real user decision. For user-executed work, make the immediate step and purpose clear. For agent-executed work, complete authorized operations without manufacturing approval gates. Report meaningful changes or blockers and any progress the harness requires; keep ritual recaps out. Give time estimates only when evidence supports them.

**Continuing preset.** Use compact answers with a visible main point, coherent chunks, little repetition, and necessary context close to where it is used. Preserve full reasoning complexity. Treat the request as a presentation preference, without making claims about the person's memory, intelligence, motivation, or biology. Answer conceptual questions conceptually. Supply a next action when action is requested or a real user action remains; let a complete explanation end without an unsolicited task or follow-up offer.

For example, after “The Sunday start is conditional on label review and available compute; either dependency can move it,” a `tldr` can be: “Target Sunday, if label review finishes and compute is available.” After “Wall of text; keep every point,” retain the full content and change its organization instead.

## Composition

Let `domain-attunement` govern assumed knowledge and necessary conceptual bridges; let this skill govern selection, organization, and pacing. “Tldr, plain English” requests both. Preserve the smallest causal account that makes the answer intelligible. An expert's short answer may remain technical; a non-specialist's detailed answer may require substantial explanation.

When available, let `tee-up` prepare genuine preference decisions, `elicit` gather information only the user can supply, and artifact-specific skills govern implementation and rendering. This skill needs none of them for an ordinary concise rewrite. Apply presentation guidance within their tasks rather than replacing those tasks with a generic summary. Presentation requests grant no new tool, editing, or external-action permissions.

## Check before sending

Check that the answer addresses the original request, preserves its necessary reasoning and qualifications, fits the requested depth, and changes only the intended scope and duration. If brevity and intelligibility conflict, remove lower-value material before removing the mechanism. Keep a fuller explanation when the mechanism itself needs space.

Skill selection and semantic adequacy require contextual judgment; keyword hooks or word-count enforcement would misroute quoted phrases and erase valid explanations. Mechanical checks can verify metadata and adapters, while behavioral cases must assess interpretation and output.

## Additional resources

- [antipatterns.md](antipatterns.md): paired repairs for compression, organization, persistence, and action bias.
- [evaluation.md](evaluation.md): trigger, composition, and adverse-output cases for revisions.
- [lineage.md](lineage.md): prior art, scope boundaries, and evidence limits.
- `agents/openai.yaml`: Codex display and invocation metadata.
- `agents/gemini.toml`: optional Gemini CLI command that reads this canonical skill instead of duplicating its instructions.
