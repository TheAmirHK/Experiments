# Federated Learning with PyTorch: Healthcare Simulation (FederatedLearning_HospitalUsecase)

## Code Overview
FederatedLearning_HospitalUsecase demonstrates a federated learning simulation using PyTorch. The goal is to train a global model on distributed healthcare datasets from multiple hospitals without sharing raw data.
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
- A simple feedforward neural network (`SimpleNN`) is used for training.
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

## Key Results

- Global Model Accuracy: 95.40%
-  Training Rounds: 10
-  Local Epochs per Round: 5

---
# Federated Learning with MNIST using PyTorch (FederatedLearning_with_FedAvg)

This code demonstrates two methods of Federated Learning (FL) applied to the MNIST dataset using PyTorch:

- **FedAvg (Federated Averaging)**: A basic Federated Learning method where each client trains a local model, and their weights are averaged to update the global model.
- **FedProx**: An extension of FedAvg that introduces a proximal term to the local training loss, penalizing deviations from the global model weights. This can improve convergence in certain situations but may be less time-efficient than FedAvg.

## Code Breakdown

### 1. Data Loading (`load_mnist_data`)
This function splits the MNIST dataset into multiple subsets, one for each client. Each client trains their model using their respective subset of the data.

### 2. Model Definition (`SimpleNN`)
A simple neural network is used for both local and global models. The architecture consists of:
- **Input layer**: 28x28 flattened image
- **Hidden layer 1**: 128 neurons
- **Hidden layer 2**: 64 neurons
- **Output layer**: 10 neurons (corresponding to MNIST classes 0-9)

### 3. Federated Averaging (`fed_avg`)
The `fed_avg` function takes model weights from multiple clients and averages them to compute the global model weights.

### 4. Training Local Models
- **`train_local_model`**: Trains a local model using a client’s subset of the MNIST dataset for a specified number of epochs.
- **`train_local_model_fedprox`**: Similar to `train_local_model`, but adds a proximal term to the loss function, penalizing large deviations from the global model weights.

### 5. Federated Learning Functions
- **`federated_learning`**: Executes federated learning using the FedAvg method. It runs over multiple rounds, updating the global model after each round.
- **`federated_learning_fedprox`**: Executes federated learning using the FedProx method, which includes a proximal term to penalize model deviations from the global model.

### 6. Evaluation (`evaluate_global_model`)
This function evaluates the performance of the global model on the MNIST test dataset and returns the accuracy.



