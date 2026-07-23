# DL Lab 1 - Single Layer Perceptron for Binary Classification

## Overview

This experiment focuses on implementing a Single Layer Perceptron from scratch for binary classification. The model is trained using the Banknote Authentication Dataset and demonstrates how a perceptron learns by updating its weights and bias based on classification errors. Various visualizations are generated to study the learning behaviour and evaluate model performance.

---

## Objective

- Understand the concept of an artificial neuron and perceptron.
- Implement the Perceptron Learning Algorithm from scratch using Python.
- Train the model for binary classification.
- Analyze weight and bias updates during training.
- Evaluate model performance using classification metrics.
- Visualize the learning process using graphs and decision boundaries.

---

## Dataset Information

**Dataset Name:** Banknote Authentication Dataset

**Source:** UCI Machine Learning Repository

**Number of Samples:** 1372

**Input Features:**

1. Variance
2. Skewness
3. Kurtosis
4. Entropy

**Target Variable:**

- 0 → Authentic Banknote
- 1 → Forged Banknote

---

## Project Structure

```
DL Lab 1 - Single Layer Perceptron
│
├── Code
│   ├── lab1.ipynb
│   └── requirements.txt
│
├── Figures
│   ├── feature_histograms.eps
│   ├── scatter_plot.eps
│   ├── boxplots.eps
│   ├── correlation_heatmap.eps
│   ├── training_error_vs_epoch.eps
│   ├── weight_evolution.eps
│   ├── bias_evolution.eps
│   ├── confusion_matrix.eps
│   ├── learning_rate_comparison.eps
│   └── decision_boundary.eps
│
└── README.md
```

---

## Dependencies

The notebook was developed and executed using **Google Colab**.

The following Python libraries are required:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## Execution Instructions

1. Clone or download the repository.
2. Install the required dependencies.
3. Open the notebook (`lab1.ipynb`) in Google Colab.
4. Run all cells sequentially.
5. The notebook will:
   - Load and preprocess the dataset
   - Train the perceptron model
   - Display epoch-wise learning progress
   - Generate evaluation metrics
   - Produce all required plots

---

## Model Evaluation Metrics

The trained model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Visualizations Generated

The experiment generates the following plots:

- Feature Histograms
- Scatter Plot Matrix
- Boxplots
- Correlation Heatmap
- Training Error vs Epoch
- Weight Evolution
- Bias Evolution
- Decision Boundary
- Confusion Matrix

---

## Conclusion

The Single Layer Perceptron successfully learned to classify banknotes into authentic and forged categories. The experiment demonstrates the importance of weight updates, bias adjustment, and learning rate in the perceptron learning process. The generated visualizations provide insight into model convergence and classification performance.
