# A Quantum Cognitive Approach to Multimodal Emotion Recognition

This repository contains the official code and resources for the research paper, "A Quantum Cognitive Approach to Multimodal Emotion Recognition". This work investigates the application of quantum computing principles to multimodal emotion recognition, designing and evaluating a hybrid deep learning framework and comparing a classical architecture against two quantum-based classifiers.

---

## Abstract

Accurate emotion recognition is a significant challenge in human-computer interaction, largely due to the inherent ambiguity and context-dependency of human affective states. While classical deep learning models have shown success, they often struggle to capture the nuances of emotional uncertainty. This paper explores a novel hybrid framework for multimodal emotion recognition inspired by the principles of quantum cognition. We propose and investigate a deep learning architecture that fuses features from four modalities—facial images, speech, text, and EEG signals—and utilizes a Variational Quantum Classifier (VQC) as its core decision-making component. We establish a robust classical baseline model which achieves a 41.12% accuracy and demonstrates stable learning across seven emotion classes. Our key finding is that the VQC, in multiple configurations, exhibits significant training instability and suffers from mode collapse, a challenge we analyze through loss landscape visualization. As a comparative study, a Quantum Support Vector Machine (QSVM) is shown to be stable on the same feature space. Our results highlight a critical and open challenge in the practical application of current VQCs for complex, real-world classification tasks, suggesting that while theoretically promising, significant work is needed to ensure their stability and reliability.

---

## Model Architecture

Our best-performing model is a **Classical Hybrid Fusion** architecture that processes four modalities to produce a final emotion classification. The architecture is designed to first learn specialized "paired" features from key modalities (e.g., Audio-Visual) before a final global fusion.

![Model Architecture](architecture_diagram.png)  
*TODO: Upload your `architecture_diagram.png` file to this GitHub repository to make it visible here.*

---

## Datasets

This project uses four publicly available datasets:
* **Image:** FER-2013
* **Speech:** RAVDESS
* **Text:** Publicly available Kaggle Emotion Dataset
* **EEG:** DEAP

---

## Key Results

Our research produced a series of comparative results:
* **Classical Baseline:** Achieved a stable accuracy of **41.12%**.
* **Classical Hybrid Fusion Model:** Our best-performing classical model achieved an accuracy of **43.49%**.
* **Variational Quantum Classifier (VQC):** Proved to be fundamentally unstable in all configurations, consistently suffering from "mode collapse".
* **Quantum Support Vector Machine (QSVM):** Was shown to be a stable quantum learner, achieving **48.60%** accuracy on a simplified, unimodal task.

---

## Setup and Installation

The code was developed and run in a Kaggle Notebook environment with GPU acceleration. The following libraries are required for the project:
torch
pennylane
qiskit==1.1.1
qiskit-aer==0.14.2
qiskit-machine-learning==0.8.0
transformers
librosa
scikit-learn
pandas
seaborn
matplotlib


---

## How to Run

The main experiments are contained within the `Paper Code.ipynb` Jupyter Notebook. The notebook is structured to run a series of experiments in a logical order:
1.  **Classical Baseline and Hybrid Fusion Model Training**
2.  **Ablation Studies**
3.  **Variational Quantum Classifier (VQC) Analysis**
4.  **Quantum Support Vector Machine (QSVM) Analysis**

---

## Code Availability

The code and models developed for this research are available in this repository. The `Paper Code.ipynb` file contains all the experiments, and the `Paper Information.docx` file contains a detailed summary of the project.
