# Data Science Roadmap 2026 — Amirhosein

> Goal: become capable of doing real, reproducible data-science work and then bridge into Applied AI / ML Engineering.
>
> Rule: one active track at a time. Do not open a new phase until the current quality gate is passed.

## Scope

### Core capability stack
1. Python for data work
2. NumPy + pandas
3. SQL for analysis
4. Probability & statistics fundamentals
5. Exploratory Data Analysis (EDA) + visualization
6. Classical machine learning with scikit-learn
7. Model evaluation, cross-validation, leakage prevention
8. Feature engineering + pipelines
9. Communication of findings
10. End-to-end reproducible project

### Later / parking lot
- Deep Learning / PyTorch
- Time Series
- NLP / LLMs
- Causal inference
- MLOps / production ML
- Spark / distributed computing

These are intentionally not part of the first active track.

---

## Phase 0 — Baseline & environment

### TODO
- [ ] Python diagnostic: functions, classes, typing, exceptions, iterators, comprehensions
- [ ] NumPy diagnostic: arrays, shapes, broadcasting, vectorization
- [ ] pandas diagnostic: filtering, groupby, merge, missing values, datetime
- [ ] SQL diagnostic: SELECT, JOIN, GROUP BY, CTE, window functions
- [ ] Statistics diagnostic: distributions, expectation, variance, sampling, confidence intervals, hypothesis tests
- [ ] ML diagnostic: train/validation/test, regression/classification, metrics, bias/variance, leakage
- [ ] Create one Jupyter notebook from a raw CSV and produce a clean analysis

### Quality gate
Given an unfamiliar tabular dataset, independently:
- load and inspect it,
- identify data-quality problems,
- clean it without destroying information,
- produce at least 3 useful plots,
- state 3 testable questions,
- explain every transformation.

---

## Phase 1 — Data manipulation + SQL

### Core
- Python only as needed for data work
- NumPy fundamentals
- pandas: indexing, groupby, merge/join, reshape, missing values, datetime, strings
- SQL: filtering, joins, aggregation, CTEs, subqueries, window functions

### Deliverable
A mini analysis using one public dataset:
- raw data
- cleaning notebook
- SQL queries
- EDA notebook
- README with findings

### Quality gate
- 15 non-trivial SQL queries
- 3 joins
- 3 CTE/subquery tasks
- 3 window-function tasks
- pandas analysis reproduces at least 5 SQL results
- no copy-paste solution code without explanation

---

## Phase 2 — Statistics + EDA

### Core
- descriptive statistics
- probability intuition
- sampling and uncertainty
- confidence intervals
- hypothesis testing
- correlation vs causation
- linear regression interpretation
- visualization and communication

### Deliverable
An EDA + inference report on a messy real-world dataset.

### Quality gate
You can explain and demonstrate:
- sampling variability
- confidence interval
- p-value and its limitations
- Type I / Type II errors
- when correlation is misleading
- why train/test splitting is not statistical inference

---

## Phase 3 — Classical Machine Learning

### Core models
- linear regression
- logistic regression
- decision trees
- random forests / gradient boosting
- k-nearest neighbors
- clustering basics
- regularization
- preprocessing pipelines

### Core evaluation
- train/validation/test
- cross-validation
- classification metrics
- regression metrics
- imbalanced data
- calibration intuition
- leakage
- baseline comparison
- error analysis

### Deliverable
One classification or regression project with:
- baseline
- preprocessing pipeline
- at least 3 model families
- cross-validation
- metric selection justified by product/business goal
- error analysis
- reproducible training script

### Quality gate
You can predict likely failure modes before running the model and diagnose underfitting, overfitting, leakage, bad metric choice, and unstable validation.

---

## Phase 4 — End-to-end Data Scientist project

### Project requirements
- real public dataset or API
- explicit problem statement
- data dictionary
- cleaning pipeline
- EDA
- statistical reasoning
- baseline model
- improved model
- evaluation
- interpretation
- limitations
- README
- reproducible environment
- simple report or dashboard only if it helps communicate the result

### Quality gate
A reviewer can clone the repo and reproduce the main result from documented steps.


---

## Phase 5 — Python → Go for AI Systems

### Why this phase exists
Python remains the primary language for data analysis, experimentation, model training, evaluation, notebooks, and the mainstream ML ecosystem. Go is added as the systems language for production services around AI/ML.

### Learn in Go
- syntax and project/module structure
- structs, interfaces, methods
- pointers and value/reference semantics
- error handling
- JSON and file I/O
- HTTP clients and servers
- context and cancellation
- goroutines and channels
- testing and benchmarks
- configuration and logging
- calling Python/ML services over HTTP/gRPC

### Do not migrate these from Python just for practice
- pandas/NumPy exploration
- scikit-learn training
- notebooks
- model experimentation
- PyTorch training

### Deliverable
Take one Python ML/AI project from an earlier phase and split it into:
- Python: model/data/evaluation layer
- Go: production API/service layer

Then implement:
- health endpoint
- prediction/request endpoint
- timeout/cancellation
- validation
- structured errors
- logging
- tests
- simple benchmark

