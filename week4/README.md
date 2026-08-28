# Week 4 — HealthConnect Experience Lab: Problem Understanding

**Track:** Data Science
**Project:** HealthConnect Clinic — Improving Patient Appointment Attendance and Healthcare Support Using Data and AI

## Overview

From Week 4 onward, this repository transitions from the standalone Heart Disease project (Weeks 2-3) to the shared **HealthConnect Experience Lab**, a multi-track project where each AnalystLab Africa internship track contributes to a common business problem from its own professional perspective.

**Central project question:** How can HealthConnect Clinic use data and AI to reduce missed appointments and improve the patient support experience?

This week's focus (per the official Week 4 brief) was understanding the problem, reviewing the provided resources, and defining an initial approach — not building or training a model.

## Data Science Track Contribution — Week 4

- Reviewed the HealthConnect appointment dataset (5,000 records) and its data dictionary.
- Assessed data quality: no duplicates or logically invalid records; limited, well-explained missingness.
- Framed the core task as a **binary classification problem**: predicting appointment no-shows.
- Explicitly decided how to handle `Cancelled` appointments (excluded from the primary target, with documented reasoning) — a required decision point in the brief.
- Proposed a target variable, candidate input features, an initial modelling approach, and key risks (e.g. data leakage from repeat patients).

## Files

| File | Description |
|---|---|
| `HealthConnect_ML_Problem_Definition.ipynb` | Main Week 4 output: problem definition, data assessment, target/feature proposal, initial modelling approach |
| `Week4_Project_Summary.docx` | Concise summary of Week 4 work and proposed Week 5 focus |

## Next Steps (Week 5)

Prepare a modelling-ready dataset (missing value handling, encoding), implement a patient-aware or time-based train/test split, and train/evaluate a baseline model to test the feasibility assessed this week.

---
*Part of the AnalystLab Africa Data Science Internship Programme — Batch D.*
