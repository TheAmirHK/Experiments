# Federated Learning with PyTorch: Healthcare Simulation

## Code Overview
This repository demonstrates a federated learning simulation using PyTorch. The goal is to train a global model on distributed healthcare datasets from multiple hospitals without sharing raw data.
The simulation uses synthetic data for simplicity, but it can be adapted to real-world datasets.

### Key Features
- Synthetic Data Generation: Simulated healthcare datasets for 5 hospitals.
- Federated Learning Workflow:
  -  Local training on each hospital's data.
  -  Aggregation of model weights to update the global model.
- Evaluation: The global model is evaluated on a test dataset.

## Code Structure

### 1. Data Generation
- Synthetic healthcare datasets are generated for 5 hospitals.
- Each dataset contains:
  - Features: Age, BMI, blood pressure, cholesterol levels, glucose levels.
  - Labels: Binary classification (1 for readmission, 0 for no readmission).

### 2. Model Architecture
- A simple feedforward neural network (SimpleNN) is used for training.
- Architecture:
  - Input layer: 5 features.
  - Hidden layers: 32 and 16 neurons with ReLU activation.
  - Output layer: 2 neurons (binary classification).

### 3. Federated Learning Workflow
- **Local Training**: Each hospital trains a local model on its dataset.
- **Weight Aggregation**: Local model weights are averaged to update the global model.
- **Global Model Update**: The global model is updated iteratively over multiple rounds.

### 4. Evaluation
- The global model is evaluated on a test dataset.
- Accuracy is reported as the performance metric.
- 
---
## Key Results

- Global Model Accuracy: 95.40%
-  Training Rounds: 10
-  Local Epochs per Round: 5
