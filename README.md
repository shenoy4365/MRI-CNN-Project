# Brain Tumor Detection and Localization Using Deep Learning

## Problem Statement

In the rapidly evolving healthcare landscape, Artificial Intelligence (AI) is playing a pivotal role in transforming medical diagnosis and treatment. This project focuses on leveraging deep learning techniques to enhance the speed and accuracy of detecting and localizing brain tumors in MRI scans. The primary goal is to build a robust AI model capable of automating the detection and localization process, aiding medical professionals in early diagnosis and improving patient outcomes.

## Key Objectives

The primary objectives of this project are:

- **Detection of Brain Tumors:** Develop a deep learning model to detect the presence or absence of brain tumors in MRI scans.
- **Localization of Tumors:** Use segmentation techniques to localize the tumor, providing a detailed mask of the affected region.
- **Model Robustness:** Ensure that the model is efficient, accurate, and scalable by leveraging the power of modern deep learning architectures.

### Dataset Overview
- **Dataset Size:** 3929 annotated brain MRI scans.
- **Annotations:** Each MRI scan is labeled with the location of the tumor.

## Solution Architecture

The solution comprises two primary deep learning components to tackle both detection and localization:

### 1. **ResNet Deep Learning Classifier Model**
The classification model is based on **Residual Neural Networks (ResNet)**. ResNet's residual learning mechanism helps address the vanishing gradient problem, allowing for effective training of very deep networks. This model classifies MRI scans into two categories: 
- Tumor present
- No tumor present

### 2. **ResUNet Segmentation Model**
The segmentation model is built using the **ResUNet** architecture, an extension of U-Net with residual connections. ResUNet is particularly effective for pixel-level segmentation tasks, enabling detailed localization of tumors. This model outputs a binary mask indicating the precise location of the tumor in each MRI scan.

## Transfer Learning

To accelerate model training and improve accuracy, **transfer learning** is employed. A pre-trained **ResNet model** is fine-tuned on our dataset. Transfer learning enables the model to leverage learned features from large-scale datasets (e.g., ImageNet), drastically reducing the time required to train and improving performance, especially with smaller datasets (~4000 images) like ours.
