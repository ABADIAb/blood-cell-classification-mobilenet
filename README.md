# Blood Cell Classification using MobileNetV3 🩸🔬

## Project Overview
An automated computer vision pipeline to classify 8 distinct types of peripheral blood cells. This project leverages **Transfer Learning** with a pre-trained **MobileNetV3Small** architecture, chosen for its efficiency in resource-constrained environments (potential for edge deployment).

## Key Features
* **Architecture:** MobileNetV3Small (Pre-trained on ImageNet) with custom top layers.
* **Data Pipeline:** * Automated download from Google Drive using `gdown`.
    * **Outlier Detection:** Statistical cleaning using **Z-Score** (threshold: 1.4) to remove anomalous images before training.
    * **Data Augmentation:** Random rotation, brightness, contrast, and translation to improve generalization.
* **Training Strategy:** Two-phase training (Feature Extraction -> Fine Tuning) with Early Stopping to prevent overfitting.

## Performance
* **Test Accuracy:** **96.57%**
* **F1-Score:** 0.9657
* *Note: The model demonstrates high precision across all 8 classes, including Erythroblasts and Platelets.*

## Tech Stack
* Python 3.x
* TensorFlow / Keras
* Scikit-learn (Metrics & Preprocessing)
* Matplotlib / Seaborn (Visualization)

## Credits
Developed as part of the Artificial Neural Networks and Deep Learning course at Politecnico di Milano.
Team members: Felipe Abadia Bermeo, Alberto Capoti, Juan Garcia.
My contribution: Focused on Outlier Detection and Data Preprocessing.
