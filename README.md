# Pain Recognition Using Multi-Level Deep Learning on Physiological Signals

This project presents a **deep learning-based approach for automatic pain recognition** using physiological signals like EEG and EDA. The aim is to eliminate the dependency on medical expertise for feature extraction by using a multi-level model that performs both **feature optimization and classification**.

Traditional uni-level models (e.g., SVM, Random Forest, Linear Regression) are limited in recognizing pain levels from complex signals. Our proposed system employs **CNN + Bi-LSTM**, and the extended model uses **CNN + Bi-LSTM + Bi-GRU**, which significantly improves prediction performance.

---

## 📘 Abstract

In the proposed paper, the authors use **multi-level deep learning algorithms** for pain recognition. Unlike traditional ML models, these deep models extract and select features automatically and more effectively.

### Key Contributions:

- Propose a **multi-level architecture (CNN + Bi-LSTM)** for automatic pain recognition.
- Further extend it with **CNN + Bi-LSTM + Bi-GRU** for three-level feature optimization.
- Evaluate performance using **LOSO (Leave-One-Subject-Out cross-validation)** and classification metrics like accuracy, precision, recall, and F1-score.
- Use **EEG and EDA signals** from the **BioVid Heat Pain database (Part A)** and **Emopain 2021 dataset**.

---

## 🧠 Model Architecture

### 1. **CNN**:  
Used to **optimize and extract** spatial features from raw EEG/EDA signals.

### 2. **Bi-LSTM**:  
Processes temporal dependencies in the extracted features bidirectionally.

### 3. **Bi-GRU** (in extension):  
Further refines temporal features extracted by Bi-LSTM for better classification accuracy.

> This 3-level architecture enhances recognition accuracy compared to uni-level or two-level approaches.

---

## 📊 Datasets Used

| Dataset         | Source                          | Type      | Notes                                  |
|-----------------|----------------------------------|-----------|----------------------------------------|
| BioVid Part A   | [Link not public]               | EEG, EDA  | Contains pain levels from 0 to 4       |
| Emopain 2021    | [Link not public]               | EEG, EDA  | Additional pain recognition dataset    |
| GitHub subset   | Custom downloaded from GitHub   | EEG       | Used for training due to availability  |

- Pain Levels: **0 (no pain) to 4 (high pain)**
- Total Subjects: **57**
- Each row in the dataset represents EEG signals from a subject

> **Note**: Due to restricted access, GitHub-sourced sample data has been used for demonstration.

---

## 📈 Evaluation Strategy

- **LOSO (Leave-One-Subject-Out)** cross-validation:
  - Trains on all but one subject, tests on the remaining.
  - Repeated for each subject to ensure robustness.

- **Confusion Matrix**: Visualizes prediction vs. actual pain levels

- **Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1-Score

---

## 🔌 Dependencies

To set up the environment, install the following specific versions of dependencies:

```bash
pip install numpy==1.19.2
pip install pandas==0.25.3
pip install matplotlib==3.1.1
pip install Keras==2.2.4
pip install tensorflow==1.14.0
pip install h5py==2.10.0
pip install protobuf==3.16.0
pip install jupyter==1.0.0
pip install jupyter-client==6.1.3
pip install jupyter-console==6.4.0
pip install jupyter-core==4.6.3
pip install jupyterlab-widgets==1.0.0
pip install scikit-learn==0.22.2.post1
pip install seaborn==0.10.1
pip install ipython==7.9.0
pip install ipython-genutils==0.2.0
pip install ipykernel==6.5.0
