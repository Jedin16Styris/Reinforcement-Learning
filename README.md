# 📈 Deep Reinforcement Learning for Algorithmic Trading 🤖

This project demonstrates an **automated stock trading strategy** using **Deep Reinforcement Learning (DRL)**.  
An agent was trained using a **Deep Q-Learning algorithm** on historical stock data to learn how to make profitable trading decisions.  
The goal is to create a **self-learning system** that dynamically adapts its strategy to maximize financial returns by deciding whether to **buy**, **sell**, or **hold** assets.

The model was trained and evaluated on historical daily data for **NVIDIA (NVDA)**, chosen for its high liquidity and volatility, providing a challenging and realistic test case.

---

## ⚙️ Methodology

The trading agent was built using a value-based reinforcement learning method, where it learns the **expected return of taking an action in a given state**.

### 📊 1. Data and Environment
* **Data Source**: Historical stock data from **Polygon.io**  
* **State Representation**: A **rolling window of 15 days** of prices is used as the state input  
* **Data Preprocessing**: Prices are standardized and normalized using a sigmoid function  
* **Dataset Split**: **80%** of data for training, **20%** for testing  

### 🏋️‍♂️ 2. Training Process
* **Learning Algorithm**: **Deep Q-Network (DQN)**  
* **Episodes**: Trained over **300 episodes** for stable learning  
* **Experience Replay**: Stores past transitions (state, action, reward, next state) to break correlations  
* **Exploration vs. Exploitation**: **Epsilon-greedy strategy** with epsilon decaying from `1.0` → `0.01`  

---

## 🏗️ Q-Network Architecture

The **Deep Q-Network** is the 🧠 brain of the agent.  

* **Layers**: **3 fully connected (dense) layers**  
* **Activation**: **Leaky ReLU** to prevent the “dying ReLU” problem  
* **Optimizer**: **Adam** optimizer with learning rate `0.00005`  
* **Loss Function**: **Mean Squared Error (MSE)**  
* **Regularization**: **Dropout layers** to prevent overfitting  

---

## 🏆 Results and Performance

The trained agent was evaluated on unseen test data, showing **strong performance**:  

* **Win Rate**: Consistently between **60–70%** ✅  
* **Sharpe Ratio**: Healthy **risk-adjusted returns** ⚖️  
* **Max Drawdown**: Kept at **low levels**, indicating strong risk management 📉  
* **Total Profit**: Outperformed simple benchmark strategies 💰  

These results show that the agent can **identify profitable opportunities** while **managing risk effectively**.

---

## 💡 Conclusion and Future Work

This project demonstrates that **Deep Reinforcement Learning is a viable approach** for building automated trading systems.  
The agent successfully learned to **adapt to market conditions** and make **profitable trading decisions** in a simulated environment.

**Future improvements** could include:  
* Using **higher frequency data** (hourly/minutely) for more responsive trading  
* Expanding the **action space** (e.g., varying position sizes)  
* Integrating **advanced risk management** techniques  
* Adapting the system for **real-time market data** 🚀  

---
## 📄 Project Report & Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XgHF7jBear0og38RSdF2Ll_S0yp2LqhM?usp=sharing)
[![View FULL Code and Output](https://img.shields.io/badge/View%20Report-PDF-blue)](https://github.com/Jedin16Styris/Reinforcement-Learning/blob/main/Reinforcement%20Learning%20in%20Trading%20CnO.pdf)
 

---
