# PyTorch-MNIST-digit-recognition-model

This code trains a fully connected neural network using PyTorch on the MNIST dataset to recognize handwritten digits (0–9).

# Imports
![image](https://github.com/user-attachments/assets/3f748490-1228-4a07-8dc1-48fb8ab291d4)

Imports PyTorch, neural network tools, data loading utilities, and dataset + transformation tools.

# Downloading and Transforming the MNIST Dataset
![image](https://github.com/user-attachments/assets/47eb0517-2763-46b9-86ea-d07c42180963)

Downloads the MNIST dataset (handwritten digits).

Converts the 28×28 grayscale images into normalized PyTorch tensors (values between 0 and 1).

# Data Loaders
![image](https://github.com/user-attachments/assets/6b0a717c-a21c-40cd-acbf-3ebff3edb3e6)

Prepares batches of data (64 images per batch) for efficient training and testing.

# Data Inspection
![image](https://github.com/user-attachments/assets/e3a0b6e6-9758-4db2-9a84-b371cf5e0426)

Confirms dataset sizes and inspects shape of image tensors.

X shape: [64, 1, 28, 28] → 64 images, 1 channel, 28×28 size.