### Quality gate
You pass this phase when you can independently:
1. explain why a component belongs in Python vs Go,
2. build a small Go service without copying a full tutorial,
3. call a Python model service or model endpoint,
4. handle timeout/error/retry cases,
5. write tests,
6. benchmark one hot path,
7. explain goroutine/channel usage without hand-waving.

### Estimated time
About 3–5 focused weeks at 10–15 hours/week, assuming general programming experience.


---

## Phase 6 — Specialization (choose only one)

Choose based on target jobs/projects:
- Product / experimentation data science
- NLP / text data
- Time series / forecasting
- Recommendation systems
- Computer vision
- Causal inference

Only one specialization should be active at a time.

---

# Resource hierarchy

## Core

### UC Berkeley Data 100
Use as the main map for the data-science lifecycle, data cleaning, EDA, inference and prediction.
- https://ds100.org/
- https://github.com/DS-100

### An Introduction to Statistical Learning with Applications in Python (ISLP)
Use for classical statistical learning and labs.
- https://www.statlearning.com/
- https://www.statlearning.com/resources-python

### DataTalksClub Machine Learning Zoomcamp
Use after the foundations for hands-on model building, evaluation and deployment.
- https://github.com/DataTalksClub/machine-learning-zoomcamp

## Just-in-time / drills

### Kaggle Learn
Use small modules only when a gap appears: pandas, SQL, data cleaning, visualization, intro/intermediate ML, feature engineering, explainability.
- https://www.kaggle.com/learn

### Official pandas docs
- https://pandas.pydata.org/docs/getting_started/intro_tutorials/

### Official NumPy docs
- https://numpy.org/doc/stable/user/absolute_beginners.html

### scikit-learn documentation
- https://scikit-learn.org/stable/user_guide.html

### SQLBolt
- https://sqlbolt.com/

### Google Machine Learning Crash Course
Use as a compact refresher for concepts and interactive exercises.
- https://developers.google.com/machine-learning/crash-course

## Strong references, not primary track

### Harvard CS109
Excellent framing around wrangling, EDA, prediction and communication, but much of the public material is older.
- https://cs109.org/
- https://github.com/cs109/content

### Stanford CS229
Rigorous ML theory. Use later when a mathematical gap blocks progress; do not make it the first course.
- https://cs229.stanford.edu/

### MIT 18.05 Probability and Statistics
Use selectively for probability/statistics gaps.
- https://ocw.mit.edu/courses/18-05-introduction-to-probability-and-statistics-spring-2022/

### Microsoft Data Science for Beginners
Good structured project-based beginner curriculum. Sweep selectively if the baseline shows basic gaps.
- https://github.com/microsoft/Data-Science-For-Beginners

### Python Data Science Handbook
Useful reference, but some original code targets an older Python stack. Prefer current official docs when APIs differ.
- https://github.com/jakevdp/PythonDataScienceHandbook

## Later / bridge to AI & ML Engineering

### Made With ML
Production-grade ML systems and software-engineering practices.
- https://github.com/GokuMohandas/Made-With-ML

### Full Stack Deep Learning
Use after classical ML foundations.
- https://fullstackdeeplearning.com/

### Dive into Deep Learning
Hands-on deep learning with code + math.
- https://github.com/d2l-ai/d2l-en

### MIT 6.S191
Compact university deep-learning course.
- https://introtodeeplearning.com/

---

# Repositories worth following

## High-confidence
- microsoft/Data-Science-For-Beginners
- DS-100/* (official UC Berkeley Data 100)
- DataTalksClub/machine-learning-zoomcamp
- GokuMohandas/Made-With-ML
- d2l-ai/d2l-en
- fastai/fastbook (later, deep learning)
- jakevdp/PythonDataScienceHandbook (reference)

## Do not use as the primary roadmap
Generic "2026 Data Science Roadmap" repositories can be useful for ideas, but authority, maintenance quality and pedagogy vary. Prefer official university/course repos and maintained industry curricula above.

---

# Time model

Assume 10–15 focused hours/week.

A realistic range is roughly:
- Phase 0: 2–5 days
- Phase 1: 2–4 weeks
- Phase 2: 3–5 weeks
- Phase 3: 5–8 weeks
- Phase 4: 3–5 weeks
- Phase 5 (Python → Go for AI Systems): 3–5 weeks

Total through the Data Science foundation + one strong end-to-end project: about 13–22 weeks depending on baseline and how much can be skipped.

Adding the Go systems transition brings the broader path to about 16–27 weeks before later specialization/AI-engineering depth.

This is not a promise of “job-ready” status; the gate is independent performance on unfamiliar data, not course completion.

---

# Study loop

For every capability:
1. Build
2. Explain
3. Debug
4. Rebuild from memory
5. Generalize to a new dataset

A concept is not complete until there is evidence: code, notebook, SQL query set, report, or a reproducible project.

---

# Current active track

**Phase 0 — Baseline & environment**

Do not start Phase 1 until the baseline gate is checked.
