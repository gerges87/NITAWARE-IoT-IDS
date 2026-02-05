# NITAWARE: Intelligent IoT Intrusion Detection System (IDS)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Generative AI](https://img.shields.io/badge/Generative_AI-CTGAN-purple)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Project Overview
**NITAWARE** is a robust Deep Learning-based Intrusion Detection System (IDS) designed to secure IoT environments against modern cyber threats like **DDoS**, **DoS**, **Reconnaissance**, and **Data Theft**.

The project addresses the critical challenge of **Imbalanced Data** in IoT traffic (where attacks vastly outnumber normal traffic) by utilizing **Generative AI (CTGAN)** for realistic data synthesis, outperforming traditional methods like SMOTE.

## 🚀 Key Features & Innovations
* **Generative Data Augmentation:** Utilizes **CTGAN (Conditional Tabular GAN)** to generate high-fidelity synthetic samples, solving the "Precision Collapse" problem in benign traffic detection.
* **Spatial Feature Extraction:** Implements a **1D-Convolutional Neural Network (1D-CNN)** to capture spatial patterns in sequential network flows.
* **High Performance:** Achieved **94.5% Accuracy** and **0.97 Precision** for benign traffic on the **Bot-IoT Dataset**.
* **End-to-End Pipeline:** From data cleaning and log transformation to model training and evaluation.

## 🛠️ Tech Stack
* **Language:** Python 3.10
* **Deep Learning:** TensorFlow, Keras
* **Data Manipulation:** Pandas, NumPy
* **Generative Models:** CTGAN (Conditional Tabular Generative Adversarial Networks)
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Google Colab / Jupyter Notebook

## 📊 Methodology (The 4-Phase Approach)
This project compares four distinct modeling phases to find the optimal architecture:

1.  **Model 1 (Baseline ANN):** Trained on raw imbalanced data (Suffered from Majority Class Bias).
2.  **Model 2 (ANN + SMOTE):** Used Linear Interpolation for balancing (High False Positives).
3.  **Model 3 (1D-CNN + SMOTE):** Improved feature extraction but limited by SMOTE's noise.
4.  **Model 4 (1D-CNN + CTGAN):** **(Proposed Solution)** Used Generative AI to learn the real data distribution, achieving the best results.

## 📈 Results & Performance
The proposed **CNN + CTGAN** model significantly outperformed other configurations, specifically in distinguishing "Benign" traffic from attacks.

| Metric | Model 1 (ANN) | Model 2 (ANN+SMOTE) | Model 3 (CNN+SMOTE) | Model 4 (CNN+CTGAN) |
| :--- | :---: | :---: | :---: | :---: |
| **Technique** | Imbalanced | Linear Oversampling | Feature Extraction | **Generative AI** |
| **Final Accuracy** | 83.5% | 64.6% | 82.2% | **94.5%** |
| **Benign Precision** | 0.93 (Biased) | 0.09 (Fail) | 0.24 (Poor) | **0.97 (Excellent)** |
| **Benign Recall** | 0.49 (Fail) | 0.49 (Fail) | 1.00 | **1.00** |

## 🧠 System Architecture
*(You can upload the Block Diagram image from your thesis here)*
The system follows a pipeline:
`Data Acquisition (Bot-IoT) -> Preprocessing -> Data Balancing (CTGAN) -> 1D-CNN Classification`

## 💿 Dataset
This project utilizes the **BoT-IoT Dataset** created by the Cyber Range Lab at UNSW Canberra. It simulates a realistic smart home environment with legitimate and botnet traffic.

## 📬 Contact
**Gerges Sobhi** - Machine Learning Engineer
* [www.linkedin.com/in/gerges-sobhy]
* [https://www.upwork.com/freelancers/~01e489c25ce14506ed?mp_source=share]

---
*This project was developed as part of a graduation thesis under the supervision of Dr. Amel Mohamed at the Canadian International College (CIC).*
