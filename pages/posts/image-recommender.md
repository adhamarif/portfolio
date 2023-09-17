---
title: Image Recommender
date: 2023/9/17
description: A big data project using transfer learning method to output a recommended image based on the similarity of characteristics
tags: big data, transfer learning
author: Adham Arif
---

# ImageRecommender
A big data project using transfer learning method to output a recommended image based on the similarity of characteristics

🔗 [Link to GitHub repository](https://github.com/adhamarif/ImageRecommender)

## Concept
Since images are large vectors with 3 colour channels, it requires high computational resources to calculate the mathematical operations such as Euclidean or Cosine distance to calculate similarity. Hence, we need to downscale its complexity but still retain the information of it, so that we can still measure the similarity of the images in their simplified form.

**Code design**:
![image](https://github.com/adhamarif/ImageRecommender/assets/92054450/ec9bfac5-abaf-499a-964e-86d6bf0f8d8d)


## Image Preprocessing
- Preprocess the imageusing **opencv** to get the colour histogram of every pixel in the images. 
- Use a transfer learning model such as **MobileNet** to get the image embeddings.
- Save the information including the image path in **SQLite** database and **.csv** file as a backup. 

## Find image similarity
- After all the images are preprocessed, the input image can be given so that it will output 5 similar images from the database in the **ImageRecommender** function. The similarity is calculated using Euclidean distance.
- Used a dimension reductional technique such as **t-SNE** or **UMAP** to visualize high dimensional data to see the clustering patterns between all images.

## Result
- **ImageRecommender** with 5 similar output images
![combi](https://github.com/adhamarif/ImageRecommender/assets/92054450/3e74281b-efca-451c-968c-4618affefd17)

- **t-SNE** plot for all the images in the database
![image](https://github.com/adhamarif/ImageRecommender/assets/92054450/23b057dd-60c7-485a-babd-74952c82f9a0)

- **t-SNE** plot for human face images vs all other istances
![image](https://github.com/adhamarif/ImageRecommender/assets/92054450/dd377835-b839-4a0a-a891-ee497d131573)