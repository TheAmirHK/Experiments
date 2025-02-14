# What is distributed learning
Distributed learning refers to the process of training machine learning models across multiple machines or nodes instead of a single system. This approach is used to speed up training, handle large datasets, and improve scalability. There are different types of distributed learning, including:

  -  Data Parallelism – The dataset is split across multiple machines, and each machine trains the same model on different subsets of data. The results are then aggregated.
  -  Model Parallelism – The model itself is split across different machines, with each machine handling a portion of the computations.
  -  Federated Learning – A decentralized form of distributed learning where multiple devices train a model locally and share only model updates instead of raw data.
  -  Reinforcement Learning (RL) Distributed Training – Used in reinforcement learning, where multiple agents explore an environment in parallel and share their experiences to improve learning.

## Code Overview
In DistributedLearning_HandwritingRecognition, I ran an experiment comparing normal training and distributed training of a Convolutional Neural Network (CNN) on the MNIST dataset to train a handwriting recognization model.
The goal is to demonstrate the performance and efficiency of distributed training using TensorFlow's MirroredStrategy.
### 1. Normal CNN Training
- A standard CNN model is trained on the MNIST dataset.
- **Model Architecture**:
  - Two convolutional layers with ReLU activation.
  - Max-pooling layers.
  - Fully connected layers with softmax output.
- **Training Details**:
  - Epochs: 5
  - Batch Size: 64
- **Metrics Recorded**:
  - Training time.
  - Test accuracy.

---

### 2. Distributed CNN Training
- The same model is trained using TensorFlow's `MirroredStrategy` for distributed training across multiple GPUs (if available).
- **Model Architecture** (Simplified for Distributed Training):
  - A flattening layer followed by two dense layers.
- **Training Details**:
  - Epochs: 5
  - Batch Size: 64
- **Metrics Recorded**:
  - Training time.
  - Test accuracy (compared to normal training).

---

## Key Results

| **Training Method**   | **Training Time** | **Test Accuracy** |
|------------------------|-------------------|-------------------|
| Normal Training        | ~343.63 seconds   | 99%               |
| Distributed Training   | ~31.81 seconds    | 99%               |

- Training times and accuracy may vary depending on the hardware used (e.g., CPU vs. GPU).
