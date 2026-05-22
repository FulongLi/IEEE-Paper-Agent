# Paper Production Workflow

Use this workflow after the idea has a clear paper plan.

## Stage 1: Create the Manuscript Workspace

1. Select the closest IEEE template.
2. Copy the template directory into a manuscript workspace.
3. Rename the main `.tex` file if desired.
4. Keep official `.cls`, `.bst`, font, and image assets unchanged unless the venue requires otherwise.

Recommended workspace layout:

```text
manuscripts/
└── paper-slug/
    ├── main.tex
    ├── refs.bib
    ├── figures/
    ├── tables/
    └── notes/
```

## Stage 2: Draft the Skeleton

Create the paper skeleton before full prose:

- title
- abstract placeholder
- keywords
- section headings
- contribution bullets
- figure/table placeholders
- citation placeholders
- experiment checklist

## Stage 3: Draft in Evidence Order

Recommended order:

1. Method or system section
2. Experiment setup
3. Results
4. Introduction
5. Related Work
6. Abstract
7. Conclusion

This order keeps the Introduction and Abstract honest because they are written after the evidence is visible.

## Stage 4: IEEE Style Pass

Check:

- claims are specific and evidence-linked,
- acronyms are defined,
- figures are referenced and readable,
- tables include units and metric direction,
- equations define all symbols,
- citations support related work and technical claims,
- limitations are stated without weakening the contribution unnecessarily.

## Stage 5: LaTeX Submission Pass

Use:

```text
skills/ieee-paper-latex-writing/references/latex-submission-checklist.md
```

Check:

- clean compile,
- no undefined references or citations,
- no serious overfull boxes,
- correct page limit,
- correct author metadata,
- correct bibliography style,
- no template filler text,
- no local absolute file paths.

## Stage 6: Publication-Readiness Review

Review the manuscript as if acting as a strict IEEE reviewer:

- Is the novelty explicit?
- Is the baseline fair?
- Are claims supported by evidence?
- Are experimental conditions clear?
- Are figures and tables necessary and interpretable?
- Are limitations handled honestly?
- Would a reviewer know why the work matters?
