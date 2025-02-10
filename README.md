# README

## Project Overview

### 1. Name:
**Research on the Impact of CNN Architecture and Loss Functions in Image Segmentation**

### 2. Objective:
To investigate the influence of different convolutional neural network (CNN) architectures and loss functions on image segmentation performance. The study focuses on comparing models such as SegNet and UNet (including two versions of UNet) using various loss functions to determine their effectiveness in improving segmentation accuracy.

### 3. Evaluation Metric:
- **Intersection Over Union (IoU)**: A standard metric for evaluating the quality of image segmentation by measuring the overlap between predicted and ground truth masks.

### 4. Convolutional Neural Network Architectures:
- **SegNet**: A popular architecture for semantic segmentation that uses an encoder-decoder structure with skip connections.
- **UNet**: Known for its efficient design, UNet employs a contracting path to capture context and an expansive path to enable precise localization.
- **UNet2 (Stride Version)**: An updated version of UNet utilizing stride techniques to enhance performance.

### 5. Loss Functions:
The project evaluates the following loss functions:
- **Binary Cross-Entropy (BCE)**: A standard loss function for binary classification tasks.
- **DICE Loss**: Measures the similarity between predicted and true masks, often used in medical image segmentation.
- **FOCAL LOSS**: Designed to address class imbalance by focusing on hard-to-classify examples.
- **BCE Supervised Regularization**: Combines BCE with regularization techniques to improve model stability and generalization.

### 6. Results Analysis:
The analysis includes:
- **Comparison of IoU metrics across epochs for each neural network architecture with different loss functions on the validation dataset**.
- **Comparison of IoU metrics across epochs for each loss function across neural network architectures on the validation dataset**.
- **Final comparison of IoU metrics on the test dataset to identify the best-performing model**.

---

## Project Structure

- **Data**: Contains the datasets used for training, validation, and testing.
- **Models**: Includes implementations of SegNet, UNet, and UNet2 architectures.
- **Loss_Functions**: Definitions and implementations of the loss functions (BCE, DICE, FOCAL LOSS, BCE Supervised Regularization).
- **Results**: Stores the results of experiments, including IoU metrics and visualizations.
- **Notebooks**: Jupyter notebooks with detailed steps for data preprocessing, model training, evaluation, and result analysis.

---

## Key Findings

1. **Architecture Comparison**:
   - SegNet demonstrated robust performance but was outperformed by UNet variants in terms of IoU on complex datasets.
   - UNet2 (stride version) showed improvements over the original UNet due to its stride-based optimizations.

2. **Loss Function Impact**:
   - FOCAL LOSS proved effective in handling class imbalance, significantly improving IoU for datasets with uneven class distributions.
   - DICE Loss performed well in cases where high precision in boundary detection was required.

3. **Best Model**:
   - The combination of **UNet2 (stride)** with **FOCAL LOSS** achieved the highest IoU score on the test dataset, making it the leading model in this study.

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repository-link.git
