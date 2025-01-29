# Boosting

- Boosting is an ensemble learning technique that improves model performance by sequentially training weak learners, where each model tries to correct the mistakes of the previous one. 


# How Boosting Works

## 1. Sequential Learning
- Models (**weak learners**) are trained one after another.
- Each new model focuses more on the **misclassified examples** from the previous model.

## 2. Weighted Data Points
- Initially, all data points are assigned **equal weights**.
- After each iteration:
  - Incorrectly predicted data points receive **higher weights**.
  - The next model focuses more on these difficult cases.

## 3. Aggregation
- The final prediction is made by **combining the outputs** of all weak learners.
- Often, a **weighted sum** is used to determine the final result.



# **Boosting: A Step-by-Step Guide**

1. **Initialization:**
   * Assign equal weights to all training samples.
   * Train the first weak learner (e.g., a simple decision tree) on the initial weighted dataset.

2. **Weight Adjustment:**
   * Analyze the performance of the first weak learner.
   * Increase the weights of misclassified samples.
   * Decrease the weights of correctly classified samples.

3. **Subsequent Learners:**
   * Train subsequent weak learners on the updated weighted dataset, focusing on the samples that were previously misclassified.
   * Adjust the weights of each weak learner based on their performance.

4. **Final Model:**
   * Combine the predictions of all weak learners:
        * Typically through weighted voting or averaging.
   * This combined output forms the final prediction.



**Boosting**

Boosting is an ensemble learning technique aimed at improving the accuracy of predictions by training models sequentially, where each model tries to correct the errors of its predecessor.

1. **Initialization**: Start with assigning equal weights to all training samples.

2. **Training**: Fit the first model to the data. For each subsequent model, adjust the weights of the training samples based on the errors of the previous model's predictions. More weight is given to misclassified samples to focus the next model on correcting those errors.

3. **Combining**: The final prediction is made by combining the predictions of all models, often with a weighted vote or sum.

Some well-known algorithms that use boosting include:
- **AdaBoost** (Adaptive Boosting)
- **Gradient Boosting Machines (GBM)**
- **XGBoost** (Extreme Gradient Boosting)
- **LightGBM**
