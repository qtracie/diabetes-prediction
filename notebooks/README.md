# Analysis Notebooks

This folder contains the core analytical workflow for the diabetes classification project.

### 📋 Workflow Summary:
1. **Data Cleaning:** Filtering and removing non-significant variables based on p-values (e.g., `Smoker`, `Fruits`, `AnyHealthcare`).
2. **Feature Engineering:** Implementing an interaction term between `DiffWalk` and `Age` to capture age-dependent mobility risks.
3. **Data Partitioning:** Splitting the dataset into **60% Train / 20% Validation / 20% Test** to prevent overfitting.
4. **Handling Imbalance:** Applying **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the target classes, increasing diabetic samples to ~130,000.
5. **Model Evaluation:** Comparing multiple algorithms with a focus on **Recall** to prioritize the detection of actual diabetic cases.
