# 🩺 Ultra-Lightweight Skin Disease Detection Using Knowledge Distillation
![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-DeepLearning-red.svg)
![GradCAM](https://img.shields.io/badge/GradCAM-ExplainableAI-yellow.svg)
![Dataset](https://img.shields.io/badge/Dataset-HAM10000-purple.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

---

## 🌟 Project Highlight  
⚡ **Ultra-Lightweight Model: Only 148K Parameters** ⚡  
Our custom CNN achieves **80.43% accuracy** and **67.02% Macro-F1 score**, while being small enough to run on **microcontrollers, mobile devices, and embedded medical systems**.  

> 🔑 **Key Achievement:** State-of-the-art performance with a **tiny model (148K params)** optimized for **resource-limited healthcare devices**.  

---

## 📖 Abstract  
Skin cancer is a major global health issue, and detecting skin lesions accurately is crucial for early treatment. While large deep learning models like EfficientNet-B4 achieve high accuracy, they are **too heavy for mobile and embedded systems**.  

To address this, we propose a **Knowledge Distillation (KD) framework** using the **HAM10000 dataset**:  
- 🧠 **Teacher:** Fine-tuned EfficientNet-B4 (first 20% layers frozen).  
- 🎓 **Student:** Custom CNN with **just 148K parameters** using  
  - Depthwise-Separable Convolutions  
  - Residual Connections  
  - Dropout Layers  
- 📌 **Confidence-Masked KD:** Student learns only from reliable teacher predictions.  

📊 **Results:**  
- Accuracy: **69.20% → 80.43%** (with KD)  
- Macro-F1: **58.5% → 67.02%** (with KD)  

---

## ✨ Key Features  
- ⚡ **Extremely Lightweight CNN (148K params)** → runs on small devices  
- 🧠 **EfficientNet-B4 Teacher → Student Distillation**  
- 🎯 **Confidence-Masked Knowledge Transfer**  
- 📈 **Improved Accuracy & F1 with same tiny size**  
- 🔍 **Grad-CAM visualizations for explainability**  

---

## 📊 Dataset  
We used the **HAM10000 dataset**:  
- 10,015 dermatoscopic images  
- 7 classes of skin lesions  
- Publicly available: [HAM10000 on Kaggle](https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000)  

---

## 🏗️ Model Architecture  

### 🔹 Teacher Model (EfficientNet-B4)  
- Pretrained on ImageNet  
- 20% layers frozen  
- Fine-tuned on HAM10000  

### 🔹 Student Model (148K Parameters – Ultra-Lightweight)  
- Depthwise-Separable Convolutions  
- Residual Connections  
- Dropout Layers  

📌 **Knowledge Distillation Flow**  
<img width="1341" height="321" alt="KD2" src="https://github.com/user-attachments/assets/05273e09-7b9a-4e3a-ad73-54cd63f1d251" />

