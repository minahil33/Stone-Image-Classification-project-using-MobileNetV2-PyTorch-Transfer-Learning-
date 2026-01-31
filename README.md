Stone Image Classification using MobileNetV2 (PyTorch)
Overview

This project is an image classification system built using PyTorch and MobileNetV2 with transfer learning. A pretrained MobileNetV2 model (trained on ImageNet) is used, where the backbone network is frozen and only the classifier head is trained on a custom stone image dataset to improve efficiency and accuracy.

Features

Pretrained MobileNetV2 model
Transfer learning with frozen backbone
Custom classifier head
Train / validation split
GPU support (CUDA if available)
Accuracy and loss tracking
Evaluation on test dataset

Model Architecture

Base Model: MobileNetV2 (ImageNet weights)
Input Size: 224 × 224 RGB images
Classifier: Fully connected layer customized for dataset classes
Loss Function: CrossEntropyLoss
Optimizer: Adam

Dataset Structure

The dataset should be organized as follows:
dataset/
├── train/
│   ├── class_1/
│   ├── class_2/
│   └── ...
└── test/
    ├── class_1/
    ├── class_2/
    └── ...
Each class directory should contain its corresponding images.

Data Preprocessing

Resize images to 224 × 224
Convert images to tensors
Normalize using ImageNet mean and standard deviation

Installation & Requirements
Requirements

Python 3.8+
PyTorch
torchvision
matplotlib
numpy

Install Dependencies

pip install torch torchvision matplotlib numpy

Training Strategy

80% training data
20% validation data
Backbone frozen for faster convergence
Only classifier parameters are trainable

Device Support

The code automatically detects:

GPU (CUDA) if available
Otherwise defaults to CPU

Results

The model demonstrates stable convergence with improving training and validation accuracy while reducing loss, indicating effective use of transfer learning.

Future Improvements

Fine-tune deeper layers of MobileNetV2
Add data augmentation
Implement early stopping
Save and load trained model
Add confusion matrix and per-class accuracy


Author

Minahil
BS Artificial Intelligence Student
