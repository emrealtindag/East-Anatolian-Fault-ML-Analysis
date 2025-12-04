# 🌍 Seismic Risk Analysis: East Anatolian Fault Zone

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Course](https://img.shields.io/badge/Inspired%20By-Andrew%20Ng%20(DeepLearning.AI)-green?style=for-the-badge)

## 📌 Project Overview & Motivation

This project applies **Supervised Machine Learning** techniques to analyze real-world seismic data from the **East Anatolian Fault Zone (Turkey)**. The primary objective is to explore the relationship between focal depth and earthquake magnitude using **Linear and Logistic Regression**.

> **🇹🇷 Developer's Note:**
> "Eğitim sürecinde sadece dersleri izleyip teorik kavramları öğrenmekle kalmayıp, bu bilgileri **ülkemizin en kritik gerçeklerinden biri olan deprem sorunu** üzerine uygulamayı hedefledim. Bu amaçla, sentetik veri setleri yerine **AFAD**'ın sağladığı gerçek deprem kataloglarını kullanarak Doğu Anadolu Fay Hattı'nı analiz ettim."
>
> *(Translation: Beyond learning theoretical concepts, I aimed to apply this knowledge to one of my country's most critical realities: the earthquake problem. Therefore, I analyzed the East Anatolian Fault Line using real data provided by AFAD instead of synthetic datasets.)*

## 🛠️ Tech Stack
* **Python:** Core programming language.
* **Pandas & NumPy:** For data manipulation and vectorization.
* **Matplotlib:** For visualizing the fault line and decision boundaries.
* **Scikit-Learn:** For implementing ML algorithms (Linear & Logistic Regression).
* **Dataset:** Real-time seismic data cataloged by **AFAD** (Disaster and Emergency Management Authority).

## 🧠 Methodology and Insights

This project bridges the gap between the theory taught in **Andrew Ng's Machine Learning Specialization (Course 1)** and real-world application.

### 1. Spatial Visualization
Before modeling, I visualized the coordinates (`Latitude`, `Longitude`) to confirm the data quality. The scatter plot clearly delineates the geometry of the East Anatolian Fault.

### 2. Linear Regression (Univariate)
* **Goal:** Predict earthquake Magnitude ($y$) based on Focal Depth ($x$).
* **Model:** $f_{w,b}(x) = wx + b$
* **Result:** The model demonstrated **High Bias (Underfitting)**.
* **Insight:** Real-world seismic data is noisy. Magnitude is influenced by complex geological factors (stress accumulation, rock type), proving that a single feature (depth) is insufficient for precise prediction.

### 3. Logistic Regression (Binary Classification)
* **Goal:** Classify earthquakes as **"Major"** ($Ml \ge 4.0$) or **"Minor"**.
* **Model:** Sigmoid Function $g(z) = \frac{1}{1 + e^{-z}}$
* **Result:** The model successfully established a probabilistic **Decision Boundary**.
* **Insight:** Unlike linear regression, this approach provided a useful statistical framework to assess the probability of significant seismic events based on depth.

## 🚀 How to Run
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
    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/emrealtindag/East-Anatolian-Fault-ML-Analysis/blob/main/Earthquake_Analysis.ipynb)
---
*Created by [Emre Altındağ](https://www.linkedin.com/in/emrealtindag1/)*
