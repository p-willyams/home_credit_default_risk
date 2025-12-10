<img width="1920" height="1080" alt="Home Credit risk" src="https://github.com/user-attachments/assets/3041002a-1781-4b88-8ff0-1571673c10c2" />

## Project Overview

This project focuses on developing a **predictive model to estimate the probability of customer default** (TARGET variable) using demographic, financial, credit history, and behavioral data. The goal is to support **safer and more profitable credit decisions**, such as adjusting credit limits, approving or rejecting applications, and prioritizing preventive collection actions.

The model was built using the *Home Credit Default Risk* dataset, which is characterized by **high complexity, more than 800 variables, and strong class imbalance** (approximately **8% defaulters**).

---

## Business Problem

The main business objective was to **reduce financial losses from default** without harming the experience of good customers.

Key challenges addressed:

* Early identification of **high-risk customers**
* Reducing **false negatives** (undetected defaulters)
* Controlling **false positives** and operational costs
* Ensuring scalability with hundreds of features

---

## Solution

A **binary classification model** was developed using more than **800 features**, including:

* Demographic data
* Socioeconomic variables
* Behavioral patterns
* Credit history information

The model was calibrated with an **optimal threshold of 0.191 (F1-score ≈ 0.344)**, prioritizing the detection of high-risk customers while limiting unnecessary loss of good clients.

Key insights from the model:

* Employment stability and strong credit history reduce default risk
* High numbers of credit inquiries increase risk
* Recent behavioral changes indicate financial instability
* Combining multiple weak signals improves predictive power

---

## Model Performance

| Metric                 | Value |
| ---------------------- | ----- |
| Recall (Defaulters)    | 38%   |
| Precision (Defaulters) | 31%   |
| AUC-ROC                | 0.80  |
| MCC                    | 0.28  |
| Overall Accuracy       | 88%   |

The model showed **strong discriminatory power**, even under severe class imbalance.

---

## Financial Impact

Based on realistic simulations:

* Total customers: 46,127
* Avg loss per defaulter: **R$ 5,000**
* Avg preventive action cost: **R$ 500**

| Scenario           | Net Profit       |
| ------------------ | ---------------- |
| Without model      | R$ 23.78 million |
| With model (0.191) | R$ 30.17 million |

**Estimated incremental profit:** **R$ 6.39 million**

This demonstrates that the model delivers **direct financial value** even after operational costs and false positives.

---

## Confusion Matrix (Threshold = 0.191)

|                       | Pred 0 | Pred 1 |
| --------------------- | ------ | ------ |
| Actual 0 (Good payer) | 39,255 | 3,148  |
| Actual 1 (Defaulter)  | 2,298  | 1,426  |

* TP: 1,426
* FN: 2,298
* FP: 3,148
* TN: 39,255

---

## Key Results

* Optimal threshold: **0.191**
* F1-score (defaulters): **0.3437**
* AUC-ROC: **0.795**
* MCC: **0.281**

---

## Practical Recommendation

Use a threshold close to **0.19** as an **initial risk screening filter** to prioritize loss prevention. For final credit approval, a more conservative threshold is recommended to balance approval volume and profitability.

---

## Data Source

The dataset used is the **Home Credit Default Risk** dataset, containing financial, demographic, and behavioral information from thousands of customers with diverse socioeconomic profiles.

---

## Conclusion

This project demonstrates that, even in highly complex environments with:

* More than **800 variables**
* Strong class imbalance
* Weak individual signals

it is possible to build models that are:

✅ Robust

✅ Interpretable

✅ Scalable

✅ Financially impactful

The model not only improves technical metrics but also delivers **real, measurable business value**.

