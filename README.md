## Using Lung ultrasound images for building a reliable Point-of-care COVID-19 testing system

### About the Project
This project aims to develop a quick and reliable Point-of-care Covid diagnosis system that returns the results instantly.A machine learning based diagnosis system can be developed that classifies patients into right category of results – Positive or Negative using their lung ultrasound images. Such a model would help the healthcare professionals by saving a great deal of their time as the classification model would return the results momentarily. Moreover, the final deployed model’s promising accuracy would save the trouble of conducting a series of follow up tests. The solution would change the clinical decision support as this would not only save care providers and patients from unnecessary delays and waiting times but will also enable healthcare professionals to take the necessary actions timely.

The goal is compare and evaluate the performance of different convolutional neural networks in combination with Transfer learning and other approaches for choosing a highly accurate model for deployment.

### Pre-requisites
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

### Dataset
COVIDx-US is an open access benchmark dataset of ultrasound imaging related to COVID-19. 192 lung ultrasound videos and 18,628 images have been extracted from 8 sources - GrepMed (20 videos) , PocusAtlas (32 videos), Clarius (6 videos) , LITFL (63 videos), CoreUltrasound (18 videos) , Radiopaedia (5 videos), Papers (22 videos), UF (26 videos).The videos have been captured with either of the two probes - Convex or Linear.The images belong to four classes namely Covid, Normal, Pneumonia and Other.

The following table contains the image distribution by class -

Class | Number of Images 
:---: | :---: 
COVID | 4003
Normal | 2201
Pneumonia | 4449
Other | 7975


*The COVIDx-US dataset details can be found at [here](https://github.com/nrc-cnrc/COVID-US)*









