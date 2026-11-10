# Report structure

## Prominent report headings

Use one `#` report title. Put each major output under its own `##` heading with blank lines around it. Use `###` for individual figures, tables, theorems, decisions, claims, or actions; use `####` for explanatory questions inside an item. Bold inline labels may identify fields but must not substitute for major headings. In HTML, keep the main sections visually distinct and include them in the table of contents.

The following outlines name the main outputs, not mandatory filler. Translate their headings into the user's report language, adapt them to paper type, and omit unsupported or irrelevant material with an explanation where it affects coverage. Do not present the four modes as four report sections; use the outline for the selected task.

### quick

Use separate `##` headings for **Research question**, **Core design**, **Key results**, **Evidence gaps**, **Future research insights and next steps**, and **Reading priority**. Keep the insights/steps section compact; omit it for an explicit summary-only request or a strict scope constraint. Open with a concise recommendation if helpful. Explain whether to read closely, read selectively, use as background, or defer, in relation to the user's goal.

### deep

Use separate `##` headings for **Core assessment and reading scope**, **Full research storyline**, **Key design decisions**, **Figures and tables, item by item** (or **Key theorems and proofs**), **Necessary equations**, **Evidence cards**, **Open questions and unread material**, **Future research insights**, **Next-step research plan**, and **Sources and reading record**. The final two analytical sections are default outputs unless the user excludes extensions. Follow [future-research-planning.md](future-research-planning.md); connect the plan to checked evidence and identify the first useful action. Each figure/table gets its own `###` heading and an original image directly underneath, followed by explanation. Do not bury equations inside a figure paragraph when they require substantial explanation.

### extend

Establish the necessary deep evidence, reusing an existing verified reading when available. Then add separate `##` headings for **Future research insights**, **Transfer conditions**, **Reproduction checklist**, **Research action cards**, and **Prioritized research roadmap**. Explain differences between the paper's conditions and the user's project, prerequisites, missing resources, controls, and observable outcomes. The roadmap orders actions by dependencies and evidence value, with deliverables, milestones, and stop/pivot conditions; it references action cards rather than repeating them. If no grounded action is available, state why and prioritize acquiring the necessary evidence rather than inventing advice.

### focused

Use a clear `##` heading naming the requested figure, table, equation, or passage, then only the necessary **Context**, **Explanation**, and **Evidence boundary** subheadings. For a figure/table, insert its original image immediately below the item heading. Do not generate a whole-paper report for a local question.

## Deliver the useful content early

For an unqualified summary request, use quick. Give a concise paragraph or short list under each relevant heading, with decisive results, conditions, source locations, and a compact future insight/next step unless excluded. For an unqualified whole-paper analysis request, use deep with future insights and a next-step plan. Keep quick concise, with detailed derivations and full evidence records reserved for the requested scope. HTML delivery follows html-output.md. A separately explained figure/table still requires its original image.

In lengthy deep/extend work, give a short, source-grounded initial overview before image refinement, evidence serialization, or packaging. State coverage and whether results are only author-reported; continue all requested reading in the same task. The final report still contains the required detailed sections and original visuals. If the user requests a single saved report, place the concise overview first in that report and keep progress commentary brief.

Explain each result thoroughly once and use C/E/D/A cross-references in subsequent cards instead of repeating whole explanations. Group similar panels while naming coverage. Avoid repeating definitions and generic caveats. Build saved Markdown/evidence and requested HTML from the same checked content; do not independently rewrite the scientific analysis for each format. Run the note validator after content/assets are ready, not after every paragraph or image.

## Original images next to explanations

For every figure or table explained individually, embed the original source image in that item's section before the analysis. Include a source line giving figure/table number, panel coverage, PDF page or web locator, and source-block ID when available. Figures and tables discussed only as brief cross-references do not need duplicate images; link to their explanation instead. All substantially explained main figures/tables need an image or an explicit local missing-image disclosure.

For saved notes, keep images inside the note output directory, such as `assets/figures/fig-1.png`, and use relative Markdown links. For chat, use the host's native image display or an absolute local path that actually renders; filenames alone are insufficient. For multipage tables or figures, show all parts in order. Do not replace source images with recreated charts or tables. See [figure-and-equation-reading.md](figure-and-equation-reading.md) for capture and inspection rules.

## Delivery and verification

quick/focused can be answered directly. Saved deep/extend notes include evidence JSON; comparisons identify each paper's sources and IDs. If extend yields no viable action, explain why and record `action_status` rather than inventing one.

```text
"<reader-executable>" validate "<output>/reading-note.md" --mode deep --evidence "<output>/evidence.json" --source-map "<output>/source/source_map.json"
```

Repair broken links and source references. If source material is unavailable, change its inspection status and disclose the gap; do not invent sources to pass validation. Check version, numbers, symbols, statistical units, original images, inference labels, and grounds for actions during analysis. At delivery, resolve outstanding checks and validate structure; do not repeat completed inspection steps without a new issue. State completed scope and material unfinished items at delivery.

Final HTML follows [html-output.md](html-output.md), including direct authoring, offline assets, scientific citations, and delivery checks.
