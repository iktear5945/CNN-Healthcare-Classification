# Problem Set 01 - Pneumonia Detection Using CNN

## 1. Problem Statement

The objective of this project is to develop a Convolutional Neural Network (CNN) model to classify chest X-ray images into two categories: Normal and Pneumonia.

The model is trained using pediatric chest X-ray images and evaluated using a separate test dataset.

## 2. Dataset

The dataset contains chest X-ray images categorized into:

- Normal
- Pneumonia

The dataset is divided into three subsets:

- Training set
- Validation set
- Test set

### Dataset Distribution

| Dataset | Normal | Pneumonia | Total |
|---|---:|---:|---:|
| Train | 1341 | 3881 | 5222 |
| Validation | 8 | 8 | 16 |
| Test | 244 | 390 | 634 |

## 3. Objective

The main objective is to build a CNN model that can automatically classify chest X-ray images as either Normal or Pneumonia.

## 4. Methodology

The project follows these steps:

1. Load the dataset from Google Drive.
2. Explore and visualize sample X-ray images.
3. Resize images to 150 × 150 pixels.
4. Normalize pixel values from 0-255 to 0-1.
5. Apply data augmentation to the training images.
6. Build a CNN model.
7. Train the model using the training dataset.
8. Evaluate the model using the test dataset.
9. Generate a confusion matrix and classification report.
10. Test the model on individual X-ray images.

## 5. Data Preprocessing

All images were resized to 150 × 150 pixels.

Pixel values were normalized using:

1/255

Data augmentation was applied to the training data using rotation, zoom, width shift, height shift, and horizontal flip.

## 6. CNN Architecture

The CNN model contains:

- Three convolutional layers
- Three max-pooling layers
- One flatten layer
- One dense layer with 128 neurons
- Dropout layer with 0.5 dropout rate
- One sigmoid output layer

The output layer performs binary classification:

- 0 = Normal
- 1 = Pneumonia

## 7. Model Training

The model was compiled using:

- Optimizer: Adam
- Loss Function: Binary Crossentropy
- Evaluation Metric: Accuracy
- Epochs: 10
- Batch Size: 32

## 8. Results

The model achieved:

- Test Accuracy: 76.97%
- Test Loss: 0.7260

### Classification Report

| Class | Precision | Recall | F1-Score |
|---|---:|---:|---:|
| Normal | 0.95 | 0.43 | 0.59 |
| Pneumonia | 0.73 | 0.98 | 0.84 |

## 9. Confusion Matrix

The confusion matrix shows that:

- 104 Normal images were correctly classified.
- 140 Normal images were classified as Pneumonia.
- 6 Pneumonia images were classified as Normal.
- 384 Pneumonia images were correctly classified.

## 10. Findings

The model achieved an overall test accuracy of 76.97%.

The model performed particularly well in detecting Pneumonia, achieving a recall of 98%. However, the recall for Normal images was lower at 43%, meaning that a considerable number of Normal images were incorrectly classified as Pneumonia.

## 11. Conclusion

A CNN-based model was successfully developed for classifying pediatric chest X-ray images into Normal and Pneumonia categories.

The model achieved 76.97% test accuracy and showed strong sensitivity toward Pneumonia cases. Further improvements could be achieved through a larger validation set, hyperparameter tuning, class balancing, and transfer learning using pretrained CNN architectures.
