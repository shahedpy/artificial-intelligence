# Artificial Intelligence

## Confusion Matrix

A confusion matrix is a table that is often used to describe the performance of a classification model (or “classifier”) on a set of test data for which the true values are known.
- It allows the visualization of the performance of an algorithm.
- We compare each class with every other class and see how many samples are misclassified.
- We actually come across several key metrics that are very important in the field of machine learning.

### Confusion Matrix Classification
Let's consider a binary classification case where the output is either **0** or **1**.

**True Positive(TP):**  
- These are the samples for which we predicted 1 (positive) as the output and the ground truth is 1 (positive) too.
- You projected positive and its turn out to be true.
- **For example**, you had predicted that France would win the world cup, and it won.  

**True Negative(TN):**  
- These are the samples for which we predicted 0 (negative) as the output and the ground truth is 0 (negative) too.
- When you predicted negative, and it's true.
- **For example**, you had predicted that England would not win and it lost.  

**False Positive(FP):**  
- These are the samples for which we predicted 1 (positive) as the output but the ground truth is 0 (negative).
- Your prediction is positive, and it is false.
- **For example**, you had predicted that England would win, but it lost.  

**False Negative(FN):**  
- These are the samples for which we predicted 0 (negative) as the output but the ground truth is 1 (positive).
- Your prediction is negative, and result it is also false.
- **For example**, you had predicted that France would not win, but it won.

|                       | Predicted Positive | Predicted Negative ||
|-----------------------|--------------------|----------------------------------|-|
| **Actual Positive**   | True Positive (TP)<br> 3 | False Negative (FN) <br> Error II<br> 1| Sensitivity <br> $\frac{TP}{TP + FN}$ |
| **Actual Negative**   | False Positive (FP) <br> Error I<br> 2| True Negative (TN) <br> 4| Specificity <br> $\frac{TN}{TN + FP}$ |
|                       | Precision <br> $\frac{TP}{TP + FP}$ | Negative Predictive Value <br> $\frac{TN}{TN + FN}$ | Accuracy <br> $\frac{TP + TN}{TP + TN + FP + FN}$ |

Precision = $\frac{TP}{TP + FP}$ = $\frac{3}{3 + 2}$ = 0.6 = 60%
Recall (Sensitivity) = $\frac{TP}{TP + FN}$ = $\frac{3}{3 + 1}$ = 0.75 = 75%

[Recall == Sensitivity]

F1 Score = 2 * $\frac{Precision * Recall}{Precision + Recall}$  
= 2 * $\frac{0.6 * 0.75}{0.6 + 0.75}$  
= 2 * $\frac{0.45}{1.35}$  
= 0.6667 = 66.67%   
