# 🖼️ Image Sharpening using Knowledge Distillation

This project implements a deep learning pipeline for sharpening blurry images using Knowledge Distillation (KD). A powerful **Teacher** model transfers its learned features to a lightweight **Student** model for efficient deployment.

## 📌 Goal
Train a small model that can convert blurry images into sharp ones, mimicking the output of a high-capacity model.

## 🧠 Concepts Used
- **Knowledge Distillation**
- **Image Deblurring/Sharpening**
- **Perceptual & Feature Distillation Losses**

## 🔧 Architecture Overview
- **Teacher Model**: Restormer / SwinIR / MPRNet (pretrained)
- **Student Model**: Lightweight CNN or UNet
- **Loss Functions**:
  - L1 Reconstruction Loss
  - Perceptual Loss (VGG-based)
  - Feature Distillation Loss
  - (Optional) Edge/Gradient Loss

## 📂 Dataset
You can use datasets like:
- GoPro Deblurring Dataset
- REDS Dataset
- DIV2K
- Folder Structure
```
  image-sharpening-kd/
├── models/               # (optional) contains teacher and student models
│   ├── teacher.py
│   └── student.py
├── data/                 # (optional) sample images or instructions to download datasets
├── utils/                # (optional) helper functions (losses, transforms)
├── IMAGE SHARPENING USING KNOWLEDGE DISTILLATION.ipynb
├── requirements.txt
└── README.md
```
## 🚀 How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
