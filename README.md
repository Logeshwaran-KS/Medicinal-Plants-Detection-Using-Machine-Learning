# ***Medicinal Plants Detection Using Machine Learning :shamrock:***
***Machine Learning / Deep Learning: Project 1***

Medicinal Plants Detection using Machine Learning is to Identify the Medicinal Plants through images by Segmentation, Gray Scale Conversion, Feature Extractions like GLCM, Gabor and LBP. Later the data is Trained with Multiple Model to track the Performace and get the suitable Model for Prediction

The Complete description is given below :arrow_down:
## ***Data Collection***  
The dataset was downloaded and features were extracted from images representing 30 different species, each varying in size. The images are labeled with both common names and botanical names, providing a comprehensive set of data for classification tasks.

URL - [Medicinal Leaf Dataset](https://data.mendeley.com/datasets/nnytj2v3n5/1)
## ***Pre Processing***
### ***Segmentation***
In Pre processing, the images are Segmented with the help of HSV (Hue Saturation Value) to remove the unwanted outer region.
The image below depicts the result of Segmentation
<div>
  <img src="https://github.com/user-attachments/assets/aee5227f-2b46-44f1-a2ed-b34d91959011" alt="ImgSeg" width="400" />
</div>

### ***Gray Scale converison***
As a Second step, the Semented images are later converted into GrayScale image for the futhur process.
The image below depicts the result of Gray Scale converison
<div>
  <img src="https://github.com/user-attachments/assets/38c27710-bd6f-42bb-a8ba-8b07ea5af34b" alt="ImgSeg" width="400" />
</div>

### ***Sobel Filter***
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
### ***Color Moments***
  They typically include the mean, standard deviation, and skewness of the pixel values within each color channel (e.g., RGB), capturing essential color characteristics. These moments are effective in image retrieval and classification tasks due to their ability to represent color features compactly
  
Finally 62 features of each image is extracted and stored in the FeatureExtracted CSV file for the later purpose. If FeatureExtracted File required, please contact (information provided at the end)

## ***Feature Reduction***
The FeatureExtracted CSV file is splited into X and Y (Label) and splitted into train and test data. For removing irrelavant feature, Two techiques are used Principle Component Analysis and StandardScaler
### ***Principal Component Analysis***
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
Support Vector Machine (SVM) demonstrated the highest performance with an accuracy of 99%, outperforming all other algorithms used in the project. Its ability to find the optimal hyperplane that maximizes the margin between different classes makes SVM particularly effective for this classification task. This exceptional accuracy highlights SVM's robustness and suitability for complex data patterns.
## ***Prediction***
Real-time data can be utilized for prediction by leveraging pre-trained models, including Principal Component Analysis (PCA) for dimensionality reduction, StandardScaler (SC) for data normalization, and a Support Vector Machine (SVM) for classification. The process begins with the incoming data being preprocessed using the saved StandardScaler to ensure consistency with the training data. Next, the data is transformed using the saved PCA model, reducing its dimensionality while retaining the most significant features. Finally, the transformed data is fed into the saved SVM model to generate predictions in real-time. This approach allows for efficient and accurate predictions on new, unseen data by utilizing the computational efficiency and learned patterns from the pre-trained models.
## Contact
If you have any questions, data requirement, suggestions, or feedback, feel free to contact me:

:email: **Email:** logeshwaranks01@gmail.com

**LinkedIn:** [logeshwaran-ks](https://www.linkedin.com/in/logeshwaran-ks/)

**Thank You for Checking Out This Project!**  :smile:
