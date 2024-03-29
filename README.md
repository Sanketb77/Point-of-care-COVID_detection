<div align = 'center'>

# Using Lung ultrasound images for building a reliable Point-of-care COVID-19 testing system

</div>

<div align = 'center'>

![antibodies-medium](https://user-images.githubusercontent.com/86565759/180339435-94d68b97-7239-4b33-833e-e7b654dc82a1.png)

</div>

<img align="left" width="40" height="40" src = https://user-images.githubusercontent.com/86565759/180346595-fc1b1854-37cf-487a-8b2a-e96a4f410788.png >

## Table of Contents

1. [About the project](https://github.com/Sanketb77/Point-of-care-COVID_detection/blob/main/README.md#about-the-project)
2. [Pre-requisites](https://github.com/Sanketb77/Point-of-care-COVID_detection/blob/main/README.md#pre-requisites)
3. [Dataset](https://github.com/Sanketb77/Point-of-care-COVID_detection/blob/main/README.md#dataset)
4. [Roadmap](https://github.com/Sanketb77/Point-of-care-COVID_detection/blob/main/README.md#roadmap)
5. [Results and Discussion](https://github.com/Sanketb77/Point-of-care-COVID_detection/blob/main/README.md#results-and-discussion)


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

### <em>Binary Classification</em>

<div align = "center">

<img width="600" alt="Screenshot 2022-07-21 at 4 05 12 PM" src="https://user-images.githubusercontent.com/86565759/180589613-ec84dbeb-2efd-413f-8234-712a28c40aae.png">

</div>

<div align = "center">

<img width="600" alt="Screenshot 2022-07-27 at 1 12 59 AM" src="https://user-images.githubusercontent.com/86565759/181166677-fb551a54-043e-4f0c-a0d2-49c6810974ed.png">

</div>


### <em>Multi-class Classification</em>
  
<img src="https://user-images.githubusercontent.com/86565759/180591224-d1b19e85-7d77-4933-b7c0-a4e8bf7bf99d.png" width="510"/> <img src="https://user-images.githubusercontent.com/86565759/180591125-9523009c-7355-4e8b-837a-f5ede440d7d0.png" width="448"/> 


Finally, Xception model has been deployed as a web application using Streamlit. The application allows user to upload the images and it correctly predicts it's class.

<img align="left" width="60" height="60" src= https://user-images.githubusercontent.com/86565759/180590754-cca99cb6-ec8f-4b92-9b92-302f02c99058.jpg>

## Instructions

The following steps must be followed for reproducing the code :-

* The python script named 'Data_Collection.ipynb' contains the code for extracting lung ultrasound videos from the 8 sources listed in the [Dataset](https://github.com/Sanketb77/Point-of-care-COVID_detection/blob/main/README.md#dataset) section. The script also contains the code for video pre-processing and extracting lung ultrasound images from the same.

* The R code in 'Data_Assessment.html' can be replicated for assessing the data quality, fitness for use and for conducting an ethical assessment. The 'image_details.csv' file contains information about the images extracted. The same can be obtained by successfully exceuting the data collection script.

* It is recommended to use Google Colab since training the machine learning models on thousands of images takes up alot of time and computational power.

* The python scripts containing the code for classifiers can be executed using the images extracted and by placing them in the current working directory in the google drive.

* The binary classification part has three scripts, the same can be executed to train and test the performance of the 6 binary classifiers on the lung ultrasound images dataset.

* The file 'FourClass_Part01.ipynb' consists of ResNet50V2 and Xception trained with balanced class weights on all the four classes i.e. Covid, Normal, Pneumonia and Other.

* 'FourClass_Part02.ipynb' can be executed starting from the very first cell to see techniques like 'Balanced Bagging Classifier' and 'Startification' in use in combination with Decision Tree Classifier and Logistic Regression model respectively.

NOTE - All the code scripts can be found in the 'scripts' directory.

<img align="left" width="60" height="60" src= https://user-images.githubusercontent.com/86565759/181162325-347bd16d-692f-4c42-b8b9-33193fdbe609.png>

## Web Application Demo

The web application can be seen in working here -

<div align = "center">

https://user-images.githubusercontent.com/86565759/180590942-48c9a783-4d12-4699-8598-9b94156abfa5.mp4
  
</div>




