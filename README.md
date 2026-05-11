This documentation describes the typical structure and purpose of the **Rock-Paper-Scissor-Classifier-V2** project by **themehmi**. Projects of this nature in this repository are standard machine learning classification tasks focused on computer vision.

---

# 🖐️ Rock-Paper-Scissor-Classifier-V2 Documentation

## 1. Project Overview

**Rock-Paper-Scissor-Classifier-V2** is a computer vision project designed to classify images of hand gestures into three categories: **Rock**, **Paper**, or **Scissors**. This project is built to demonstrate the capabilities of Deep Learning, specifically Convolutional Neural Networks (CNNs), in image recognition.

## 2. Key Features

* **Image Classification:** Recognizes and classifies static hand gesture images.
* **Deep Learning Architecture:** Utilizes Convolutional Neural Networks (CNN) to extract spatial features from images.
* **Automated Preprocessing:** Includes steps for resizing images, normalizing pixel values, and data augmentation.
* **Performance Visualization:** Generates plots for training/validation accuracy and loss to monitor model convergence.

## 3. Technology Stack

* **Python:** The core programming language.
* **TensorFlow/Keras:** The primary deep learning framework for building and training the model.
* **Matplotlib/Seaborn:** Used for visualizing training metrics and image data.
* **NumPy:** Used for array manipulations required by image data.

## 4. Workflow

The typical pipeline for this classifier follows these stages:

1. **Dataset Preparation:**
* Images are organized into subdirectories (e.g., `train/rock`, `train/paper`, `train/scissors`).
* Data is loaded using `ImageDataGenerator` for efficient batching.


2. **Data Augmentation:**
* Techniques like rotation, zooming, and horizontal flipping are applied to prevent overfitting and improve model generalization.


3. **Model Architecture:**
* Sequential model containing **Conv2D** layers for feature detection.
* **MaxPooling2D** layers to downsample the image.
* **Flatten** and **Dense** layers for classification.


4. **Training:** The model is compiled with an optimizer (e.g., RMSprop or Adam) and trained over multiple epochs.
5. **Evaluation:** Performance is tested against a validation set to ensure accuracy on unseen data.

## 5. Getting Started

### Requirements

You will need a Python environment with the following libraries:

```bash
pip install tensorflow matplotlib numpy

```

### Typical Usage

The project usually contains a Jupyter Notebook or a Python script. To run the training:

1. **Configure Paths:** Point the script to your training and validation image directories.
2. **Initialize the Model:** Load the architecture defined in the script.
3. **Train:** Run the training loop to save the model.
4. **Predict:** Use the `model.predict()` function to classify a new, single image.

## 6. Model Evaluation

Success is measured by:

* **Accuracy Score:** The percentage of gestures correctly predicted.
* **Loss Curves:** Tracking how quickly the model minimizes error during training.
* **Confusion Matrix:** A visual representation to see if the model confuses specific classes (e.g., mistaking Rock for Paper).

---

### 📂 Typical Repository Structure

* `dataset/`: Folder containing the training and validation imagery.
* `model.h5`: (Optional) The saved trained neural network model.
* `classifier.ipynb` / `train.py`: Main executable file for training the model.
* `requirements.txt`: List of dependencies.

> **Note:** If you are using this for a course (like Dicoding or similar platforms), ensure your directory structure matches the code exactly, as these scripts often rely on relative paths for data loading.
