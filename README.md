# Ensemble Techniques

## 📌 What is Ensemble Learning?

**Ensemble Learning** is a machine learning technique where multiple models are combined to create a stronger and more accurate model.

Instead of depending on a single model, ensemble methods use several **base models (weak or strong learners)** and combine their predictions.

### Main Ensemble Techniques

1. **Bagging**
2. **Boosting**
3. **Stacking**

---

# 1. Bagging

## 📌 What is Bagging?

**Bagging** stands for **Bootstrap Aggregating**.

It creates multiple training datasets from the original dataset using **random sampling with replacement**. A separate model is trained on each dataset, and their predictions are combined.

### How Bagging Works

1. Start with the original training dataset.
2. Create multiple bootstrap samples by randomly selecting data **with replacement**.
3. Train a separate model on each sample.
4. Each model makes a prediction.
5. Combine the predictions:

   * **Classification:** Majority voting
   * **Regression:** Average of predictions

### Example

**Random Forest** is a popular Bagging-based algorithm.

```text
                 Original Dataset
                        |
          -----------------------------
          |            |              |
      Sample 1      Sample 2       Sample 3
          |            |              |
       Model 1       Model 2        Model 3
          |            |              |
          -------- Predictions -------
                        |
                 Final Prediction
```

### Advantages

* Reduces **variance**
* Helps prevent overfitting
* More stable than a single model
* Can be trained in parallel

### Disadvantages

* Can require more computational resources
* Does not necessarily reduce bias
* Multiple models can make the final model less interpretable

### Common Bagging Algorithms

* Bagging Classifier
* Bagging Regressor
* Random Forest
* Extra Trees

---

# 2. Boosting

## 📌 What is Boosting?

**Boosting** is an ensemble technique where models are trained **sequentially**.

Each new model focuses more on the errors made by the previous models.

The models are then com
