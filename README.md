# 🩺 Early Glaucoma Screening Using YOLO and Deep Features from Fundus Images
![Python](https://img.shields.io/badge/Python-3.8-blue)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Object%20Detection-red)
![ResNet50](https://img.shields.io/badge/ResNet50-Deep%20Learning-orange)
![Deep Learning](https://img.shields.io/badge/AI-Healthcare-purple)

<p align="center">
Automated Deep Learning Framework for Robust Glaucoma Detection  
Using Retinal Fundus Imaging
</p>

---

## 📌 Overview

Glaucoma is one of the leading causes of irreversible blindness worldwide.  
Early diagnosis is critical to prevent permanent optic nerve damage.

This repository presents an automated deep learning pipeline that integrates:

- 🔍 **YOLOv8** for Optic Disc & Cup localization  
- 🧠 **ResNet50** for deep feature extraction  
- 📊 Binary classification for glaucoma detection  

The system demonstrates strong generalization across multiple benchmark datasets.

---

## 🧠 Abstract

We propose a multi-stage deep learning framework for early glaucoma screening using retinal fundus images. The pipeline performs:

1. Fundus image acquisition  
2. ROI localization (Optic Disc & Cup)  
3. Segmentation of anatomical regions  
4. Deep feature extraction  
5. Binary classification  

The model achieves up to **99.56% accuracy** on the G1020 dataset, demonstrating robustness and clinical potential :contentReference[oaicite:1]{index=1}.

---

# 🏗️ Proposed Methodology

## 🔬 Model Architecture

<p align="center"><img width="1021" height="507" alt="image" src="https://github.com/user-attachments/assets/80bdb747-7f3d-45d2-b074-e329a42ff8d8" />
</p>

The framework consists of four major stages:

### 1️⃣ Data Acquisition
- Fundus images divided into training & testing sets.

### 2️⃣ ROI Localization (YOLOv8)
- Detects Optic Disc (OD)
- Detects Optic Cup (OC)
- Generates bounding boxes
- Performs segmentation

Mathematically:

\[
B = Y(RF)
\]

Where:
- RF = Fundus image  
- Y = YOLOv8 detection model  
- B = Bounding box set  

Cup-to-Disc Ratio (CDR):

\[
CDR = |Ω_{OC}| / |Ω_{OD}|
\]

---

### 3️⃣ Feature Extraction (ResNet50)

- Pretrained 50-layer deep residual network  
- Extracts high-dimensional discriminative features  
- Captures structural variations in retinal morphology  

\[
f = Φ_{ResNet50}(R)
\]

---

### 4️⃣ Classification

Binary output:

- 1 → Glaucomatous  
- 0 → Normal  

Threshold τ = 0.5

---

# 📊 Datasets

| Dataset      | Total Images | Glaucoma | Normal |
|--------------|-------------|----------|--------|
| DRISHTI-GS   | 101         | 31       | 70     |
| ORIGA        | 650         | 168      | 482    |
| G1020        | 1020        | 278      | 742    |

All datasets were augmented to improve generalization :contentReference[oaicite:2]{index=2}.

---

# 📈 Experimental Results

## 🔎 Performance Summary

| Dataset      | Accuracy (%) | Sensitivity (%) | Specificity (%) | F1-Score (%) |
|--------------|--------------|----------------|----------------|--------------|
| DRISHTI-GS   | 97.06       | 97.14          | 97.01          | 95.77        |
| ORIGA        | 97.46       | 98.03          | 96.89          | 97.44        |
| G1020        | 99.56       | 99.70          | 99.41          | 99.56        |

---

## 📊 Confusion Matrices

<p align="center"><img width="1052" height="365" alt="image" src="https://github.com/user-attachments/assets/47d734e7-a4be-4210-b448-92d015b9f388" />
</p>

The results confirm strong classification performance and cross-dataset generalization :contentReference[oaicite:3]{index=3}.

---

## 🖼️ Segmentation Examples

<p align="center"><img width="527" height="345" alt="image" src="https://github.com/user-attachments/assets/7c368319-5627-4963-b754-e5ad8c11a1cd" />
</p>

YOLOv8 robustly segments optic disc and cup regions for both normal and glaucomatous eyes :contentReference[oaicite:4]{index=4}.

---

# ⚙️ Implementation Details

### 💻 Software Stack
- Python 3.8
- TensorFlow 2.x
- PyTorch
- YOLOv8
- ResNet50
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn

### 🖥️ Environment
- Google Colab (GPU-enabled)
- NVIDIA Tesla T4 / A100
- 13GB RAM

---

# 🌟 Key Contributions

✔ Automated ROI detection using YOLOv8  
✔ Deep hierarchical feature extraction via ResNet50  
✔ High performance across diverse datasets  
✔ Scalable & clinically deployable architecture  
✔ Robust cross-dataset generalization  

---


## 📁 Dataset Access

Datasets used:
- DRISHTI-GS
- ORIGA
- G1020

Due to licensing restrictions, datasets are not included in this repository.

---

## 📄 Citation

If you use this work, please cite:

@inproceedings{Singh2025Glaucoma,
  title={Early Glaucoma Screening Using YOLO and Deep Features from Fundus Images},
  author={Singh, Lavanya and Singh, Divyanshi and Tagore, Nirbhay Kumar and Singh, Y. N.},
  year={2025}
}

---

