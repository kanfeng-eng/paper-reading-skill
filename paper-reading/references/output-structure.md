# Detailed note consolidation after reading

## Prominent report headings

Use one `#` report title. Put each major output under its own `##` heading with blank lines around it. Use `###` for individual figures, tables, theorems, decisions, claims, or actions; use `####` for explanatory questions inside an item. Bold inline labels may identify fields but must not substitute for major headings. In HTML, keep the main sections visually distinct and include them in the table of contents.

The outlines below organize the detailed final notes after the agreed reading dialogue is complete. Follow [guided-reading.md](guided-reading.md) for live interaction and progress. Consolidate only actual discussion-derived research insights and corpus items, labeling their states. An explicit direct-output or partial-note request defines its own scope.

### quick

Use separate `##` headings for **Research question**, **Core design**, **Key results**, **Evidence gaps**, **Future research insights and next steps**, and **Reading priority**. Keep the insights/steps section compact; omit it for an explicit summary-only request or a strict scope constraint. Open with a concise recommendation if helpful. Explain whether to read closely, read selectively, use as background, or defer, in relation to the user's goal.

### deep

Use separate `##` headings for **Core assessment and reading scope**, **Full research storyline**, **Key design decisions**, **Figures and tables, item by item** (or **Key theorems and proofs**), **Necessary equations**, **Evidence cards**, **Open questions and unread material**, **Future research insights**, **Next-step research plan**, and **Sources and reading record**. The final two analytical sections are default outputs unless the user excludes extensions. Follow [future-research-planning.md](future-research-planning.md); connect the plan to checked evidence and identify the first useful action. Each figure/table gets its own `###` heading and an original image directly underneath, followed by explanation. Do not bury equations inside a figure paragraph when they require substantial explanation.

### extend

Establish the necessary deep evidence, reusing an existing verified reading when available. Then add separate `##` headings for **Future research insights**, **Transfer conditions**, **Reproduction checklist**, **Research action cards**, and **Prioritized research roadmap**. Explain differences between the paper's conditions and the user's project, prerequisites, missing resources, controls, and observable outcomes. The roadmap orders actions by dependencies and evidence value, with deliverables, milestones, and stop/pivot conditions; it references action cards rather than repeating them. If no grounded action is available, state why and prioritize acquiring the necessary evidence rather than inventing advice.

### focused

Use a clear `##` heading naming the requested figure, table, equation, or passage, then only the necessary **Context**, **Explanation**, and **Evidence boundary** subheadings. For a figure/table, insert its original image immediately below the item heading. Do not generate a whole-paper report for a local question.

## Deliver the useful content early

An explicit brief summary can use quick. Unqualified whole-paper reading/analysis starts guided deep reading. The final report follows the completed dialogue scope, including discussed future insights and plans with their actual status. Explicit batch requests can deliver the requested report directly. HTML delivery follows html-output.md; individually explained figures use inspected region crops.

In guided work, teach one source unit and wait for the learner's response. After the completion gate is met, assemble detailed final notes with the full reasoning chain, necessary derivations, meaningful questions and corrections, and the research-plan and corpus discussion results. Explicit batch delivery may provide progress updates while completing its requested report.

Explain each result thoroughly once and use C/E/D/A cross-references in subsequent cards instead of repeating whole explanations. Group similar panels while naming coverage. Avoid repeating definitions and generic caveats. Build saved Markdown/evidence and requested HTML from the same checked content; do not independently rewrite the scientific analysis for each format. Run the note validator after content/assets are ready, not after every paragraph or image.

## Original images next to explanations

For every figure or table explained individually, embed the original source image in that item's section before the analysis. Include a source line giving figure/table number, panel coverage, PDF page or web locator, and source-block ID when available. Figures and tables discussed only as brief cross-references do not need duplicate images; link to their explanation instead. All substantially explained main figures/tables need an image or an explicit local missing-image disclosure.

For saved notes, use inspected figure/table-region crops such as assets/figures/fig-1.png, and embed them in HTML. Preserve all panels and captions, splitting large tables into ordered readable parts. Full-page renders remain internal locating assets. Follow [figure-and-equation-reading.md](figure-and-equation-reading.md).

## Delivery and verification

An explicit direct quick/focused explanation can remain conversational. Guided requests retain their turn-by-turn interaction. Final deep/extend notes include evidence JSON; comparisons identify each paper's sources and IDs. If no viable action emerged from the discussion, explain the gap and record action_status.

```text
"<reader-executable>" validate "<output>/reading-note.md" --mode deep --evidence "<output>/evidence.json" --source-map "<output>/source/source_map.json"
```

Repair broken links and source references. If source material is unavailable, change its inspection status and disclose the gap; do not invent sources to pass validation. Check version, numbers, symbols, statistical units, original images, inference labels, and grounds for actions during analysis. At delivery, resolve outstanding checks and validate structure; do not repeat completed inspection steps without a new issue. State completed scope and material unfinished items at delivery.

Final HTML follows [html-output.md](html-output.md), including direct authoring, offline assets, scientific citations, and delivery checks.
