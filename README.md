# 🚦 Darknet Traffic Analysis

### Investigating the Impact of Modified Tor Traffic on Onion Service Traffic Classification

This project explores how traditional and advanced machine learning algorithms can classify anonymized Tor traffic as either **regular Tor services** or **Onion services**, even after data modification techniques like padding.

---

### 📌 Objective

To evaluate the effectiveness of multiple machine learning models (SVM, KNN, Random Forest, and AdaBoost) in detecting Onion services over Tor by analyzing traffic patterns—even when those patterns are modified to evade detection (e.g., WTF-PAD).

---

### 🧠 Algorithms Used

* ✅ Support Vector Machine (SVM)
* ✅ K-Nearest Neighbors (KNN)
* ✅ Random Forest
* ✅ AdaBoost (Extension - Achieved 100% accuracy)

---

### 📊 Datasets

* **No Defence Tor Traffic** – Original unmodified Tor traffic
* **OS Dataset** – Traffic from Onion services
* **WTFPAD** – Tor traffic modified using Website Fingerprinting defenses
* ✅ Merged and preprocessed for feature selection and accuracy comparison

> 📦 Datasets are in `.pkl` format and sourced from:
>
> * [deep-fingerprinting/df](https://github.com/deep-fingerprinting/df)
> * [fingerprintability/fingerprintability](https://github.com/fingerprintability/fingerprintability/tree/master)

---

### 🔍 Feature Selection Techniques

* Information Gain
* Correlation Coefficient
* Fisher Score

Best performance observed with **top 6 selected features**.

---

### 📈 Model Performance Summary

| Model        | Dataset                             | Accuracy    |
| :----------- | :---------------------------------- | :---------- |
| KNN          | Original                            | 86.00%      |
| RandomForest | Original                            | 86.57%      |
| SVM          | Original                            | 86.89%      |
| KNN          | WTFPAD                              | 84.15%      |
| SVM          | WTFPAD                              | 99.00%      |
| SVM/KNN      | Merged OS + WTFPAD (Top 6 Features) | 97.92%      |
| **AdaBoost** | Extension                           | **100.00%** |

---

### 🧪 Highlights

* Demonstrated successful classification even after dataset modification
* Feature selection improved performance significantly
* Extension using AdaBoost gave perfect classification results

---

### 💻 Tech Stack

* Jupyter Notebook (Python)
* Scikit-learn
* Pandas / NumPy
* Matplotlib / Seaborn

---

### 📂 File Structure (Important Note)

Due to GitHub file size limits, large `.pkl` files (like `X_train_NoDef.pkl` or `WTFPAD.pkl`) are **not included** in this repository. You can:

* Download them manually from the above sources
* Or use [Git LFS](https://git-lfs.github.com) to manage them if needed

---

### 📸 Screenshots

Includes step-by-step code outputs in the notebook with comments and visuals:

* Data Loading & Preprocessing
* Feature Importance Graphs
* Confusion Matrices
* Performance Tables

---

### ✅ How to Run

1.  Clone the repo:

    ```bash
    git clone [https://github.com/vamsi5410/Darknet-Traffic-Analysis.git](https://github.com/vamsi5410/Darknet-Traffic-Analysis.git)
    ```

2.  Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3.  Run the notebook:

    ```bash
    jupyter notebook DarknetClassification.ipynb
    ```
