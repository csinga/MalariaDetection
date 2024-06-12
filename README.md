# Malaria Detection based on the domain - Deep Learning

## Problem Definition

The goal of this project is to create a robust automated system capable of classifying red blood cells in microscopic images as either infected with malaria (parasitized) or not (uninfected). This system aims to alleviate the challenges of traditional diagnostic methods, which require manual examination by skilled professionals, are time-consuming, and subject to human error due to variability in expert interpretation.

### Context

Malaria detection is crucial due to the disease's high prevalence and mortality rate, particularly among young children. Traditional manual diagnosis is labor-intensive and subject to human error, potentially leading to misdiagnosis and delays in treatment that can result in severe health consequences or fatality. An automated system could significantly reduce these risks by providing rapid and accurate diagnoses.

### Objectives

- Build a computer vision model that can distinguish between parasitized and uninfected red blood cells from microscopic images.
- Provide high diagnostic accuracy to support healthcare professionals in making informed decisions quickly, improving patient outcomes, and optimizing the use of medical resources.

### Key Questions

1. How can we ensure the model generalizes well to new, unseen data?
2. What features most accurately signify malaria infection in blood cells?
3. How can the model's performance be balanced between precision and recall to minimize the impact of false negatives and positives?

## Data Description

- **Parasitized**: Contains the Plasmodium parasite which causes malaria.
- **Uninfected**: Free of the Plasmodium parasites.

The images have been preprocessed to ensure uniform size and converted to 4D arrays suitable for input into a convolutional neural network. Labels have been created for both types of images for training and testing the model.

- **Training images shape**: (24957, 64, 64, 3)
- **Test images shape**: (2600, 64, 64, 3)
- **Training images pixel range**: 0 - 255
- **Testing images pixel range**: 0 - 255

## Models Used

### Deep Learning Models

1. **Model 1**: Basic Convolutional Neural Network (CNN)
2. **Model 2**: CNN with Batch Normalization
3. **Model 3**: CNN with Data Augmentation
4. **Model 4**: Pre-trained model (VGG16)

## Visualization and Evaluation Metrics

- **Accuracy**: Measures the overall correctness of the model.
- **Precision**: Measures the accuracy of the positive predictions.
- **Recall**: Measures the ability of the model to find all relevant cases.
- **F1 Score**: Harmonic mean of precision and recall.
- **Confusion Matrix**: Visual representation of the model's performance.

## Usage

Clone the repository:
git clone https://github.com/csinga/MalariaDetection.git
cd MalariaDetection

## Install dependencies:

pip install -r requirements.txt

## Repository Structure

```plaintext
MalariaDetection/
├── data/
│   ├── train/
│   │   ├── parasitized/
│   │   └── uninfected/
│   └── test/
│       ├── parasitized/
│       └── uninfected/
├── models/
│   ├── model1_basic_cnn.ipynb
│   ├── model2_batch_norm.ipynb
│   ├── model3_data_augmentation.ipynb
│   └── model4_vgg16.ipynb
├── notebooks/
│   ├── data_preprocessing.ipynb
│   ├── exploratory_data_analysis.ipynb
│   └── model_training_evaluation.ipynb
├── utils/
│   ├── data_loader.ipynb
│   ├── image_preprocessing.ipynb
│   └── evaluation_metrics.ipynb
├── README.md
├── requirements.txt
└── .gitignore
