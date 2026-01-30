---
title: Face Recognition
date: 2024/1/31
description: Developed a deep learning solution to detect and recognize faces in real-time using live video feeds. Built a robust data pipeline for training and validation, implementing multiple deep learning architectures to optimize detection accuracy.
author: Adham Arif
---

# Image Recommender
A deep learning project to explore the use of neural network and autoencoder network architecture to train and 
distinguish between known and unknown faces.

🔗 [Link to GitHub repository](https://github.com/adhamarif/face-recognition)


## Architecture
Below are the overview of the code architecture of the project. More details are available in the code repository.

**Autoencoder architecture:**
![image](https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/AE.png?raw=true)

**Neural network architecture:**
![image](https://github.com/adhamarif/face-recognition/raw/main/readme_graphics/Network%20Architecture.PNG)

## Datasets
This project used images datasets collected from the DAISY peers at HSD on 2023.

## Image Preprocessing
- Preprocess the image using **opencv** to prepare the images for the training dataset.
- Prepare data augmentation to enrich the images datasets with different criteria (rotation, different colour scale, horizontal flip)
- Label the image datasets by locating it to different folder.

### Result
**CNN** results with known faces within the dataset :

<img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/Kenny%20-%20Detected.PNG" width="360" height="360"> <img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/Dennis%20-%20Detected.PNG" width="360" height="360">

**CNN** results with random unknown faces from the internet :

<img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/MJ%20-%20Undetected.PNG" width="360" height="360"> <img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/Son%20-%20Undetected.PNG" width="360" height="360">

**Autoencoder** results with known faces within the dataset :

 <img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/AE-detected.jpg" width="360" height="360"> <img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/Syahid%20AE%20-%20Detected.PNG" width="360" height="360">
 
**Autoencoder** results with unknown faces from the internet :

 <img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/Jon%20AE%20-%20Undetected.PNG" width="360" height="360"> <img src="https://github.com/adhamarif/face-recognition/blob/main/readme_graphics/Messi%20AE%20-%20Undetected.PNG" width="360" height="360">
