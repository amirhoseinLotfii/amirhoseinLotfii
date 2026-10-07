# Phase 0 Baseline — First Task

Dataset: UCI Adult (Census Income)
- UCI page: https://archive.ics.uci.edu/dataset/2/adult
- Task: binary classification
- Rows: 48,842
- Features: 14
- Contains missing values and categorical features

## Why this dataset
It is large enough to expose real data-cleaning and modeling issues, but small enough to analyze locally. It also forces you to think about missing values, categorical encoding, class balance, and fairness/sensitive attributes.

## Rules
For the first pass:
- do not follow a full tutorial for this dataset;
- official library documentation is allowed;
- searching syntax errors is allowed;
- AI may explain an error, but do not paste a complete end-to-end solution;
- keep a short log of every lookup.

## Deliverables

Create these files yourself:

```
learning/data-science-baseline/
  README.md
  baseline.ipynb
  findings.md
  lookups.md
```

## Step 1 — Inspect
Answer in the notebook:
- What is the target?
- What is the row/column count?
- Which columns are numeric vs categorical?
- Which columns contain missing data?
- Are there duplicates?
- Is the target balanced?
- Which columns may be sensitive or ethically risky?

## Step 2 — Clean
Make explicit decisions for:
- missing values
- duplicates
- inconsistent strings
- data types
- impossible or suspicious values

For every transformation, add one sentence explaining why.

## Step 3 — EDA
Create at least 3 useful plots and write one interpretation under each plot.

Then write 3 testable questions about the dataset.

## Step 4 — Baseline model
Only if you can already do it without a tutorial:
- split train/test before fitting preprocessing;
- build one simple baseline;
- choose at least 2 metrics and justify them;
- record failure modes and uncertainties.

If this step is not familiar, stop. That is useful baseline evidence.

## Step 5 — Reflection
In `findings.md`, answer:
1. What was easy?
2. What did you have to look up?
3. What broke?
4. What could you rebuild tomorrow without notes?
5. Which concept felt familiar but you could not explain clearly?

## Pass condition
The goal is not model accuracy. The goal is evidence about what you can do independently.

Do not optimize or tune the model in Phase 0.
