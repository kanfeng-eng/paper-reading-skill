---
name: paper-reading
description: Summarize or closely read scientific papers, reconstruct problem discovery and solution rationale, inspect evidence, produce HTML notes with frontend-design, and collect argument patterns and precise expressions. Offline Windows and Mac helpers are embedded.
metadata:
  version: "1.4.0"
---

# Offline compiled entry

Use the executable matching this computer: `norman-paper-reading.exe` on Windows x64, `norman-paper-reading-macos-arm64` on Apple Silicon, or `norman-paper-reading-macos-x64` on Intel Mac. Run `guide` first, `list` to see embedded resources, and `read <resource>` to load one. The commands `extract`, `render`, `validate`, `reader`, and `version` run with their complete bundled runtime. No Python installation or network download is needed. The runtime is unpacked into a local cache on first use. Internet literature search by the AI client remains separate from these local helpers.

The full source workflow follows. For its old `bin/norman-reader` examples, invoke the matching executable above instead. Upstream resource paths are logical names loaded with `read`. Locally added Markdown references are read directly from the skill directory as linked below.

This portable paper-reading distribution adds problem-discovery and solution-rationale, output-notes, argument-and-expression corpus, and HTML delivery modules. The packaged SKILL.md governs behavior when upstream embedded guides use the original skill name or describe Markdown-first or request-only HTML behavior.

# paper-reading

Explain the research storyline, evidence boundaries, and what the reader can do next. Whole-paper analysis normally includes future research insights and a prioritized next-step plan, not only a summary or list of limitations. Follow the user's language, scope, and delivery location; English instructions do not require English reports. Use Chinese only when language cannot otherwise be inferred or configured. Start from the supplied paper without a questionnaire; use relevant known background or assume research experience with limited familiarity with this field.

## Choose the mode

| Intent | Mode | Major report headings |
|---|---|---|
| Summarize, main points, worth reading, quick overview | quick | Research question; Core design; Key results; Evidence gaps; Future research insights and next steps; Reading priority; Compact review notes |
| Analyze this paper, close reading, detailed explanation, journal club, whole-paper understanding | deep | Core assessment and scope; Full research storyline; Problem discovery and solution rationale; Key design decisions; Figures/tables or key theorems; Necessary equations; Evidence cards; Open questions; Future research insights; Next-step research plan; Output notes; Argument and expression corpus; Sources |
| Reproduce, apply to my project, future research planning | extend | Necessary deep evidence; Problem discovery and solution rationale; Future research insights; Transfer conditions; Reproduction checklist; Research action cards; Prioritized research roadmap; Output notes; Argument and expression corpus; Sources |
| One figure, equation, or passage | focused | Requested item; Necessary context; Explanation; Evidence boundary |

An unqualified summary uses quick; an unqualified whole-paper analysis (including “分析这篇文章”) or close reading uses deep. Include a compact insight and next step in quick, and distinct future-insights and research-plan sections in deep. Explicit research planning uses extend. Respect requests for summary only, no extensions, or strict brevity; focused explanations do not automatically acquire a whole-paper plan. Preserve explicit or established mode/coverage in follow-ups. Speed changes execution, not requested completeness. Guided reading, full parallel translation, and paper comparison are additions only on request. General literature discovery and unspecified field reviews do not trigger full close reading.

## Fast start and selective loading

Quick text-only summaries need only this entry point. Do not pre-load every reference, template, example, or script source, inspect unrelated folders, or create a profile. Read each applicable reference once:

- reading-workflow.md (`read references/reading-workflow.md`): deep/extend workflow and input fallbacks.
- figure-and-equation-reading.md (`read references/figure-and-equation-reading.md`): explaining original visuals or equations.
- evidence-and-research-cards.md (`read references/evidence-and-research-cards.md`): saved evidence JSON or research actions.
- future-research-planning.md (`read references/future-research-planning.md`): default future insights and plans for deep analysis; detailed roadmaps for extend. Quick uses the compact guidance below without loading this reference.
- paper-types.md (`read references/paper-types.md`): specialized study-type checks.
- teaching-and-comparison.md (`read references/teaching-and-comparison.md`): requested teaching, parallel translation, or comparison.

For the output-notes module, read the local file [references/output-notes.md](references/output-notes.md) directly before drafting notes. This file is outside the executable's embedded resources. Quick uses the compact guidance below without loading the reference unless detailed notes are requested.

For deep/extend or an explicit writing/corpus request, read the local [references/argument-expression-corpus.md](references/argument-expression-corpus.md) directly. It specifies excerpt selection, analysis, reusable patterns, and project-local accumulation.

