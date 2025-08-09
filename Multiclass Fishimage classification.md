

# 🐟 Multiclass Fish Image Classification

## 📌 Overview

The **Multiclass Fish Image Classification** project leverages deep learning techniques to identify fish species from images. Using **Convolutional Neural Networks (CNN)** and **Transfer Learning** with state-of-the-art architectures such as **MobileNetV2**, **VGG16**, **ResNet50**, **InceptionV3**, and **EfficientNetB0**, the project aims to achieve high accuracy while maintaining computational efficiency.

A **Streamlit web application** is also provided for real-time fish species prediction and model confidence display, enabling practical deployment in fisheries, aquaculture, and research settings.

---

## 🎯 Problem Statement

Manual fish species identification is time-consuming, prone to human error, and inefficient for large-scale applications such as fisheries management, biodiversity monitoring, and aquaculture.
This project solves the problem by:

* Automating fish image classification.
* Ensuring high accuracy with minimal computational resources.
* Providing an easy-to-use web interface for real-time predictions.

---

## 🗂 Dataset

* **Structure:**

  ```
  fish_dataset/
  ├── train/
  │   ├── class_1/
  │   ├── class_2/
  │   ├── ...
  ├── val/
  │   ├── class_1/
  │   ├── class_2/
  │   ├── ...
  └── test/
      ├── class_1/
      ├── class_2/
      ├── ...
  ```
* Images are organized in separate folders per class.
* Preprocessing included resizing to **224×224 pixels** and normalizing pixel values to `[0, 1]`.

---

## 🏗 Project Workflow

1. **Data Loading & Preprocessing**

   * Applied ImageDataGenerator for data augmentation (rotation, zoom, shift, flip).
2. **Model Development**

   * Built a custom CNN model from scratch.
   * Implemented Transfer Learning with pre-trained models (MobileNetV2, VGG16, ResNet50, InceptionV3, EfficientNetB0).
3. **Model Training & Evaluation**

   * Trained each model with Early Stopping and Model Checkpoint callbacks.
   * Compared models based on Accuracy, Precision, Recall, and F1-score.
4. **Model Selection**

   * **MobileNetV2** achieved the best trade-off between accuracy and efficiency.
5. **Deployment**

   * Built a **Streamlit app** to classify uploaded fish images in real-time.

---

## 📊 Results & Insights

* **Best Model:** MobileNetV2
* **Accuracy:** \~98% on the test dataset.
* **Confusion Matrix** showed minimal misclassification between visually similar species.
* **Classification Report** confirmed high Precision, Recall, and F1-scores across all classes.

---

## 🖥 Streamlit Web App Usage

### 1️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 2️⃣ Run the App

```bash
streamlit run app.py
```

### 3️⃣ Upload an Image

* Select a fish image (`.jpg`, `.jpeg`, `.png`).
* Click **Predict** to see:

  * **Predicted Fish Species**
  * **Model Confidence (%)**

---

## 📦 File Structure

```
.
├── fish_dataset/             # Dataset folder
├── models/                   # Saved models
│   └── MobileNetV2_best_model.h5
├── notebooks/                # Jupyter notebooks for training & EDA

```

---

## 🚀 Future Improvements

* Expand dataset with more fish species.
* Add real-time video stream classification.
* Develop a mobile-friendly version of the application.
* Use ensemble learning for even higher accuracy.

---

## 🏆 Conclusion

This project proves that **Transfer Learning with MobileNetV2** can efficiently classify multiple fish species with high accuracy. The deployment-ready **Streamlit app** ensures usability for researchers, fisheries, and aquaculture businesses, enabling **faster, more accurate, and scalable fish identification**.

---

