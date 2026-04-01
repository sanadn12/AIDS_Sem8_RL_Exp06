# 📘 Multi-Armed Bandit Exploration Strategies

## 🎯 Aim
To implement and compare different exploration strategies—specifically **Epsilon-Greedy** and **UCB1 (Upper Confidence Bound)**—in solving the Multi-Armed Bandit problem using reinforcement learning techniques.

---

## 🧩 Problem Statement
The **Multi-Armed Bandit problem** is a fundamental problem in reinforcement learning where an agent must choose between multiple actions (arms), each providing a reward from an unknown probability distribution.  

The objective is to maximize the total reward over time by effectively balancing:
- **Exploration** (trying new actions)
- **Exploitation** (choosing the best-known action)

---

## 📚 Brief Theory

### 🔹 Multi-Armed Bandit
- A scenario with `k` different actions (arms)
- Each arm has an unknown reward distribution
- The agent learns the optimal strategy through repeated interactions

---

### 🔹 Exploration vs Exploitation
- **Exploration:** Discovering new actions to improve knowledge  
- **Exploitation:** Using current knowledge to maximize reward  

---

### 🔹 Strategies Used

#### 1. Epsilon-Greedy
- With probability **ε**, select a random action  
- Otherwise, select the action with the highest estimated reward  

#### 2. UCB1 (Upper Confidence Bound)
- Selects action using:

---

### 🔹 Exploration vs Exploitation
- **Exploration:** Discovering new actions to improve knowledge  
- **Exploitation:** Using current knowledge to maximize reward  

---

### 🔹 Strategies Used

#### 1. Epsilon-Greedy
- With probability **ε**, select a random action  
- Otherwise, select the action with the highest estimated reward  

#### 2. UCB1 (Upper Confidence Bound)
- Selects action using:
Q(a) + c * sqrt(log(t) / N(a))



- Balances exploration and exploitation using confidence bounds

---

## ⚙️ Implementation Explanation

### 1. MultiArmedBandit Class
- Initializes `k` arms with rewards drawn from a normal distribution
- Identifies the optimal arm
- Returns a reward when an arm is selected

---

### 2. Agent Class
- Stores:
- Estimated rewards (`Q`)
- Number of times each arm is selected (`N`)
- Implements:
- Epsilon-Greedy strategy
- UCB1 strategy
- Updates estimates using incremental averaging

---

### 3. run_strategy Function
- Simulates multiple runs of the experiment
- Executes different strategies over several steps
- Computes average rewards for comparison

---

### 4. Visualization
- Uses **Matplotlib** to plot:
- Steps vs Average Reward
- Comparison of strategies

---

## 📊 Results

- **UCB1** shows better long-term performance due to systematic exploration.
- **Epsilon-Greedy** performs well but depends heavily on the value of ε.
- The graph demonstrates:
- Gradual improvement in rewards
- Better convergence for UCB1

---

## ✅ Conclusion

- Balancing exploration and exploitation is crucial in reinforcement learning.
- **UCB1** is more efficient for long-term optimization.
- **Epsilon-Greedy** is simple and effective but requires parameter tuning.
- These strategies form the basis of many real-world decision-making systems.

---

## 📖 References

1. Sutton, R. S., & Barto, A. G.  
 *Reinforcement Learning: An Introduction*

2. NumPy Documentation  
 https://numpy.org/

3. Matplotlib Documentation  
 https://matplotlib.org/

---

## 📦 requirements.txt

numpy
matplotlib
