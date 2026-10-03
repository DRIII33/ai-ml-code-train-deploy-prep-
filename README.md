# AI & Machine Learning: Code, Train & Deploy — Free-Tier Preparation Course

A structured, hands-on preparation course designed to mirror the provided **Skillspire AI and Machine Learning: Code, Train, & Deploy** syllabus week by week while giving the learner additional processable practice before entering the live course.

> **Current status:** Week 1 is implemented as a standalone Google Colab notebook. Weeks 2–16 are intentionally scaffolded so each week can be developed, completed, reviewed, and unlocked sequentially.

## Purpose

The goal is not to replace the source course. The goal is to remove avoidable friction from the course by giving the learner a repeatable environment in which to practice the underlying concepts before encountering them in class.

The preparation model is:

**Learn → Process → Practice → Debug → Challenge → Submit → Review → Advance**

Each week is treated as an independent learning unit. The learner completes that week's notebook, performs its independent work and assessment, submits the completed notebook for instructor-style review, and only then advances to the next week.

## Source Curriculum Alignment

The uploaded syllabus describes a 16-week hands-on AI/ML program covering data preprocessing, classical machine learning, deep learning, NLP, reinforcement learning, cloud platforms, deployment, and a capstone.

The preparation repository preserves the syllabus terminology and sequence.

### Syllabus sequence

| Week | Source syllabus focus                                                                                                          |
| ---: | ------------------------------------------------------------------------------------------------------------------------------ |
|    1 | Introduction to Data Science; Python Review; Variables and Data Types; Conditional Statements and Loops; Functions and Modules |
|    2 | Data Manipulation with Pandas; loading data; manipulation; aggregation/grouping; cleaning/preprocessing                        |
|    3 | Databases and APIs; SQL review; APIs; Python API access; JSON                                                                  |
|    4 | Project 1 — Data Wrangling and Analysis                                                                                        |
|    5 | Descriptive/inferential statistics; probability; distributions; statistical inference; hypothesis testing                      |
|    6 | Experimental design; sampling; power analysis; A/B testing                                                                     |
|    7 | Data visualization; Matplotlib; Seaborn; basic/advanced plots                                                                  |
|    8 | Regression; linear/logistic regression; multiple regression; model evaluation; L1/L2/Elastic Net                               |
|    9 | Project 2 — Exploratory Data Analysis and Visualization                                                                        |
|   10 | Classification; logistic regression; decision trees; random forests; Naive Bayes; evaluation                                   |
|   11 | Machine Learning with Scikit-Learn; supervised/unsupervised learning; model selection/evaluation; real-world ML                |
|   12 | Project 3 — Machine Learning Modeling and Evaluation                                                                           |
|   13 | Deep learning/neural networks; TensorFlow/Keras; training; tuning; deployment; prompt engineering                              |
|   14 | Advanced Data Science: time series; NLP; reinforcement learning; ethical AI/bias                                               |
|   15 | MLOps: versioning/reproducibility; CI/CD for ML; monitoring/maintenance                                                        |
|   16 | Final capstone presentation; report; findings; feedback/iteration; career/job readiness                                        |

**Note:** The source PDF prints Weeks 13–16 before Weeks 11–12 on the later pages. This repository uses the logical numeric order 1–16 for navigation while preserving the source week's topics. It does not silently change the underlying curriculum.

## Free-Tier Philosophy

The preparation course is designed to run primarily in free or low-cost learning environments:

* **Google Colab** for Python, statistics, ML and deep-learning exercises.
* **Google BigQuery Sandbox/free-tier usage** for SQL and larger analytical exercises when a week requires a database environment.
* **GitHub** for notebooks, source code, documentation, version control and portfolio organization.
* CSV/JSON/local synthetic data when an external service is unnecessary.

Week 1 requires no BigQuery account, GPU, API key or paid service.

## Repository Architecture

```text
ai-ml-code-train-deploy-prep/
│
├── README.md
├── ARCHITECTURE.md
├── LICENSE
├── .gitignore
│
├── notebooks/
│   ├── week01/
│   │   └── AI_ML_Code_Train_Deploy_Week_01_Preparation.ipynb
│   ├── week02/
│   ├── week03/
│   ├── week04/
│   ├── week05/
│   ├── week06/
│   ├── week07/
│   ├── week08/
│   ├── week09/
│   ├── week10/
│   ├── week11/
│   ├── week12/
│   ├── week13/
│   ├── week14/
│   ├── week15/
│   └── week16/
│
├── curriculum/
│   ├── rubrics/
│   └── checkpoints/
│
├── projects/
│   ├── project01_data_wrangling/
│   ├── project02_eda_visualization/
│   ├── project03_ml_modeling/
│   └── capstone/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── sample/
│
├── sql/
├── src/
├── tests/
├── config/
├── docs/
│   └── assets/
├── submissions/
│   └── week01/
└── .github/
    └── workflows/
```

