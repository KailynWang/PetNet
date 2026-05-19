# PetNet🐶🐱

The Impact of Training Data Bias on CNN-Based Classification

# Training Data Bias in Pet Image Classification

This project investigates how different forms of training data bias affect image classification performance using the Oxford-IIIT Pet dataset and a custom convolutional neural network implemented in PyTorch.


The study compares a baseline model trained on clean and balanced data with multiple biased models trained using:

- Class imbalance
- Label noise

The impact of these biases is analysed using quantitative metrics, learning curves, confusion matrices, and inference visualisation.

---

## Project Objectives

The aims of this project are to:

1. Develop a convolutional neural network (PetNet) for multi-class pet image classification.
2. Introduce controlled training data biases.
3. Compare the effect of different biases on model performance.
4. Evaluate both quantitative and qualitative differences in model behaviour.

---

## Dataset

The project uses the Oxford-IIIT Pet dataset, which contains 37 cat and dog breeds.

- Total classes: 37
- Image classification task
- Automatically downloaded using `torchvision.datasets.OxfordIIITPet`

The dataset was split into:

- Training set
- Validation set
- Test set

The test set was kept completely separate and used only for final evaluation.

---

## Model Architecture

A custom convolutional neural network (`PetNet`) was implemented using PyTorch.

Key components:

- Convolutional layers with ReLU activation
- Max pooling
- Dropout (0.5)
- Fully connected classifier
- CrossEntropyLoss

---

## Training Configuration

| Parameter | Value |
|--------|--------:|
| Optimizer | Adam |
| Learning rate | 0.0005 |
| Batch size | 64 |
| Epochs | 250 |
| Weight decay | 1e-4 |
| Dropout | 0.5 |
| Loss function | CrossEntropyLoss |

---

## Bias Experiments

### 1. Class Imbalance

Two biased datasets were created by reducing the number of training samples for selected classes.

### 2. Label Noise

Three biased datasets were created by randomly replacing:

- 10% of training labels
- 20% of training labels
- 30% of training labels

---

## Evaluation Methods

Models were evaluated using:

- Accuracy
- Macro Precision
- Macro Recall
- Macro F1-score
- Weighted F1-score
- Validation accuracy and loss curves
- Confusion matrices
- Inference visualisation

---

## Key Findings

- The baseline model achieved the best performance.
- Both class imbalance and label noise reduced generalisation performance.
- Class imbalance mainly affected underrepresented classes.
- Label noise caused a progressive decline in performance as noise level increased.
- Severe label noise (30%) produced the weakest results.

---


## Authors
Jialing Wang, Jianan Ding
MSc Medical Physics in Cancer Radiation Therapy
University of Manchester

## Repository Structure
```text
pet-bias-classification/
├── main.ipynb
├── README.md
├── requirements.txt
├── .gitignore
├── logs/
├── results/
└── figures/

