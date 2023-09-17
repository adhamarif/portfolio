---
title: Pneumonia Prediction
date: 2023/7/1
description: Train a model by using deep learning and transfer learning on x-ray images to predict pneumonia disease.
tag: Python, Deep Learning, Transfer Learning
author: Adham Arif
---

# Pneumonia Prediction
Train a model by using deep learning and transfer learning on x-ray images to predict pneumonia disease.

🔗 [Link to GitHub repository](https://github.com/adhamarif/pneumonia-prediction)

## Libraries used

| **Library** | **Description** |
| ---------- | --------------------------------------------------------------------------------------------------------------------------- |
| Pandas     | Data processing and analysis |
| Tensorflow   | Deep Learning & Transfer Learning   |
| Keras  | Deep Learning & Transfer Learning   |
| Matplotlib     | Data Visualization |

## Datasets
This project used [ChestX-ray8](https://cocodataset.org/#home) dataset from Cornell University, where here have a smaller X-ray dataset containing 5856 images. Instead of 14 different diseases we will here concentrate on much fewer possible labels so that hopefully the number of images is enough to train good deep learning classifiers.

## Process

* Load the metadata and do the data cleaning and preprocessing using **Pandas**.
* Build an image generator pipeline using **Keras**.
* Build CNN model and pre-trained model by using **Keras** and **Tensorflow**. The goal is to train the X-ray image to predict pneumonia disease.
* Train both model and evaluate the results

## Results

* Both model shows high accuracy and low loss value after 10 epochs.

*CNN model*
![CNN-loss](https://github.com/adhamarif/pneumonia-prediction/assets/92054450/4bdc4c6a-0db6-464e-9dd4-634268a715f7)

*Pretrained model*
![TL-loss](https://github.com/adhamarif/pneumonia-prediction/assets/92054450/f786241f-92ed-4ee3-b05f-f050d34b226f)

* Both model have same AUC-ROC value (0.99) which shows it have higher True Positive rate and lower False Positive rate. Both models perform well to predict pneumonia.

*CNN model*
![ROC-CNN](https://github.com/adhamarif/pneumonia-prediction/assets/92054450/9f350e3e-c1a3-4a23-9a58-fada62277404)

*Pretrained model*
![ROC-TL](https://github.com/adhamarif/pneumonia-prediction/assets/92054450/68640e51-a209-4340-a578-7c32c243ea87)

## Conclusion

1. Both model show similar performance (0.99) AUC value. It shows that both model has higher True Positive rate and lower False Positive rate. Both models perform well to predict pneumonia.

2. Since custom CNN model is less complex (and has less layer) compared to the transfer learning model, it is a simple model and faster to train. The simple network layer of our CNN model can give similar performance as the transfer learning model. It is preferable to use our custom CNN model in actual prediction application, because in practice, the hardware is limitation. Hence, simpler model that deliver good performances is a good choice.