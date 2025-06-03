# PyTorch-MNIST-digit-recognition-model

This code trains a fully connected neural network using PyTorch on the MNIST dataset to recognize handwritten digits (0–9).

# Imports
![image](https://github.com/user-attachments/assets/2d9bf5f6-bfd4-4e7b-8daf-8ad36bc15402)

Imports PyTorch, neural network tools, data loading utilities, and dataset + transformation tools.

# Downloading and Transforming the MNIST Dataset
![image](https://github.com/user-attachments/assets/2bfd11b6-50b9-4612-a564-2fb7a3d53123)

Downloads the MNIST dataset (handwritten digits).

Converts the 28×28 grayscale images into normalized PyTorch tensors (values between 0 and 1).

# Data Loaders
![image](https://github.com/user-attachments/assets/9b14184c-25bb-4e25-bb59-c39497cbfd29)

Prepares batches of data (64 images per batch) for efficient training and testing.

# Data Inspection
![image](https://github.com/user-attachments/assets/d5ba0cc0-f527-4bdd-b49e-36b2f168bc31)

Confirms dataset sizes and inspects shape of image tensors.

X shape: [64, 1, 28, 28] → 64 images, 1 channel, 28×28 size.

# Device Selection
![image](https://github.com/user-attachments/assets/bd420b3d-c0e3-4008-848a-93290fa8f994)

Selects GPU (NVIDIA or Apple Silicon) if available, otherwise defaults to CPU.

# Defining the Neural Network
![image](https://github.com/user-attachments/assets/c58214ac-19f7-4981-8206-5cee7d2184bb)

A fully connected (dense) neural network with:

Input layer: 784 features (flattened 28×28 image)

2 hidden layers: 512 neurons each, ReLU activation

Output layer: 10 neurons (for 10 digit classes)
