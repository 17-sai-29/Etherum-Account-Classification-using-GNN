# Etherum-Account-Classification-using-GNN
Utilized graph-based visualizations to analyze the flow of Ethereum transactions,extracting node types and temporal features over defined time windows. Leveragedthese features as sequential inputs across timestamps and implemented graphneural networks (GNNs) to effectively predict node types and their behavioralpatterns.

# 🧠 Ethereum Account Classification using Graph Neural Networks (GNNs)

This project aims to classify Ethereum accounts as **Externally Owned Accounts (EOAs)** or **Smart Contracts** using a **graph-based approach**. By modeling the Ethereum transaction network as a temporal graph, we apply **Graph Neural Networks (GNNs)** to capture both structural and temporal patterns in transaction behavior.

---

## 📌 Overview

Ethereum’s decentralized and dynamic nature makes account classification a non-trivial task. To address this, we:

- 📊 Extracted **graph-based features** from Ethereum transaction data.
- ⏱️ Incorporated **temporal windows** to model behavioral changes over time.
- 🔗 Built **transaction graphs**, treating addresses as nodes and transfers as edges.
- 🧠 Trained **Graph Neural Networks (GNNs)** to predict node types and patterns.

---

## 🛠️ Key Features

- 🧩 **Graph Construction**:
  - Nodes = Ethereum accounts (`from` and `to` addresses).
  - Edges = Transactions (with weights like value, gas, etc.).
  - Temporal segmentation into hourly/daily windows.

- ⏳ **Temporal Feature Engineering**:
  - In-degree, out-degree, transaction frequency.
  - Rolling activity stats (e.g., moving average of gas usage).
  - Time-aware node embeddings.

- 🤖 **GNN-based Classification**:
  - Implemented using PyTorch Geometric / DGL.
  - GNN layers like `GCNConv`, `GraphSAGE`, or `GAT`.
  - Trained to classify node types (EOA vs Smart Contract).

---

## 🧪 Pipeline

1. **Data Ingestion**:
   - Raw transaction data (blockNumber, from, to, gasUsed, value, etc.).

2. **Graph Generation**:
   - Create dynamic graphs per time window (e.g., per day/hour).

3. **Feature Extraction**:
   - Node-centric features: contract status, degree, transaction stats.
   - Temporal statistics over sliding windows.

4. **Model Training**:
   - Feed sequential graph snapshots into the GNN.
   - Train on labeled accounts with known types.

5. **Evaluation**:
   - Accuracy, precision, recall, ROC curves.
   - Visualization of predicted labels and misclassifications.

---


## 💻 Technologies Used

| Component               | Tool/Library             |
|-------------------------|--------------------------|
| Data Processing         | Python, Pandas, NumPy    |
| Graph Construction      | NetworkX, PyTorch Geometric / DGL |
| GNN Models              | GCN, GraphSAGE, GAT      |
| Visualization           | Matplotlib, Seaborn, Graphviz |
| Dataset                 | Ethereum transaction logs (custom or public) |

---

## 🧩 Potential Applications

- 🚩 **Anomaly detection** (e.g., identifying malicious contracts).
- 📉 **Behavioral forecasting** of addresses.
- 🔐 **Smart contract auditing** via structural properties.

---

