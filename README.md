# ML4SCI GSoC 2026: Quantum Circuit Design with LLMs

**Candidate:** Antony Selva Jasfer A.  
**Program:** B.Tech in AI & DS, Amrita Vishwa Vidyapeetham, Nagercoil Campus  
**Organization:** Machine Learning for Science (ML4SCI)  

---

## 🔬 Project Overview

This repository contains the evaluation tasks for the **Google Summer of Code (GSoC) 2026** application for the ML4SCI organization. The project demonstrates a robust pipeline integrating classical Deep Learning, Quantum Machine Learning (QML), and Orchestral AI to analyze high-energy physics data.

The core deliverable is a single Jupyter Notebook (`ML4SCI_GSoC2026_Evaluation.ipynb`) divided into three primary objectives:

### 1. Classical Baseline (MNIST)
A lightweight Convolutional Neural Network (CNN) implemented in PyTorch to establish a classical baseline for image classification. It features a sequential architecture optimized for fast convergence on normalized 28x28 grayscale inputs.

### 2. Quantum Interactive Neural Network (QINN)
A hybrid quantum-classical architecture designed to classify Quark and Gluon jets from complex `.parquet` datasets. 
* **Classical Feature Extraction:** Reduces 125x125 3-channel images into a dense latent vector.
* **Quantum Processing:** Utilizes `pennylane` to feed the latent vector into a 4-qubit Parameterized Quantum Circuit (PQC) using Angle Embedding and Basic Entangler Layers to capture quantum correlations.
* **Fault Tolerance:** Includes automated structural fallback mechanisms to handle OS-level serialization discrepancies in sequence data.

### 3. Agentic Hyperparameter Optimization (Closed-Loop)
An autonomous evaluation pipeline governed by a Large Language Model (LLM) using the `google.genai` SDK and the **Gemini 2.0 Flash** model. 
* The training loop acts as a callable tool, returning real-time loss metrics to the agent.
* The LLM controller dynamically analyzes the loss and autonomously steers the hyperparameter schedule (e.g., dynamically decaying the learning rate from 0.1 to 0.0001).
* Features a graceful simulation fallback mechanism to ensure reproducible execution and deterministic logic demonstration under strict free-tier API rate limits (`429 RESOURCE_EXHAUSTED`).

---

## 🚀 Installation & Usage

To run this notebook locally, ensure you have Python 3.13+ installed.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/antonyjasfer/GSOC-2026-ML4SCI-Tasks.git
cd GSOC-2026-ML4SCI-Tasks
