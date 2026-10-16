# Traffic Sign Classification using PyTorch 🚦

A deep learning computer vision project that classifies **43 categories of German traffic signs** using a custom Convolutional Neural Network (CNN) built with PyTorch and the German Traffic Sign Recognition Benchmark (GTSRB) dataset.

This project explores image preprocessing, data augmentation, model training, evaluation, and robustness to visual variations.

## 📌 Project Overview

Traffic sign recognition is an important computer vision task for intelligent transportation systems and autonomous driving applications.

The objective of this project is to train a CNN to recognize traffic signs from images and investigate how image transformations affect classification performance.

## 📂 Dataset

**Dataset:** German Traffic Sign Recognition Benchmark (GTSRB)

- Training images: 26,640
- Test images: 12,630
- Number of classes: 43
- Image format: RGB
- Input image size: 64 × 64 pixels

The images are resized to a consistent resolution before being passed to the model.

## 🛠️ Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## 🧠 Implementation

### 1. Data Preparation

- Loaded the GTSRB dataset.
- Explored image dimensions and class labels.
- Resized images to 64 × 64 pixels.
- Converted images into PyTorch tensors.
- Normalized image channels using calculated dataset statistics.
- Prepared data loaders for model training and evaluation.

### 2. Data Augmentation

To improve generalization and explore robustness, I experimented with training-time transformations:

- **Random Rotation:** Rotations within ±10 degrees.
- **Color Jitter:** Random brightness and contrast adjustments.
- **Normalization:** Applied consistent channel-wise normalization.

These transformations introduce visual variation during training. Evaluation on transformed images helps investigate how well the model handles changes in appearance.

### 3. Model Training

A custom Convolutional Neural Network (CNN) was implemented using PyTorch.

The workflow includes:

- Forward propagation and prediction.
- Loss calculation.
- Backpropagation and gradient computation.
- Parameter optimization.
- Training and validation loss tracking.
- Training and validation accuracy tracking.

### 4. Model Evaluation

Model evaluation focuses on more than a single accuracy score.

The project investigates:

- Training and validation performance.
- Test loss and accuracy.
- Performance on transformed test images.
- Class-wise recall and potential weaknesses.
- The effect of preprocessing and data augmentation on predictions.

## 📊 Current Experimental Results

| Evaluation | Loss | Accuracy |
|---|---:|---:|
| Augmented test evaluation | 0.7268 | 84.95% |

**Important:** The result above represents evaluation on augmented test images, not the standard clean-test benchmark. It should not be interpreted as the model's clean-test accuracy.

Results may change as the training pipeline, model, and evaluation setup are refined.

## 🔍 Key Learnings

- Building an end-to-end image classification workflow with PyTorch.
- Understanding the importance of consistent training and evaluation preprocessing.
- Applying data augmentation to introduce visual variation.
- Monitoring training and validation metrics.
- Investigating class-wise recall rather than relying solely on overall accuracy.
- Evaluating how image transformations affect model performance.

## 🚀 Future Improvements

- Compare clean-test and augmented-test performance using the same trained model.
- Analyze a confusion matrix and per-class precision, recall, and F1-score.
- Investigate classes with lower recall.
- Experiment with CNN architecture and hyperparameter improvements.
- Explore transfer learning with pretrained vision models.
- Save and document the best-performing model.

## 📁 Project Structure

```text
traffic-sign-classification-with-pytorch/
├──traffic_sign_classification_with_pytorch.ipynb
├── README.md
```
## 🎯 Project Goal

This project is part of my ongoing learning journey in **Deep Learning, Computer Vision, and PyTorch**, with a focus on building practical machine learning projects and understanding model performance through experimentation.

## 📚 Dataset Reference

German Traffic Sign Recognition Benchmark (GTSRB).

