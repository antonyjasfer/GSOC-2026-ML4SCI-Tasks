# GSoC 2026: ML4SCI Evaluation Tasks

This repository contains my completed evaluation tasks for the Google Summer of Code (GSoC) application for the **Machine Learning for Science (ML4SCI)** umbrella organization. 

The focus of these tasks is implementing both classical and quantum machine learning architectures for high-energy physics data analysis.

## Task 1: Classical Image Classification (MNIST)
A baseline classical Convolutional Neural Network (CNN) implemented in PyTorch. 
* **Objective:** Establish a robust classical training pipeline and evaluation loop.
* **Stack:** `torch`, `torchvision`
* **Dataset:** Standard MNIST digit classification.

## Task 2: Quantum-Classical Hybrid Architecture (Quark-Gluon Classification)
A Quantum Interactive Neural Network (QINN) designed to classify Quark and Gluon jets from collider data.
* **Objective:** Downsample complex high-energy physics images using a classical CNN and feed the extracted features into a Parameterized Quantum Circuit (PQC).
* **Stack:** `torch`, `pennylane`, `pyarrow`
* **Dataset:** CMS Open Data (Parquet format). 
* **Architecture:** 1. Classical Convolutional layers for feature extraction and dimensionality reduction.
  2. A 4-qubit Quantum Layer (`qml.qnn.TorchLayer`) utilizing Angle Embedding and Basic Entangler Layers.
  3. Classical fully connected output layer for binary classification.

## Implementation Details
The notebook is structured modularly with clear separation between data pipelines, architecture definition, and training execution. It includes dynamic exception handling for structural variances in nested Parquet files to ensure uninterrupted end-to-end execution across different hardware environments.
