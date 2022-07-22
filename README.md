# Using Lung ultrasound images for building a reliable Point-of-care COVID-19 testing system

<div align = 'center'>

![antibodies-medium](https://user-images.githubusercontent.com/86565759/180339435-94d68b97-7239-4b33-833e-e7b654dc82a1.png)

</div>

## Table of Contents

1. [About the project](https://github.com/Sanketb77/Point-of-care-COVID_detection/edit/main/README.md#about-the-project)
2. [Pre-requisites](https://github.com/Sanketb77/Point-of-care-COVID_detection/edit/main/README.md#pre-requisites)
3. [Dataset](https://github.com/Sanketb77/Point-of-care-COVID_detection/edit/main/README.md#dataset)
4. [Roadmap](https://github.com/Sanketb77/Point-of-care-COVID_detection/edit/main/README.md#roadmap)
5. [Results and Discussion](https://github.com/Sanketb77/Point-of-care-COVID_detection/edit/main/README.md#results-and-discussion)


<img align="left" width="60" height="60" src = https://user-images.githubusercontent.com/86565759/180340694-dcfa2013-6d04-4cbc-a5ff-ff99ea3f864f.jpeg >

## About the Project

This project aims to develop a quick and reliable Point-of-care Covid diagnosis system that returns the results instantly.A machine learning based diagnosis system can be developed that classifies patients into right category of results – Positive or Negative using their lung ultrasound images. Such a model would help the healthcare professionals by saving a great deal of their time as the classification model would return the results momentarily. Moreover, the final deployed model’s promising accuracy would save the trouble of conducting a series of follow up tests. The solution would change the clinical decision support as this would not only save care providers and patients from unnecessary delays and waiting times but will also enable healthcare professionals to take the necessary actions timely.


<div align = 'center'>

<img width="944" alt="Screenshot 2022-07-21 at 9 04 19 PM" src="https://user-images.githubusercontent.com/86565759/180339853-9d230d63-84db-47bd-b702-a2764665b27c.png">

</div>

The goal is compare and evaluate the performance of different convolutional neural networks in combination with Transfer learning and other approaches for choosing a highly accurate model for deployment.

<img align="left" width="40" height="40" src=https://user-images.githubusercontent.com/86565759/180341113-b84cb9df-48d7-47f5-bfa9-ee582e1f1d7c.png>

## Pre-requisites
The following open source packages have been used in the project :

* Numpy
* Pandas
* Scikit-Learn
* Tensorflow
* Keras
* Sklearn
* Seaborn
* Matplotlib
* Imbalanced-Learn

<img align="left" width="60" height="60" src= https://user-images.githubusercontent.com/86565759/180341438-e48f955c-f57c-412d-a11b-c3715e0f8fa0.png>

## Dataset
COVIDx-US is an open access benchmark dataset of ultrasound imaging related to COVID-19. 192 lung ultrasound videos and 18,628 images have been extracted from 8 sources - GrepMed (20 videos) , PocusAtlas (32 videos), Clarius (6 videos) , LITFL (63 videos), CoreUltrasound (18 videos) , Radiopaedia (5 videos), Papers (22 videos), UF (26 videos).The videos have been captured with either of the two probes - Convex or Linear.The images belong to four classes namely Covid, Normal, Pneumonia and Other.

The following table contains the image distribution by class -
<div align="center">
  
Class | Number of Images 
:---: | :---: 
COVID | 4003
Normal | 2201
Pneumonia | 4449
Other | 7975
  


<img width="839" alt="Screenshot 2022-07-21 at 3 58 18 PM" src="https://user-images.githubusercontent.com/86565759/180304457-718d7844-aadf-48aa-9647-882d79217a9f.png">
  
</div>



*The COVIDx-US dataset details can be found at [here](https://github.com/nrc-cnrc/COVID-US)*

<img align="left" width="60" height="60" src= https://user-images.githubusercontent.com/86565759/180341674-a136fb61-a24d-45a0-8cd7-ba38e246b914.png>

## Roadmap

Binary and Multi classifiers have been used for the classification purpose after pre-processing the image dataset. Data preprocessing includes resizing the images to handle dimension variability, normalizing pixel values, removing the duplicate images from each class and storing the images in RGB format. The binary classifiers take two classes into consideration : COVID and Non-Covid. However, the multi classifiers works with all the four classes.

<img align="left" width="60" height="60" src= https://user-images.githubusercontent.com/86565759/180341784-34ef882d-c8ce-41ae-bec1-d21619046795.jpg>

## Results and Discussion

The machine learning models used for both kinds of classifiers along with the performance metrics are shown in the following tables. ResNet50V2 turned out to be the best binary classifier as per it's prediction performance. Whereas, Xception outperformed all models for four class classification.

<div align = "center">


<img width="942" alt="Screenshot 2022-07-21 at 4 05 12 PM" src="https://user-images.githubusercontent.com/86565759/180305688-3355e09d-f62b-464e-8b9e-8478350ce073.png">

</div>


Finally, Xception model has been deployed as a web application using Streamlit. The application allows user to upload the images and it correctly predicts it's class.