## What Each Layer Does

### `notebooks/`

The primary student learning environment. **One standalone Colab notebook per week.**

A week notebook should be independently executable and should contain:

1. syllabus alignment;
2. learning objectives;
3. environment check;
4. lesson instruction;
5. runnable examples;
6. guided exercises;
7. prediction exercises;
8. debugging exercises;
9. independent challenges;
10. knowledge check;
11. practical assessment;
12. mastery self-assessment;
13. submission instructions;
14. explicit advancement gate.

### `curriculum/rubrics/`

Instructor-style evaluation criteria for each week.

Each rubric should distinguish:

* conceptual understanding;
* coding correctness;
* independent problem solving;
* debugging;
* code quality;
* data/ML reasoning;
* reproducibility;
* readiness for the next week.

### `curriculum/checkpoints/`

Short checkpoints that determine whether the learner should:

* **ADVANCE**
* **TARGETED REVIEW**
* **REPEAT**

### `projects/`

The three explicit projects and final capstone from the syllabus receive dedicated folders so their deliverables are not buried inside weekly practice notebooks.

### `data/`

Data is separated by lifecycle. Raw data should not be overwritten. Processed data should be reproducible from source data and code. Sample/synthetic data should be clearly labeled.

### `sql/`

SQL becomes important beginning in Week 3 and later project work. Queries should be version-controlled rather than trapped inside notebooks.

### `src/`

Reusable Python code belongs here once notebook work becomes repetitive or project-oriented.

### `tests/`

Validation and unit tests are introduced progressively. Early weeks can use simple assertions; later weeks should use more formal testing for pipelines and ML artifacts.

### `config/`

Environment-neutral configuration such as project identifiers, dataset names, random seeds, model settings, and paths. Secrets must never be committed.

### `submissions/`

This is the learner's evidence trail. A completed weekly notebook can be copied here when submitted for review. Review notes should be separate from the original learning notebook.

### `.github/workflows/`

Reserved for later reproducibility/CI demonstrations. Do not introduce CI/CD merely for appearance; it should be introduced when it supports the curriculum, especially around Week 15 MLOps.

## Weekly Notebook Contract

Every future weekly notebook should follow the same high-level contract.

```text
01 — Title / syllabus alignment
02 — Learning contract
03 — Environment setup
04 — Lesson 1
05 — Lesson 2
...
XX — Integrated laboratory
XX — Independent challenge
XX — Debugging challenge
XX — Knowledge check
XX — Practical examination
XX — Self-assessment
XX — Submission package
XX — Instructor review gate
```

The number of internal sections will vary by week; the learning lifecycle should not.

## Week Processing Model

### Step 1 — Open only the current week

Do not jump ahead. The repository is intentionally designed as a progression rather than a reference dump.

### Step 2 — Read the learning objectives

Know what capability the week is intended to develop.

### Step 3 — Execute the examples

Run the code, inspect the output, and change parameters.

### Step 4 — Complete `YOUR CODE HERE` cells

These are deliberately processable exercises. Do not treat them as optional.

### Step 5 — Complete debugging exercises

Diagnose the problem before viewing a corrected implementation.

### Step 6 — Complete the independent challenge

This is the first major test of transfer. A solution that only works when copied from an example does not demonstrate mastery.

### Step 7 — Complete the knowledge check

Answer conceptual questions without relying on execution alone.

### Step 8 — Complete the practical examination

This is the weekly readiness test.

### Step 9 — Calculate the mastery score

Use the weekly rubric and self-assessment.

### Step 10 — Submit the notebook

Upload the completed `.ipynb` for instructor-style review.

### Step 11 — Receive a gate decision

The review returns one of:

**ADVANCE** — proceed to the next week.

**TARGETED REVIEW** — repeat specific lessons/exercises, then resubmit.

**REPEAT** — redo the week's core work before advancing.

## Why the Gate Matters

The actual course is cumulative. Later topics depend on earlier skills.

For example:

```text
Python
  ↓
Pandas
  ↓
SQL / APIs
  ↓
Data Wrangling
  ↓
Statistics
  ↓
Experimentation
  ↓
Visualization
  ↓
Regression
  ↓
Classification
  ↓
Scikit-Learn
  ↓
Deep Learning
  ↓
Advanced DS
  ↓
MLOps
  ↓
Capstone
```