Before producing reading notes in any mode, read [references/html-output.md](references/html-output.md) and apply `frontend-design`. Use its installed skill when available, otherwise read and apply the complete bundled [vendor/frontend-design/SKILL.md](vendor/frontend-design/SKILL.md). Resolve bundled resources relative to this skill directory. Read the design instructions before designing the page.

Reuse extracted text, source maps, inspected images, and evidence only after checking source identity/version, fingerprint where available, and coverage. File existence proves neither freshness nor inspection. Process missing/changed material and keep stable IDs. Extract required PDF coverage once; locate passages from text/source maps rather than repeatedly dumping the full extraction. quick/focused can use selected pages; whole-paper deep requires the relevant full main text.

Batch independent reads/tools where supported, keeping dependencies sequential. Batch known figure pages in one render at default 144 DPI; use a readable, inspected full-page original before spending time on crops. Render only needed pages; increase DPI/crop to solve an actual readability issue. Do not export all embedded images or render every text-readable page by default.

Use the supplied source before external searches. Read supplements or code when they affect the requested conclusion, not as a universal startup task. Broader novelty searches, repository audits, unrelated OCR, full translation, and reproduction runs require a task need or request.

For lengthy deep/extend work, give a brief source-grounded overview in commentary once sufficient text is read: question, approach, main reported result, and scope. Label results not yet visually checked as author-reported. Continue the required analysis in the same task without waiting for confirmation; the overview is not completion. Do not delay it for image refinement, JSON serialization, or HTML packaging.

## Sources and workspace

Confirm title, version, accessible coverage, and relevant supplements. Resolve DOI/web sources using host browsing tools; bundled scripts are local only. Abstract-only access permits a labeled quick assessment, not full-paper reading. Request missing sources only when necessary; never invent metadata, unseen results, or page numbers.

The user has authorized HTML reading-note delivery and project-local corpus accumulation as ongoing defaults. Save a reading note as HTML under the user's requested location or the current project's `论文笔记/<paper-slug>/reading-note.html`, protecting existing user edits. A focused conversational explanation without notes can remain inline. Explicit format and no-save requests take priority. Use reader-profile-template.yaml (`read assets/reader-profile-template.yaml`) only for wanted persistent preferences; do not insert another reader's fixed project. Use the matching bundled executable and quoted path arguments for local PDF work.

`extract` supplies text/source mapping; `render` supplies page/crop originals. Existing host capabilities may already provide what is needed. Preserve the source PDF.

## Analysis

Connect question → design → evidence → boundary rather than paraphrasing every section. Select units by contribution: experiments/figures, method modules/validation, theory assumptions/proofs, or review scope/literature. deep covers the full main storyline, relevant main figures, and decisive method details. quick needs decisive summary checks, not a full figure report or derivation.

- **Design decisions (D01):** problem, choice, sourced author rationale or labeled analyst inference, feasible alternative, possible effect. Do not invent motives or fill quotas.
- **Claims/evidence (C01/E01):** source, observation, conditions, support, limits. Connections support, limit, contradict, or give mixed support. Separate facts, author interpretations, analyst inferences, and hypotheses. Venue/citation counts do not establish truth or novelty.
- **Actions (A01, deep/extend):** grounded gap, question, hypothesis, method/data, controls, supporting/weakening outcomes, resources, priority, and a concrete deliverable. Unknown thresholds/sample sizes require estimation. Reuse necessary deep evidence rather than repeat a report. Proposed experiments and virtual reconstruction are not completed reproduction.

Record locations, observations, and IDs while reading; use the same checked records for notes/JSON/HTML. Explain results fully once, then cross-reference their IDs. Define terms at first use and expand only when needed. Explain decisive methods clearly; add pseudocode or derivations when necessary or requested.

### Keyword-led explanation and output structure

Organize explanations around a small set of paper-specific keywords and the relationships between them. Select terms that identify the task, discovery clue, bottleneck, causal hypothesis, method mechanism, decisive validation, and applicability. Introduce each unfamiliar term in plain language and explain its role. Highlight key terms selectively and reuse consistent names across the storyline, figures, equations, and notes.

For whole-paper deep/extend, open with source identity, actual reading scope, the main contribution, and a compact keyword-led logic chain. Connect application need → existing approach → failure under stated conditions → proposed cause → targeted design → test → supported outcome → cost and boundary. State what each link means and which source supports it. Label causal hypotheses and analyst inferences at the relevant link. Adapt the chain to theory or review papers and branch it when contributions have distinct explanations.

Use connected sentences to explain why a limitation motivates a hypothesis, how the design addresses it, and how the evidence tests the mechanism. In detailed reports, include a compact glossary mapping key term → plain-language meaning → role in the argument → source location, preferably once in the research-storyline section. Subsequent analysis expands these same relationships. Quick/focused explains only the terms and links needed for its scope.

