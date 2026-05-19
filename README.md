# PetNet🐶🐱
This project investigates how class imbalance and label noise affect image classification performance using the Oxford-IIIT Pet dataset and a custom PyTorch convolutional neural network.

The dataset was split into:

- Training set

- Validation set

- Test set

The test set was kept completely separate and used only for final evaluation.
## Dataset Samples
<img src="figures/dataset_samples.png" width="600">


## Installation
```bash
pip install -r requirements.txt
```

## Running the Project
```bash
jupyter notebook main.ipynb
```

## Project Objectives
The aims of this project are to:
1. Develop a convolutional neural network (PetNet) for multi-class pet image classification.
2. Introduce controlled training data biases.
3. Compare the effects of class imbalance and label noise.
4. Evaluate how these biases affect model generalisation.


## Training Configuration
| Parameter | Value |
|--------|--------:|
| Optimizer | Adam |
| Learning Rate | 0.0005 |
| Batch Size | 32 |
| Epochs | 250 |
| Weight Decay | 1e-4 |
| Dropout | 0.5 |
| Loss Function | CrossEntropyLoss |


## Bias Experiments

### Class Imbalance
Two biased training datasets were created by reducing the number of samples in selected classes.
<img src="figures/dataset_samples.png" width="600">
### Label Noise
Three biased training datasets were created by randomly replacing:
- 10%/20%/30% of labels
<img src="figures/dataset_samples.png" width="600">

