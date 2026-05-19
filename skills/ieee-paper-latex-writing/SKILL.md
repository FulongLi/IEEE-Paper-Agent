---
name: ieee-paper-latex-writing
description: Write, revise, audit, and prepare IEEE-style research manuscripts in LaTeX. Use when the user asks for help with IEEE conference papers, IEEE Transactions or journal articles, IEEE Access/Open Journal manuscripts, LaTeX paper templates, abstracts, introductions, related work, methods, experiments, figures, tables, equations, BibTeX/citations, reviewer responses, or publication-readiness checks for top-tier scientific papers.
---

# IEEE Paper LaTeX Writing

## Overview

Turn research results into a publishable IEEE manuscript and keep the LaTeX source submission-safe. Optimize for a clear scientific story, defensible claims, reproducible evidence, and IEEE-compliant typography.

## Workflow

1. Identify the target venue and template before editing.
   - Use `IEEEtran` conference mode for conference proceedings.
   - Use `IEEEtran` journal/lettersize mode for Transactions and journals.
   - Use the venue-specific class for IEEE Access and open journals when provided.
   - In this repo, inspect the matching folder under `IEEE paper Template/` before changing class options or author metadata.

2. Extract the paper's spine before drafting.
   - One-sentence thesis: "We solve X for Y by Z, improving A under B."
   - Gap: what prior work cannot do, not merely what it has not tried.
   - Contributions: 2-4 concrete claims that can be verified by sections, figures, or experiments.
   - Evidence: each contribution needs a method detail, experiment, ablation, theorem, dataset, or qualitative analysis.
   - Boundary: state assumptions and limitations precisely enough to prevent overclaiming.

3. Draft from argument to prose.
   - Start with title, contribution bullets, figure/table plan, and section outline.
   - Write the Introduction as a funnel: problem importance, technical barrier, gap in existing work, core idea, evidence and contributions.
   - Write Methods for reproducibility, not narrative charm.
   - Write Experiments around research questions, baselines, metrics, ablations, and failure cases.
   - Write Related Work as a taxonomy that positions the paper, not as a citation dump.

4. Edit for IEEE style and reviewer trust.
   - Prefer active, specific claims: "Our method reduces latency by 18.4%" over "The results are promising."
   - Tie every strong claim to a number, figure, table, theorem, or citation.
   - Use cautious language for generalization: "in our benchmark", "under the tested workloads", "for this class of systems".
   - Define acronyms on first use in the abstract and again in the main text if needed by the venue template.

5. Make LaTeX changes conservatively.
   - Preserve the official class file, margins, fonts, column widths, and bibliography style unless the venue instructions explicitly require a change.
   - Use semantic cross-references: `\label`, `\ref`, `\eqref`, `\cite`.
   - Put figure/table `\label` commands after or inside the corresponding `\caption`.
   - Avoid hard-coded equation numbers, manual spacing hacks, and `eqnarray`.
   - Keep figures, tables, algorithms, and equations close to first reference when possible, but let floats float.

6. Validate before calling the manuscript ready.
   - Compile from a clean state and inspect warnings, missing references, overfull boxes, undefined citations, and font substitutions.
   - Check page limits, abstract word limits, keyword format, author metadata, funding notes, copyright lines, and anonymization rules.
   - Confirm every figure is readable in two-column PDF scale and every table has units, baselines, and statistical context where relevant.

## Task Patterns

For a new paper, produce in this order: thesis, contribution list, outline, figure/table plan, then section drafts.

For rewriting, preserve the user's technical meaning but improve the argument structure, specificity, and IEEE tone. Do not invent results, baselines, datasets, or citations. Mark missing evidence explicitly.

For LaTeX debugging, first identify the class/template and compiler path, then inspect only the relevant source, log, bibliography, and figure declarations. Prefer small source edits over template rewrites.

For publication audit, review both manuscript quality and LaTeX readiness. Lead with blocking issues, then high-impact improvements, then minor style fixes.

For reviewer responses, build a response matrix: reviewer concern, manuscript action, exact location changed, and concise response text. Keep responses respectful, evidence-based, and traceable to edits.

## References

Load these only when the task needs more detail:

- `references/writing-playbook.md`: section-by-section writing heuristics for strong IEEE research papers.
- `references/latex-submission-checklist.md`: IEEE LaTeX, figures, equations, citations, and pre-submission checks.
- `references/reviewer-response.md`: revision and rebuttal workflow for peer review.

## Output Standards

When writing manuscript text, return polished paper-ready prose unless the user asks for notes. When auditing, separate "must fix before submission" from "quality upgrades". When editing LaTeX files, keep diffs narrow and explain any venue-sensitive assumptions.
