# Paintings_Classification

## Project Overview:
This project focuses on developing a neural network model capable of classifying paintings by identifying their respective painters. The goal is to build a reliable image classification system that can accurately predict the artist behind a given painting. The challenge lies in processing diverse artistic styles while ensuring high accuracy despite variations in brushwork, color schemes, and composition.

## Problem Description:
The task can be formulated as a supervised image classification problem. Given a dataset of paintings from multiple artists, the objective is to train a deep learning model to recognize and classify paintings based on their visual features. The chosen approach is to use a Convolutional Neural Network (CNN), which is well-suited for image classification tasks due to its ability to extract hierarchical features from images.

The project is structured into two phases:
Binary Classification: The model is first trained to distinguish between paintings by Picasso and Monet, testing its ability to differentiate between two distinct artistic styles.
Multi-Class Classification: The model is expanded to classify paintings from four artists (Monet, Picasso, Van Gogh, and Renoir), refining its predictive capabilities on a broader dataset.

Approach:
Data Collection: Images and metadata were gathered using a web-scraping algorithm from WikiArt. The images were stored in Google Drive, categorized by artist, while additional metadata was compiled into an Excel file.

Data Preprocessing:
Irrelevant images were removed.
Images were resized to consistent dimensions (210x210 and 220x220).
Images were converted into arrays and normalized for training.

Model Specification:
A CNN architecture was implemented, leveraging convolutional layers with ReLU activation and max pooling to extract features.
The binary classification model used a sigmoid activation function, while the multi-class model applied softmax activation.
The Adam optimizer and loss functions (binary cross-entropy for two painters, sparse categorical cross-entropy for four painters) were used to train the models.

Model Optimization:
Various architectures were tested, adjusting the number of convolutional layers, dense layers, and neurons.
The best-performing binary classification model had three convolutional layers, one dense output layer, and 128 neurons per layer, optimized over five epochs.
The best-performing multi-class classification model had four convolutional layers, one dense output layer, and 64 neurons per layer, optimized over six epochs.

Evaluation:
The dataset was split into training (80%), validation (30% of training), and test (20%) sets.
Accuracy and validation loss were analyzed to identify the optimal architecture and prevent overfitting.
The binary classification model achieved ~90% accuracy, while the multi-class model reached ~68% accuracy.

Conclusion:
The project demonstrated the potential of CNNs for artistic style recognition. However, challenges such as dataset imbalance and computational limitations affected the final accuracy. Future work could involve expanding the dataset, refining the model architecture, and leveraging more powerful computational resources to improve classification performance.
