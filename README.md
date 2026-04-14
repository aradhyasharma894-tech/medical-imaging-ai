#  Pneumonia Detection Using Deep Learning

##  Overview

This project focuses on detecting pneumonia from chest X-ray images using deep learning techniques. A baseline CNN model and a transfer learning approach using ResNet18 are implemented and compared to evaluate performance improvements.

---

##  Problem Statement

Pneumonia is a life-threatening disease that requires early and accurate diagnosis. Manual analysis of X-ray images is time-consuming and prone to human error. This project aims to develop an automated system to classify chest X-rays as **Normal** or **Pneumonia**.

---

##  Dataset

* Source: Chest X-ray dataset (Kaggle)
* Total images: ~5800
* Classes:

  * NORMAL (1341 images)
  * PNEUMONIA (3875 images)
  * Class Counts: Counter({1: 3875, 0: 1341})
Class Weights: [3.889634601043997, 1.3460645161290323]

---

##  Methodology

### 🔹 Data Preprocessing

* Resized images to 224×224
* Applied normalization using ImageNet values
* Data augmentation:

  * Horizontal Flip
  * Rotation
  * Brightness & Contrast adjustment

---

### 🔹 Models Used

#### 1. Baseline CNN

* Built from scratch
* Used for performance comparison

#### 2. Transfer Learning (ResNet18)

* Pretrained on ImageNet
* Final layer modified for binary classification
* Achieved higher accuracy

---

### 🔹 Handling Class Imbalance

* Class weights used:

  * NORMAL: 3.88
  * PNEUMONIA: 1.34
* Helps reduce bias toward majority class

---

##  Training Details

* Loss Function: CrossEntropyLoss
* Optimizer: AdamW
* Learning Rate: 0.0003
* Epochs: 5
* Batch Size: 32

---

##  Results

| Model    | Accuracy |
| -------- | -------- |
| CNN      | ~79.8%   |
| ResNet18 | ~90.06%  |

* Training loss decreased steadily
* Validation accuracy stabilized around 94%

---

##  Observations

* Transfer learning significantly improved performance
* Data augmentation improved generalization
* Class weights reduced bias
* Slight overfitting observed at later epochs

---

##  Conclusion

The project demonstrates that transfer learning is highly effective for medical image classification, especially with limited data. The model can assist in early pneumonia detection.

---

##  Future Work

* Use larger datasets
* Apply advanced models (DenseNet, EfficientNet)
* Add explainable AI (Grad-CAM)
* Build real-time web application

---

##  Tech Stack

* Python
* PyTorch
* Torchvision
* Matplotlib
* Scikit-learn

---

##  Author

Aradhya Sharma
