This project implements brain tumor detection from MRI images using the VGG19 convolutional neural network architecture through transfer learning. The system is built with Keras and trained on the publicly available brain tumor MRI dataset from Kaggle.
📌 Overview
Uses the VGG19 model pretrained on ImageNet as a base

Custom fully connected layers added on top for binary classification (Tumor / No Tumor)

Dataset: Kaggle Brain MRI Dataset by Navoneel

Built and tested in Google Colab using TensorFlow, Keras, OpenCV, and Matplotlib

Prediction results are visualized with the original MRI scan

🛠 Technologies Used
Python

TensorFlow & Keras

VGG19 (pretrained model)

Scikit-learn

OpenCV

Matplotlib

Kaggle API

🧪 Steps Performed
Dataset Setup

Downloaded via Kaggle API

MRI images categorized into yes (tumor) and no (non-tumor)

Image Preprocessing

Resized images to 224x224 (required input size for VGG19)

Encoded labels using LabelEncoder

One-hot encoded for binary classification

Model Architecture

Base: VGG19 without top layers (include_top=False)

Custom head: GlobalAveragePooling2D → Dense layers → Softmax output

All VGG19 layers frozen to use pretrained features

Training

Adam optimizer with categorical crossentropy

Trained for 20 epochs with validation split

Prediction

Given an MRI image, the model classifies it as Tumor or No Tumor

Visualization of prediction results with matplotlib

✅ Future Enhancements
Implement fine-tuning of VGG19 layers for improved accuracy

Use Grad-CAM for tumor region visualization

Deploy model with Streamlit or Flask

📌 Credits
Dataset: Navoneel Brain MRI Dataset on Kaggle

VGG19: Visual Geometry Group, Oxford