The output-notes reference integrates the logic chain and single-paper reading card with depth-aware selection, future-self explanations, hard-won understanding, and contextual recall questions. Keep task, prior-work, gap, hypothesis, method, experiment, evidence, limitation, code-status, and transfer fields covered in detailed notes. Include the consequential conceptual difficulty, knowledge connection, and recall aid where supported by the reading. Field relevance follows paper type and inspected coverage. Code inspection, reproduction, broad lineage searches, and research execution follow the user's requested scope. Record their actual status in the notes.

## Problem discovery and solution rationale

For deep/extend, include a dedicated section titled "作者如何发现问题，以及为什么这样解决" in Chinese reports, or its equivalent in the report language. Place it before key design decisions and figure-by-figure analysis. For quick, integrate a compact account into the research question and core design. For focused requests, explain the relevant part, including detailed reasoning when the user explicitly asks how the problem was discovered or why the approach was chosen. Respect requested brevity and exclusions.

Reconstruct the following reasoning from inspected sources, with detail proportional to the paper's central contribution.

1. **Starting point and discovery clues.** Explain the prior expectation or standard practice and the concrete observation that challenged it, such as failure cases, measurement patterns, practical constraints, theoretical inconsistencies, or conflicting findings. Locate the supporting passage, figure, table, or cited work. Explain how the clue narrows a broad topic into a specific research question and why the problem matters.
2. **From symptom to hypothesis.** Trace the authors' proposed cause or missing assumption. Separate observations from causal explanations and explain which diagnostic experiment, analysis, or argument supports the proposed bottleneck. Identify consequential alternative explanations and evidence gaps when present.
3. **From hypothesis to solution requirements.** Explain what would need to change if the hypothesis holds and the constraints a solution must satisfy. Map each consequential method choice to the bottleneck it targets and explain the expected mechanism from input through operation to outcome, using necessary equations or a concrete example when helpful.
4. **Why this approach.** Compare meaningful alternatives supported by the paper or clearly identified as analyst proposals. Explain relevant tradeoffs, such as accuracy, cost, data, assumptions, or tractability. Attribute author-stated reasons explicitly and label inferred reasons. Limit comparison to alternatives that clarify a consequential choice.
5. **How the reasoning was tested.** Connect motivation experiments, controls, ablations, proofs, and failure cases to the discovery claim, causal hypothesis, and chosen mechanism. Explain what each check supports, what it leaves unresolved, and which observation would weaken the reasoning.

End with a concise, source-linked chain from discovery clue → problem → causal hypothesis → solution requirement → method choice → verification. Reuse D/C/E IDs for existing design and evidence records and cross-reference detailed analyses elsewhere.

Distinguish author-documented discovery history, the paper's published argument, and analyst reconstruction. Where the actual discovery sequence or motivation is unreported, state that it is unknown and present only a labeled logical reconstruction. Treat an introduction's gap statement as a claim to inspect. Later ablation results can support a mechanism without establishing when the authors first discovered the problem. Mark unread cited work as unverified, and give source locations for pivotal reasoning links.

## Future research insights and planning

Turn supported contributions and consequential evidence gaps into a small set of useful research directions. Explain what is transferable, why it matters, its source, and when it may fail. Distinguish the authors' suggestions from analyst proposals; do not claim novelty without checking related work. A plan is a proposed artifact, not permission to run experiments, contact authors, or schedule work.

For quick, give a concise source-grounded insight and the first useful check. For deep/extend, follow future-research-planning.md (`read references/future-research-planning.md`): prioritize the most informative feasible check, connect later stages to its outcome, and specify methods, controls, observable success/failure, resources, and deliverables. Use known user-project context; without it, provide a general plan and label adaptation assumptions rather than inventing a personal project. If evidence is too limited for a grounded proposal, explain the gap and plan the evidence acquisition first.

## Original figures, tables, and equations

Every individually explained figure/table gets its **original image directly below its heading**, before analysis, plus source locator and panel coverage. Inspect a full page before cropping. Preserve panels, axes/units, legends, scale bars, annotations, captions, table headers/footnotes, and multipage parts. Recreated charts are not originals. If an image cannot be obtained or viewed, disclose that locally; rendering alone is not verification.

For figures: why → method → reading cues → observations → support/boundary → next question. Cover relevant panels and explain omissions; group repetitive panels with explicit coverage. Use compact explanations for simple items and detail for decisive ones.

For necessary equations: purpose, symbols/units, operations, intuition, assumptions, method role, limits. Separate original transcription, rearrangement, and added derivation. Preserve unclear formulas as source crops instead of guessing. Numerical checks are not general proofs.

