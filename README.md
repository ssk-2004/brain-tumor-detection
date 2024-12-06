# brain-tumor-detection
 A CNN-based project for detecting brain tumors from MRI scans.
 A Convolutional Neural Network (CNN)-based project for detecting brain tumors from MRI scans. This project uses Google Colab for implementation, performs data augmentation, and builds multiple CNN architectures for comparison.
 Overview
This project focuses on leveraging deep learning techniques to classify MRI scans as either benign or malignant. The objective is to create a robust, accurate, and interpretable model that aids in early detection of brain tumors.

Dataset and Preprocessing
Dataset:

The dataset is stored as folders of images in two categories: Yes (Tumor) and No (No Tumor).
Images are resized to 224x224 pixels.
Preprocessing:

Images are normalized to the range [0, 1].
Labels are extracted from folder names and one-hot encoded using LabelBinarizer.
Dataset is split into training and testing sets (90% train, 10% test).
Data Augmentation:

Rotation: 15°
Fill Mode: Nearest
Model Architectures
The project implements and compares three different CNN architectures:

Pretrained VGG16:

The VGG16 model is fine-tuned by adding custom layers on top of its convolutional base.
Top layers include Average Pooling, Flatten, Dense (ReLU), Dropout, and Dense (Softmax).
Custom CNN (Simple):

Two convolutional layers with ReLU activation followed by max-pooling layers.
Fully connected layers and a single sigmoid output for binary classification.
Custom CNN (Deeper):

Three convolutional layers followed by max-pooling.
Replaced Flatten with Global Average Pooling for reduced parameters and better generalization.

