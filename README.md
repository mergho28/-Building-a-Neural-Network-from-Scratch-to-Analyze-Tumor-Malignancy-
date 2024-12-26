# -Building-a-Neural-Network-from-Scratch-to-Analyze-Tumor-Malignancy-

This project implements a neural network from scratch to predict tumor malignancy using the Wisconsin Breast Cancer dataset. This dataset rated tumors on their malignancy due to individual scores ranging from 1-10 that were given to different features of the tumors' microenvironment. These 9 features ranged from cell size and shape to characteristics such as cell adhesion. It demonstrates key machine learning concepts such as forward propagation, backpropagation, loss computation, and gradient descent while providing a foundation for developing more advanced models.

---

## Features

- **Neural Network Architecture**:
  - Input layer: 9 features.
  - Hidden layer: 15 neurons using ReLU activation.
  - Output layer: 1 neuron using Sigmoid activation for binary classification.

- **Dataset Preprocessing**:
  - Handles missing values.
  - Scales features to a range of 0 to 1 using MinMaxScaler.
  - Splits data into training and validation sets.

- **Evaluation Metrics**:
  - Binary Cross-Entropy Loss for optimization.
  - Accuracy and confusion matrices for performance evaluation.

---

## How It Works

### 1. **Preprocessing**
- Loads the Wisconsin Breast Cancer dataset.
- Maps the target class: `2` (benign) → `0`, `4` (malignant) → `1`.
- Drops irrelevant columns (e.g., ID) and handles missing values in the `Bare_Nuclei` feature.
- Scales features using `MinMaxScaler` for uniform input ranges.
- Splits the data into training and validation sets.

### 2. **Network Architecture**
- **Input Layer**: Accepts 9 normalized features.
- **Hidden Layer**: Uses 15 neurons with ReLU activation to introduce non-linearity and prevent vanishing gradients.
- **Output Layer**: Uses Sigmoid activation to produce a probability value for classification (benign or malignant).

### 3. **Training**
- **Forward Propagation**:
  - Computes weighted sums and activations for each layer.
  - Stores intermediate results in a cache for efficient backpropagation.
- **Loss Calculation**:
  - Uses binary cross-entropy to evaluate prediction accuracy.
- **Backpropagation**:
  - Computes gradients for weights and biases using the chain rule.
  - Updates parameters using gradient descent with a fixed learning rate (`lr`).

### 4. **Evaluation**
- Predictions are generated by thresholding the Sigmoid output.
- Calculates accuracy by comparing predictions with actual labels.
- Generates confusion matrices to visualize performance.

### 5. How to run 
- Click on the "code" file in this repository
- Copy and paste the code and run in a Python environment
---
