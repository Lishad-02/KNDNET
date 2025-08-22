# KNDNet: Ultra-Lightweight Skin Disease Detection Using Knowledge Distillation

**KNDNet** is a lightweight deep learning framework for classifying skin lesions with high accuracy while keeping computational requirements low, making it suitable for embedded systems, mobile devices, and resource-limited healthcare settings.

## 📋 Overview

Skin cancer is a major global health concern, and accurate detection of skin lesions is critical for early treatment. While deep learning models achieve strong performance in medical imaging, most require high computational power, making them difficult to deploy on microprocessors or mobile devices.

This project implements a **Knowledge Distillation (KD) framework** to train a small yet effective CNN model for skin lesion classification using the **HAM10000 dataset**.

## 🧠 Approach

- **Teacher Model**: EfficientNet-B4 fine-tuned on HAM10000 by freezing the first 20% of layers.
- **Student Model**: Custom lightweight CNN with only 148K parameters, featuring:
  - Depthwise-separable convolutions  
  - Residual connections  
  - Dropout layers
- **Knowledge Distillation**:
  - Student trained with both ground-truth labels and teacher’s soft predictions.  
  - Confidence-masked KD strategy: knowledge transferred only when the teacher is confident.

## 📊 Results

| Metric          | Student Only | Student + KD |
|-----------------|--------------|--------------|
| Accuracy        | 69%          | 80%       |
| Macro-F1 Score  | 58%          | 67%       |

The results demonstrate that knowledge distillation significantly improves the performance of small models, enabling deployment on **microprocessors, mobile devices, and embedded medical systems**.

## ⚡ Features

- Lightweight custom CNN for skin lesion classification  
- Knowledge distillation from a fine-tuned EfficientNet-B4 teacher  
- Confidence-masked training for better knowledge transfer  
- Suitable for resource-constrained environments  

## 🛠️ Technologies

- Python  
- PyTorch
- DL
- KD



