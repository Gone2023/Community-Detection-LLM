# 🧠 Community Detection in Social Networks using LLMs

**Author:** Govind

A research-inspired project that explores how **Large Language Models (LLMs)** can be used for **community detection in graphs**, moving beyond traditional structural algorithms.

> ⚠️ Note: This project is for research and educational purposes.

---

## 🚀 Overview

Community detection is a key problem in graph mining where the goal is to identify groups of nodes that are more densely connected internally than externally.

Traditional methods rely purely on graph structure. This project implements a **novel approach (CommLLM)** that leverages:

* 🧠 Natural Language Understanding (LLMs)
* 🔄 Graph-to-Text Conversion
* 💬 Prompt-based Reasoning

Instead of running graph algorithms, we:

> Convert the graph into text → Feed it to an LLM → Let it infer communities

---

## 🧩 Key Idea

The pipeline consists of two main steps:

### 1️⃣ Graph → Text Conversion

Each node and its connections are converted into natural language:

```
Node 0 is connected to: 1, 2, 3, 4, ...
Node 1 is connected to: 0, 2, 3, ...
```

---

### 2️⃣ LLM-based Community Detection

We prompt the model:

```
"A community is a group of nodes that are more densely connected internally than externally.
Based on these node connections, assign each node to a community."
```

The LLM outputs:

```
Node:0; Community:1
Node:1; Community:1
...
```

---

## 🏗️ Architecture

```
Graph Data (Karate Club)
        ↓
Graph → Text Encoding
        ↓
Prompt + LLM (LLaMA3-70B via Groq)
        ↓
Community Assignment
        ↓
Evaluation Metrics
```

---

## 📊 Results

| Metric   | Score         |
| -------- | ------------- |
| NMI ↑    | 0.7212        |
| ARI ↑    | 0.6320        |
| Purity ↑ | **1.0000** 🔥 |
| VOI ↓    | 0.7731        |

> ⭐ Achieved **higher purity than the original paper (0.98)**

---

## 🧪 Dataset

* **Zachary’s Karate Club Dataset**
* Standard benchmark for community detection

---

## 🛠️ Tech Stack

* Python 🐍
* NetworkX
* NumPy / Pandas
* LLaMA3-70B (via Groq API)
* Jupyter Notebook

---

## ⚙️ Implementation Details

* ✔️ Graph-to-text encoding preserves full adjacency
* ✔️ Prompt engineering for structured output
* ✔️ Majority voting across multiple LLM runs (to reduce randomness)
* ✔️ Evaluation using:

  * NMI
  * ARI
  * Purity
  * VOI

---

## 📂 Project Structure

```
Community-Detection-LLM/
│
├── notebook/
│   └── special_topic.ipynb
│
├── report/
│   └── community_detection.pdf
│
├── results/
│   └── outputs.json
│
├── README.md
```

---

## 🚧 Limitations

* LLM responses are **non-deterministic**
* Performance depends on **prompt quality**
* Not scalable to very large graphs (token limits)

---

## 🔮 Future Improvements

* Fine-tuning LLMs for graph reasoning
* Hybrid models (Graph Neural Networks + LLMs)
* Better graph encoding strategies
* Scaling to large real-world networks

---

## 📌 Why This Project Matters

This project explores a **new paradigm shift**:

> From **mathematical optimization → reasoning-based AI**

It shows that LLMs can:

* Understand graph structure via text
* Infer communities without explicit algorithms
* Open new directions in **Graph + NLP research**

---

## 📎 References

* CommLLM Paper (Gujral & Sinha, 2025)
* LLaMA3 Model
* NLGraph Benchmark

---

## 🤝 Contributing

Feel free to fork the repo and experiment with:

* Different prompts
* Other datasets
* Alternative LLMs

---

## ⭐ Acknowledgment

Inspired by recent research in **LLMs for graph reasoning** and community detection.

---

## 📬 Contact

For questions or collaborations:

* GitHub: *https://github.com/Gone2023*
* LinkedIn: *https://www.linkedin.com/in/govind-singh-1575051b9/*

---

⭐ If you found this project interesting, consider giving it a star!
