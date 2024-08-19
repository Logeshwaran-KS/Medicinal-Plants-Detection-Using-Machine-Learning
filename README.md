# ***Medicinal Plants Detection Using Machine Learning***
***Machine Learning / Deep Learning: Project 1***

Medicinal Plants Detection using Machine Learning is to Identify the Medicinal Plants through images by Segmentation, Gray Scale Conversion, Feature Extractions like GLCM, Gabor and LBP. Later the data is Trained with Multiple Model to track the Performace and get the suitable Model for Prediction

The Complete description is given below:
## ***Data Collection***  
The dataset is download and feature extracted from . It has 30 Species of different image size, named with normal and botanical name.

URL - [Medicinal Leaf Dataset](https://data.mendeley.com/datasets/nnytj2v3n5/1)
## ***Pre Processing***
In Pre processing, the images are Segmented with the help of HSV (Hue Saturation Value) to remove the unwanted outer region.
The image below depicts the result of Segmentation
<div>
  <img src="https://github.com/user-attachments/assets/aee5227f-2b46-44f1-a2ed-b34d91959011" alt="ImgSeg" width="400" />
</div>
As a Second step, the Semented images are later converted into GrayScale image for the futhur process.
The image below depicts the result of Gray Scale converison
<div>
  <img src="https://github.com/user-attachments/assets/38c27710-bd6f-42bb-a8ba-8b07ea5af34b" alt="ImgSeg" width="400" />
</div>
Final Step of Pre processing is applying Sobel Filter to make the image edge highlighted.
The image below depicts the result of Sobel Filter
<div>
  <img src="https://github.com/user-attachments/assets/a807095a-0e98-466c-9356-e4488c332393" alt="ImgSeg" width="400" />
</div>

## ***Feature Extraction***
Feature are extracted for both Segmented and Segmented + GrayScaled image. Here, 3 Extraction techniques are used
### ***LBP***
  LBP converts an image into a binary representation by thresholding the neighborhood pixels against the center pixel. It generates a binary code, which is then converted to a decimal value, resulting in a texture descriptor.
### ***GLCM***
  GLCM computes how often pairs of pixel with specific values and in a specified spatial relationship occur in an image, creating a matrix that represents the frequency of these combinations. From this matrix, various texture features like contrast, correlation, energy, and homogeneity can be derived.
### ***Gabor***
  Gabor filters operate by convolving the image with a sinusoidal plane wave modulated by a Gaussian envelope. The filter is oriented in various directions and scales, making it sensitive to specific features in the image, such as edges and textures.
Finally 62 features are extracted and stored in the CSV file for the later purpose

## ***Feature Reduction***
The CSV file is splited into X and Y (Label) for remove irrelavant feature. Two techiques are used Principle Component Analysis and StandardScaler
### ***Principle Component Analysis***
  PCA identifies the directions (principal components) in which the data varies the most and projects the data onto these directions. This reduces the dimensionality of the data while retaining most of its variance.
### ***StandardScaler***
  The Standard Scaler transforms data such that the mean of each feature becomes 0, and the standard deviation becomes 1. It accomplishes this by subtracting the mean of each feature from the data and then dividing by the standard deviation:
## ***Model Training***
Here, the data is trained with different model to obtained high performed model.
### ***Model Comparison***
<div>
  <img src="https://github.com/user-attachments/assets/b1cdb539-347a-40a1-8c49-9182446f67aa" alt="ImgSeg" width="400" />
</div>

### ***Support Vector Machine***
Support Vector Machine gives the highest perfomance of accuracy 99% among all the other
## ***Prediction***
Real time data can be used for prediction with the help of saved PCA, SC and SVM Model
