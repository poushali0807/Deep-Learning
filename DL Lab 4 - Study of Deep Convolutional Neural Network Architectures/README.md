
# DL Lab 4 - Comparative Study of Deep CNN Architectures Using Transfer Learning

## Overview
This experiment focuses on implementing and comparing deep Convolutional Neural Network (CNN) architectures — LeNet-5, AlexNet, VGG16, GoogleNet (InceptionV3) and ResNet50 — for image classification on the CIFAR-10 dataset. The experiment demonstrates transfer learning using pretrained ImageNet models (VGG16, ResNet50, InceptionV3), fine-tuning of convolutional layers, and a hyperparameter study across learning rate, batch size, optimizer, dense units, and frozen-layer configurations. Various visualizations are generated to analyze the training process and evaluate model performance.

## Objective
* Study the evolution of deep CNN architectures.
* Compare LeNet-5, AlexNet, VGG16, GoogleNet and ResNet.
* Understand and implement transfer learning.
* Fine tune pretrained CNN models.
* Compare classification performance of different architectures using performance metrics.

## Dataset Information
**Dataset Name:** CIFAR-10
**Source:** Available through TensorFlow/Keras (`tf.keras.datasets.cifar10`)
**Training Samples:** 45,000 (after carving out a validation split)
**Validation Samples:** 5,000
**Testing Samples:** 10,000
**Image Size:** 32 × 32 × 3 (RGB)
**Number of Classes:** 10

### Class Labels
* Airplane
* Automobile
* Bird
* Cat
* Deer
* Dog
* Frog
* Horse
* Ship
* Truck

## Project Structure
```
DL Lab 4 - CNN Architectures Transfer Learning
│
├── Code
│   ├── Experiment_4_Transfer_Learning.ipynb
│   └── requirements.txt
│
├── Figures
│   ├── sample_images.png
│   ├── training_accuracy.png
│   ├── validation_accuracy.png
│   ├── training_loss.png
│   ├── validation_loss.png
│   ├── confusion_matrix.png
│   └── misclassified_images.png
│
├── Results
│   ├── cnn_comparison_results.csv
│   └── hyperparameter_study_results.csv
│
└── README.md
```

## Dependencies
The notebook was developed and executed using Google Colab (GPU runtime).
The following Python libraries are used:

* numpy
* pandas
* matplotlib
* scikit-learn
* tensorflow

If running locally, install them using:
```
pip install numpy pandas matplotlib scikit-learn tensorflow
```

## Execution Instructions
1. Clone or download the repository.
2. Install the required dependencies.
3. Open the notebook (`Experiment_4_Transfer_Learning.ipynb`) in Google Colab.
4. Upload the notebook if opening it from your local machine.
5. Enable GPU: **Runtime → Change runtime type → T4 GPU**.
6. Run all cells sequentially.

The notebook will:
* Load and preprocess the CIFAR-10 dataset (normalize to [0,1], split into train/validation/test)
* Display sample images and print dataset dimensions
* Build a transfer-learning model (VGG16 by default) with a frozen pretrained base
* Train the classifier head (Task 3)
* Fine-tune the last convolutional block of the pretrained base (Task 4)
* Evaluate the model on the held-out test set (Accuracy, Precision, Recall, F1-score, Confusion Matrix)
* Generate all mandatory plots
* Train LeNet-5 and AlexNet from scratch for architecture comparison
* Run the transfer-learning pipeline for ResNet50 and GoogleNet (InceptionV3)
* Build the final CNN architecture comparison table
* Run a hyperparameter study varying one setting at a time

## Model Evaluation Metrics
The trained models are evaluated using:
* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

## Transfer Learning Pipeline
Each pretrained model (VGG16, ResNet50, InceptionV3) follows the same workflow:
1. Load pretrained ImageNet weights, excluding the original classification layer.
2. Freeze the convolutional base.
3. Add a Global Average Pooling layer.
4. Add a Dense layer with ReLU activation.
5. Add a Softmax output layer for 10-class classification.
6. Train the classifier head (frozen base) with Adam, learning rate 0.001.
7. Unfreeze the last convolutional block and fine-tune with a lower learning rate (1e-5).

**Note:** Pixel values are normalized to [0,1] as required, and re-scaled internally immediately before each model's `preprocess_input` call, since ImageNet-pretrained models expect their own specific input preprocessing (e.g. mean-subtracted [0,255]-range values).

## Hyperparameter Study
One factor is varied at a time from a fixed baseline configuration to compare the effect of:
* Learning Rate: 0.001, 0.0001
* Batch Size: 16, 32, 64
* Epochs: 10, 20
* Optimizer: Adam, SGD
* Dense Units: 128, 256
* Frozen Layers: All, Partial

## Visualizations Generated
The experiment generates the following plots:
* Sample CIFAR-10 Images
* Training Accuracy vs Epoch
* Validation Accuracy vs Epoch
* Training Loss vs Epoch
* Validation Loss vs Epoch
* Confusion Matrix
* Misclassified Images (optional)

## Architecture Comparison
LeNet-5 and AlexNet are trained from scratch on CIFAR-10 (not available as pretrained ImageNet models in Keras). VGG16, ResNet50, and GoogleNet (via InceptionV3, its closest available successor in `keras.applications`) are run through the full transfer-learning pipeline. All five models are evaluated on the same held-out test set for a fair, direct comparison of Parameters, Accuracy, and Training Time.

## Conclusion
Five CNN architectures — LeNet-5, AlexNet, VGG16, GoogleNet (InceptionV3) and ResNet50 — were implemented and compared for CIFAR-10 image classification. Transfer learning with pretrained ImageNet weights was used for VGG16, ResNet50 and GoogleNet, followed by fine-tuning of the final convolutional block to improve performance further. The experiment demonstrates the complete workflow of dataset preparation, transfer learning, fine-tuning, evaluation, hyperparameter analysis, and visualization, providing insight into the trade-offs between model depth, parameter count, accuracy, and training time across classical and modern CNN architectures.

