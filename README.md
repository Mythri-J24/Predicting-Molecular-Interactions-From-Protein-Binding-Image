# Predicting Molecular Interactions from Protein Binding Images

## 📌 Project Overview
This project presents a **deep learning–based framework** for predicting **protein–ligand interactions** using **protein binding images** derived from the **Protein Data Bank (PDB)**.  
The proposed approach employs a **hybrid architecture combining 3D Convolutional Neural Networks (3D-CNN) and VGG16** to capture both spatial and structural features of protein–ligand complexes.

The model performs **binary classification** to determine whether a ligand **binds or does not bind** to a target protein.

---

## 🧬 Motivation
Protein–ligand interactions are fundamental to:
- Drug discovery  
- Molecular medicine  
- Protein engineering  

Traditional methods such as **X-ray crystallography, NMR spectroscopy, cryo-electron microscopy**, and **molecular docking** are accurate but:
- Time-consuming  
- Computationally expensive  
- Difficult to scale  

This project provides an **automated, scalable, and AI-driven alternative** using image-based deep learning techniques.

---

## 🏗️ Proposed Methodology
The system follows a **dual-branch hybrid architecture**:

### 🔹 3D-CNN Branch
- Input: **32 × 32 × 32 voxel grids**
- Learns fine-grained **volumetric and spatial features**
- Captures atomic-level interactions in protein binding pockets

### 🔹 VGG16 Branch (Transfer Learning)
- Input: **224 × 224 protein binding images**
- Pre-trained on PyMol
- Extracts **high-level structural and visual features**

### 🔹 Feature Fusion & Classification
- Features from both branches are concatenated
- Fully connected layers integrate information
- Output: **Binding / Non-Binding**

---

## 📂 Dataset
- **Source:** Protein Data Bank (PDB)
- **Total samples:** 120  
  - Binding: 60  
  - Non-Binding: 60  
- **Data representations:**
  - 3D voxel grids  
  - 2D protein binding images  

> ⚠️ Due to size constraints, raw PDB files and processed voxel data are not included in this repository.

---

## 📊 Experimental Results

| Model | Accuracy | Precision | Recall | F1-score |
|------|---------|-----------|--------|----------|
| 3D-CNN | 66% | 0.71 | 0.55 | 0.62 |
| VGG16 | 50% | 0.50 | 0.22 | 0.30 |
| **3D-CNN + VGG16 (Hybrid)** | **77.78%** | **0.85** | **0.78** | **0.77** |

✅ The hybrid model outperforms individual models across all evaluation metrics.

---

## ⚙️ Technologies Used
- Python  
- TensorFlow / Keras  
- NumPy  
- OpenCV  
- Biopython  
- Scikit-learn  
- Matplotlib
- PyMol
- Google Colab (GPU support)
---

## 👩‍💻 Team
- **Mythri J Reddy**
- **B Sai Swaroop** 

## 📜 License
This project is licensed under the **MIT License**.

---

## 🚀 Future Scope
- Scaling to larger and diverse protein–ligand datasets  
- Incorporating molecular dynamics and attention-based fusion  
- Extending predictions to binding affinity estimation  
- Improving generalization using advanced data augmentation  
