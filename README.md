# Unsupervised GNN Anomaly Detection

## 📌 Overview
This project focuses on detecting anomalies in the manufacturing process using **Graph Neural Networks (GNNs)**. By analyzing **machine-worker interactions** and **operational status**, the model aims to identify deviations from expected behavior.

## 🏭 Manufacturing Process Flow (SOP)
The product manufacturing process follows a sequential flow:

1️⃣ **Task 1 → Requires Machine 1**  
2️⃣ **Task 2 → Requires Machine 2** *(Starts only after Task 1 is completed)*  
3️⃣ **Task 3 → Requires Machine 3** *(Starts only after Task 2 is completed)*  

### ⏱ Task Timings:
- **Task 1:** ⏳ Start - `17:58:07` | 🛑 End - `17:59:47`
- **Task 2:** ⏳ Start - `17:59:47` | 🛑 End - `18:01:27`
- **Task 3:** ⏳ Start - `18:01:27` | 🛑 End - `18:02:59`

## 📊 Available Data
- 🏭 **Machine status** (running or not) recorded every second.
- 👷 **Number of workers** assigned to each machine.

## 🎯 Objective
Develop a **GNN-based anomaly detection model** to identify **irregularities** in the manufacturing process by:
- 🔗 **Converting tabular data into a graph** to capture relationships between variables.
- 🧠 **Training an unsupervised GNN model** to detect potential anomalies.
- 📈 **Analyzing machine-worker interactions** and operational status.

## ⚠️ Important Considerations
- The dataset **does not contain labeled anomalies**.
- Some deviations from SOP are **expected due to dynamic manufacturing conditions**.

### 🔄 Example of Expected Variation:
- If **material density is too high** during **Task 1** (Machine 1 processing), the material may be **temporarily processed in Machine 3** before resuming Task 1.
- **❌ This is not an anomaly** but rather an **adaptive behavior** in the manufacturing process.

## 🚀 Goal
The project aims to **differentiate between expected process variations and real anomalies**, ensuring **accurate detection** without misclassifying normal operational adjustments.

---

## 🛠 Tech Stack
- **Python 🐍**
- **PyTorch Geometric 🔥**
- **NetworkX 📊**
- **Pandas & NumPy 📊**
- **Google Colab 🚀**

## 📌 Setup Instructions
```bash
git clone https://github.com/Akhil-Kambhatla/GNN-Based-Anomaly-Detection.git
cd your-repo-name
pip install -r requirements.txt
