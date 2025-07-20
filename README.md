# CNN-Based-Lung-Cancer-Identification

## Project Overview

This project implements a deep learning model to classify chest CT scan images into four categories:
- Adenocarcinoma
- Large Cell Carcinoma
- Squamous Cell Carcinoma
- Normal (no cancer)

The model uses transfer learning with the ResNet50 architecture, fine-tuned to detect and classify lung cancer types with high accuracy. This helps automate early diagnosis and supports medical professionals in making informed decisions.

## Dataset

The dataset consists of chest CT scan images organized into folders by class and split into training, testing, and validation sets. The data is not in DICOM format but as JPEG and PNG images resized to 224x224 pixels.

The four classes included are:
- Adenocarcinoma
- Large Cell Carcinoma
- Squamous Cell Carcinoma
- Normal

The data split is approximately:
- Training set: 70%
- Testing set: 20%
- Validation set: 10%

**Dataset source:**  
[Chest CT Scan Images - Kaggle](https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images/data)

## Project Structure

- `Lung_cancer_detection.ipynb` — Jupyter notebook containing full implementation including data loading, preprocessing, model building, training, and evaluation.

## Installation and Setup

1. Clone the repository:

  ```
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
  ````

2. Download the dataset from Kaggle and extract it inside the project folder as `dataset/` following the structure:

   ```
   dataset/
     train/
     test/
     valid/
   ```

## Usage

* Open and run the Jupyter notebook `Lung_cancer_detection.ipynb`.
* The notebook covers:

  * Loading and preprocessing images
  * Data visualization
  * Model creation using ResNet50 transfer learning
  * Model training and evaluation
  * Plotting classification report and confusion matrix

## Model Details

* Uses **ResNet50** pretrained on ImageNet.
* Fine-tunes the last 30 layers of ResNet50.
* Adds custom dense layers, batch normalization, dropout, and softmax output for 4-class classification.
* Trained using Adam optimizer and categorical crossentropy loss.
* Achieves high accuracy in detecting and classifying lung cancer types.

## Results

* The model provides classification metrics including precision, recall, and F1-score.
* Confusion matrix visualization helps assess per-class performance.
* Can assist healthcare professionals by automating early detection of lung cancer from CT scans.

## Acknowledgements

* Dataset provided by Mohamed Hany on Kaggle.
* Developed using TensorFlow, Keras, OpenCV, and other Python libraries.
* Inspired by medical imaging and AI research communities.

---

If you have any questions or want to contribute, feel free to open an issue or a pull request.

Thank you for checking out this project!

```
