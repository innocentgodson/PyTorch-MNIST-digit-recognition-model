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

# Model Instantiation
![image](https://github.com/user-attachments/assets/2cfda773-567c-4c0c-89ba-f3ac8ffffd78)

Creates and moves the model to the selected device.

# Loss and Optimizer
![image](https://github.com/user-attachments/assets/3414ec85-f11c-430d-a8e9-09b02c0acf2c)

CrossEntropyLoss for classification.

Adam optimizer for fast convergence.

# Training Loop
![image](https://github.com/user-attachments/assets/88f952f7-d77f-4e73-9d60-cff9f4360e74)

Loops over each batch:

Moves data to device

Makes predictions

Calculates loss

Backpropagates errors

Updates model weights

# Testing Loop
![image](https://github.com/user-attachments/assets/144f1441-16fe-4b94-adc6-fb4baf1668b3)

Evaluates model on test data:

Computes average loss and accuracy

pred.argmax(1) picks the most likely digit class

# Training Execution
![image](https://github.com/user-attachments/assets/a61353fb-9790-4f78-b388-fa29e98e1acd)

Trains the model for 5 epochs while monitoring performance.

# Saving the Model
![image](https://github.com/user-attachments/assets/746b9a82-4935-4734-ab42-e85189eda697)

Saves the trained model's weights to disk.

# Loading and Using the Model for Inference
![image](https://github.com/user-attachments/assets/0e679d12-a8ef-48e0-9b9f-50daa1afc0bd)

Loads the saved model.

Runs inference on 10 individual images from the test set.

Compares predicted and actual digits.
