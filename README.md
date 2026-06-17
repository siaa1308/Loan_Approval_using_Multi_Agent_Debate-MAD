# Loan Approval Prediction using Multi-Agent Debate (MAD)

## Overview

This project implements a **Multi-Agent Debate (MAD) framework** for loan approval decision-making.Instead of relying on a single model, multiple specialized AI agents independently analyze a loan applicant's financial profile, debate their viewpoints, and collaboratively arrive at a final lending decision.
The goal is to improve **transparency, explainability, and robustness** in credit risk assessment.

---

## Dataset

The project uses the **Lending Club Loan Dataset**, one of the most widely used public datasets for credit risk and loan default prediction.

Dataset Source:
Kaggle Lending Club Dataset

---

## Multi-Agent Debate Architecture

1. Generator Agent -> Provides the initial loan approval recommendation.
2. Risk Analyst Agent -> Performs detailed risk assessment.
3. Policy Checker Agent -> Ensures compliance with responsible lending policies.
4. Evidence Agent -> Validates decisions using factual indicators only.
5. ML Agent -> Uses a trained machine learning model prediction as additional evidence.

### Judge Agent

After reviewing all agent arguments and rebuttals, the Judge Agent produces the final decision.

Outputs:

* Final Approval/Denial
* Confidence Score
* Detailed Explanation

---

## Workflow

```text
Applicant Profile
        │
        ▼
 ML Model Prediction
        │
        ▼
 ┌─────────────────────┐
 │  Generator Agent    │
 ├─────────────────────┤
 │  Risk Agent         │
 ├─────────────────────┤
 │  Policy Agent       │
 ├─────────────────────┤
 │  Evidence Agent     │
 ├─────────────────────┤
 │  ML Agent           │
 └─────────────────────┘
        │
        ▼
 Multi-Agent Debate
        │
        ▼
   Judge Agent
        │
        ▼
 Final Loan Decision
```

---
## Technologies Used

* Python
* Google Gemini API
* Pandas
* NumPy
* Scikit-Learn
* Jupyter Notebook

---
