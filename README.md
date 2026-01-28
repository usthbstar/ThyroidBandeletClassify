# Adaptive Bandelet Transform and Transfer Learning for Geometry-Aware Thyroid Cancer Ultrasound Classification

This repository provides the implementation of the methodology proposed in the paper:

**Adaptive Bandelet Transform and Transfer Learning for Geometry-Aware Thyroid Cancer Ultrasound Classification**  
Y. Habchi, H. Kheddar, M. C. Ghanem, J. Hwaidi (2025)

The framework integrates a geometry-adaptive Bandelet Transform (BT) with Transfer Learning (TL) to improve feature representation and classification performance of thyroid ultrasound (US) images.

---

## 📌 Overview

The proposed pipeline consists of three main stages:

1. **Pre-processing**
   - Class balancing using SMOTE
   - Data augmentation (rotation, flipping, brightness, resizing)
   - Image normalization

2. **Feature Selection (Bandelet Transform)**
   - Quadtree decomposition
   - Warped wavelet coefficients
   - Geometry-adaptive bandelet coefficients extraction

3. **Deep Classification (Transfer Learning)**
   - Pre-trained CNN architectures (VGG19, ResNet, DenseNet, etc.)
   - Fine-tuning for benign vs malignant classification
   - Performance evaluation using Accuracy, Sensitivity, Specificity, and F1-score

---

## 📂 Project Structure


---

## 🧪 Dataset

This work uses the **DDTI (Digital Database of Thyroid Ultrasound Images)** dataset:

- 134 ultrasound images  
- 14 benign / 62 malignant (original)  
- Balanced using SMOTE to 28 benign / 28 malignant  
- Augmented to 2048 images  
- Images resized to 512×512 then 224×224  

Dataset link:  
http://cimalab.unal.edu.co/?lang=en&mod=project&id=31

---

## ⚙️ Requirements

- MATLAB (R2022+ recommended)
- Python 3.8+
- MATLAB Toolboxes:
  - Deep Learning Toolbox
  - Image Processing Toolbox

Python libraries:


---

## 🚀 How to Run

### Step 1: Pre-processing

Run scripts in:


- `Smote.m` → balance the dataset  
- `Data_augmentation.py` → perform data augmentation  
- `Imageresize.m` → resize images  

---

### Step 2: Feature Selection (Bandelet Transform)

Run:


- `Smote.m` → balance the dataset  
- `Data_augmentation.py` → perform data augmentation  
- `Imageresize.m` → resize images  


This step generates geometry-adaptive bandelet coefficient maps using quadtree decomposition and warped wavelets.

---

### Step 3: Deep Classification (Transfer Learning)

Run:

or


Pre-trained models include:
- VGG19 (best performing)
- ResNet50
- DenseNet201
- MobileNetV2
- EfficientNetB0

---

## 📊 Performance (Best Result)

Using BT + TL (VGG19) with quadtree threshold **T = 30**:

- Accuracy: **98.91%**
- Sensitivity: **98.11%**
- Specificity: **97.31%**
- F1-score: **98.89%**
- Precision: **99.68%**

The proposed method outperforms classical wavelet and standalone transfer learning approaches.

---

## 🧠 Key Contributions

- Geometry-aware feature extraction using Bandelet Transform
- Quadtree-based adaptive decomposition
- Integration with Transfer Learning
- Robust classification under limited labeled data
- Ablation study on quadtree threshold parameter T

---

## 📑 Citation

If you use this code, please cite our paper:

```bibtex

to be annonced







