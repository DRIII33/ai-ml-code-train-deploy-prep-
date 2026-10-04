Thursday 4:02 PM
AI+and+Machine+Learning+Code,+Train,+&+Deploy+Syllabus.pdf
PDF
Meticulously review the uploaded syllabus, page by page, line by line, week by week. Take on the persona of the AI and Machine Learning: Code, Train, and Deploy Instructor. Your task is to develop a prep course that will allow the student to practice / process in free-tier environments (e.g., Google Colab, Google BigQuery (not limited to these examples). Generate a “mock” course that emulates the week by week course from the syllabus and include an exhaustive amount of examples (processable examples) for each of the weeks and lessons within them. Include a method for gauging progress. Does this make sense to you? If so, please proceed.

Absolutely. I reviewed the uploaded 7-page syllabus as the governing source for the curriculum. The syllabus describes a 16-week, hands-on AI/ML program covering Python, Pandas, databases/APIs, statistics, experimental design, visualization, regression, classification, Scikit-Learn, deep learning/TensorFlow/Keras, prompt engineering, time series, NLP, reinforcement learning, ethical AI, MLOps, deployment, and a final capstone.

One important structural detail: the syllabus lists Weeks 1–10, then Weeks 13–16, and subsequently Weeks 11–12. I will preserve the syllabus's actual curriculum content but organize the mock course into the logical Week 1 → Week 16 learning progression so you can actually study it sequentially. The source itself places Weeks 11–12 after the Week 16 material in the document.

AI & Machine Learning: Code, Train & Deploy
Free-Tier Mock Preparation Course

Purpose: Build enough practical fluency before entering the actual course that the student's first exposure to each topic is not the classroom.

The mock course is designed around:

Google Colab — primary Python/ML environment
Google BigQuery Sandbox/free-tier usage — SQL, analytical datasets, larger-data practice
Google Sheets/CSV — lightweight data creation and inspection
GitHub — version control, portfolio, reproducibility
TensorFlow/Keras — neural-network practice
scikit-learn — classical ML
Matplotlib/Seaborn — visualization
Local/browser-based alternatives when a cloud service is unnecessary

The objective isn't merely to "finish tutorials." Each week produces processable artifacts: datasets, notebooks, SQL queries, models, evaluations, visualizations, APIs, experiments, deployment artifacts, and eventually a capstone.

0. How to Use This Mock Course

I recommend treating each syllabus week as a five-part learning cycle:

Stage	Activity	Output
1	Learn	Concept notes
2	Code	Small executable examples
3	Practice	Guided exercises
4	Challenge	Independent problem
5	Validate	Quiz + coding checkpoint
Weekly mastery rule

Don't advance simply because you've completed the material.

Use:

GREEN — Ready

≥80% conceptual quiz
≥80% coding exercises
Can explain the major concepts without notes
Can modify an example rather than merely reproduce it

YELLOW — Needs reinforcement

65–79%
Can execute code but cannot yet explain/modify it reliably

RED — Revisit

<65%
Significant gaps in fundamentals
Course Architecture

The syllabus itself identifies four major instructional movements:

Section 1

Programming Fundamentals & Data Manipulation

Weeks 1–4

Section 2

Statistics, Experimental Design & Visualization

Weeks 5–7

Section 3

Advanced Statistical Modeling & Machine Learning

Weeks 8–16

The syllabus explicitly describes the course as hands-on and says students work with Python, TensorFlow, PyTorch and cloud platforms, with data preprocessing, ML models, deep learning, NLP and reinforcement learning culminating in a real-world capstone.

WEEK 1 — Introduction to Data Science + Programming Fundamentals
Syllabus topics
Introduction to Data Science
Python Review
Variables and Data Types
Conditional Statements and Loops
Functions and Modules

Learning objective

By the end of Week 1, you should be able to open a blank Colab notebook and write a small Python program without relying on copied code.

Lesson 1 — Introduction to Data Science
Exercise 1: Define a data problem

Create:

Business Question
↓
Data Required
↓
Transformation
↓
Analysis
↓
Insight
↓
Decision

Example:

Which products generate the highest revenue?

Dataset:

products = [
    {"product": "Coffee", "price": 4.50, "quantity": 100},
    {"product": "Tea", "price": 3.50, "quantity": 80},
    {"product": "Sandwich", "price": 8.00, "quantity": 40}
]

Calculate:

revenue = price * quantity

Then determine the highest-revenue product.

Lesson 2 — Python Review
Exercise set

Create variables representing:

name = "Daniel"
age = 30
height = 5.11
is_student = True

Then practice:

type(name)
type(age)
type(height)
type(is_student)
Conversion exercises

Convert:

"42" → integer
42 → float
42.7 → integer
42 → string
Challenge

Write a program that accepts:

price
quantity
tax_rate

and returns:

subtotal
tax
total
Lesson 3 — Conditional Statements

Build:

Exercise A
score = 87

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
else:
    grade = "F"

Then modify the logic yourself.

Exercise B — ML-flavored classification

Given:

risk_score = 0.73

Create:

< .30 = Low
.30–.69 = Medium
>= .70 = High
Lesson 4 — Loops

Process:

sales = [100, 250, 175, 300, 125]

Calculate:

total
average
maximum
minimum
number of days above average

Then reproduce the same result using a different loop structure.

Lesson 5 — Functions and Modules

Create:

def calculate_revenue(price, quantity):
    return price * quantity

Then build:

def calculate_profit(revenue, cost):
    return revenue - cost

Then:

def calculate_margin(profit, revenue):
    return profit / revenue
Week 1 Challenge

Build a miniature:

Sales Analytics Calculator

Input:

product
price
quantity
cost

Output:

revenue
profit
margin
performance classification
WEEK 2 — Pandas

The syllabus moves into:

Introduction to Pandas
Loading Data
Data Manipulation
Aggregation/Grouping
Cleaning/Preprocessing

Dataset progression

Start with:

import pandas as pd

df = pd.DataFrame({
    "product": ["A","A","B","B","C"],
    "price": [10,12,8,9,20],
    "quantity": [5,7,10,12,3]
})
Exercises
head()
tail()
shape
columns
dtypes
describe()
filtering
sorting
creating columns
deleting columns
GroupBy laboratory

Calculate:

df.groupby("product")["quantity"].sum()

Then:

average price
total revenue
average quantity
count of transactions
Cleaning laboratory

Create intentional problems:

None
"unknown"
-5
999999
duplicate rows

Then identify and resolve them.

WEEK 3 — Databases and APIs

Syllabus:

Introduction to Databases
SQL Review
Introduction to APIs
Accessing Web APIs with Python
Processing JSON

SQL laboratory

Create a BigQuery table:

customers
orders
products

Practice:

SELECT *
FROM orders;

Then:

SELECT
    product_id,
    SUM(quantity) AS units
FROM orders
GROUP BY product_id;

Then progressively introduce:

WHERE
GROUP BY
HAVING
ORDER BY
JOIN
CASE
CTEs
window functions
API laboratory

Use a public API that does not require credentials.

Practice:

import requests

response = requests.get(API_URL)
data = response.json()

Then inspect:

type(data)
data.keys()

Transform JSON → DataFrame.

Challenge

Build:

API → JSON → Pandas → Clean → Analyze → CSV

pipeline.

WEEK 4 — PROJECT 1: Data Wrangling & Analysis

The syllabus explicitly makes Week 4 the first project and calls for a real-world dataset, cleaning, preprocessing and EDA.

Mock Project
Business scenario

A company wants to understand customer purchasing behavior.

You receive:

customers.csv
transactions.csv
products.csv
Required work

Phase 1 — Load

Phase 2 — Inspect

Phase 3 — Clean

Phase 4 — Join

Phase 5 — Engineer features

Phase 6 — EDA

Phase 7 — Findings

Deliverables
project1/
├── notebook.ipynb
├── cleaned_data.csv
├── README.md
├── findings.md
└── data_dictionary.md
Gate

You cannot proceed until you can explain every transformation.

WEEK 5 — Statistics

Syllabus:

Descriptive Statistics
Probability Theory
Common Probability Distributions
Statistical Inference
Hypothesis Testing

Laboratory sequence
Descriptive statistics

Generate:

import numpy as np

x = np.array([12,15,17,20,21,25,30])

Calculate:

mean
median
mode
variance
standard deviation
range
quartiles
IQR
Probability simulation

Simulate a coin:

np.random.choice(["H","T"], size=10000)

Calculate:

P(H)
P(T)

Repeat with:

die rolls
card draws
customer conversion
defective products
Hypothesis testing laboratory

Create two synthetic groups:

Control
Treatment

Ask:

Is the observed difference plausibly attributable to random variation?

Practice:

null hypothesis
alternative hypothesis
p-value
significance level
confidence interval
Type I error
Type II error
WEEK 6 — Experimental Design

Syllabus topics:

Experimental Design
Types of Experimental Designs
Sampling
Power Analysis
A/B Testing

Mock A/B laboratory

Create:

Control
Treatment

Metric:

conversion_rate

Generate:

np.random.binomial(...)

Then calculate:

conversion rate
absolute lift
relative lift
confidence interval
p-value
Experiment design exercise

You must explicitly document:

Population
Unit of randomization
Treatment
Control
Primary metric
Secondary metrics
Guardrail metrics
Hypothesis
Sample size
Experiment duration
Decision rule

This becomes the foundation for later ML experimentation.

WEEK 7 — Visualization

Syllabus:

Data Visualization
Matplotlib
Seaborn
Basic Plots
Advanced Plots

Required visualization laboratory

Produce:

line chart
bar chart
histogram
box plot
scatter plot
heatmap
pair plot
distribution plot
categorical comparison
time-series chart
Visualization challenge

Given one dataset, tell three different stories using three different visualizations.

Then explain why each visualization is appropriate.

WEEK 8 — Regression

Syllabus:

Linear Regression
Simple Linear Regression
Simple Logistic Regression
Multiple Linear Regression
Model Selection/Evaluation
L1
L2
Elastic Net

Laboratory

Predict:

house_price

from:

square_feet
bedrooms
bathrooms
age
location_score
Models

Start with:

Y = β0 + β1X

Then:

Y = β0 + β1X1 + β2X2 + ...

Evaluate:

MAE
MSE
RMSE
R²

Then experiment with:

Ridge
Lasso
Elastic Net
WEEK 9 — Project 2: EDA & Visualization

The syllabus requires:

real-world dataset
cleaning
preprocessing
EDA
visualization

Mock project

Question:

What factors appear associated with customer churn?

Deliver:

EDA notebook
Data dictionary
Cleaning log
10+ visualizations
5+ statistical observations
Executive summary
Important rule

Do not claim:

X causes churn.

unless the design actually supports causal inference.

Practice distinguishing:

association
vs.
causation
WEEK 10 — Classification

Syllabus:

Classification
Logistic Regression
Decision Trees
Random Forests
Naive Bayes
Model Selection/Evaluation

Classification laboratory

Predict:

customer_churn = 0/1
Models

Build:

Logistic Regression
Decision Tree
Random Forest
Naive Bayes

Evaluate:

accuracy
precision
recall
F1
ROC-AUC
confusion matrix
Critical exercise

Create an imbalanced dataset.

Example:

95% No Churn
5% Churn

Then demonstrate why:

95% accuracy

can be misleading.

WEEK 11 — Machine Learning with Scikit-Learn

The syllabus introduces:

Scikit-Learn
Supervised Learning
Unsupervised Learning
Model Selection/Evaluation
Real-world ML

Supervised laboratory

Create a reusable pipeline:

Pipeline([
    ("preprocessor", preprocessor),
    ("model", model)
])

Practice:

train/test split
preprocessing
encoding
scaling
model fitting
prediction
evaluation
Unsupervised laboratory
K-Means

Cluster customers based on:

recency
frequency
monetary_value

Investigate:

K=2
K=3
K=4
K=5

Compare clustering behavior.

Then learn why clustering evaluation differs from supervised learning.

WEEK 12 — Project 3: ML Modeling & Evaluation

The syllabus requires:

real-world dataset
cleaning
preprocessing
feature engineering
model selection
evaluation
deployment

Mock project
Business question

Can we predict customer churn early enough for intervention?

Required pipeline
Raw Data
 ↓
Validation
 ↓
Cleaning
 ↓
Feature Engineering
 ↓
Train/Test Split
 ↓
Preprocessing
 ↓
Baseline
 ↓
Candidate Models
 ↓
Evaluation
 ↓
Model Selection
 ↓
Error Analysis
 ↓
Deployment
Required model card

Document:

Problem
Population
Target
Features
Training data
Evaluation data
Metrics
Limitations
Potential bias
Known failure modes
Deployment assumptions
WEEK 13 — Deep Learning & Neural Networks

The syllabus includes:

Neural Networks
TensorFlow/Keras
Training Deep Learning Models
Hyperparameter Tuning
Model Deployment
Prompt Engineering

Neural-network progression

Start with:

Input
 ↓
Dense Layer
 ↓
Output

Then:

Input
 ↓
Dense
 ↓
ReLU
 ↓
Dense
 ↓
Output

Train on a small classification dataset.

TensorFlow laboratory

Practice:

model = tf.keras.Sequential([
    tf.keras.layers.Dense(32, activation="relu"),
    tf.keras.layers.Dense(16, activation="relu"),
    tf.keras.layers.Dense(1, activation="sigmoid")
])

Then investigate:

epochs
batch size
learning rate
hidden layers
neurons
activation functions
dropout
Hyperparameter experiment

Create a table:

Experiment	Layers	Learning Rate	Epochs	Validation Accuracy
A	1	.001	10	
B	2	.001	10	
C	2	.0001	20	
D	3	.001	20	

The goal is not merely finding the largest number.

You must explain the tradeoffs.

WEEK 14 — Advanced Data Science

Syllabus:

Time Series
NLP
Reinforcement Learning
Ethical AI & Bias

This week becomes four mini-courses.

14A — Time Series

Dataset:

date
sales

Practice:

datetime conversion
sorting
rolling average
lag features
trend
seasonality
train/test split by time

Critical rule:

Never randomly shuffle a time-series forecasting problem without understanding the leakage implications.

14B — NLP

Start with:

"I love this product"
"I hate this product"
"The product is okay"

Practice:

tokenization
text cleaning
bag-of-words
TF-IDF
classification

Then build a sentiment classifier.

14C — Reinforcement Learning

Build a tiny grid world:

S . . .
. . # .
. # . .
. . . G

Where:

S = Start
G = Goal
# = obstacle

Teach an agent to maximize reward.

Start conceptually:

State
Action
Reward
Policy
Environment

Then implement a simple Q-learning example.

14D — Ethical AI

For every model from this point forward, answer:

Who is represented?
Who is missing?
What could the model get wrong?
What harms could occur?
What proxy variables exist?
What measurements could reveal disparate performance?
What human oversight exists?
WEEK 15 — MLOps

The syllabus specifically includes:

Introduction to MLOps
Versioning/Reproducibility
CI/CD
Model Monitoring/Maintenance

Mock production pipeline

Build:

data/
src/
models/
tests/
notebooks/
configs/
README.md
requirements.txt
Reproducibility laboratory

Record:

Python version
package versions
random seed
dataset version
model parameters
training date
evaluation results
Model versioning

Create:

model_v1
model_v2
model_v3

Record:

model
features
hyperparameters
metrics
timestamp
Monitoring laboratory

Simulate:

training distribution
production distribution

Then introduce:

missing values
shifted feature distributions
changed class balance
degraded accuracy

Detect the changes.

WEEK 16 — Capstone

The syllabus ends with:

Final Capstone Presentation
Final Project Report
Presentation of Findings
Feedback/Iteration
Career Pathways & Job Readiness

Mock Capstone

You will build a complete AI/ML system.

Required architecture
BUSINESS PROBLEM
       ↓
DATA
       ↓
DATA QUALITY
       ↓
EDA
       ↓
STATISTICAL ANALYSIS
       ↓
FEATURE ENGINEERING
       ↓
BASELINE
       ↓
ML MODEL
       ↓
EVALUATION
       ↓
ERROR ANALYSIS
       ↓
DEPLOYMENT
       ↓
MONITORING
       ↓
BUSINESS RECOMMENDATION
The Free-Tier Capstone Environment

A practical architecture would be:

Google Colab
   │
   ├── Python
   ├── Pandas
   ├── NumPy
   ├── Scikit-Learn
   ├── TensorFlow
   └── Matplotlib/Seaborn
          │
          ▼
Google BigQuery
   │
   ├── Raw data
   ├── Analytical tables
   └── SQL transformations
          │
          ▼
GitHub
   │
   ├── Code
   ├── README
   ├── Model Card
   └── Documentation

This keeps the preparation environment inexpensive while still forcing you to practice the same conceptual workflow used in production ML.

The Most Important Part: Progress Measurement

I recommend a 100-point AI/ML Readiness Index.

Category 1 — Python

15 points

Can you independently:

manipulate variables?
write conditions?
write loops?
write functions?
import modules?
debug basic errors?
Category 2 — Data

15 points

Can you:

load data?
inspect data?
clean data?
join datasets?
aggregate?
handle missing values?
engineer columns?
Category 3 — SQL

10 points

Can you:

SELECT?
filter?
aggregate?
JOIN?
use CTEs?
write analytical queries?
Category 4 — Statistics

15 points

Can you explain:

mean vs median?
variance?
probability?
distributions?
confidence intervals?
hypothesis tests?
p-values?
statistical significance?
Category 5 — Experimentation

10 points

Can you design an A/B test and identify:

unit of randomization?
primary metric?
guardrail?
hypothesis?
sample size?
statistical test?
decision rule?
Category 6 — Machine Learning

20 points

Can you:

split data correctly?
establish a baseline?
preprocess?
train?
evaluate?
compare models?
identify overfitting?
perform error analysis?
Category 7 — Deep Learning / Deployment / MLOps

15 points

Can you explain and demonstrate:

neural networks?
TensorFlow/Keras?
hyperparameter tuning?
deployment?
reproducibility?
model versioning?
monitoring?
Readiness Levels
Score	Status	Meaning
0–49	Foundation	Significant preparation required
50–64	Developing	Fundamentals emerging
65–79	Functional	Can complete guided projects
80–89	Course Ready	Strong preparation
90–100	Advanced Prep	Ready for substantial independent work

But: the score is only useful if the underlying skills are genuine.

Someone who memorizes:

model.fit(X, y)

without understanding what X, y, training data, leakage, evaluation data, or generalization mean has not actually mastered ML.

Weekly Gate System

Every week ends with four gates:

Gate A — Explain

Explain the concept without code.

Gate B — Reproduce

Recreate a guided example from scratch.

Gate C — Modify

Change the example.

Gate D — Create

Solve a new problem without being given the solution.

For example:

You don't truly know Pandas because you can execute groupby().

You know Pandas when you can receive an unfamiliar dataset and determine when and why you should use groupby().

The 16-Week Practice Portfolio

By the end, your preparation should contain:

01_python_foundations/
02_pandas/
03_sql_apis/
04_data_wrangling/
05_statistics/
06_experiment_design/
07_visualization/
08_regression/
09_eda_project/
10_classification/
11_scikit_learn/
12_ml_project/
13_deep_learning/
14_advanced_ds/
15_mlops/
16_capstone/

Each folder should contain:

README.md
notebook.ipynb
data/
src/
results/

where appropriate.

A Second, More Rigorous Progress System

For each exercise, assign:

0 — Cannot complete
1 — Completed with heavy guidance
2 — Completed with minor assistance
3 — Completed independently
4 — Can explain and modify
5 — Can teach it to someone else

Then calculate:

Weekly Mastery = Points Earned / Points Available × 100

This gives you two measurements:

KNOWLEDGE SCORE
+
PRACTICAL EXECUTION SCORE

That's substantially more informative than a conventional quiz score.

The Final Mock-Course Examination

Before entering the actual program, you should be able to complete this sequence without a tutorial:

Challenge 1

Load an unfamiliar CSV.

Challenge 2

Identify data-quality problems.

Challenge 3

Clean the data.

Challenge 4

Write SQL against an equivalent BigQuery table.

Challenge 5

Perform EDA.

Challenge 6

Produce appropriate visualizations.

Challenge 7

Formulate a statistical hypothesis.

Challenge 8

Perform the appropriate statistical test.

Challenge 9

Create a baseline ML model.

Challenge 10

Train multiple candidate models.

Challenge 11

Evaluate them using appropriate metrics.

Challenge 12

Perform error analysis.

Challenge 13

Build a neural-network version.

Challenge 14

Document reproducibility.

Challenge 15

Package the model.

Challenge 16

Explain how it would be deployed and monitored.

Challenge 17

Present the entire project as if speaking to a hiring manager.

One Important Distinction

The uploaded syllabus says the actual program is beginner-friendly and states that no prior AI/ML experience is required. It also says students are expected to spend time outside class on homework, projects, and skill review.

Therefore, this preparation course shouldn't attempt to turn you into an ML engineer before the program.

Its purpose is more strategic:

Remove the friction of the fundamentals so that the actual course can be used for acceleration rather than first exposure.

That means we deliberately build from:

Python → Pandas → SQL → Statistics → Experiments → Visualization → Regression → Classification → Scikit-Learn → Deep Learning → Advanced DS → MLOps → Capstone.

The result is a parallel 16-week "shadow course" that mirrors the syllabus while giving you substantially more repetitions and executable practice than the syllabus itself specifies.

The syllabus itself emphasizes hands-on projects and real-world application, so this preparation structure deliberately makes every major concept culminate in something executable rather than leaving it at lecture/theory level.

If you want to take this one step further, the next logical artifact is a complete Week 1–16 workbook: every lesson broken into individual Colab cells, synthetic datasets, SQL tables, exercises, expected outputs, quizzes, answer keys, debugging challenges, and weekly scoring rubrics—essentially a full self-paced version of the course you can actually run in the free tier.

Instead of crunching the complete Week 1-16 workbook into one Colab environment. Generate an exhaustive Colab environment covering all lessons from week 1. Upon completion of week, one and a submission for your review, considering the great I receive, People, then advance to or progress to week 2. Your output should be a complete Google Collab notebook covering all of the lessons included in week one with an exhaustive amount of processable components. Does this make sense? If so, proceed.
Analyzed
import json, os, textwrap, random, math

out = "/mnt/data/AI_ML_Code_Train_Deploy_Week_01_Preparation.ipynb"

cells = []

def md(s):
    cells.append({"cell_type":"markdown","metadata":{}, "source":textwrap.dedent(s).strip().splitlines(True)})

def code(s):
    cells.append({"cell_type":"code","execution_count":None,"metadata":{}, "outputs":[], "source":textwrap.dedent(s).strip().splitlines(True)})

md("""
# AI & Machine Learning: Code, Train & Deploy
## Week 1 — Programming Fundamentals & Data Science Preparation Lab

**Environment:** Google Colab / free tier  
**Week:** 1 of 16  
**Mode:** Learn → Process → Practice → Debug → Challenge → Submit

### Syllabus alignment

This notebook covers every Week 1 topic listed in the provided syllabus:

1. **Introduction to Data Science**
2. **Python Review**
3. **Variables and Data Types**
4. **Conditional Statements and Loops**
5. **Functions and Modules**

The syllabus places these topics under **Section 1: Programming Fundamentals & Data Manipulation**. This notebook deliberately stays within Week 1 and does not advance into the Week 2 Pandas curriculum.

### How to use this notebook

Do not simply run every cell.

For cells marked **TRY IT**, modify the code and observe what changes.  
For cells marked **PREDICT**, write your answer before running the code.  
For cells marked **DEBUG**, diagnose the error before looking at the explanation.  
For cells marked **INDEPENDENT**, solve the problem without copying the preceding solution.

At the end, complete the **Week 1 Submission** section and submit the completed notebook for review. A successful review becomes the gate for Week 2.
""")

md("""
# 0. Learning Contract & Progress Tracker

## Week 1 mastery targets

By the end of this notebook, you should be able to:

- explain what data science does in a practical business context;
- recognize common Python data types;
- create, inspect, update, and convert variables;
- use arithmetic and comparison operators;
- write conditional logic;
- use `for` and `while` loops;
- work with strings, lists, tuples, dictionaries, and sets;
- write reusable functions;
- use parameters, return values, and default arguments;
- import and use Python modules;
- read basic documentation/help output;
- debug common Python errors;
- translate a small business question into executable Python logic.

## Progress scale

Score each skill after practicing:

| Score | Meaning |
|---:|---|
| 0 | I cannot do this yet |
| 1 | I can do it only by copying |
| 2 | I can do it with substantial guidance |
| 3 | I can do it independently |
| 4 | I can modify it and explain why it works |
| 5 | I can teach the concept or solve a novel version |

Record your scores in the final assessment section.
""")

md("""
# 1. Colab Environment Check

This section confirms that the free-tier environment is working before you begin.

**No paid services, GPUs, external datasets, or API keys are required for Week 1.**
""")
code("""
import sys
import platform
import math
import statistics
import random

print("Python version:", sys.version)
print("Platform:", platform.platform())
print("Environment check: READY")
""")

md("""
## Processable Exercise 1 — Environment Variables

Create three variables:

- `course_name`
- `week_number`
- `student_status`

Then print a sentence using all three.

**Do not copy the example from the next cell; write your own first.**
""")
code("""
# YOUR CODE HERE
""")
code("""
# Example solution — compare only after attempting the exercise.
course_name = "AI & Machine Learning: Code, Train & Deploy"
week_number = 1
student_status = "Preparing"

print(f"{course_name} | Week {week_number} | Status: {student_status}")
""")

md("""
# 2. Lesson 1 — Introduction to Data Science

The syllabus begins Week 1 with **Introduction to Data Science**.

For this preparation course, think of data science as a workflow rather than a single programming language:

**Question → Data → Processing → Analysis → Evidence → Decision**

A useful distinction:

- **Data:** observations or measurements.
- **Information:** organized data with context.
- **Analysis:** systematic examination of the data.
- **Insight:** a meaningful finding.
- **Decision:** an action informed by the evidence.

## Processable Example

Suppose a fictional store records daily sales:

| Day | Sales |
|---|---:|
| Mon | 120 |
| Tue | 155 |
| Wed | 90 |
| Thu | 180 |
| Fri | 210 |

Business question:

> What was the average daily sales amount, and which day had the highest sales?
""")
code("""
sales = {
    "Mon": 120,
    "Tue": 155,
    "Wed": 90,
    "Thu": 180,
    "Fri": 210
}

total_sales = sum(sales.values())
average_sales = total_sales / len(sales)
best_day = max(sales, key=sales.get)

print("Total sales:", total_sales)
print("Average sales:", average_sales)
print("Highest-sales day:", best_day)
print("Highest sales:", sales[best_day])
""")

md("""
## TRY IT — Change the Business Question

Modify the previous example to answer:

1. Which days were above the average?
2. Which day had the lowest sales?
3. How many days exceeded 150?
4. What percentage of the week's sales occurred on Friday?

Write the code yourself.
""")
code("""
# YOUR CODE HERE
""")

md("""
## Data Science Translation Drill

For each scenario, identify:

1. **Business question**
2. **Potential data**
3. **Possible analysis**
4. **Potential decision**

### Scenario A
A streaming service wants to understand why some users stop using the service.

### Scenario B
A retailer wants to determine which products sell most during weekends.

### Scenario C
A mobile app team wants to know whether a new interface changes user behavior.

Write your answers in comments or Markdown below.
""")
md("""
### YOUR RESPONSES

**Scenario A**

- Business question:
- Potential data:
- Possible analysis:
- Potential decision:

**Scenario B**

- Business question:
- Potential data:
- Possible analysis:
- Potential decision:

**Scenario C**

- Business question:
- Potential data:
- Possible analysis:
- Potential decision:
""")

md("""
## Lesson 1 Checkpoint

Without running code, answer:

1. What is the difference between a business question and a dataset?
2. Why should the question be defined before blindly analyzing data?
3. What is the difference between an observation and an insight?
4. Give one example where correlation might be mistaken for causation.

Write your answers before continuing.
""")

md("""
# 3. Lesson 2 — Python Review

Python is the primary programming language used throughout this preparation course.

We will practice Python in progressively harder layers:

1. expressions
2. variables
3. data types
4. operators
5. collections
6. control flow
7. functions
8. modules
9. debugging
""")

md("""
## 3.1 Expressions and Arithmetic

Run the examples, then change the numbers.

Operators:

`+` addition  
`-` subtraction  
`*` multiplication  
`/` division  
`//` floor division  
`%` remainder/modulo  
`**` exponentiation
""")
code("""
print("Addition:", 10 + 3)
print("Subtraction:", 10 - 3)
print("Multiplication:", 10 * 3)
print("Division:", 10 / 3)
print("Floor division:", 10 // 3)
print("Remainder:", 10 % 3)
print("Power:", 10 ** 3)
""")

md("""
### TRY IT

Calculate:

- 17 divided by 4
- the remainder of 17 divided by 4
- 9 squared
- 125 divided by 5
- the average of 82, 91, 77, and 88
""")
code("""
# YOUR CODE HERE
""")

md("""
## 3.2 Strings

Practice:

- concatenation
- f-strings
- `.upper()`
- `.lower()`
- `.strip()`
- `.replace()`
- `len()`
- indexing
- slicing
""")
code("""
first_name = "Daniel"
role = "Data Analyst"

print(first_name + " — " + role)
print(f"{first_name} — {role}")
print(role.upper())
print(role.lower())
print(len(role))
print(role[0])
print(role[:4])
""")

md("""
### TRY IT

Given:

```python
raw_name = "   Ada Lovelace   "

Produce:

Ada Lovelace
ADA LOVELACE
Ada

using Python string operations.
""")
code("""
raw_name = " Ada Lovelace "

YOUR CODE HERE

""")

md("""

3.3 Collections — Lists

Lists are ordered, mutable collections.
""")
code("""
scores = [82, 91, 77, 88, 95]

print(scores)
print(scores[0])
print(scores[-1])
print(scores[1:4])
print(len(scores))

scores.append(100)
print(scores)

scores.remove(77)
print(scores)
""")

md("""

LIST LAB

Given:

temperatures = [72, 75, 69, 81, 84, 77, 70]

Calculate:

number of observations
first temperature
last temperature
minimum
maximum
average
temperatures above 75
""")
code("""
temperatures = [72, 75, 69, 81, 84, 77, 70]
YOUR CODE HERE

""")

md("""

3.4 Tuples

Tuples are ordered collections that are generally used for fixed groups of values.
""")
code("""
coordinate = (31.55, -97.19)

print("Latitude:", coordinate[0])
print("Longitude:", coordinate[1])

latitude, longitude = coordinate
print(latitude, longitude)
""")

md("""

TRY IT

Create a tuple representing:

product_id
product_name
price

Then unpack it into three variables.
""")
code("""

YOUR CODE HERE

""")

md("""

3.5 Dictionaries

Dictionaries store key-value pairs.
""")
code("""
customer = {
"id": 101,
"name": "Alex",
"age": 34,
"active": True
}

print(customer["name"])
print(customer["age"])

customer["age"] = 35
customer["segment"] = "Returning"

print(customer)
""")

md("""

DICTIONARY LAB

Create a dictionary representing an ML experiment configuration containing:

experiment name
model name
learning rate
number of epochs
random seed

Then retrieve each value individually.
""")
code("""

YOUR CODE HERE

""")

md("""

3.6 Sets

Sets contain unique values and are useful when uniqueness matters.
""")
code("""
artist_ids = ["A12", "A12", "B44", "C90", "B44", "A12"]

unique_artist_ids = set(artist_ids)

print("Original:", artist_ids)
print("Unique:", unique_artist_ids)
print("Unique count:", len(unique_artist_ids))
""")

md("""

TRY IT

Given two lists of customer IDs, find:

customers appearing in both
customers appearing only in the first
customers appearing only in the second
""")
code("""
customers_a = {"C01", "C02", "C03", "C04"}
customers_b = {"C03", "C04", "C05", "C06"}
YOUR CODE HERE

""")

md("""

4. Lesson 3 — Variables and Data Types

The Week 1 syllabus explicitly includes Variables and Data Types.

Core Python types to recognize:

int
float
str
bool
list
tuple
dict
set
NoneType

Use type() rather than guessing.
""")
code("""
examples = {
"integer": 42,
"float": 42.5,
"string": "42",
"boolean": True,
"list": [1, 2, 3],
"tuple": (1, 2, 3),
"dictionary": {"x": 1},
"set": {1, 2, 3},
"none": None
}

for label, value in examples.items():
print(label, "=>", type(value))
""")

md("""

Type Conversion Laboratory

Practice:

string → integer
string → float
integer → float
float → integer
number → string

Also observe what happens when conversion is impossible.
""")
code("""
print(int("42"))
print(float("42.5"))
print(float(42))
print(int(42.9))
print(str(42))
""")

md("""

DEBUG

What will happen?

int("42.5")

Predict first. Then run it.
""")
code("""

PREDICT BEFORE RUNNING

try:
result = int("42.5")
print(result)
except Exception as e:
print(type(e).name, ":", e)
""")

md("""

FIX THE PROBLEM

Convert "42.5" to an integer without directly calling int("42.5").
""")
code("""
value = "42.5"

YOUR CODE HERE

""")

md("""

Variable Mutation Lab

Variables can be reassigned.

Create a score variable and progressively transform it:

0
→ 50
→ 75
→ 90

Then create passing = True if the final score is at least 70.
""")
code("""

YOUR CODE HERE

""")

md("""

PREDICT THE TYPE

Before running each expression, write the expected type:

10 / 2
10 // 2
"10"
10 == 10
[10, 20]
{"score": 10}
None

Then verify with Python.
""")
code("""
expressions = [
10 / 2,
10 // 2,
"10",
10 == 10,
[10, 20],
{"score": 10},
None
]

for value in expressions:
print(repr(value), "=>", type(value))
""")

md("""

5. Lesson 4 — Conditional Statements and Loops

The syllabus explicitly combines:

Conditional Statements
Loops

This is where Python begins behaving like a decision-making system.

The core pattern is:

condition → decision → action

""")

md("""

5.1 Comparison Operators

Practice:

==
!=
>
<
>=
<=

Logical operators:

and
or
not
""")
code("""
score = 87

print(score >= 90)
print(score >= 80)
print(score == 87)
print(score != 50)
print(score >= 80 and score < 90)
print(score < 50 or score > 90)
print(not (score < 50))
""")

md("""

Grade Classification

Write a function-like decision structure:

90–100 → A
80–89 → B
70–79 → C
60–69 → D
below 60 → F

First implement it with if/elif/else.
""")
code("""
score = 87

YOUR CODE HERE

""")

md("""

EDGE-CASE LAB

Test your logic with:

100
90
89
80
79
70
69
60
59
0

Your boundaries should behave exactly as intended.
""")
code("""
test_scores = [100, 90, 89, 80, 79, 70, 69, 60, 59, 0]

YOUR CODE HERE

""")

md("""

5.2 Nested Conditions

Create a simple eligibility system:

A fictional applicant is eligible if:

age >= 18
and account is active

If eligible, distinguish:

premium
standard

based on spending >= 1000.
""")
code("""
age = 34
account_active = True
spending = 1250

YOUR CODE HERE

""")

md("""

5.3 For Loops

A for loop repeats a block over a sequence.
""")
code("""
numbers = [3, 7, 2, 9, 4]

total = 0

for number in numbers:
total += number

print("Total:", total)
""")

md("""

LOOP LAB

Given:

sales = [120, 155, 90, 180, 210]

Use a loop to calculate:

total
count
number above 150
maximum
minimum

Do not use sum(), max(), or min() for this exercise.
""")
code("""
sales = [120, 155, 90, 180, 210]

YOUR CODE HERE

""")

md("""

5.4 Loop + Condition

Count how many values are:

below 50
between 50 and 79
80 or higher

Dataset:

scores = [45, 62, 81, 90, 73, 55, 88, 39, 100, 76]

""")
code("""
scores = [45, 62, 81, 90, 73, 55, 88, 39, 100, 76]

YOUR CODE HERE

""")

md("""

5.5 range()

Practice:

range(5)
range(1, 6)
range(0, 11, 2)

""")
code("""
print(list(range(5)))
print(list(range(1, 6)))
print(list(range(0, 11, 2)))
""")

md("""

TRY IT

Use range() to calculate the sum of integers from 1 through 100.
""")
code("""

YOUR CODE HERE

""")

md("""

5.6 While Loops

Use a while loop when repetition depends on a condition.
""")
code("""
counter = 1

while counter <= 5:
print("Iteration:", counter)
counter += 1
""")

md("""

DEBUG

Why is this dangerous?

counter = 1

while counter <= 5:
    print(counter)

Explain the problem before modifying it.
""")
code("""

Safe demonstration — DO NOT create an infinite loop.

counter = 1
while counter <= 5:
print(counter)
counter += 1
""")

md("""

5.7 Loop Control

Practice:

break
continue

""")
code("""
for number in range(1, 11):
if number == 6:
break
print(number)
""")
code("""
for number in range(1, 11):
if number % 2 == 0:
continue
print(number)
""")

md("""

LOOP CHALLENGE

Given:

transactions = [120, -10, 85, 0, 200, -50, 150]

Build a loop that:

skips zero
skips negative values
totals positive transactions
counts valid transactions
""")
code("""
transactions = [120, -10, 85, 0, 200, -50, 150]
YOUR CODE HERE

""")

md("""

6. Lesson 5 — Functions and Modules

The syllabus concludes Week 1 with Functions and Modules.

A function should let you package logic that can be reused.

Basic structure:

def function_name(parameters):
    ...
    return result

""")
code("""
def calculate_revenue(price, quantity):
return price * quantity

revenue = calculate_revenue(4.50, 100)

print("Revenue:", revenue)
""")

md("""

Function Laboratory

Write these functions independently:

Function 1

calculate_tax(amount, tax_rate)

Function 2

calculate_profit(revenue, cost)

Function 3

calculate_margin(profit, revenue)

Function 4

classify_score(score)

Function 5

is_valid_transaction(amount)

Each function should return a result rather than only printing it.
""")
code("""

YOUR CODE HERE

""")

md("""

Parameters vs Arguments

Understand the distinction:

def greet(name):
    ...

name is a parameter.

greet("Alex")

"Alex" is an argument.

TRY IT

Write a function that accepts:

name
role
years_experience

and returns one formatted sentence.
""")
code("""

YOUR CODE HERE

""")

md("""

Default Arguments

Create:

def calculate_total(price, quantity, tax_rate=0.08):
    ...

Test it with:

the default tax rate
a custom tax rate
""")
code("""
YOUR CODE HERE

""")

md("""

Return Values

Why is this more reusable?

def add(a, b):
    return a + b

versus:

def add(a, b):
    print(a + b)

Test the difference by assigning the returned value to a variable.
""")
code("""
def add(a, b):
return a + b

result = add(10, 20)
print("Result:", result)
print("Can continue processing:", result * 2)
""")

md("""

Function Composition

Build a pipeline:

price + quantity
        ↓
revenue
        ↓
profit
        ↓
margin

Use your functions rather than repeating arithmetic.
""")
code("""
def calculate_revenue(price, quantity):
return price * quantity

def calculate_profit(revenue, cost):
return revenue - cost

def calculate_margin(profit, revenue):
if revenue == 0:
return 0
return profit / revenue

price = 12
quantity = 50
cost = 350

revenue = calculate_revenue(price, quantity)
profit = calculate_profit(revenue, cost)
margin = calculate_margin(profit, revenue)

print("Revenue:", revenue)
print("Profit:", profit)
print("Margin:", margin)
""")

md("""

7. Modules

A module is reusable Python code that can be imported.

Practice standard-library modules before installing anything.
""")
code("""
import math

print("Pi:", math.pi)
print("Square root:", math.sqrt(144))
print("Ceiling:", math.ceil(4.2))
print("Floor:", math.floor(4.8))
""")

md("""

Randomness Laboratory

Use the random module to simulate simple data.
""")
code("""
import random

random.seed(42)

scores = [random.randint(50, 100) for _ in range(10)]

print(scores)
print("Average:", sum(scores) / len(scores))
""")

md("""

Reproducibility Experiment

Run the previous cell twice with the seed 42.

Then change the seed to 99.

Observe the difference.

Concept: a fixed random seed allows you to reproduce a pseudo-random result.
""")
code("""
import random

for seed in [42, 42, 99]:
random.seed(seed)
values = [random.randint(1, 10) for _ in range(5)]
print("Seed:", seed, "| Values:", values)
""")

md("""

statistics Module

Use the standard library to calculate descriptive statistics.
""")
code("""
import statistics

values = [10, 12, 14, 15, 18, 21, 25]

print("Mean:", statistics.mean(values))
print("Median:", statistics.median(values))
print("Population stdev:", statistics.pstdev(values))
""")

md("""

8. Debugging Laboratory

Debugging is a core skill, not an optional skill.

The objective is to learn to read:

error type
error message
line number
surrounding code
likely cause
""")

md("""

DEBUG 1 — NameError

Predict the problem:

print(customer_name)

What type of error occurs? How would you fix it?
""")
code("""

Broken version intentionally replaced with a safe demonstration.

try:
print(customer_name)
except Exception as e:
print(type(e).name, ":", e)

customer_name = "Alex"
print(customer_name)
""")

md("""

DEBUG 2 — TypeError

Why does this fail?

"Revenue: " + 125

Fix it using an f-string.
""")
code("""
try:
print("Revenue: " + 125)
except Exception as e:
print(type(e).name, ":", e)

revenue = 125
print(f"Revenue: {revenue}")
""")

md("""

DEBUG 3 — IndexError

Why does this fail?

items = ["A", "B", "C"]
items[3]

Find the valid indexes and retrieve the final element.
""")
code("""
items = ["A", "B", "C"]

try:
print(items[3])
except Exception as e:
print(type(e).name, ":", e)

print("Valid indexes:", list(range(len(items))))
print("Final element:", items[-1])
""")

md("""

DEBUG 4 — KeyError

What is wrong here?

customer = {"name": "Alex"}
customer["email"]

Fix it using a safer dictionary-access pattern.
""")
code("""
customer = {"name": "Alex"}

try:
print(customer["email"])
except Exception as e:
print(type(e).name, ":", e)

print(customer.get("email", "Email unavailable"))
""")

md("""

DEBUG 5 — Logic Error

The following code is syntactically valid but logically wrong:

score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"

What should happen for 85? What about 95?

Now add a final else and test boundary values.
""")
code("""
def classify_score(score):
if score >= 90:
return "A"
elif score >= 80:
return "B"
elif score >= 70:
return "C"
elif score >= 60:
return "D"
else:
return "F"

for score in [95, 85, 75, 65, 55]:
print(score, "=>", classify_score(score))
""")

md("""

9. Integrated Week 1 Laboratory

Now combine everything.

Scenario

You are analyzing a fictional set of customer transactions.

Each transaction contains:

customer ID
product
price
quantity
customer age
active status
""")
code("""
transactions = [
{"customer_id": "C001", "product": "Coffee", "price": 5.00, "quantity": 3, "age": 34, "active": True},
{"customer_id": "C002", "product": "Tea", "price": 4.00, "quantity": 2, "age": 22, "active": True},
{"customer_id": "C003", "product": "Coffee", "price": 5.00, "quantity": 5, "age": 45, "active": False},
{"customer_id": "C004", "product": "Sandwich", "price": 9.00, "quantity": 1, "age": 29, "active": True},
{"customer_id": "C005", "product": "Tea", "price": 4.00, "quantity": 8, "age": 51, "active": True},
{"customer_id": "C006", "product": "Coffee", "price": 5.00, "quantity": 1, "age": 67, "active": True},
]
""")

md("""

Integrated Task A — Transaction Revenue

Write a function:

calculate_transaction_revenue(transaction)

It should return:

price × quantity

Then calculate revenue for every transaction.
""")
code("""

YOUR CODE HERE

""")

md("""

Integrated Task B — Customer Classification

Create a function that classifies a customer:

age < 30 → "Young"
30–49 → "Adult"
50+ → "Mature"

Then add the classification to each transaction.
""")
code("""

YOUR CODE HERE

""")

md("""

Integrated Task C — Active Customer Logic

Count:

total transactions
active transactions
inactive transactions
active transaction revenue
inactive transaction revenue
""")
code("""
YOUR CODE HERE

""")

md("""

Integrated Task D — Product Revenue

Using loops and dictionaries, calculate total revenue by product.

Expected conceptual structure:

Coffee → ...
Tea → ...
Sandwich → ...

Do not use Pandas. Pandas belongs to Week 2.
""")
code("""

YOUR CODE HERE

""")

md("""

Integrated Task E — Business Insight

Using only the results you calculated, write three factual observations.

Example format:

Coffee generated ___ in revenue across ___ transactions.

Do not make causal claims.
""")
code("""

YOUR CODE HERE

""")

md("""

10. Independent Challenge — Week 1 Mini Project
Project: Small Business Transaction Analyzer

Build your own Python program from scratch.

Requirements

Create a dataset containing at least 15 transactions.

Each record must contain:

transaction ID
product
price
quantity
customer age
active status
Your program must calculate
total transactions
total revenue
average transaction value
highest transaction
lowest transaction
active transaction count
inactive transaction count
active revenue
inactive revenue
revenue by product
age-group counts
number of transactions above the average
percentage of active transactions
Technical requirements

You must use:

variables
at least 1 list
at least 1 dictionary
at least 2 loops
at least 2 conditionals
at least 4 functions
at least 1 imported module
at least 1 exception-handling/debugging strategy
Restriction

Do not use Pandas.

The purpose is to demonstrate Week 1 programming fundamentals before Week 2 introduces Pandas.
""")
code("""

============================================================
WEEK 1 INDEPENDENT MINI PROJECT
Build your solution here.
============================================================
1. Create your dataset
2. Create your functions
3. Process the transactions
4. Calculate summary statistics
5. Print your final report

""")

md("""

11. Week 1 Debugging Challenge

The following program contains multiple problems.

Your job:

identify the problem;
describe why it happens;
fix it;
explain the fix.

Do not immediately rewrite everything.

Challenge code
sales = ["100", "250", "175", "bad", "300"]

total = 0

for sale in sales:
    total += sale

average = total / len(sales)

if average > "200":
    print("High average")
else:
    print("Normal average")
Questions
What type is each element?
What happens when "bad" is processed?
What should the program do with invalid data?
What type should average be?
What is wrong with comparing average to "200"?
""")
code("""
Write your corrected version here.

""")

md("""

12. Week 1 Knowledge Check

Answer these before running any validation code.

Part A — Concepts
What is data science?
What is a variable?
What is the difference between an integer and a float?
What is a Boolean?
When would you use a dictionary?
When would you use a list?
What does if do?
What is the difference between for and while?
What does return do in a function?
What is a module?
Why are random seeds useful?
What is a TypeError?
What is a KeyError?
What is a logic error?
Why should data processing be reproducible?
Part B — Predict the output

Before running:

x = 10
y = 3

print(x // y)
print(x % y)
print(x ** y)
Part C — Predict the type
result = 10 / 2

What is type(result)?

Part D — Write code

Create a function that accepts a list of numbers and returns the count of values greater than the list's average.

Do not use Pandas.
""")
code("""

KNOWLEDGE CHECK — YOUR ANSWERS/CODE
Part B/C: verify your predictions here after writing them above.
Part D: implement your function here.

""")

md("""

13. Week 1 Practical Examination
Rules

For this examination:

do not copy earlier solutions;
do not use Pandas;
use only Python and standard-library modules;
you may use Python documentation/help;
document assumptions;
test edge cases.
Problem

A fictional company wants a simple customer-value screening tool.

Each customer has:

customer_id
annual_spend
number_of_orders
active
Your program must:
create at least 12 customers;
calculate average annual spend;
identify customers above average;
classify customers:
"High Value" if spend >= 1000
"Standard" if spend >= 500
"Low Value" otherwise
exclude inactive customers from a separate active-customer analysis;
calculate average orders;
calculate the percentage of active customers;
calculate total spend among active customers;
use functions;
use loops;
use conditionals;
use at least one dictionary;
handle at least one possible data-quality problem;
produce a concise text report.
Required final output

Your notebook should print a report containing:

WEEK 1 CUSTOMER VALUE REPORT
----------------------------
Customers:
Active customers:
Average spend:
Average orders:
Active customer percentage:
Active-customer spend:
High-value customers:
Standard customers:
Low-value customers:

""")
code("""

============================================================
WEEK 1 PRACTICAL EXAM
Complete independently.
============================================================
YOUR CODE HERE

""")

md("""

14. Week 1 Submission Package

Before submitting for review, complete all of the following.

Required notebook sections
 Environment check completed
 Lesson 1 exercises completed
 Python arithmetic exercises completed
 String exercises completed
 List exercises completed
 Tuple exercise completed
 Dictionary exercise completed
 Set exercise completed
 Data-type exercises completed
 Conditional exercises completed
 Loop exercises completed
 Function exercises completed
 Module exercises completed
 Debugging exercises completed
 Integrated laboratory completed
 Independent mini-project completed
 Debugging challenge completed
 Knowledge check completed
 Practical examination completed
Submission instructions

Submit this completed notebook for review.

For review, include:

the completed .ipynb;
any exported .py file if you created one;
a short Markdown reflection answering:
What was easiest?
What was hardest?
Which Python concept still feels uncertain?
Which exercise required the most debugging?
What can you now do independently that you could not do before Week 1?
""")

md("""

15. Self-Assessment — Week 1 Mastery Matrix

Give yourself a 0–5 score for each skill.

Skill	Score
Explain the basic data-science workflow	
Variables	
Data types	
Type conversion	
Strings	
Lists	
Tuples	
Dictionaries	
Sets	
Arithmetic/operators	
Conditional logic	
for loops	
while loops	
Loop control	
Functions	
Parameters/arguments	
Return values	
Modules	
Debugging	
Reproducibility/random seeds	
Translating a business question into code	
Building a small Python program independently	
Score calculation

Maximum possible score:

110 points

Calculate:

Mastery % = Total Score / 110 × 100
Suggested gate

85%+ AND successful practical examination: ready to request Week 2.

70–84%: review weak areas before requesting Week 2.

Below 70%: repeat the relevant laboratories and resubmit.

This is a preparation-course gate, not a grade from the actual Skillspire course.
""")

code("""

SELF-ASSESSMENT CALCULATOR
Enter your 22 scores (0–5) in the list below.

scores = [
# Explain data-science workflow
0,
# Variables
0,
# Data types
0,
# Type conversion
0,
# Strings
0,
# Lists
0,
# Tuples
0,
# Dictionaries
0,
# Sets
0,
# Arithmetic/operators
0,
# Conditional logic
0,
# for loops
0,
# while loops
0,
# Loop control
0,
# Functions
0,
# Parameters/arguments
0,
# Return values
0,
# Modules
0,
# Debugging
0,
# Reproducibility
0,
# Business question -> code
0,
# Independent program
0
]

total = sum(scores)
maximum = len(scores) * 5
percentage = total / maximum * 100

print(f"Total: {total}/{maximum}")
print(f"Mastery: {percentage:.1f}%")

if percentage >= 85:
print("SELF-ASSESSMENT STATUS: READY TO REQUEST WEEK 2 REVIEW")
elif percentage >= 70:
print("SELF-ASSESSMENT STATUS: REVIEW WEAK AREAS BEFORE WEEK 2")
else:
print("SELF-ASSESSMENT STATUS: REINFORCEMENT REQUIRED")
""")

md("""

16. Instructor Review Submission
STOP HERE

Do not automatically move to Week 2.

Submit the completed Week 1 notebook for review.

Review criteria

The review will examine:

1. Conceptual understanding

Can you explain what your code is doing?

2. Programming correctness

Does the code run?
Does it produce the intended result?

3. Independent problem solving

Can you solve a variation rather than only reproduce an example?

4. Debugging ability

Can you identify and fix errors?

5. Code quality

Are variables understandable?
Are functions appropriately used?
Is logic organized?

6. Data-science reasoning

Can you translate a business question into a computational problem?
Do your conclusions stay within the evidence?

7. Readiness

Are Week 1 fundamentals strong enough that Week 2 Pandas work will build on them rather than expose unresolved Python gaps?
Instructor decision

The next stage should be one of:

ADVANCE → Week 2
TARGETED REVIEW → specific lessons/exercises
REPEAT → Week 1 reinforcement

The goal is mastery, not merely completion.
""")

md("""

Week 1 Completion Reflection

Write your reflection below before submitting.

1. What did I learn?
2. What can I now do independently?
3. Where did I struggle?
4. What errors did I encounter and how did I fix them?
5. What do I need to practice again?
6. What question would I ask the instructor?
7. My Week 1 mastery score:
8. I believe I am ready for Week 2 because:

""")

Add Colab metadata

nb = {
"cells": cells,
"metadata": {
"colab": {
"name": "AI_ML_Code_Train_Deploy_Week_01_Preparation.ipynb",
"provenance": [],
"toc_visible": True
},
"kernelspec": {
"display_name": "Python 3",
"language": "python",
"name": "python3"
},
"language_info": {
"name": "python",
"version": "3.x"
}
},
"nbformat": 4,
"nbformat_minor": 5
}

with open(out, "w", encoding="utf-8") as f:
json.dump(nb, f, ensure_ascii=False, indent=2)

print(f"Created: {out}")
print(f"Cells: {len(cells)}")

STDOUT/STDERR
Created: /mnt/data/AI_ML_Code_Train_Deploy_Week_01_Preparation.ipynb
Cells: 135


Yes. I built Week 1 as a standalone, submission-gated Colab environment rather than compressing the entire 16-week curriculum into one notebook.

Week 1 notebook contents

The notebook contains 135 cells covering every Week 1 syllabus topic:

Introduction to Data Science
Data-science workflow
Business-question translation
Processable examples
Data/insight/decision exercises
Python Review
Arithmetic
Strings
Lists
Tuples
Dictionaries
Sets
Collections laboratories
Multiple independent exercises
Variables & Data Types
int, float, str, bool
lists, tuples, dictionaries, sets
None
Type inspection
Type conversion
Type-prediction exercises
Conversion/debugging challenges
Conditional Statements & Loops
Comparisons
Boolean logic
if/elif/else
Nested conditions
for
while
range
break
continue
Boundary testing
Multiple data-processing laboratories
Functions & Modules
Functions
Parameters
Arguments
Return values
Default arguments
Function composition
math
random
statistics
Reproducibility/random seeds
Debugging Laboratory
NameError
TypeError
IndexError
KeyError
Logic errors
Error diagnosis rather than simply fixing code
Integrated Week 1 Laboratory
Transaction dataset
Revenue calculations
Customer classification
Active/inactive analysis
Product-level analysis
Business observations
Independent Week 1 Mini-Project
15+ transactions
Multiple functions
Loops
Conditions
Dictionaries
Data-quality handling
Business report
Knowledge Check
Practical Examination
Mastery Matrix
22 skills
0–5 scoring system
Automated mastery calculation
Instructor Review Submission
Explicit Advance / Targeted Review / Repeat gate

Importantly, I kept Pandas out of the Week 1 exercises where appropriate, because Pandas is explicitly a Week 2 syllabus topic. This makes the progression meaningful rather than prematurely solving Week 1 problems with Week 2 tools. The source syllabus places Python fundamentals in Week 1 and Pandas/data manipulation in Week 2.

Download the Week 1 Colab notebook

Download — AI & Machine Learning Week 1 Preparation Colab Notebook

Once you complete it, upload the completed .ipynb back here. I can then review it as the instructor—checking both whether the code works and whether your solutions demonstrate actual understanding—and determine whether you should advance to Week 2 or receive targeted Week 1 remediation. 

Today 4:48 PM
Perfect. I'd like for you to review the entire chat transcript to refresh on the context in detail. Your task is to generate a detailed GitHub Repository structure/architecture for the prep course/ google colab notebooks that will be generated (plus the week 1 google colab notebook). *Include a detailed README.md with explanation of the prep course, what it covers, how the prep course weeks and how to process / move forward. Does this make sense? If so, proceed.

Yes. After refreshing the prior context and checking the actual Week 1 notebook, I agree that the repository should be designed as a progressive, gated learning system, not simply as 16 notebooks placed in a folder.

The architecture below preserves the source syllabus, keeps one standalone Colab environment per week, separates the larger projects from weekly practice, and creates a clear complete → submit → review → advance workflow.

The uploaded syllabus establishes the 16-week course and Week 1's five lessons: Introduction to Data Science, Python Review, Variables and Data Types, Conditional Statements and Loops, and Functions and Modules.

Repository architecture
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
│   │
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
│   │   ├── week01_rubric.md
│   │   ├── week02_rubric.md
│   │   └── ...
│   │
│   └── checkpoints/
│       ├── week01_gate.md
│       ├── week02_gate.md
│       └── ...
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
│
├── submissions/
│   ├── week01/
│   ├── week02/
│   └── ...
│
├── docs/
│   └── assets/
│
└── .github/
    └── workflows/
Why this architecture matters

The key distinction is:

NOT:

16 notebooks → finish them all

BUT:

Week 1
   ↓
Complete
   ↓
Submit
   ↓
Instructor Review
   ↓
ADVANCE / TARGETED REVIEW / REPEAT
   ↓
Week 2
   ↓
...

That makes the repository function as an actual pre-course training system.

The source syllabus itself emphasizes hands-on learning and real-world projects, so this architecture intentionally separates foundational practice from the larger projects.

Detailed README

I created the complete repository README.md with:

purpose and scope
syllabus alignment
all 16 weeks
free-tier philosophy
complete directory architecture
role of every repository layer
standard notebook contract
weekly processing workflow
advancement gates
mastery model
Git workflow
reproducibility rules
free-tier guardrails
project separation
Week 1 status
submission convention
final progression model

It also explicitly documents the unusual ordering in the source PDF: Weeks 13–16 appear before Weeks 11–12 in the document. The repository uses numeric Week 1–16 navigation without silently changing the underlying syllabus topics. The source places Weeks 11–12 after Week 16 in the PDF.

Repository README.md
AI & Machine Learning: Code, Train & Deploy — Free-Tier Preparation Course

A structured, hands-on preparation course designed to mirror the provided Skillspire AI and Machine Learning: Code, Train, & Deploy syllabus week by week while giving the learner additional processable practice before entering the live course.

Current status: Week 1 is implemented as a standalone Google Colab notebook. Weeks 2–16 are intentionally scaffolded so each week can be developed, completed, reviewed, and unlocked sequentially.

Purpose

The goal is not to replace the source course. The goal is to remove avoidable friction from the course by giving the learner a repeatable environment in which to practice the underlying concepts before encountering them in class.

The preparation model is:

Learn → Process → Practice → Debug → Challenge → Submit → Review → Advance

Each week is treated as an independent learning unit. The learner completes that week's notebook, performs its independent work and assessment, submits the completed notebook for instructor-style review, and only then advances to the next week.

Source Curriculum Alignment

The uploaded syllabus describes a 16-week hands-on AI/ML program covering data preprocessing, classical machine learning, deep learning, NLP, reinforcement learning, cloud platforms, deployment, and a capstone.

The preparation repository preserves the syllabus terminology and sequence.

Syllabus sequence
Week	Source syllabus focus
1	Introduction to Data Science; Python Review; Variables and Data Types; Conditional Statements and Loops; Functions and Modules
2	Data Manipulation with Pandas; loading data; manipulation; aggregation/grouping; cleaning/preprocessing
3	Databases and APIs; SQL review; APIs; Python API access; JSON
4	Project 1 — Data Wrangling and Analysis
5	Descriptive/inferential statistics; probability; distributions; statistical inference; hypothesis testing
6	Experimental design; sampling; power analysis; A/B testing
7	Data visualization; Matplotlib; Seaborn; basic/advanced plots
8	Regression; linear/logistic regression; multiple regression; model evaluation; L1/L2/Elastic Net
9	Project 2 — Exploratory Data Analysis and Visualization
10	Classification; logistic regression; decision trees; random forests; Naive Bayes; evaluation
11	Machine Learning with Scikit-Learn; supervised/unsupervised learning; model selection/evaluation; real-world ML
12	Project 3 — Machine Learning Modeling and Evaluation
13	Deep learning/neural networks; TensorFlow/Keras; training; tuning; deployment; prompt engineering
14	Advanced Data Science: time series; NLP; reinforcement learning; ethical AI/bias
15	MLOps: versioning/reproducibility; CI/CD for ML; monitoring/maintenance
16	Final capstone presentation; report; findings; feedback/iteration; career/job readiness

Note: The source PDF prints Weeks 13–16 before Weeks 11–12 on the later pages. This repository uses the logical numeric order 1–16 for navigation while preserving the source week's topics. It does not silently change the underlying curriculum.

Free-Tier Philosophy

The preparation course is designed to run primarily in free or low-cost learning environments:

Google Colab for Python, statistics, ML and deep-learning exercises.
Google BigQuery Sandbox/free-tier usage for SQL and larger analytical exercises when a week requires a database environment.
GitHub for notebooks, source code, documentation, version control and portfolio organization.
CSV/JSON/local synthetic data when an external service is unnecessary.

Week 1 requires no BigQuery account, GPU, API key or paid service.

Repository Architecture
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
What Each Layer Does
notebooks/

The primary student learning environment. One standalone Colab notebook per week.

A week notebook should be independently executable and should contain:

syllabus alignment;
learning objectives;
environment check;
lesson instruction;
runnable examples;
guided exercises;
prediction exercises;
debugging exercises;
independent challenges;
knowledge check;
practical assessment;
mastery self-assessment;
submission instructions;
explicit advancement gate.
curriculum/rubrics/

Instructor-style evaluation criteria for each week.

Each rubric should distinguish:

conceptual understanding;
coding correctness;
independent problem solving;
debugging;
code quality;
data/ML reasoning;
reproducibility;
readiness for the next week.
curriculum/checkpoints/

Short checkpoints that determine whether the learner should:

ADVANCE
TARGETED REVIEW
REPEAT
projects/

The three explicit projects and final capstone from the syllabus receive dedicated folders so their deliverables are not buried inside weekly practice notebooks.

data/

Data is separated by lifecycle. Raw data should not be overwritten. Processed data should be reproducible from source data and code. Sample/synthetic data should be clearly labeled.

sql/

SQL becomes important beginning in Week 3 and later project work. Queries should be version-controlled rather than trapped inside notebooks.

src/

Reusable Python code belongs here once notebook work becomes repetitive or project-oriented.

tests/

Validation and unit tests are introduced progressively. Early weeks can use simple assertions; later weeks should use more formal testing for pipelines and ML artifacts.

config/

Environment-neutral configuration such as project identifiers, dataset names, random seeds, model settings, and paths. Secrets must never be committed.

submissions/

This is the learner's evidence trail. A completed weekly notebook can be copied here when submitted for review. Review notes should be separate from the original learning notebook.

.github/workflows/

Reserved for later reproducibility/CI demonstrations. Do not introduce CI/CD merely for appearance; it should be introduced when it supports the curriculum, especially around Week 15 MLOps.

Weekly Notebook Contract

Every future weekly notebook should follow the same high-level contract.

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

The number of internal sections will vary by week; the learning lifecycle should not.

Week Processing Model
Step 1 — Open only the current week

Do not jump ahead. The repository is intentionally designed as a progression rather than a reference dump.

Step 2 — Read the learning objectives

Know what capability the week is intended to develop.

Step 3 — Execute the examples

Run the code, inspect the output, and change parameters.

Step 4 — Complete YOUR CODE HERE cells

These are deliberately processable exercises. Do not treat them as optional.

Step 5 — Complete debugging exercises

Diagnose the problem before viewing a corrected implementation.

Step 6 — Complete the independent challenge

This is the first major test of transfer. A solution that only works when copied from an example does not demonstrate mastery.

Step 7 — Complete the knowledge check

Answer conceptual questions without relying on execution alone.

Step 8 — Complete the practical examination

This is the weekly readiness test.

Step 9 — Calculate the mastery score

Use the weekly rubric and self-assessment.

Step 10 — Submit the notebook

Upload the completed .ipynb for instructor-style review.

Step 11 — Receive a gate decision

The review returns one of:

ADVANCE — proceed to the next week.

TARGETED REVIEW — repeat specific lessons/exercises, then resubmit.

REPEAT — redo the week's core work before advancing.

Why the Gate Matters

The actual course is cumulative. Later topics depend on earlier skills.

For example:

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

The purpose of the gate is therefore to prevent a weak foundation from being carried invisibly into later weeks.

Week 1 — Current Implementation

notebooks/week01/AI_ML_Code_Train_Deploy_Week_01_Preparation.ipynb is the first completed notebook.

It contains 135 cells and covers all Week 1 syllabus lessons:

Introduction to Data Science
Python Review
Variables and Data Types
Conditional Statements and Loops
Functions and Modules

It additionally contains processable exercises for collections, type conversion, debugging, integrated transaction analysis, an independent mini-project, a knowledge check, a practical examination, mastery scoring, and an instructor-review submission gate.

Week 1 constraint

Pandas is deliberately not used for the core Week 1 programming exercises. Pandas is a Week 2 syllabus topic. This keeps the preparation course cumulative rather than allowing later tooling to conceal Week 1 Python gaps.

Mastery Model

Each skill is scored from 0–5:

Score	Meaning
0	Cannot do it yet
1	Can only copy it
2	Can do it with substantial guidance
3	Can do it independently
4	Can modify it and explain it
5	Can teach it or solve a novel version

The Week 1 notebook uses 22 skill dimensions for a maximum of 110 points.

Suggested advancement threshold:

85%+ and successful practical examination: request Week 2 review.
70–84%: targeted reinforcement before advancing.
Below 70%: repeat the relevant Week 1 work.

The instructor review is the final gate; the self-score does not override observed performance.

Submission Convention

Recommended pattern:

submissions/
└── week01/
    ├── completed_notebook.ipynb
    └── reflection.md

For future weeks:

submissions/week02/
submissions/week03/
...
submissions/week16/

Do not overwrite the canonical learning notebook with a student's submitted copy. Keep the original template intact.

Git Workflow

Recommended progression:

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

For a personal repository, a simpler workflow is also acceptable:

main
  ├── completed Week 1
  ├── completed Week 2
  └── ...

The important rule is that the repository history should make progress visible.

Reproducibility Rules

Every notebook should:

state its environment assumptions;
use deterministic seeds when randomness is involved;
avoid hard-coded personal file paths;
keep secrets out of GitHub;
document external dependencies;
make synthetic data visibly synthetic;
explain when an external service is required;
separate raw and processed data;
preserve the original dataset when practical.
Free-Tier Guardrails

The course should favor small, intentionally sized datasets for routine exercises. Larger datasets should be introduced only when the lesson requires them.

Do not create infrastructure merely to imitate production. Use the simplest free-tier component that teaches the intended concept.

For BigQuery exercises, the repository should document the expected dataset/table names and provide SQL that can be reproduced in a free-tier-compatible environment.

Portfolio vs Preparation Work

This repository is primarily a learning repository. Not every exercise is expected to become a portfolio project.

The portfolio-quality outputs should be concentrated around:

Project 1 — Data Wrangling and Analysis
Project 2 — Exploratory Data Analysis and Visualization
Project 3 — Machine Learning Modeling and Evaluation
Final Capstone

The smaller weekly exercises exist to build the skills needed to execute those projects successfully.

Expected Final State

At completion, the repository should demonstrate a progression from:

Python fundamentals → data manipulation → SQL/API work → statistics → experimentation → visualization → regression → classification → ML engineering → deep learning → advanced data science → MLOps → capstone.

The final repository should therefore tell a coherent story: not simply that notebooks were completed, but that the learner progressed from foundational programming to an end-to-end AI/ML workflow.

Current Next Step

Week 1 is the active gate.

Open the Week 1 notebook in Google Colab.
Complete every YOUR CODE HERE, challenge, knowledge check and examination section.
Run the notebook from top to bottom and resolve errors.
Complete the self-assessment.
Submit the completed notebook for review.
Wait for the instructor-style decision: ADVANCE, TARGETED REVIEW, or REPEAT.
Only after an ADVANCE decision should the Week 2 notebook be generated/used.
License / Attribution

This repository is a personal preparation environment built around the structure and topics of the provided course syllabus. It is not presented as an official Skillspire course or official Skillspire instructional material.

Generated repository package

I also created the actual GitHub-ready repository scaffold, including the README, architecture specification, Week 1 notebook, all Week 2–16 directory placeholders, project directories, curriculum/rubric locations, submissions structure, .gitignore, and license.

Download the complete GitHub repository ZIP

Download the standalone Week 1 Colab notebook

The important design decision going forward is that I would not generate Week 2 yet. Week 1 is now the active gate. Once you complete and submit that notebook, I can review it against the Week 1 objectives and decide whether you genuinely demonstrate readiness for the Pandas/data-manipulation material that begins Week 2. The syllabus explicitly puts Pandas, loading data, manipulation, grouping/aggregation, and cleaning/preprocessing in Week 2.
