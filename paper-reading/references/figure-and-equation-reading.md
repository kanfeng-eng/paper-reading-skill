# Reading figures, tables, and equations

## Capture and show the original

Each individually explained figure or table must appear as an original source image directly below its own heading, before the explanation. This applies to chat, Markdown notes, and HTML, including focused requests. A source locator or link alone is not a substitute when an image can be obtained. Keep original captions near the image, preserving their scientific wording; translations or commentary must be labeled separately.

For a local PDF, inspect the complete page internally to locate the actual figure/table and caption, then visually confirm the bounding box and crop that region with the available PDF renderer. Preserve all relevant panels, axes, units, legends, annotations, table headers, footnotes, and captions. Capture large or multipage tables as ordered readable crops. If the crop boundary is uncertain, inspect again or mark the crop unavailable; never embed a whole paper page as the figure.

For web papers, use the actual publisher/source figure or a faithful source screenshot available through the host. Inspect it and retain a traceable locator. Do not generate, redraw, recolor, or reconstruct a figure and label it as the paper's original. If an original is unavailable, state **Original image unavailable** in that item, give the reason and available locator, and limit the explanation to accessible text/captions. Missing visual access must not be labeled verified.

The packaged render command uses one-based pages and unrotated PyMuPDF page coordinates, with a top-left origin and points as units. Inspect render --help for the actual crop options. Confirm crop coordinates from the source map and internal full-page view. Preserve PDF fingerprint, page, bounding box, DPI, and path in a capture record. Inspect every delivered crop for completeness and legibility; rendering alone is not visual verification.

For saved notes, store source images within the output directory and embed them as, for example:

```markdown
### Figure 2 — Does the effect hold in an independent cohort?

![Original Figure 2, panels a–f](assets/figures/fig-2.png)

Source: Figure 2, PDF page 5, panels a–f and original caption; source block P0005.

#### Why was this done?

Explain the question left open by the preceding result.
```

Use the actual paper's numbering, page, coverage, path, and source ID; the example is only a format. In chat, use a native image display or a renderable absolute local path. If a table is too dense to read at once, include a complete original plus useful enlarged regions. An optional transcribed table supplements the original and must be checked against it.

## Efficient image handling

Locate figures/tables from source maps and inspect relevant pages in batches for internal preparation. Deliver region crops or original standalone figures. Increase DPI where axis labels, symbols, table cells, or captions need it.

Reuse matching-source crops and inspection records after checking identity and actual coverage. When a page contains several figures, produce a separate region crop for each individually explained item. A full-page render can remain an internal locating asset. Check that delivered images exclude unrelated body text and page furniture while preserving all scientific context.

## Six questions for a figure

1. **Motivation:** What did the previous result leave open, and how does this analysis follow?
2. **Method:** What data, samples/repeats, controls, interventions, statistics, and necessary parameters were used?
3. **How to read it:** Explain panel types, axes and units, colors, symbols, and reference groups.
4. **Observation:** Cover relevant panels and verifiable directions, numbers, effect sizes, and intervals. Label visually estimated values as estimates.
5. **Interpretation and boundary:** Distinguish measured, calculated, predicted, associated, and mechanistic/causal findings. Check alternative explanations, statistical units, and extrapolation.
6. **Next question:** What does this figure establish, what does it leave open, and why is the next analysis needed?

Group repetitive panels by scientific question while naming the covered panels. Include supplementary figures when they determine an important judgment, control, or reproduction requirement. Do not prescribe a fixed number of lines. Use `####` question headings when explanations are substantial.

## Tables

Show the original table image first. Check columns, units, bolding rules, missing values, aggregation, and comparison conditions. Explain what comparison the table supports and its limits. Differences in metric direction, budget, or uncertainty can make direct ranking invalid. Preserve all parts and footnotes of multipage tables.

## Equations

Explain purpose → symbols and units/dimensions → operations → intuition → assumptions → method role → implementation or derivation limits. Clarify indices, sums/expectations, normalization, and constraints. Label demonstration data as demonstrations.

Distinguish original transcription, equivalent rearrangement, and added derivation; state additional assumptions. Similar-looking symbols do not prove equivalence. Do not confuse a training objective, estimator, and evaluation metric. Numerical checks are not general proofs.

Use mathematical markup with an inspected offline renderer in the final HTML, or a clear crop of the original equation when transcription is uncertain. Explain important symbols and assumptions; a formula crop contains the equation itself and any indispensable adjacent definitions.
