# Lung Cancer Classification on CT-Scan Images Using an Enhanced VGG16 Model

Personal project on detection lung cancer from Chest CT Scan dataset using VGG16 with SERES and Residual Blocks.

## Overview
Lung cancer remains one of the most prevalent and deadly cancers worldwide. Early and accurate detection of lung cancer subtypes is crucial for improving patient outcomes. This project presents a deep learning-based approach for classifying chest CT-scan images into four categories:
- **Squamous Cell Carcinoma**
- **Large Cell Carcinoma**
- **Adenocarcinoma**
- **Normal**

Using a modified **VGG16 architecture** enhanced with **Squeeze-and-Excitation (SE) blocks** and **residual connections**, the model improves feature extraction and classification accuracy.

## Dataset
The dataset consists of preprocessed **chest CT-scan images**, which are divided into:
- **Training set**: 613 images
- **Validation set**: 315 images
- **Test set**: 72 images

Data augmentation techniques are applied to enhance generalization and model robustness.

## Model Architecture
- Base Model: **VGG16** (pretrained on ImageNet)
- Added **Squeeze-and-Excitation (SE) blocks** for better feature representation.
- Integrated **residual connections** to improve gradient flow.
- Fully connected layers with **Batch Normalization** and **Dropout** to reduce overfitting.
- Output Layer: **Softmax activation function** for multi-class classification.

## Performance Metrics
The model's performance is evaluated using standard classification metrics:
- **Accuracy**: 95%
- **Precision**: 94% to 99% (class-wise)
- **Recall**: 88% to 99% (class-wise)
- **F1-Score**: 93% to 96%
- **Confusion Matrix**: Shows strong classification performance across all classes.

## Training Procedure
1. Load and preprocess the dataset.
2. Apply data augmentation using `ImageDataGenerator`.
3. Build the enhanced **SERES_VGG16** model.
4. Train the model with **SGD optimizer** and **categorical crossentropy loss**.
5. Evaluate performance on the test set.
6. Generate a **confusion matrix and classification report**.

## Results
The model achieved an accuracy of **95%** on the test dataset, demonstrating high reliability in classifying lung cancer subtypes.

## Limitations and Future Work
- **Dataset size**: The dataset is relatively small, limiting the model’s generalization capability.
- **Clinical parameters**: The model does not consider genetic or other clinical factors.
- **Future improvements**:
  - Expanding the dataset for better generalization.
  - Integrating multi-modal clinical data (e.g., genetic and demographic information) for improved classification.
  - Implementing explainability techniques to enhance model interpretability for radiologists.

## Contributors
- Karunakar Cheekolu (M.Tech CSE - AI & Data Science, Christ University, Bangalore)

## Acknowledgment
This work highlights the importance of deep learning in medical image classification and contributes to the development of **automated diagnostic systems** for lung cancer detection.
