# covid19-xray-vgg19-densenet201-ensemble
This project classifies chest X-ray images into four classes—COVID-19, Lung Opacity, Normal, and Viral Pneumonia—using VGG19, DenseNet201, and an ensemble model. Images were preprocessed using bilateral filtering and CLAHE to improve quality and enhance model performance.

# COVID-19 Chest X-ray Classification Using Deep Learning

## Project Overview
This project focuses on **automated four-class classification of chest X-ray images** using deep convolutional neural networks. The four classes are:

- COVID-19  
- Lung Opacity  
- Normal  
- Viral Pneumonia  

The dataset used is the publicly available **COVID-19 Radiography Database**. A subset of **2,000 images per class** was selected for this project. Only the raw X-ray images were used; lung masks were excluded.

A **preprocessing pipeline** was applied to enhance image quality and stability for deep learning models, including:

- **Bilateral filtering** for noise reduction  
- **CLAHE (Contrast Limited Adaptive Histogram Equalization)** for contrast enhancement

---

## Models Implemented
Four notebooks implement different stages of the project:

1. **01_preprocessing.ipynb** – Data loading, denoising, enhancement, and train-test splitting  
2. **02_vgg19_model.ipynb** – Fine-tuned VGG19 model using ImageNet weights  
3. **03_densenet201_model.ipynb** – Fine-tuned DenseNet201 model using ImageNet weights  
4. **04_ensemble_model.ipynb** – Ensemble of VGG19 and DenseNet201 for improved performance

---

## Results
Training curves, loss plots, confusion matrices, and ROC curves for each model are included in the **results/** folder.  

- VGG19, DenseNet201, and ensemble models are evaluated and compared using:  
  - Accuracy  
  - Loss  
  - Confusion matrix  
  - ROC Curves

These outputs allow full analysis of model behavior and performance.

---

## Repository Structure
covid19-xray-project/
├─ notebooks/
│ ├─ 01_preprocessing.ipynb
│ ├─ 02_vgg19_model.ipynb
│ ├─ 03_densenet201_model.ipynb
│ └─ 04_ensemble_model.ipynb
├─ results/ # Accuracy/loss plots and confusion matrices
├─ requirements.txt # Python dependencies
├─ .gitignore # Ignore unnecessary files
├─ README.md # Project description


---

## Installation
```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd covid19-xray-project
pip install -r requirements.txt

Usage
Open notebooks in Google Colab or locally.
Run 01_preprocessing.ipynb to prepare data.
Run 02_vgg19_model.ipynb or 03_densenet201_model.ipynb to train and evaluate models.
Run 04_ensemble_model.ipynb to see ensemble performance.
View all plots and confusion matrices in the results/ folder.

Acknowledgments
COVID-19 Radiography Database
TensorFlow and Keras libraries for deep learning
OpenCV for image preprocessing
