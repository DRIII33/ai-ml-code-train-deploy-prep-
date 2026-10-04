# Fair Artist Discovery & Recommendation System

## Business scenario

The music industry is increasingly driven by recommendation systems, playlist placement, and artist discovery. Major streaming platforms must balance two objectives at the same time:

1. keep listeners engaged by surfacing familiar music they are likely to enjoy;
2. increase exposure for emerging, independent, and underrepresented artists that do not yet have the same audience or metadata footprint as established acts.

The research in `research/AI_Skills_in_Music_Industry_with_Detailed_Syllabus_Mapping.md` highlights a core challenge: popularity bias and algorithmic filter bubbles can suppress long-tail artists, reduce genre diversity, and create unfair concentration of value among a small set of already-successful catalog entries.

## Business problem

A streaming platform wants to understand whether a recommendation engine is accidentally reinforcing popularity bias and limiting long-tail discovery. The business question is not just whether the model predicts what a user will click, but whether it also:

- surfaces diverse artists to listeners;
- increases discovery of niche genres and independent artists;
- avoids overconcentrating attention among top-tier catalog items;
- presents explainable, fair recommendations to platform stakeholders.

## Why this matters

This is a real strategic problem in the music ecosystem. If the platform over-optimizes for historical engagement, it may create:

- low discovery of new artists;
- reduced supply diversity and lower long-tail revenue;
- degraded listener experience due to repetitive recommendations;
- brand risk if fairness and transparency are questioned by artists, labels, regulators, or investors.

## Portfolio-ready capstone objective

Build an end-to-end, fairness-aware music recommendation and discovery project that can be presented to executives, music-tech stakeholders, and hiring managers. The final system should answer:

- Which artists are currently under-discovered relative to their potential?
- Which listeners would be most likely to engage with niche or emerging artists?
- How can the recommendation system balance engagement with fairness and discovery?
- How can the model be monitored and explained for production use?

## Project structure

The repository is organized around a single capstone narrative:

- Week 1: define the business scenario, prepare Python environment, and profile music data
- Week 2: clean and transform artist and listening data
- Week 3: store and query the data using SQL and data pipelines
- Week 4: perform data wrangling and validate quality issues
- Week 5: analyze bias and statistical variation in discovery data
- Week 6: design experiments to compare recommendation strategies
- Week 7: visualize fairness and engagement trends
- Week 8: train baseline regression models for popularity and engagement
- Week 9: produce an EDA and artist-discovery analysis report
- Week 10: classify artist audience fit or track likelihood to convert
- Week 11: build scikit-learn models with fairness-aware evaluation
- Week 12: produce a first recommendation ranking pipeline
- Week 13: use deep learning / embeddings for audio and artist similarity
- Week 14: implement exploration-exploitation for long-tail discovery
- Week 15: deploy, monitor, and version the model
- Week 16: deliver the final business presentation and capstone submission

## Deliverables

Each week produces a concrete artifact for the overall capstone:

- Music data dictionary
- Clean feature set
- SQL-backed data warehouse view
- EDA and quality report
- Fairness dashboard
- Baseline predictive model
- Fairness-aware ranking prototype
- Deep learning embeddings and similarity model
- MLOps-ready deployment package
- Executive summary presentation

## Business success metrics

The project will evaluate success using both business and technical KPIs:

- listener engagement;
- click-through or play-through rate on recommended tracks;
- long-tail discovery rate;
- artist exposure distribution;
- fairness gap across artist groups;
- model explainability and performance stability;
- production readiness of deployment workflow.

## Stakeholders

- product managers for music discovery;
- data scientists and ML engineers;
- artist relations teams;
- legal/compliance and trust & safety teams;
- executive leadership and investors;
- potential employers and hiring managers.

This capstone is designed not only to teach AI/ML skills, but also to demonstrate how data science can drive a strategic product decision in the modern music ecosystem.
