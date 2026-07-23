# DL Lab 2 - Multi Layer Perceptron for Fashion-MNIST Classification

## Overview

This experiment focuses on implementing a Multi-Layer Perceptron (MLP) using TensorFlow/Keras for image classification on the Fashion-MNIST dataset. The experiment also demonstrates hyperparameter optimization using RandomizedSearchCV to identify the best model configuration. Various visualizations are generated to analyze the training process and evaluate model performance.

---

## Objective

- Understand the architecture of a Multi-Layer Perceptron (MLP).
- Implement an MLP using TensorFlow/Keras.
- Preprocess and normalize the Fashion-MNIST dataset.
- Train and evaluate the baseline MLP model.
- Perform hyperparameter optimization using RandomizedSearchCV.
- Compare the baseline and optimized models.
- Visualize training performance and classification results.

---

## Dataset Information

**Dataset Name:** Fashion-MNIST

**Source:** Zalando Research (available through TensorFlow/Keras)

**Training Samples:** 60,000

**Testing Samples:** 10,000

**Image Size:** 28 × 28 grayscale images

**Number of Classes:** 10

### Class Labels

- T-shirt/Top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle Boot

---

## Project Structure

```
DL Lab 2 - Multi Layer Perceptron
│
├── Code
│   ├── DL_LAB2.ipynb
│   └── requirements.txt
│
├── Figures
│   ├── sample_images.png
│   ├── class_distribution.png
│   ├── baseline_accuracy.png
│   ├── baseline_loss.png
│   ├── baseline_confusion_matrix.png
│   ├── optimized_accuracy.png
│   ├── optimized_loss.png
│   ├── optimized_confusion_matrix.png
│   ├── hyperparameter_search_results.png
│   └── baseline_vs_optimized.png
│
└── README.md
```

---
## Dependencies

The notebook was developed and executed using **Google Colab**.

The following Python libraries are used:

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- tensorflow
- scikeras

If running locally, install them using:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow scikeras
```

---

## Execution Instructions

1. Clone or download the repository.
2. Install the required dependencies.
3. Open the notebook (`DL_LAB2.ipynb`) in **Google Colab**.
4. Upload the notebook if opening it from your local machine.
5. Run all cells sequentially.

The notebook will:

- Load the Fashion-MNIST dataset
- Perform data preprocessing and normalization
- Build and train the baseline MLP model
- Evaluate the baseline model
- Perform hyperparameter optimization using RandomizedSearchCV
- Train the optimized model
- Compare baseline and optimized model performance
- Generate all required plots

---

## Model Evaluation Metrics

The trained models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Classification Report

---

## Hyperparameter Optimization

RandomizedSearchCV is used to optimize the following hyperparameters:

- Number of Hidden Layers
- Number of Neurons
- Activation Function
- Optimizer
- Learning Rate
- Dropout Rate
- Batch Size
- Number of Epochs

---

## Visualizations Generated

The experiment generates the following plots:

- Sample Images
- Class Distribution
- Training Accuracy vs Epoch
- Validation Accuracy vs Epoch
- Training Loss vs Epoch
- Validation Loss vs Epoch
- Baseline Confusion Matrix
- Optimized Confusion Matrix
- Hyperparameter Search Results
- Baseline vs Optimized Model Comparison

---

## Conclusion

The Multi-Layer Perceptron was successfully implemented for Fashion-MNIST image classification. A baseline model was trained and compared with a hyperparameter-optimized model obtained using RandomizedSearchCV. The experiment demonstrates the complete workflow of data preprocessing, model training, hyperparameter tuning, evaluation, and visualization, providing insight into the performance of deep learning models for image classification tasks.
