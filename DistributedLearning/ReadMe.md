# Code Overview and Results

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

---

This format is clean, easy to read, and well-suited for a GitHub `README.md` file. Let me know if you need further adjustments!
