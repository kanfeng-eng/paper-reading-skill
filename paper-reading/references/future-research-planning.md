# From a paper to future research insights and a plan

## Scope and depth

In guided deep/extend reading, develop future research insights and the next-step plan in conversation before final note consolidation. Introduce one grounded direction at a useful point, listen to the learner's interpretation, and refine it with their actual goals and constraints. Explicit direct-output requests may instead receive labeled AI proposals.

Use checked evidence and the learner's actual responses. Identify author suggestions, AI proposals, learner ideas, revisions, accepted priorities, rejected routes, and unresolved assumptions. In final notes, consolidate the discussion faithfully and mark topics that were skipped or not discussed.

## Future research insights

Select directions by scientific value, evidence support, and feasibility rather than filling a fixed quota. A deep report will often benefit from two or three strong directions, but fewer are better than unsupported ideas. Look for:

- A supported method or design principle that could transfer to another setting.
- A limitation or alternative explanation whose resolution would change the main conclusion.
- A new hypothesis suggested by a result pattern or unresolved comparison.

For each direction, connect **source result/gap → research insight → why it matters → transfer conditions → testable next question**. Cite the original section, figure, or E ID. Say whether the idea comes from the authors or is an analyst proposal. Explain both applicability and likely failure conditions. Distinguish established evidence, inference, and an untested hypothesis.

Avoid generic recommendations such as “use more data,” “combine AI,” or “improve interpretability.” Identify which data or comparison is needed, what uncertainty it resolves, and what scientific conclusion would change. Do not claim a publishable or first-ever direction from reading a single paper; targeted related-work checking can be a planned prerequisite.

## Next-step research plan

In dialogue, compare candidate first actions with the learner using information value, prerequisites, cost, and feasibility. Ask about a resource constraint only when it changes the choice. In final notes, state the resulting priority and rationale, including remaining disagreement or unknowns. Link actions to A IDs and checked evidence. A planning table can use:

| Priority / stage | Question and hypothesis | Method and comparison | Deliverable | Decision and next step |
|---|---|---|---|---|
| First useful check | The uncertainty that matters most | Data, procedure, baseline/control | A concrete analysis, figure, dataset, or protocol | What supports/weakens the idea; what follows in each case |

Include resources and missing prerequisites in the table or nearby prose. For each substantive action, make clear:

- **Grounding:** result or gap and source/E IDs.
- **Question:** a testable hypothesis or explicitly exploratory question.
- **Execution:** required data, method, baseline or control, and validation design.
- **Decision:** observable supporting and weakening outcomes; justified metrics and thresholds if known.
- **Output:** a concrete deliverable that can be inspected.
- **Feasibility:** available/missing resources, dependencies, and why its priority is appropriate.

Unknown sample sizes, effect sizes, thresholds, compute budgets, or completion times need estimation. Do not invent improvement percentages or treat failure to reject a null hypothesis as proof of equivalence. For exploratory analyses, state which observations would justify a confirmatory test.

## Stage the work around decisions

Prefer stages tied to evidence and dependencies rather than an arbitrary calendar:

1. **Near term: establish the premise.** Obtain key missing material, verify labels and splits, reproduce a decisive baseline, or perform the smallest informative check. Deliver an evidence check or pilot result.
2. **Next: test the promising direction.** Run the controlled comparison or targeted validation only after its prerequisites are met. Deliver comparative results and an uncertainty assessment.
3. **Later: extend if supported.** Test external generalization, a mechanism, a new setting, or a practical application. State the earlier milestone that permits this stage; narrow or replace the direction if the premise fails.

These are adaptable stages, not mandatory three-part filler. In deep, a compact sequence is enough. Extend should clarify dependencies, milestones, stop/pivot conditions, and the first concrete task the reader can start. Provide calendar estimates only when the user asks or project information makes them useful, labeling estimates and assumptions. Never create schedules or execute the proposed work merely because a report includes a plan.

## Project fit and evidence boundaries

Use known project goals, datasets, skills and constraints. In guided discussion, ask about a missing condition when it changes the proposed test, then refine with the learner. Otherwise label a proposal as general and keep adaptation assumptions explicit. Do not infer user resources, experiments or affiliations from paper authors or filenames.

Preserve the paper's original sample unit and validation setting. Model-generated labels call for independent measurements when the goal is real-world accuracy; association-based findings call for suitable causal or mechanistic evidence when the proposed claim is causal. Adapt checks to the study type rather than applying every possible control.

## Deliver and check

During dialogue, use the headings 未来研究启示 and 下一步研究规划 when helpful, and summarize their actual development in the final note. Preserve the question, evidence, alternatives, user input, revision, test, controls, supporting/weakening outcomes, and next decision. Keep assumptions visible and distinguish planned work from completed experiments.

For saved deep/extend notes, record substantive proposals in `actions[]` using the existing action schema. Optional `priority`, `phase`, `dependencies`, `deliverable`, and `milestone` fields can retain planning details. If no grounded action is possible, record `action_status` and explain what evidence must be obtained first. Check that each proposal is traceable, feasible under its stated conditions, and has an observable outcome; structural validation does not establish scientific novelty or feasibility.
