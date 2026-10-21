---
name: i-have-adhd
description: 'Shape responses for the requested reading effort: summarize for "tldr", "tl;dr", "short version", "just the essentials", or "be concise"; reorganize for "wall of text" or "make this easier to scan"; pace work for "one step at a time". Applies to requested answer or artifact presentation, including readability corrections. Standalone "adhd", "i have adhd", or explicit invocation without a narrower request rewrites the preceding answer and activates continuing concise, navigable presentation. Keeps compression, organization, and pacing independent; composes with domain-attunement for "plain English" explanations. Questions about these phrases or this skill do not activate its modes.'
license: MIT
metadata:
  tags: "Response Shaping, ADHD, Summarization, Readability"
  category: "communication"
---

# Response shaping

Make the answer easy to find, understand, and use at the depth the user requests. Keep `i-have-adhd` as the callable handle and preserve its familiar ADHD invocation. Judge success by the reading and reconstruction work removed, not by word count alone.

## Interpret the request

Select and combine only the operations requested or supported by the conversation. A presentation correction changes presentation; preserve the underlying question, task, and authority. Mentioning or asking about a trigger is not invoking it: answer that question normally.

| Signal | Operation | Scope |
|---|---|---|
| `tldr`, `tl;dr`, `short version`, `just the essentials`, `be concise` | Summarize or compose a concise answer | Current answer or named material |
| `wall of text`, `make this easier to scan`, readability correction | Reorganize information while preserving requested substance | Current answer or named artifact |
| `one step at a time` | Pace the user-facing instructions or choices | Requested sequence |
| Standalone `adhd` / `i have adhd`, or explicit skill invocation without a narrower request | Concise, navigable presentation with action support when relevant | Rewrite the preceding answer, then retain for the session |
| `keep replies short`, `from now on`, `always in this conversation` | Retain the named preference | User-specified duration; otherwise this session |
| `plain English`, `what does that mean?` | Ground unfamiliar concepts through `domain-attunement` | Current explanation; this alone requests no length change |

Recognize standalone ADHD triggers case-insensitively with surrounding punctuation ignored. With a substantive request, apply the requested shaping to that request. With no preceding answer, apply it to the next substantive answer. A narrower invocation such as “use $i-have-adhd to shorten this paragraph only” stays local.

On a reply correction, immediately deliver the corrected answer without an activation announcement. A local `tldr` does not create a persistent mode or erase an existing preference. Retain continuing preferences across topic changes until revised or revoked; `stop adhd mode`, `normal mode`, and equivalent ordinary language end the ADHD preset. A request for detail overrides brevity for that answer while retaining helpful organization. If deactivation is the entire request, acknowledge it briefly; otherwise answer its substantive content.

## Shape the answer

**Summarize.** Lead with the answer or conclusion. Preserve the minimum reasoning needed to understand it, facts needed to act, and conditions that change its meaning. Preserve alternatives when comparing alternatives is the task. Trim repetition and background first; discard required substance only when the user explicitly narrows scope. A concise rewrite may be one paragraph or a few points; a fixed word or bullet quota is not the success criterion. Keep uncertainty and attribution intact rather than making compression sound more certain.

**Reorganize.** Make the information's relationships legible: sequence as steps, parallel alternatives as a comparison, dependencies as a flow, and related facts as coherent groups. Use the simplest representation that carries the meaning. A readability request alone calls for restructuring, not summarization. Keep central conclusions, blockers, and meaning-changing conditions visible; use optional detail for supporting material, not to conceal the answer. Preserve the requested depth even if a complete overview needs more screen space.

**Pace.** Present a coherent unit the user can understand or act on. For user-executed work, make the immediate step and its purpose clear, supplying context at the point of use. For agent-executed work, complete authorized operations without converting every step into a request for permission. State progress when it helps orientation or reports a meaningful change; avoid ritual recaps. Give time estimates only when evidence supports them, with the uncertainty that matters.

**Continuing ADHD preset.** Prefer compact answers with a visible main point, coherent chunks, little repetition, and relevant context close to where it is used. These are accommodations, not claims about the person's memory, intelligence, motivation, or biology. Answer conceptual questions conceptually. Give a next action when action is requested or a real user action remains; end a complete explanation when it is complete.

## Composition

Let `domain-attunement` govern assumed knowledge and necessary conceptual bridges; let this skill govern selection, organization, and pacing. “Tldr, plain English” requests both. Preserve the smallest causal account that makes the answer intelligible. An expert's short answer may remain technical; a non-specialist's detailed answer may require substantial explanation.

Keep `tee-up` responsible for preparing genuine preference decisions. Keep `elicit` responsible for gathering information only the user can supply. Keep artifact-specific skills responsible for implementation and rendering. Apply presentation guidance within their tasks rather than replacing those tasks with a generic summary. Presentation requests do not grant new tool, editing, or external-action permissions.

## Check before sending

Check that the answer addresses the original request, preserves its necessary reasoning and qualifications, fits the requested depth, and changes only the intended scope and duration. If brevity and intelligibility conflict, remove lower-value material before removing the mechanism. Keep a fuller explanation when the mechanism itself needs space.

Skill selection and semantic adequacy require contextual judgment; keyword hooks or word-count enforcement would misroute quoted phrases and erase valid explanations. Mechanical checks can verify metadata and adapters, while behavioral cases must assess interpretation and output.

## Additional resources

- [antipatterns.md](antipatterns.md): paired repairs for compression, organization, persistence, and action bias.
- [evaluation.md](evaluation.md): trigger, composition, and adverse-output cases for revisions.
- [lineage.md](lineage.md): prior art, scope boundaries, and evidence limits.
- `agents/openai.yaml`: Codex display and invocation metadata.
- `agents/gemini.toml`: optional Gemini CLI command that reads this canonical skill instead of duplicating its instructions.
