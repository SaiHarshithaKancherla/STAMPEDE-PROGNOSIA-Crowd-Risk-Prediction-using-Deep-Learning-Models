#STAMPEDE PROGNOSIA:Crowd Risk Prediction using Deep Learning Models

---

## Project Title:STAMPEDE PROGNOSIA:Crowd Risk Prediction using Deep Learning Models

The term “Prognosia” is derived from the word prognosis, which refers to the prediction or forecasting of future conditions based on current observations. In this project, Stampede Prognosia represents the prediction of crowd risk levels by analyzing images.

## Project Overview

This project aims to develop a system that classifies crowd images into three categories: low, medium, and high risk. The system is intended to assist in crowd monitoring, safety management, and early risk detection using image-based analysis.

## Dataset Size

A total of 1,217 unlabeled crowd images were collected from various sources. These images represent different crowd scenarios with varying levels of density.

## Data Labelling

Since the dataset was initially unlabeled, an automated labeling approach was used. Three key features were extracted from each image:

 * Density: Approximate number of people present in the image.
 * Occupancy: Proportion of the area occupied by the crowd.
 * Compactness: Degree of crowd clustering

These features were combined to compute a congestion score. Based on this score:

* Images with high congestion score were labeled as high risk
* Images with low congestion score were labeled as low risk
* Images with intermediate values were labeled as medium risk

## Models Applied

The following deep learning models were implemented:

* Convolutional Neural Network (CNN)
* ResNet50
* DenseNet121
* EfficientNetB0
* InceptionV3
* VGG16
* MobileNetV2

To improve model performance, Data Augmentation techniques such as Rotation, Zooming, and Flipping were applied. Pixel normalization was also performed to scale input values.

## Evaluation Metrics

The models were evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1-score
* Cohen’s kappa

In addition, multiple train-test splits (0.2, 0.25, 0.3, and 0.4) were used to ensure consistency and robustness of the results.

## Conclusion

Among all the implemented models, VGG16 performed the best with the highest accuracy of 76.86% at a 60:40 train-test split. The corresponding evaluation metrics are as follows:

Precision: 0.776
Recall: 0.765
F1-score: 0.765
Kappa score: 0.65

These results indicate that VGG16 is effective in learning meaningful patterns from crowd images and provides balanced performance across all evaluation metrics.
