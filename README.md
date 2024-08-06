# Image Classification Based on Marvel Dataset

## Overview
This project focuses on image classification using the "Marvel Avengers" dataset. Two models were utilized: a classical model, Support Vector Machine Classifier (SVC), and a deep learning model, DenseNet201. The goal was to classify images into one of eight Marvel character labels and evaluate the models' performances, including their robustness to various perturbations.

## Models Used
1. **Support Vector Machine Classifier (SVC)**:
   - Utilized with Scale-Invariant Feature Transform (SIFT) for feature extraction.
   - Employed Bag of Visual Words (BoVW) for creating a dictionary of visual words.
   - Achieved an accuracy of 27%.

2. **DenseNet201**:
   - A Convolutional Neural Network (CNN) with 201 layers.
   - Applied to resized images (128x128) and trained using the Adam optimizer.
   - Achieved an accuracy of 49%.

## Data
The dataset consists of:
- **Training Data**: 2584 images
- **Validation Data**: 451 images
- Labels: Loki, Black Widow, Hulk, Doctor Strange, Captain America, Spider-Man, Thanos, Ironman

## Methodology
1. **Data Preparation**:
   - Cropped faces from images using OpenCV libraries.
   - Applied label encoding: Loki (0), Black Widow (1), Hulk (2), Doctor Strange (3), Captain America (4), Spider-Man (5), Thanos (6), Ironman (7).

2. **Training**:
   - **SVC**: Features extracted using SIFT, followed by BoVW.
   - **DenseNet201**: Images resized to 128x128, trained with Adam optimizer and log loss.

3. **Evaluation**:
   - Models were evaluated based on accuracy and F1-Score.
   - Perturbation tests applied to assess robustness against Gaussian noise, Gaussian blur, contrast changes, brightness changes, salt & pepper noise, and occlusion.

## Results
- **DenseNet201** performed better than SVC, with higher accuracy and better handling of perturbations.
- The label "Spider-Man" consistently showed high true positive and true negative scores, likely due to its distinct visual features.

## Limitations & Future Recommendations
- Combining classical and deep learning models could potentially yield better results.
- A larger and more balanced dataset would improve training effectiveness.
- Access to more powerful GPUs could enhance model performance by allowing the use of higher resolution images.

## Conclusion
DenseNet201 outperformed the SVC model, demonstrating the effectiveness of deep learning models for image classification tasks, especially with complex datasets like the Marvel Avengers images.
