# 🩺 Lung Cancer Detection from Chest CT-Scans

![Deep Learning](https://img.shields.io/badge/Deep%20Learning-PyTorch-orange) ![Medical Imaging](https://img.shields.io/badge/Domain-Medical%20Imaging-blue) ![License](https://img.shields.io/badge/License-MIT-green)

This repository contains a comprehensive Deep Learning pipeline for classifying lung cancer types from Chest CT-scan images. Using a pre-trained **ResNet-18** architecture and transfer learning, the model distinguishes between three types of lung cancer and normal scans with high precision.

## 📝 Project Summary
Lung cancer remains one of the leading causes of cancer-related mortality. Early diagnosis via Computed Tomography (CT) is critical. This project automates the classification of CT-scans into four categories:
1.  **Adenocarcinoma**
2.  **Large Cell Carcinoma**
3.  **Squamous Cell Carcinoma**
4.  **Normal (Healthy)**

## 📊 Dataset
The project uses the [Chest CT-Scan images Dataset](https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images) available on Kaggle. It includes training, validation, and test splits for objective performance evaluation.

## 🛠️ Technical Stack
- **Framework**: PyTorch
- **Model**: ResNet-18 (Pre-trained on ImageNet)
- **Optimization**: SGD with Momentum
- **Visualization**: Matplotlib, Seaborn, Grad-CAM, t-SNE

## 📈 Performance Highlights
- **Test Macro F1 Score**: `0.9366` 
- **Classification Accuracy**: `~93.06%` on validation.
- **Area Under Curve (AUC)**:
    - Normal: **0.999**
    - Squamous Cell: **0.991**
    - Large Cell: **0.990**
    - Adenocarcinoma: **0.975**

## 🔍 Explainable AI (XAI)
To ensure clinical relevance, this project implements:
- **Grad-CAM**: Visualizes activation heatmaps to show exactly where the model is looking in the lung tissue to make a diagnosis.
- **t-SNE Embeddings**: Shows how the ResNet-18 features naturally cluster the different cancer types in high-dimensional space.
- **Weight Matrix Analysis**: Inspects the final decision layer's learned weights.

## 🚀 Getting Started
1. **Prerequisites**: 
   - Google Colab or a local Python environment with a GPU.
   - Kaggle API credentials (`kaggle.json`).
2. **Installation**:
   ```bash
   pip install torch torchvision scikit-learn seaborn matplotlib
   ```
3. **Execution**: Run the notebook cells sequentially to download data, train the model, and generate evaluation plots.

## ⚖️ License
This project is licensed under the MIT License.
