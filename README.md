# Multimodal Biometric Recognition System

## Overview

A Computer Vision and Deep Learning project that integrates multiple biometric recognition techniques into a unified framework for identity verification and classification.

The system explores three biometric modalities:

* Face Recognition
* Fingerprint Recognition
* Signature Classification

The project was implemented in Python using OpenCV, TensorFlow/Keras, PyTorch, and image processing libraries.

## Project Objectives

* Develop computer vision models for biometric recognition.
* Compare the performance of different biometric modalities.
* Apply image preprocessing and feature extraction techniques.
* Build CNN-based classification models for fingerprint, signature, and face recognition.
* Explore the potential of combining multiple biometric modalities for more robust authentication.

## Biometric Modules

### 1. Fingerprint Classification

A CNN-based model was developed using the FVC2000 DB4 B fingerprint dataset.

The preprocessing pipeline included:

* Grayscale conversion
* Image resizing
* Pixel normalization
* Data augmentation
* CNN-based feature extraction and classification

The model used TensorFlow/Keras with convolutional, MaxPooling, and Dense layers, along with Dropout, EarlyStopping, and ModelCheckpoint to improve training stability.

### 2. Signature Classification

A CNN model was developed using the CEDAR Signature Dataset to distinguish between genuine signatures and non-signature/noise images.

The pipeline included:

* Grayscale conversion
* Image resizing
* Pixel normalization
* Label encoding
* CNN-based feature extraction
* Binary classification

The model achieved **100% accuracy on the test set** reported in the project, with no false positives or false negatives observed.

### 3. Face Recognition

A CNN-based face recognition model was developed using the **Labeled Faces in the Wild (LFW)** dataset.

The pipeline included:

* Face image preprocessing
* RGB conversion
* Image resizing and normalization
* Label encoding
* Custom PyTorch Dataset
* CNN-based classification
* Confusion matrix and classification report

The model was trained using CrossEntropyLoss, Adam optimization, DataLoader, and GPU acceleration when available.

## Technologies

* Python
* Computer Vision
* OpenCV
* TensorFlow
* Keras
* PyTorch
* Scikit-image
* NumPy
* Pandas
* Matplotlib
* Seaborn
* KaggleHub
* CNN
* Image Processing

## Results

| Modality                 | Accuracy | Avg. Processing Time |
| ------------------------ | -------: | -------------------: |
| Face Detection           |     ~95% |             ~1.2 sec |
| Fingerprint Recognition  |     ~90% |             ~1.7 sec |
| Signature Classification |      94% |             ~3.5 sec |

The project demonstrated the feasibility of combining multiple biometric modalities into a unified authentication framework. Face detection achieved approximately 95% accuracy under frontal and well-lit conditions, while fingerprint recognition achieved approximately 90% matching precision.

## Key Challenges

* Face recognition performance decreased under poor lighting conditions.
* Fingerprint preprocessing required tuning for different datasets.
* Real-time processing was limited on lower-end devices.
* The project was implemented primarily through Jupyter notebooks without a dedicated graphical interface.

## Future Improvements

* Integrate more advanced deep learning approaches such as YOLO for face detection.
* Deploy the system as a Flask or Streamlit web application.
* Expand the datasets with more diverse biometric samples.
* Improve biometric data security through encryption.
* Optimize the system for real-time deployment.

## Academic Project

Developed as a Computer Vision project under the supervision of **Dr. Ahmed Elhyek**.