The purpose of the gate is therefore to prevent a weak foundation from being carried invisibly into later weeks.

## Week 1 — Current Implementation

`notebooks/week01/AI_ML_Code_Train_Deploy_Week_01_Preparation.ipynb` is the first completed notebook.

It contains **135 cells** and covers all Week 1 syllabus lessons:

* Introduction to Data Science
* Python Review
* Variables and Data Types
* Conditional Statements and Loops
* Functions and Modules

It additionally contains processable exercises for collections, type conversion, debugging, integrated transaction analysis, an independent mini-project, a knowledge check, a practical examination, mastery scoring, and an instructor-review submission gate.

### Week 1 constraint

Pandas is deliberately not used for the core Week 1 programming exercises. Pandas is a Week 2 syllabus topic. This keeps the preparation course cumulative rather than allowing later tooling to conceal Week 1 Python gaps.

## Mastery Model

Each skill is scored from 0–5:

| Score | Meaning                               |
| ----: | ------------------------------------- |
|     0 | Cannot do it yet                      |
|     1 | Can only copy it                      |
|     2 | Can do it with substantial guidance   |
|     3 | Can do it independently               |
|     4 | Can modify it and explain it          |
|     5 | Can teach it or solve a novel version |

The Week 1 notebook uses 22 skill dimensions for a maximum of 110 points.

Suggested advancement threshold:

* **85%+ and successful practical examination:** request Week 2 review.
* **70–84%:** targeted reinforcement before advancing.
* **Below 70%:** repeat the relevant Week 1 work.

The instructor review is the final gate; the self-score does not override observed performance.

## Submission Convention

Recommended pattern:

```text
submissions/
└── week01/
    ├── completed_notebook.ipynb
    └── reflection.md
```

For future weeks:

```text
submissions/week02/
submissions/week03/
...
submissions/week16/
```

Do not overwrite the canonical learning notebook with a student's submitted copy. Keep the original template intact.

## Git Workflow

Recommended progression:

```text
main
  │
  ├── week01-development
  │       ↓
  │   week01-complete
  │       ↓
  │   review
  │       ↓
  │   week02-development
  │       ↓
  │       ...
```

For a personal repository, a simpler workflow is also acceptable:

```text
main
  ├── completed Week 1
  ├── completed Week 2
  └── ...
```

The important rule is that the repository history should make progress visible.

## Reproducibility Rules

Every notebook should:

* state its environment assumptions;
* use deterministic seeds when randomness is involved;
* avoid hard-coded personal file paths;
* keep secrets out of GitHub;
* document external dependencies;
* make synthetic data visibly synthetic;
* explain when an external service is required;
* separate raw and processed data;
* preserve the original dataset when practical.

## Free-Tier Guardrails

The course should favor small, intentionally sized datasets for routine exercises. Larger datasets should be introduced only when the lesson requires them.

Do not create infrastructure merely to imitate production. Use the simplest free-tier component that teaches the intended concept.

For BigQuery exercises, the repository should document the expected dataset/table names and provide SQL that can be reproduced in a free-tier-compatible environment.

## Portfolio vs Preparation Work

This repository is primarily a **learning repository**. Not every exercise is expected to become a portfolio project.

The portfolio-quality outputs should be concentrated around:

* Project 1 — Data Wrangling and Analysis
* Project 2 — Exploratory Data Analysis and Visualization
* Project 3 — Machine Learning Modeling and Evaluation
* Final Capstone

The smaller weekly exercises exist to build the skills needed to execute those projects successfully.

## Expected Final State

At completion, the repository should demonstrate a progression from:

**Python fundamentals → data manipulation → SQL/API work → statistics → experimentation → visualization → regression → classification → ML engineering → deep learning → advanced data science → MLOps → capstone.**

The final repository should therefore tell a coherent story: not simply that notebooks were completed, but that the learner progressed from foundational programming to an end-to-end AI/ML workflow.

## Current Next Step

**Week 1 is the active gate.**

1. Open the Week 1 notebook in Google Colab.
2. Complete every `YOUR CODE HERE`, challenge, knowledge check and examination section.
3. Run the notebook from top to bottom and resolve errors.
4. Complete the self-assessment.
5. Submit the completed notebook for review.
6. Wait for the instructor-style decision: **ADVANCE**, **TARGETED REVIEW**, or **REPEAT**.
7. Only after an **ADVANCE** decision should the Week 2 notebook be generated/used.

## License / Attribution

This repository is a personal preparation environment built around the structure and topics of the provided course syllabus. It is not presented as an official Skillspire course or official Skillspire instructional material.
