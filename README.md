# ☁️ Cloud Type Classification – Deep Learning Project

This project explores the use of deep learning to classify cloud types—**Cumulus, Stratus, Cirrus, and Nimbus**—from images using convolutional neural networks (CNNs) and transfer learning.  
It was completed as part of the *MSDS 610 – Deep Learning* course at Bryant University.

---

## 🧠 Overview

Cloud type classification is a key task in atmospheric science, as it can support climate analysis, forecasting, and environmental monitoring.  
In this project, I developed and compared two deep learning models:
- A **custom CNN** built from scratch.
- A **transfer learning** approach using a pretrained **ResNet18** model from PyTorch.

Both models were trained and evaluated on a labeled cloud dataset containing four major cloud categories.

---

## ⚙️ Methods

**Framework:** PyTorch  
**Data Preprocessing:**
- Resizing, normalization (ImageNet mean/std), and augmentation (flips, rotations, color jitter)
- Stratified splits for train, validation, and test sets  

**Models:**
- Custom CNN with three convolutional layers and max pooling  
- ResNet18 (ImageNet weights) with fine-tuned fully connected layer  

**Training Setup:**
- Optimizer: Adam  
- Loss: CrossEntropyLoss  
- Learning rate scheduling and early stopping applied  
- Evaluation metrics: Accuracy, Precision, Recall, F1-score  

---

## 📊 Results

| Model       | Validation Accuracy | Test Accuracy | Key Notes |
|--------------|--------------------:|---------------:|------------|
| Custom CNN   | ~78%                | ~80%           | Overfitting observed |
| ResNet18     | **~85%**            | **~85%**       | Best performance overall |

The **ResNet18** model demonstrated stronger generalization and faster convergence, effectively learning distinguishing features between the four cloud categories.  
However, some overlap remained between visually similar types such as Cumulus and Stratus.

---

## 🧩 Visualizations

Example output includes:
- Accuracy and loss curves over epochs  
- Confusion matrix visualizing per-class performance  
- Example image predictions  

---

## 🧾 Files in This Repository

| File | Description |
|------|--------------|
| `MSDS610_Final_Project.ipynb` | Full code notebook for preprocessing, model training, and evaluation |
| `Deep_Learning_Final_Writeup.pdf` | Written report summarizing the methodology, results, and conclusions |
| `requirements.txt` | Python dependencies for running the notebook |
| `figures/` | Optional folder for plots such as accuracy curves and confusion matrices |

---

## 🧰 How to Run

1. **Clone the repo**
   ```bash
   git clone https://github.com/lesbencosme-star/cloud-type-classification-deeplearning.git
   cd cloud-type-classification-deeplearning
