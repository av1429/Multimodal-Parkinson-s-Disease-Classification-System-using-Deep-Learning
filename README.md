# 🧠 Multimodal Parkinson’s Disease Classification System

## 📘 Overview
This project presents a **deep learning–based multimodal diagnostic framework** for the early detection of **Parkinson’s Disease (PD)**.  
The system combines three distinct physiological data types — **spiral drawings, voice acoustic features, and gait signals** — processed through specialized machine learning and deep learning models.  
The approach enhances diagnostic accuracy and robustness compared to unimodal systems.

---

## ⚙️ Key Features
- 🌀 **Spiral Drawing Analysis:** CNN model trained on grayscale handwriting spirals to detect tremor irregularities.  
- 🎤 **Voice Feature Analysis:** Random Forest classifier using jitter, shimmer, pitch, and MFCC features (with and without UPDRS clinical data).  
- 🚶 **Gait Signal Analysis:** Temporal deep learning architectures (CNN-LSTM, BiLSTM, CNN-BiLSTM) for sequence-based motion recognition.  
- 🧩 **Cross-Modal Evaluation:** Comparative study across all three modalities with visual performance metrics.  
- 🧠 **Non-Invasive & AI-Driven:** Enables potential early-stage PD diagnosis using accessible behavioral data.

---

## 📦 Dataset Information

This project utilizes three distinct datasets corresponding to **spiral drawings**, **voice features**, and **gait signals** for multimodal Parkinson’s Disease classification.

### 🌀 Spiral Drawing Dataset
- Collected from publicly available handwriting samples of Parkinson’s and healthy individuals.  
- Each image represents a hand-drawn spiral used to detect tremor irregularities.  
- Dataset is included in this repository under the `Dataset/` directory.  
- Preprocessing: grayscale conversion, normalization, rotation and flip augmentation.

### 🎤 Voice Feature Dataset
- Contains extracted acoustic features such as **jitter**, **shimmer**, **pitch**, and **MFCCs** for both PD and healthy subjects.  
- Dataset is included in this repository under `Dataset/`.  
- Each entry includes both feature values and a corresponding label (PD / Healthy).

### 🚶 Gait Signal Dataset
- The gait dataset was sourced from **PhysioNet’s Gait in Parkinson’s Disease Database**:  
  🔗 [PhysioNet GaitpDB 1.0.0](https://physionet.org/content/gaitpdb/1.0.0/)  
- This dataset contains vertical ground reaction force (GRF) signals from multiple sensors attached to the feet of participants.  
- The signals are used to analyze temporal gait variations and motor control characteristics in PD patients.  
- Due to its large size, this dataset is **not hosted in this repository**; users may download it directly from the official PhysioNet link above.

---

### 🧹 Data Preprocessing Summary
| Modality | Preprocessing Steps |
|-----------|--------------------|
| Spiral | Grayscale conversion, resizing (128×128), normalization, augmentation |
| Voice | Feature extraction (MFCC, jitter, shimmer), z-score normalization |
| Gait | Signal segmentation, denoising, standardization, sequence padding |

---

## 🧠 Model Architectures

| Modality | Model Type | Accuracy | Key Highlights |
|-----------|-------------|-----------|----------------|
| Spiral Drawings | CNN | **81%** | Strong recall (0.99) for PD cases |
| Voice Features | Random Forest | **72%** (100% w/UPDRS) | High interpretability and robustness |
| Gait Signals | CNN-LSTM / CNN-BiLSTM | **71%** | Captures spatiotemporal gait patterns |

---

## 🧩 Methodology
1. **Data Preprocessing**  
   - Spiral: resizing, grayscale, rotation & flip augmentation  
   - Voice: normalization (z-score / min-max), MFCC extraction  
   - Gait: signal denoising, standardization, and sequence padding  

2. **Model Development**  
   - CNN for spiral analysis  
   - Random Forest for acoustic feature classification  
   - LSTM, BiLSTM, CNN-LSTM, CNN-BiLSTM for gait  

3. **Training & Validation**  
   - Stratified train-test split  
   - Early stopping, dropout, and batch normalization  
   - Evaluation via accuracy, precision, recall, F1-score, confusion matrix  

---

## 📊 Results Summary
| Metric | Spiral (CNN) | Voice (RF) | Gait (CNN-LSTM) |
|---------|---------------|-------------|-----------------|
| Accuracy | 81% | 72% | 71% |
| Recall (PD) | 0.99 | 0.74 | 0.83 |
| Precision | 0.73 | 0.70 | 0.69 |
| F1-Score | 0.81 | 0.71 | 0.70 |

✅ Integration of clinical UPDRS data improved overall model accuracy to **near-perfect performance** in the voice modality.  
✅ Cross-modal fusion highlighted the complementary strengths of handwriting, vocal, and gait-based signals.

---

## 🧰 Tools & Technologies
- **Languages:** Python  
- **Frameworks:** TensorFlow, Keras, Scikit-learn  
- **Libraries:** NumPy, Pandas, OpenCV, Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook / Google Colab  

---

## 🚀 Future Work
- Implement true multimodal fusion using synchronized subject data.  
- Incorporate explainable AI (Grad-CAM, SHAP) for interpretability.  
- Optimize models for edge/real-time deployment in clinical monitoring.  
- Develop unified multimodal fusion pipeline for end-to-end PD assessment.

---

## 👥 Authors
- **Aravinthvasan S**  
  B.Tech ECE (Cyber-Physical Systems), SASTRA Deemed University  
  Role: Model implementation, architecture design, comparative analysis  

- **Armindha Gladia V** — Model evaluation & visualization  
- **Sanjanah N** — Data preprocessing & documentation  

---

## 🪪 License
This project is licensed under the **MIT License** — feel free to use, modify, and distribute it with attribution.

---

🔗 **GitHub:** [GitHub Profile](https://github.com/av1429)

---

## 🏷️ Keywords
`Parkinson’s Disease` · `Multimodal Deep Learning` · `CNN-LSTM` · `Biomedical AI` · `Machine Learning` · `Voice Analysis` · `Gait Recognition`

