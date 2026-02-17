# Iris Species Classification Analysis 🤖

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Shayan-Nami/Iris-Classification-Analysis/blob/main/Iris_pca_lda_qda.ipynb)
![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange?style=flat&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📖 Project Overview
This project is a comprehensive Machine Learning analysis aimed at classifying **Iris flower species** (*Setosa, Versicolor, Virginica*) based on their sepal and petal measurements.

The primary objective was to compare the performance of **Generative Classifiers** (LDA, QDA, GNB) and evaluate the impact of **Dimensionality Reduction** (PCA) on model accuracy. The entire workflow, from data preprocessing to visualization and evaluation, was implemented using **Google Colab**.

---

## 🔬 Methodology & Algorithms
We explored four distinct statistical approaches to understand the underlying data structure:

### 1. Principal Component Analysis (PCA)
- **Goal:** Dimensionality reduction and Data Visualization.
- **Process:** Projected the 4-dimensional feature space into 2 principal components (2D).
- **Outcome:** While PCA helped in visualizing the clusters, it resulted in a slight information loss (~4% variance), which impacted the classification accuracy of the Naive Bayes model.

### 2. Linear Discriminant Analysis (LDA)
- **Goal:** Find the linear combination of features that best separates the classes.
- **Outcome:** Achieved **perfect separation** between classes, proving that the Iris dataset boundaries are largely linear.

### 3. Quadratic Discriminant Analysis (QDA)
- **Goal:** Allow for non-linear (quadratic) decision boundaries.
- **Outcome:** Performed well but was essentially "overkill" for this specific dataset, as complex boundaries weren't necessary.

### 4. Gaussian Naive Bayes (GNB)
- **Goal:** Probabilistic classification assuming feature independence.
- **Outcome:** Tested both on raw data (100% accuracy) and PCA-reduced data (93.3% accuracy).

---

## 📊 Results Summary
The models were evaluated using **Accuracy Score** and **Confusion Matrices**. Below is the comparative performance:

| Model Architecture | Accuracy | Key Insight |
| :--- | :---: | :--- |
| **LDA (Linear Discriminant)** | **100%** | 🏆 **Best Model.** Perfectly captured the linear boundaries. |
| **GNB (Full Features)** | **100%** | Highly effective when all 4 features are retained. |
| **QDA (Quadratic Discriminant)** | **~96%** | Slightly overfitted due to unnecessary complexity. |
| **GNB + PCA (2 Components)** | **93.3%** | Dimensionality reduction caused misclassification between *Versicolor* and *Virginica*. |

> 📉 *Detailed decision boundary plots and confusion matrices are available in the notebook.*

---

## 🛠 Tech Stack
- **Environment:** [Google Colab](https://colab.research.google.com/) (Jupyter Notebook)
- **Language:** Python 3.10+
- **Libraries:**
  - `scikit-learn`: Model training & metrics.
  - `pandas` & `numpy`: Data manipulation.
  - `matplotlib` & `seaborn`: Advanced data visualization.

---

## 🚀 How to Run
You can run this project directly in your browser without installing anything:

1.  Click the **"Open in Colab"** badge at the top of this file.
2.  Press `Ctrl + F9` (or *Runtime > Run all*) to execute all cells.

Alternatively, to run locally:
```bash
git clone [https://github.com/Shayan-Nami/Iris-Classification-Analysis.git](https://github.com/Shayan-Nami/Iris-Classification-Analysis.git)
pip install -r requirements.txt
jupyter notebook Iris_pca_lda_qda.ipynb


👤 Author
Shayan Abdollahi Nami

