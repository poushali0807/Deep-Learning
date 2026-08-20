DL Lab 3 - Convolutional Neural Networks for CIFAR-10 Classification
Overview

This experiment focuses on implementing a Convolutional Neural Network (CNN) using PyTorch for image classification on the CIFAR-10 dataset. The experiment covers the convolution operation, the effect of kernel size, stride, and padding on output dimensions, feature map visualization, and a comparison of pooling strategies and activation functions. The trained CNN is evaluated using standard classification metrics, and additional exercises analyze parameter counts, activation functions, and filter counts.

Objective
Understand the working principle of Convolutional Neural Networks.
Implement convolution, pooling, and feature map visualization using PyTorch.
Study the effect of kernel size, stride, and padding on output feature map dimensions.
Build and train a CNN for image classification on CIFAR-10.
Compare Max Pooling vs Average Pooling and ReLU vs Sigmoid activation functions.
Evaluate CNN performance using standard classification metrics.
Analyze the effect of increasing convolution filters on accuracy and training time.
Dataset Information

Dataset Name: CIFAR-10
Source: University of Toronto (available through torchvision)
Training Samples: 50,000
Testing Samples: 10,000
Image Size: 32 × 32 × 3 (RGB)
Number of Classes: 10

Class Labels
Airplane
Automobile
Bird
Cat
Deer
Dog
Frog
Horse
Ship
Truck
Project Structure
DL Lab 3 - Convolutional Neural Networks
│
├── Code
│   ├── DL_EXP3.ipynb
│   └── requirements.txt
│
├── Figures
│   ├── sample_images3.png
│   ├── class_dist.png
│   ├── accuracy_plot.png
│   ├── loss_plot.png
│   ├── feature_maps.png
│   ├── confusion_matrix3.png
│   └── pooling_comparison.png
│
└── README.md
Dependencies

The notebook was developed and executed using Google Colab.
The following Python libraries are used:

numpy
matplotlib
seaborn
scikit-learn
torch
torchvision

If running locally, install them using:

pip install numpy matplotlib seaborn scikit-learn torch torchvision
Execution Instructions
Clone or download the repository.
Install the required dependencies.
Open the notebook (DL_EXP3.ipynb) in Google Colab.
Upload the notebook if opening it from your local machine.
Run all cells sequentially.

The notebook will:

Load the CIFAR-10 dataset
Display sample images and plot the class distribution
Compare feature map sizes across different kernel sizes (3×3, 5×5, 7×7)
Study the effect of stride and padding on output dimensions
Visualize feature maps after the first convolution layer
Compare Max Pooling and Average Pooling
Build and train the CNN (Conv → ReLU → MaxPool → Conv → ReLU → MaxPool → Flatten → Dense)
Evaluate the trained model on the test set
Run additional exercises: ReLU vs Sigmoid, filter count comparison, and analytical calculations
Model Architecture
Input → Conv → ReLU → MaxPool → Conv → ReLU → MaxPool → Flatten → Dense → Softmax
Optimizer: Adam
Epochs: 20
Batch Size: 32
Total Trainable Parameters: 25,578
Model Evaluation Metrics

The trained model is evaluated using:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Classification Report
Results Summary
Metric	Value
Training Accuracy	76.75%
Testing Accuracy	67.83%
Precision (macro)	68.35%
Recall (macro)	67.83%
F1-score (macro)	67.74%
Number of Parameters	25,578
Additional Exercises
Output size calculation for a 64×64 image, 5×5 kernel, stride 2, padding 2 → 32×32
Trainable parameters for 64 filters of size 3×3 with RGB input → 1,792
ReLU vs Sigmoid activation comparison
Max Pooling vs Average Pooling comparison
Filter count comparison (16 vs 64 filters) — accuracy and training time trade-off
Visualizations Generated

The experiment generates the following plots:

Sample Images
Class Distribution
Training Accuracy vs Epoch
Validation Accuracy vs Epoch
Training Loss vs Epoch
Validation Loss vs Epoch
Feature Maps (after first convolution layer)
Confusion Matrix
Max Pooling vs Average Pooling Comparison


Conclusion

A Convolutional Neural Network was successfully implemented for CIFAR-10 image classification using PyTorch. The model achieved a test accuracy of 67.83%, with the gap between training and validation performance indicating mild overfitting beyond roughly epoch 5. The experiment demonstrates the complete CNN workflow — convolution, pooling, feature map visualization, training, and evaluation — along with comparisons of pooling strategies, activation functions, and filter counts, providing insight into the design trade-offs involved in building CNNs for image classification.



