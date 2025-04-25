# RNNs  
# Advanced Sentiment Analysis System Using RNNs

---

## Table of Contents
1. [Project Overview and Objectives](#project-overview-and-objectives)
2. [Dataset Acquisition and Preparation](#dataset-acquisition-and-preparation)
3. [Text Preprocessing](#text-preprocessing)
4. [Feature Extraction](#feature-extraction)
5. [Model Training](#model-training)
6. [Hyperparameter Tuning](#hyperparameter-tuning)
7. [Model Evaluation](#model-evaluation)
8. [Carbon Footprint Analysis with CodeCarbon](#carbon-footprint-analysis-with-codecarbon)
9. [Ethical Considerations and Model Explainability](#ethical-considerations-and-model-explainability)
10. [Deployment on Embedded Systems](#deployment-on-embedded-systems)
11. [Code Release Responsibilities](#code-release-responsibilities)
12. [License](#license)

---

## Project Overview and Objectives

The goal of this project is to build an advanced **sentiment analysis model** using **Recurrent Neural Networks (RNNs)**.

Objectives include:
- Preprocess and vectorize text reviews
- Train, tune, and evaluate.
- Visualize model explainability using **SHAP** and **LIME**
- Measure the **carbon footprint** using CodeCarbon
- Reflect on **ethical considerations** in AI
- Deploy the model to an embedded system

---

## Dataset Acquisition and Preparation

- Download the IMDb dataset
- Prepare training and testing datasets
- Organize reviews into a dataframe

---

## Text Preprocessing

- Remove HTML tags and punctuation
- Convert all text to lowercase
- Remove English stopwords
- Tokenize and pad sequences to a fixed length (e.g., 200 tokens)

---

## Feature Extraction

- Use **Keras Tokenizer** to build a word index.
- Convert reviews into **integer sequences**.
- Use a **Keras Embedding layer** to learn vector representations of words.

---

## Model Training

- Stack two **Bidirectional LSTM** layers.
- Add a fully connected **Dense** layer with ReLU activation.
- Add a **Dropout** layer to prevent overfitting.
- Output layer with **sigmoid** activation for binary classification.
- Apply **EarlyStopping** with a patience of 4 epochs during training.

---

## Hyperparameter Tuning

- Experimented with different:
  - Learning rates (e.g., 0.001, 0.0005)
  - Dropout rates (e.g., 0.3, 0.5)
  - Batch sizes (e.g., 32, 64)
  - Sequence lengths (e.g., 200, 250)
- Selected the best combination based on validation performance.
- A function doing this tuning automatically should be implemented in the future.

---

## Model Evaluation

- Evaluate performance on unseen test data:
  - Accuracy and Loss metrics
  - Confusion Matrix
  - Classification Report (Precision, Recall, F1-Score)
- Run predictions on sample review texts to test generalization.

---

## Carbon Footprint Analysis with CodeCarbon

- Used the **CodeCarbon** package to track and report carbon emissions during training.
- Measured and reported total **kg of CO₂** generated.

---

## Ethical Considerations

-Potential misuse to filter out negative feedback or fail to distinguish between genuine reviews and AI-generated content
-Human judgment remains essential when interpreting results

## Model Explainability

TODO

---

## Deployment on Embedded Systems

TODO

---

## Code Release Responsibilities

When releasing the project on GitHub:
- All pull requests must be validated by at least one team member.
- Unit tests should run automatically in a CI/CD pipeline.
- Use static analysis tools (e.g., **SonarCloud**) for syntax and quality validation.
- Follow responsible bug reporting practices:
  - Use GitHub Issues for tracking
  - Require review for pull requests
- Documentation must be updated when major changes are made.

---

## License

This project is licensed under the **MIT License**.  
The MIT License permits reuse, including commercial use, while requiring attribution to the original author.

---
