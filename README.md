# Intuit — Predictive Analytics for QuickBooks Upgrade Campaign

> Replaced a blanket re-mailing strategy with a profit-driven, model-based targeting system across 75K small-business customers — projecting ~$380K in incremental revenue while significantly reducing wasted mail volume.

---

## Overview

Intuit's wave-2 QuickBooks upgrade campaign targets customers who didn't respond to wave-1. The default approach: mail everyone again. This project replaces that with a customer-level expected value framework — only mailing customers where the predicted upgrade probability justifies the mailing cost.

---

## Business Context

| Parameter | Value |
|---|---|
| Customers analyzed | 75,000 |
| Mailing cost per customer | $1.41 |
| Upgrade margin per conversion | $60 |
| Projected incremental revenue | ~$380K |

---

## Approach

### Profit-Based Targeting Framework

```
Wave-2 Non-Responders (75K customers)
           ↓
Feature Engineering
  Purchase recency · Spend · Product history · Engagement
           ↓
Propensity Model (Logistic Regression / Neural Network)
  → P(upgrade) per customer
           ↓
Expected Value Calculation
  EV = P(upgrade) × $60 margin − $1.41 mailing cost
           ↓
Target: EV > 0  →  Mail
        EV ≤ 0  →  Do not mail
           ↓
Projected Output: ~$380K incremental revenue
```

### Models Built

| Model | Purpose |
|---|---|
| Logistic Regression | Interpretable propensity model with RFM features |
| Neural Network | Non-linear capture of complex feature interactions |

### Features Used
- Purchase recency
- Spend (frequency × monetary value)
- Product history and version
- Engagement signals (opens, clicks, prior responses)

---

## Key Results

- **~$380K** projected incremental revenue from targeted wave-2 mailing
- Significant reduction in unnecessary mail volume vs. mailing all 75K
- End-to-end reproducible pipeline from raw data to final target list

---

## Project Structure

```
Intuit-QuickBooks-Upgrade-Analysis/
├── intuit_analysis.ipynb     ← Full modeling pipeline + targeting framework
├── README.md
└── LICENSE
```

---

## Tech Stack

| Tool | Purpose |
|---|---|
| **Python** | Data processing, modeling, and analysis |
| **Logistic Regression** | Upgrade propensity with interpretable coefficients |
| **Neural Networks** | Non-linear propensity modeling |
| **Pandas / NumPy** | Feature engineering and RFM construction |
| **Jupyter Notebook** | Reproducible pipeline for stakeholder handoff |
| **Profit Optimization** | Expected value framework with cost/margin assumptions |

---

## Author

**Krithika Suwarna**  
[LinkedIn](https://linkedin.com/in/krithika-suwarna) · [Portfolio](https://krithikasuwarna.com)
