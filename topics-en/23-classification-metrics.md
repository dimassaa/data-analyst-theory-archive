# Binary classification metrics

🌐 [Русская версия](../topics/23-classification-metrics.md)

### 📈 Binary classification metrics

When a model predicts a binary outcome (0/1), accuracy alone is not enough, especially with imbalanced classes. A set of metrics based on the **confusion matrix** is needed.

**Confusion matrix:**

|                     | Predicted positive (1) | Predicted negative (0) |
|---------------------|---------------------------|---------------------------|
| **Actually positive** | True Positive (TP)        | False Negative (FN)       |
| **Actually negative** | False Positive (FP)       | True Negative (TN)        |

---

#### 🔹 Core metrics

- **Accuracy (share of correct predictions):**
  $$
  \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
  $$
  *Drawback:* misleading under strong imbalance (e.g., 99% zeros — accuracy 99% for a trivial classifier).

- **Precision:**
  $$
  \text{Precision} = \frac{TP}{TP + FP}
  $$
  The share of true positives among all objects the model labeled as positive. Important when the cost of a false positive is high (spam filter: better to let spam through than to block an important email).

- **Recall (sensitivity):**
  $$
  \text{Recall} = \frac{TP}{TP + FN}
  $$
  The share of true positives that the model managed to find. Important when missing an event is critical (disease diagnosis: better a false alarm than missing the disease).

- **F1-score (harmonic mean of Precision and Recall):**
  $$
  F_1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
  $$
  Used when Precision and Recall need to be balanced. Good for imbalanced classes.

**Example:**
A model predicts customer churn. Out of 1000 customers, 100 churn. The model predicted 80 churners, of whom 60 actually churned.
TP = 60, FP = 20, FN = 40, TN = 880.
Precision = 60 / (60+20) = 0.75.
Recall = 60 / (60+40) = 0.60.
F1 = 2 * (0.75 * 0.60) / (0.75 + 0.60) ≈ 0.667.

---

#### 🔹 ROC-AUC

The **ROC curve** (Receiver Operating Characteristic) shows the dependence of the True Positive Rate (Recall) on the False Positive Rate (FPR = FP / (FP+TN)) as the classification threshold changes.

- Each point of the curve corresponds to a certain probability threshold.
- The curve starts at (0,0) (all predictions negative) and ends at (1,1) (all positive).
- Perfect model: the ROC passes through (0,1) — TPR=1, FPR=0.

**AUC (Area Under Curve)** — the area under the ROC curve.
- AUC = 1 — perfect model.
- AUC = 0.5 — model no better than random guessing.
- AUC < 0.5 — the model is "inverted" (labels can be flipped).

**Interpretation:** AUC shows the probability that the model assigns a randomly chosen positive object a higher score than a randomly chosen negative one.

**Advantage:** AUC does not depend on the chosen threshold and works well under imbalance (unlike accuracy).

---

#### 🔹 Precision-Recall curve (PR curve)

Under strong imbalance (e.g., 0.1% positives), ROC-AUC can give an overly optimistic picture because the FPR is small even with a large number of FPs. In such cases it is better to use the **Precision-Recall curve**.

- X axis — Recall, Y axis — Precision.
- Perfect model: the curve tends toward the top-right corner (Precision=1, Recall=1).
- The area under the PR curve (Average Precision, AP) — the analog of AUC.

**When to use which:**
- If classes are balanced or moderately imbalanced → ROC-AUC.
- If strong imbalance (positives < 5–10%) → Precision-Recall and AP.

---

#### 🔹 Choosing the threshold

In real problems, after training a model you need to choose the probability threshold for assigning a class. It is determined by business requirements for the Precision/Recall trade-off.

- You can optimize the F1-score on validation.
- Or minimize the cost of errors (cost-sensitive learning): different weights for FP and FN.
- Sometimes it is more important to maximize Recall at a fixed minimal Precision (and vice versa).

**Insight:** Don't rely on a single metric. Always look at the confusion matrix, Precision/Recall for a specific threshold, and ROC-AUC or PR-AUC for an overall assessment of model quality.
### ✅ Summary

| Topic | Key concepts | Practical value |
|------|------------------|------------------------|
| **Classification metrics** | Confusion matrix, Precision/Recall, F1, ROC-AUC, PR-AUC | Adequate evaluation of binary classification models, especially under imbalance |

**Key takeaways:**
- For binary models use a set of metrics: Accuracy is misleading under imbalance, ROC-AUC is good for comparing models, Precision-Recall for tasks with rare events.
- Threshold selection is determined by business requirements for the Precision/Recall trade-off.

---
Related topics: [Missing data](22-missing-data.md) · [Logistic regression](19-logistic-regression.md) · [Effect size](21-effect-size.md)