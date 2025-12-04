# 🌍 East Anatolian Fault Zone: Seismic ML Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Course](https://img.shields.io/badge/Inspired%20By-Andrew%20Ng%20ML%20Course-green)

## 📌 Project Overview
This project applies **Supervised Machine Learning** techniques to analyze real-world seismic data from the **East Anatolian Fault Zone (Turkey)**. 

The primary objective is to bridge the gap between theory and practice by applying the algorithms learned in the **DeepLearning.AI Machine Learning Specialization (Course 1)** to a critical real-world problem: Earthquake analysis.

## 🛠️ Tech Stack & Libraries
* **Python:** Core programming language.
* **Pandas:** For data manipulation and cleaning AFAD catalogs.
* **Matplotlib:** For visualizing the fault line and regression models.
* **Scikit-Learn:** For implementing Linear and Logistic Regression algorithms.
* **NumPy:** For vectorization and numerical calculations.

## 📂 Dataset
The dataset consists of seismic events recorded on the East Anatolian Fault Zone.
* **Source:** AFAD (Disaster and Emergency Management Authority)
* **Features Used:** `Latitude`, `Longitude`, `Depth` (km), `Magnitude` (Ml).
* **Data File:** `events_catalog.csv` (Included in this repository).

## 🧠 Methodology & Results

### 1. Spatial Visualization
Before modeling, the data was visualized to confirm the geographical distribution. The plot clearly shows the geometry of the East Anatolian Fault.

### 2. Linear Regression (Univariate)
* **Goal:** Predict earthquake **Magnitude ($y$)** based on **Focal Depth ($x$)**.
* **Model:** $f_{w,b}(x) = wx + b$
* **Finding:** The model successfully optimized parameters $w$ and $b$ using Gradient Descent. However, the analysis revealed a **low $R^2$ score**.
* **Interpretation:** Earthquake magnitude is a complex phenomenon influenced by fault type, stress accumulation, and rock properties. Using only "Depth" as a feature leads to **High Bias (Underfitting)**.

### 3. Logistic Regression (Binary Classification)
* **Goal:** Classify earthquakes as **"Major"** (Risk prone, $Ml \ge 4.0$) or **"Minor"**.
* **Model:** Sigmoid Function $g(z) = \frac{1}{1 + e^{-z}}$
* **Finding:** The model established a probabilistic **Decision Boundary**.
* **Interpretation:** Unlike linear regression, this approach provided a clear statistical framework to assess the probability of a significant seismic event based on depth.

## 🚀 How to Run the Project
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/emrealtindag/East-Anatolian-Fault-ML-Analysis.git](https://github.com/emrealtindag/East-Anatolian-Fault-ML-Analysis.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib scikit-learn
    ```
3.  **Run the Notebook:**
    Open `Earthquake_Analysis.ipynb` in Jupyter Notebook or Google Colab.

## 🎓 Acknowledgements
This project was developed as a portfolio piece to demonstrate the practical application of:
* **Course:** Supervised Machine Learning: Regression and Classification
* **Instructor:** Andrew Ng (DeepLearning.AI)

---
*Created by [Emre Altındağ](https://www.linkedin.com/in/emrealtindag/)*
