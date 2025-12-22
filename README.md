# Brain Tumor Detection using CNN

![Project Type](https://img.shields.io/badge/Type-Deep%20Learning%20Project-blue)
![Python](https://img.shields.io/badge/Python-3.11-blue)
![Framework](https://img.shields.io/badge/Framework-TensorFlow%20%7C%20Keras-orange)
![Domain](https://img.shields.io/badge/Domain-Medical%20Imaging-red)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Project Overview

**This project is developed by Muhammad Javed for learning and practice purposes.**

This repository presents a **Brain Tumor Detection system** using a **Convolutional Neural Network (CNN)** built with **TensorFlow and Keras**.  
The goal is to classify **Brain MRI images** into **tumorous** and **non-tumorous** categories.

The dataset is taken from **Kaggle**:  
🔗 https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection

---

## Dataset Information

The dataset consists of **253 Brain MRI images**:

- **Tumor (Yes):** 155 images  
- **No Tumor (No):** 98 images  

### After Data Augmentation

- **Tumor:** 1085 images  
- **No Tumor:** 980 images  
- **Total:** 2065 images  

> The augmented dataset also includes original images and is stored in the `augmented_data` folder.

---

## Data Augmentation

### Why Data Augmentation?

- Dataset was very small  
- Class imbalance problem  
- To reduce overfitting and improve generalization  

Detailed explanation is provided inside the Data Augmentation notebook.

---

## Data Preprocessing

Each image goes through the following steps:

1. Crop the brain region  
2. Resize to **(240, 240, 3)**  
3. Normalize pixel values to **0–1**  

---

## Data Split

- **70%** Training  
- **15%** Validation  
- **15%** Testing  

---

## CNN Architecture

![CNN Architecture](convnet_architecture.jpg)

### Architecture Summary

1. Zero Padding  
2. Convolution (32 filters, 7×7)  
3. Batch Normalization  
4. ReLU Activation  
5. Max Pooling (4×4)  
6. Max Pooling (4×4)  
7. Flatten  
8. Dense layer with Sigmoid activation  

---

## Model Training

- Trained for **24 epochs**
- Best model achieved at **epoch 23**

### Training Curves

**Loss Curve**  
![Loss Plot](Loss.PNG)

**Accuracy Curve**  
![Accuracy Plot](Accuracy.PNG)

---

## Results

| Metric     | Validation | Test |
|-----------|-----------|------|
| Accuracy  | 91%       | 89%  |
| F1 Score  | 0.91      | 0.88 |

These results are strong considering dataset size and balance.

---

## Model Usage

```python
from tensorflow.keras.models import load_model
best_model = load_model('models/cnn-parameters-improvement-23-0.91.model')

## Author

**Muhammad Javed**  
Computer Engineering Student | Machine Learning Enthusiast  

---

## Contact

- **GitHub:** https://github.com/Muhammad-Javed2005  
- **LinkedIn:** https://www.linkedin.com/in/muhammad-javed-24b262369/  
- **Email:** muhammadjaved.tech5@gmail.com  

---

⭐ If you find this study material useful, consider giving the repository a star.
