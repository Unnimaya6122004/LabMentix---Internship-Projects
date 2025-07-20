# 🧠 Brain Tumor MRI Image Classification

An AI-powered project for classifying brain tumors using MRI images. This solution leverages both custom Convolutional Neural Networks and Transfer Learning (MobileNetV2) to detect tumor types such as **Glioma**, **Meningioma**, **Pituitary**, and **No Tumor**. A user-friendly Streamlit web app is included for real-time image-based predictions.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Project Workflow](#project-workflow)
- [Model Architectures](#model-architectures)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Streamlit App](#streamlit-app)
- [How to Run](#how-to-run)
- [Conclusion](#conclusion)
- [Future Scope](#future-scope)
- [License](#license)

---

## 📖 Overview

Brain tumors are life-threatening conditions that require early detection. This deep learning project classifies MRI images into tumor types using supervised learning. It compares a **custom CNN model** with a **pretrained MobileNetV2 model**, analyzes performance, and deploys the best model through a **Streamlit** application.

---

## 🗂️ Dataset

- **Source**: [Kaggle - Brain Tumor Dataset](https://www.kaggle.com/datasets)
- **Categories**: `glioma`, `meningioma`, `pituitary`, `no tumor`
- **Data Type**: MRI images (JPG/PNG)
- **Classes**: 4
- **Preprocessing**:
  - Resized to `224x224`
  - Normalized (pixel values scaled to 0–1)
  - Data augmentation applied during training

---

## 🔁 Project Workflow

1. **Dataset Exploration**
   - Sample image visualization
   - Class balance check
2. **Preprocessing**
   - Resize and normalize images
3. **Data Augmentation**
   - Flip, rotate, zoom, brightness shifts
4. **Model Building**
   - Custom CNN from scratch
   - Transfer Learning with MobileNetV2
5. **Model Training**
   - Early stopping & learning rate scheduling
6. **Model Evaluation**
   - Accuracy, Precision, Recall, F1-Score, Confusion Matrix
7. **Model Deployment**
   - Streamlit web app for live predictions

---

## 🧱 Model Architectures

### 1️⃣ Custom CNN
- 3 Conv2D + MaxPooling layers
- Batch Normalization, Dropout
- Dense layers with softmax output

### 2️⃣ MobileNetV2 (Transfer Learning)
- Pretrained on ImageNet
- Top layers replaced with:
  - GlobalAveragePooling
  - Dense → Dropout → Softmax

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Precision, Recall, F1-Score**
- **Confusion Matrix**
- **Training vs Validation Curves**

---

## ✅ Results

| Model        | Accuracy | Macro F1-Score | Remarks                         |
|--------------|----------|----------------|----------------------------------|
| Custom CNN   | 19%      | 0.08           | Underfitting, poor performance  |
| MobileNetV2  | 91%      | 0.81           | Best results, reliable for deployment |

- **Classification Report (MobileNetV2)**:
  - No Tumor: F1 = 1.00
  - Glioma: F1 = 0.97
  - Meningioma: F1 = 0.40 (improvable)
  - Pituitary: F1 = 0.86

---

## 🌐 Streamlit App

- Upload an MRI scan image
- The app predicts the tumor type
- Displays prediction confidence
- Built-in preprocessor for uploaded images

---

## 🧪 How to Run

### 📍 In Google Colab:
```python
!pip install streamlit colabcode
from colabcode import ColabCode
ColabCode(port=10000, code=False)
