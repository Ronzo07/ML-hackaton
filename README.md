# ML-Hackathon

## Objective:
The goal of this project is to predict the number of cigarettes smoked per day by Lebanese university students, based on survey data about their habits and behaviors.

---

### Data Exploration:
In `visualize.ipynb`, we explored and visualized the dataset to understand relationships between various features and the target variable (cigarettes per day). Initial visualizations highlighted the need for feature engineering and dimensionality reduction to improve predictions.

---

### Model 1: Feature-Selected Random Forest (`model1.ipynb`)
In the first model, we selected key features for prediction:
- Gender
- Age
- First cigarette timing
- Exercise frequency
- Stress frequency
- Social media usage
- Smoker friends

We trained a **Random Forest Regressor** and initially observed low accuracy. After applying **boosting** and **hyperparameter tuning**, accuracy improved, but the model was still prone to **overfitting**. To address this, we applied **PCA (Principal Component Analysis)** to reduce feature dimensionality, which led to improved test-set performance.

---

### Model 2: Clustering and SVM with PCA (`model2.ipynb`)
Next, we explored clustering possibilities to distinguish smokers into categories. Using initial features like exercise frequency, stress frequency, and smoker friends, we observed that clustering did not yield clear separations.

We applied **PCA** to all features, reducing them to three components. With these components we applied **SVM (Support Vector Machine)**, achieving not perfect but great results:
  - Train Accuracy: **0.62**
  - Test Accuracy: **0.69**

**T-SNE (t-Distributed Stochastic Neighbor Embedding)** was used for visualization but failed to provide significant insights for clustering or improving predictions. Using **K-Means clustering** to categorize smokers based on the reduced t-sne features led to non effictive results.