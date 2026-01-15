# 📊 Implementation of Clustering and Classification in Stock Asset Selection for Portfolio Diversification

### 🎯 **Project Overview**  
This project implements a comprehensive **machine learning framework** for **dynamic stock portfolio construction**, combining:  

- 🧩 **Unsupervised Clustering:** K-Means, DBSCAN, Agglomerative  
- 🤖 **Deep Learning Forecasting:** LSTM Neural Networks  
- 🧠 **Market Regime Classification:** Support Vector Machines (SVM)  
- 📈 **Data-Driven Portfolio Optimization**  

The framework is specifically designed to handle the **volatility and complexity of emerging markets**, tested on **110 stocks** from the **Indonesia Stock Exchange (IDX)** across **11 sectors (2015–2025)**.  

---

### 🚀 **Key Features**

#### 1️⃣ Multi-Algorithm Clustering
- **K-Means:** Balanced diversification with *8 clusters* (**Recommended ⭐**)  
- **DBSCAN:** Density-based outlier detection  
- **Agglomerative:** Hierarchical risk-aware grouping  

#### 2️⃣ LSTM-Based Sharpe Ratio Forecasting
- **2-layer architecture (50 units each)**  
- **Input features:** MACD, Inflation indicators  
- **Predicts future risk-adjusted returns (Sharpe Ratios)**  
- **Representative stock selection** via MAE optimization  

#### 3️⃣ SVM Market Regime Classification
- **Beta coefficient-based regime detection**  
- **3 market states:**  
  - 📈 Uptrend (β > 1)  
  - ➖ Sideways (β ≈ 0)  
  - 📉 Downtrend (β < -1)  
- **Adaptive portfolio optimization per regime**  

#### 4️⃣ Intelligent Weight Allocation
- Data-driven weights using predicted Sharpe Ratios  
- Min-max normalization + proportional balancing  
- Mean-Variance Optimization (MVO) per regime  

---

### 📊 **Performance Metrics**

| Method           | Sharpe Ratio | Risk (σ) | Expected Return | Clusters | F1-Score |
|------------------|--------------|-----------|-----------------|-----------|-----------|
| **K-Means**       | **0.2523**   | 15%       | 8.0%             | 8         | 0.486     |
| **Agglomerative** | -0.1245      | 11%       | 4.5%             | 8         | 0.494     |
| **DBSCAN**        | **0.4789**   | 24%       | 12.0%            | 2         | 0.639     |

---

### 🏆 **Key Findings**
✅ **K-Means** delivers the most balanced and diversified portfolios  
✅ **Agglomerative** provides the lowest risk (*ideal for conservative investors*)  
✅ **DBSCAN** achieves the highest Sharpe Ratio but lacks diversification  
✅ **Healthcare stocks** (e.g., *MIKA.JK*) show highest predictability (*MAE: 0.294*)  
✅ **Regime-aware optimization** improves performance during sideways markets  

---

### 🧰 **Tech Stack**
- **Python** (NumPy, Pandas, Scikit-learn, TensorFlow, Matplotlib, Seaborn)  
- **Machine Learning Algorithms:** K-Means, DBSCAN, Agglomerative, SVM  
- **Deep Learning:** LSTM for time-series forecasting  
- **Portfolio Optimization:** Mean-Variance, Sharpe Ratio prediction  
- **Visualization:** Plotly & Seaborn for insights  

---

### 📂 **Dataset**
- **Source:** Indonesia Stock Exchange (IDX)  
- **Period:** 2014–2025  
- **Sectors:** 11 (Banking, Healthcare, Technology, Consumer, Energy, etc.)  
- **Indicators:** MACD, Inflation, Volume, Price Change, Volatility, Beta  

---
