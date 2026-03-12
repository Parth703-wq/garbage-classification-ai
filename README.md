# Garbage-classification-ai


# AI Garbage Classification System

Deep learning based image classification system that automatically identifies different categories of waste using a convolutional neural network.

## Overview

Waste sorting is critical for efficient recycling. This project uses **transfer learning with MobileNetV2** to classify garbage images into different waste categories.

The model is trained using TensorFlow/Keras with data augmentation and fine-tuning to improve classification performance.

## Features

* Image based waste classification
* Transfer learning using MobileNetV2
* Data augmentation
* Class imbalance handling using class weights
* Early stopping and learning rate scheduling
* Confusion matrix visualization
* Training performance graphs

## Model Architecture

Base Model:
MobileNetV2 (pretrained on ImageNet)

Custom Layers:

* GlobalAveragePooling2D
* Dense(256) + Dropout
* Dense(128) + Dropout
* Softmax Output Layer

Input Size:
224 × 224 RGB images

Optimizer:
AdamW

Loss Function:
Categorical Crossentropy

## Dataset

Dataset contains labeled images of different types of garbage.

Example classes:

* cardboard
* glass
* metal
* paper
* plastic
* trash

Dataset structure:

dataset/
├── cardboard
├── glass
├── metal
├── paper
├── plastic
└── trash

## Training

Training uses:

* ImageDataGenerator augmentation
* Class balancing
* Early stopping
* Learning rate reduction
* Model checkpointing

Epochs: 25
Batch Size: 32
Image Size: 224 × 224

## Evaluation

Model performance is evaluated using:

* Classification report
* Confusion matrix
* Training accuracy and loss curves

## Installation

Clone repository

git clone https://github.com/Parth703-wq/garbage-classification-ai.git

cd garbage-classification-ai

Install dependencies

pip install -r requirements.txt

## Run Training

python src/train.py

## Model Output

The trained model is saved as:

models/final_trash.keras

## Results

Training outputs:

* Confusion matrix
* Accuracy vs epochs plot
* Loss vs epochs plot

## Technologies Used

* Python
* TensorFlow / Keras
* MobileNetV2
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## Future Improvements

* Real-time garbage detection using camera
* Mobile application integration
* Waste detection with bounding boxes
* Deployment with API


