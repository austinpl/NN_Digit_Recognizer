# Neural Network Digit Recognizer
This project implements a neural network to classify handwritten digits from the MNIST dataset using PyTorch. The model is trained to recognize digits (0-9) by learning from 28x28 pixel grayscale images.

Although this is a relatively simple task, I took this opportunity to refresh my PyTorch skills and reacquaint myself with its API.

## Model Architecture
* Input Layer: 784 nodes (28x28 pixels flattened).
* Hidden Layer 1: 128 nodes, ReLU activation, Batch Normalization, Dropout (20%).
* Hidden Layer 2: 64 nodes, ReLU activation, Batch Normalization, Dropout (20%).
* Output Layer: 10 nodes, representing the digit classes (0-9).

Batch normalization and dropout are applied to each hidden layer to improve generalization. The model uses PyTorch's cross-entropy loss function, which is ideal for multi-class classification tasks, and the Adam optimizer. Training was conducted over 20 epochs.

## Output
The model produces raw logits representing the predicted probabilities for each digit. To determine the predicted digit, PyTorch's argmax function is used to identify the digit with the highest probability.

## Results
On Kaggle testing data, the model scores a 96.8% accuracy. 

## Tools
Python, Pandas, Numpy, PyTorch, Google Colab