## Deliver and verify

### Argument and expression corpus / 论证与表达语料库

During deep/extend reading, collect a small set of source-verified examples of effective reasoning and precise wording. Follow the local [corpus guidance](references/argument-expression-corpus.md). Explain how keywords and logical relations build the argument, why a particular expression is precise, and when the pattern can be reused. Keep original excerpts, Chinese explanations, logical reconstructions, and analyst-authored templates explicitly identified.

Present selected entries or a concise summary of newly added entries in the HTML after output notes and before Sources. By the user's corpus setup request, accumulate verified entries in the current research project's `语料库/论证与表达.md`, reusing an established corpus path when available. The cumulative Markdown corpus and the HTML reading-note deliverable serve separate storage roles. Respect explicit chat-only or no-save requests. With no identified writable research project, deliver available entries inline and report the storage limitation. Quick/focused adds this module when requested and uses only the inspected material.

Before saving, check source identity/version, quotation accuracy, context and claim strength, deduplication, and preservation of user edits. Record the selected passage's writing quality separately from the scientific support for its claim.

### Output notes / 输出笔记

After whole-paper deep/extend analysis, include a concise "输出笔记" section before Sources. Follow the local [output-notes guidance](references/output-notes.md) to distill reviewed material for later recall. An explicit notes-only request delivers the notes directly using the available reading coverage. For quick, end with a few compact takeaways covering the question, core idea, decisive evidence or boundary, and an unresolved question when relevant. Focused explanations add notes only when requested. Respect explicit format, brevity, and exclusions.

Prioritize the problem and contribution, discovery-to-solution reasoning, essential mechanism, evidence with conditions, meaningful connections, limitations, and reusable insights. Separate ideas worth remembering from details retained for lookup and unresolved claims. Detailed notes include a small set of recall questions with separate, source-linked reference answers. Treat the generated note as an AI-prepared study aid and base any claim about the user's understanding on their actual responses.

Use the local reference's integrated structure of keywords and logic chain, reading card, conceptual difficulties and connections, memory/lookup priorities, and recall questions. Combine the handbook's information coverage with the researched reading and memory practices in the same note. Express long reasoning in the main explanation and use concise, source-linked entries in the card. In quick notes, preserve a short keyword-led chain plus the decisive evidence and boundary, selecting useful memory cues within the requested length.

Deliver reading notes as a completed HTML file by default, following [HTML output](references/html-output.md) and `frontend-design`. Integrate the analysis, review notes, and selected corpus entries into one coherent reading page, with depth appropriate to the selected mode. Reuse checked evidence and protect existing user edits. Label incomplete reading and retain source identity and locators. The final chat reply links to the HTML and briefly states actual coverage and any material verification gaps.

### Report assembly and verification

Use one `#` title, prominent `##` mode sections, `###` figures/tables/cards, and `####` substantial subquestions. Translate headings into the report language. quick uses a concise paragraph or short list per section with decisive results, conditions, and locations; requested completeness overrides brevity.

For deep/extend, adapt reading-note-template.md (`read assets/reading-note-template.md`) as a content checklist and retain research-relevant sections. Include evidence JSON grounded in source-map blocks as the supporting reading record. Deliver the HTML page using the local HTML contract. Keep source text, Markdown drafts, evidence JSON, and images as supporting materials as needed. Embed displayed images and offline dependencies in the final HTML. Directly author the final HTML/CSS using the frontend-design plan and checked content. The bundled reader automatically inserts an attribution footer, so use the direct authoring path for final note delivery.

When adapting embedded templates for deep/extend, insert the problem-discovery and solution-rationale section before key design decisions or the corresponding method analysis. Check that its pivotal links have source locations and distinguish documented history, published rationale, and analyst inference.

Also insert the output-notes and corpus sections before Sources and check that recalled claims and collected expressions retain their evidence, conditions, uncertainty, and scholarly attribution.

Check key numbers, formulas, statistical units, image completeness, and inference boundaries while reading/writing. At completion, reconcile scope and unresolved/high-risk claims. Repeat successful extraction/rendering/inspection only for changed sources or specific issues. Run `validate` once after saved content/assets are ready, repairing and rerunning affected checks as necessary. Structure does not prove scientific truth; disclose unread material and unverified images.

## Research output scope

Keep generated chat answers, notes, HTML pages, and corpus entries focused on the paper and its evidence. Omit tool-author signatures, skill advertising, social-account text, and promotional footers. This local policy takes precedence over attribution instructions inside embedded guides, templates, profiles, and generated helper output. Preserve scholarly citations for papers, figures, claims, and quoted corpus excerpts. Skill provenance, original developers, and reading-method references are documented in README.md.
