# Deep Learning for High-Frequency Trading

This repository contains the implementation and experiments from my bachelor thesis **“Deep Learning for High-Frequency Trading”**. The project focuses on applying deep learning methods to financial time-series data, evaluating their performance, and comparing them with the traditional **Dollar-Cost Averaging (DCA)** strategy.

---

## 🎯 Objectives
- Provide an overview of deep learning methods applied to **high-frequency trading (HFT)**.  
- Design and implement deep learning models for solving selected HFT tasks.  
- Compare the performance of the models against the **DCA strategy**.  
- Visualize the results and model behavior.  

---

## 📖 Background

### High-Frequency Trading (HFT)
High-frequency trading involves the use of advanced algorithms and technologies to exploit small price movements in financial markets. It is widely used by **hedge funds** and **investment banks**.  
Main strategies include:
- **Market making**  
- **Directional trading**  
- **Statistical arbitrage**  

### Dollar-Cost Averaging (DCA)
DCA is a passive investment strategy where a fixed amount of money is invested into an asset at regular intervals, regardless of price. It reduces the impact of volatility and is widely used by retail investors.

---

## 📊 Dataset & Preprocessing
The dataset consists of **Amazon stock data** across different time periods.  

Key preprocessing steps:
- **Normalization** of input values  
- **Tagging/labeling** for supervised learning  
- Custom **Data Generator** with functions:  
  - `create_sequences_and_labels()`  
  - `get_class_indices()`  
  - `__len__()`  
  - `__getitem__()`  

---

## 🧠 Model & Strategy
The implemented strategy is based on a **Convolutional Neural Network (CNN)** with two hidden layers.  

Trading rules:
- Execute a trade only if model confidence > **60%**.  
- **Buy**: invest **1–5%** of initial capital to minimize risk.  
- **Sell**: liquidate all assets at once (highest profit probability).  

---

**Observation:** While the deep learning model was profitable in most cases, the **DCA strategy outperformed** it in long-term stability and overall gains. This shows that while machine learning can capture short-term price patterns, simple strategies like DCA remain strong competitors.

---

## 🚀 How to Use
1. Clone this repository and open the Jupyter Notebook in Google Colab or locally.  
2. Install required dependencies (`tensorflow`, `numpy`, `pandas`, `matplotlib`).  
3. Run the notebook cells to:  
   - Preprocess the dataset  
   - Train the CNN model  
   - Simulate trading performance  
   - Compare with DCA results  

---
