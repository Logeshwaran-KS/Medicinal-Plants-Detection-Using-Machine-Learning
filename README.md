# ***Medicinal Plants Detection Using Machine Learning***
***Machine Learning / Deep Learning: Project 1***

Medicinal Plants Detection using Machine Learning is to Identify the Medicinal Plants through images by Segmentation, Gray Scale Conversion, Feature Extractions like GLCM, Gabor and LBP. Later the data is Trained with Multiple Model to track the Performace and get the suitable Model for Prediction

The Complete description is given below:
## ***Data Collection***  
The dataset is download and feature extracted from . It has 30 Species of different image size, named with normal and botanical name.

URL - [Medicinal Leaf Dataset](https://data.mendeley.com/datasets/nnytj2v3n5/1)
## ***Pre Processing***
In Pre processing, the images are segmented with the help of HSV (Hue Saturation Value) to remove the unwanted outer region.
The image below depicts the result of Segmentation

As a Second step, the semented images are later converted into GrayScale image for the futhur process.
The image below depicts the result of Gray Scale converison

Final Step of preprocessing is applying Sobel filter to make the image edge highlighted.
The image below depicts the result of Sobel Filter

## ***Feature Extraction***
Feature are extracted for both Segmented and Segmented + GrayScaled image. Here, 3 main extraction techniques are used
### ***LBP***
### ***GLCM***
### ***Gabor***

Finally 62 features are extracted and stored in the CSV file for the later purpose

## ***Feature Reduction***
The CSV file is splited into X and Y (Label) for remove irrelavant feature. Two techiques are used Principle Component Analysis and StandardScaler
### ***Principle Component Analysis***
### ***StandardScaler***

## ***Model Training***
Here, the data is trained with different model to obtained high performed model.
### ***Support Vector Machine***
It gives the highest perfomance of accuracy 99% among all the other
### *** Model Comparison***

## ***Prediction***
Real time data can be used for prediction with the help of saved PCA, SC and SVM Model
