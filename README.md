# deep-learning-image-classification: Facial Recognition using CNN and MTCNN

## Overview
This project demonstrates the implementation of a deep learning pipeline for image classification and face recognition using Convolutional Neural Networks (CNN) and Multi-task Cascaded Convolutional Networks (MTCNN). It is designed to detect human faces in images, preprocess the input data, train a custom CNN model for classification, and visualize the results.

## Features
Facial Detection: Detect faces in an input image using MTCNN.
Facial Recognition: Classify detected faces using a custom CNN model architecture.
Visualization: Display processed images with recognized faces highlighted with bounding boxes.

## Requirements
This project is designed to run on Google Colab. To ensure compatibility and ease of execution, the following Python libraries are required:

- tensorflow (Deep Learning frameworks)
- opencv-python (Image-processing library)
- mtcnn (Face detection module)
- matplotlib (Visualization library)
Install these dependencies using the following command:

!pip install tensorflow opencv-python mtcnn

## Code Overview
### 1. Data Preprocessing
Resize input images to 150x150 pixels.
Normalize pixel values to the range [0, 1].
### 2. CNN Model Architecture
The CNN model includes:

- Convolutional Layers: Extract features from images.
- Max Pooling Layers: Reduce spatial dimensions and focus on essential features.
- Dense Layers: Fully connected layers for classification.
- Output Layer: Binary classification using sigmoid activation.
Model compilation:

Optimizer: Adam
- Loss Function: Binary Crossentropy
- Metric: Accuracy
### 3. Facial Recognition Logic
Utilize MTCNN to detect faces in the input images.
Pass each detected face through the CNN model for recognition.
Display results by drawing bounding boxes on detected faces.

## How to Run
### 1.Mount Google Drive:
from google.colab import drive
drive.mount('/content/drive')
### 2.Navigate to the correct directory:
cd /content/drive/MyDrive/DM
### 3.Install dependencies:
!pip install tensorflow opencv-python mtcnn
### 4. Upload an image file for facial detection and recognition:
from google.colab import files
uploaded = files.upload()
### 5. Execute face detection and recognition:
detect_and_recognize_faces(img_path, cnn_model)

## Results
After execution, the system outputs:
- Probability scores from the CNN model for face recognition.
- Visualizations of images with bounding boxes around detected faces.
Below is an example output showing detection and recognition:
<img width="449" height="299" alt="image" src="https://github.com/user-attachments/assets/c13cf1d9-b88a-4e17-81e6-a376cf8dfa5f" />

## Repository Structure
.
├── DEEP_LEARNING_Code_in_facial_recognition.ipynb  # Main code
├── example_output.png                              # Example result visualization
└── README.md                                       # Project documentation

