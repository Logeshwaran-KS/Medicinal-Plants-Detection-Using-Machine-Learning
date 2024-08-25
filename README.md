# **Medicinal Plants Detection Using Machine Learning** :shamrock:

## **Machine Learning / Deep Learning: Project 1**


This project focuses on Medicinal Plants Detection using Machine Learning techniques to identify various medicinal plants through images. The process involves Segmentation, Gray Scale Conversion, and advanced Feature Extraction methods such as GLCM, Gabor, and LBP. Multiple models are trained and evaluated to identify the most suitable one for prediction.

## **Project Overview** :page_facing_up:
The primary objective is to develop a reliable model capable of accurately identifying medicinal plants from images. The project emphasizes manual feature extraction techniques without relying on neural networks, ensuring high performance across various machine learning models.

---

## **Data Collection** :package:
The dataset comprises images of 30 different plant species, each labeled with both common and botanical names. These images vary in size, providing a comprehensive dataset for robust classification tasks.

- **Dataset URL:** [Medicinal Leaf Dataset](https://data.mendeley.com/datasets/nnytj2v3n5/1)

---

## **Preprocessing** :hammer_and_wrench:
### **1. Segmentation** :scissors:
Images are segmented using the HSV (Hue, Saturation, Value) color space to isolate the relevant plant regions, removing unnecessary background.

<div>
  <img src="https://github.com/user-attachments/assets/aee5227f-2b46-44f1-a2ed-b34d91959011" alt="ImgSeg" width="400" />
</div>

### **2. Gray Scale Conversion** :black_circle:
The segmented images are then converted to grayscale to simplify further processing while preserving essential details.

<div>
  <img src="https://github.com/user-attachments/assets/38c27710-bd6f-42bb-a8ba-8b07ea5af34b" alt="GrayScale" width="400" />
</div>

### **3. Sobel Filter** :triangular_ruler:
A Sobel Filter is applied to highlight the edges in the images, making them more suitable for feature extraction.

<div>
  <img src="https://github.com/user-attachments/assets/a807095a-0e98-466c-9356-e4488c332393" alt="Sobel" width="400" />
</div>

---

## **Feature Extraction** :mag_right:
Features are extracted from both segmented and grayscale images using the following techniques:

### **1. Local Binary Patterns (LBP)** :1234:
LBP converts an image into a binary pattern by comparing neighboring pixels to the center pixel. This binary code is then converted to a decimal value, serving as a texture descriptor.

### **2. Gray-Level Co-occurrence Matrix (GLCM)** :chart_with_upwards_trend:
GLCM analyzes pixel pairs within a specific spatial relationship, creating a matrix that reflects their frequency. This matrix is used to derive texture features such as contrast, correlation, energy, and homogeneity.

### **3. Gabor Filters** :wave:
Gabor filters process the image by convolving it with a sinusoidal wave modulated by a Gaussian envelope. These filters are sensitive to specific image features, such as edges and textures, at various scales and orientations.

### **4. Color Moments** :rainbow:
Color moments, including mean, standard deviation, and skewness, capture the color distribution in each channel (e.g., RGB). These moments are highly effective for image classification tasks.

**Note:** A total of 62 features are extracted from each image and stored in a `FeatureExtracted.csv` file. If you require this file, please contact me using the information provided at the end.

---

## **Feature Reduction** :scissors:
To improve model performance and reduce dimensionality, the dataset is split into training and test sets, and the following techniques are applied:

### **1. Principal Component Analysis (PCA)** :bar_chart:
PCA identifies the principal components that capture the most variance in the data, reducing the dimensionality while retaining essential information.

### **2. StandardScaler** :balance_scale:
The StandardScaler normalizes the data by transforming each feature to have a mean of 0 and a standard deviation of 1, ensuring consistency during model training.

---

## **Model Training** :computer:
The extracted features are used to train multiple models, with a focus on identifying the best-performing one.

### **Model Comparison** :bar_chart:
<div>
  <img src="https://github.com/user-attachments/assets/b1cdb539-347a-40a1-8c49-9182446f67aa" alt="ModelComp" width="400" />
</div>

### **Support Vector Machine (SVM)** :rocket:
SVM achieved the highest accuracy of 99%, outperforming all other models. Its ability to find the optimal hyperplane that maximizes class separation makes it particularly effective for this classification task.

---

## **Prediction** :crystal_ball:
Real-time data can be used for prediction by leveraging pre-trained models, including PCA for dimensionality reduction, StandardScaler for normalization, and SVM for classification. The process involves:

1. **Data Preprocessing:** Incoming data is normalized using the saved StandardScaler to ensure consistency.
2. **Dimensionality Reduction:** The data is transformed using the saved PCA model, retaining the most significant features.
3. **Prediction:** The transformed data is fed into the saved SVM model to generate real-time predictions.

This approach ensures efficient and accurate predictions on new, unseen data by utilizing the computational efficiency and patterns learned by the pre-trained models.

---

## **Contact** :mailbox:
If you have any questions, need additional data, or have suggestions or feedback, feel free to contact me:

- :email: **Email:** logeshwaranks01@gmail.com
- **LinkedIn:** [Logeshwaran KS](https://www.linkedin.com/in/logeshwaran-ks)

---

**Thank You for Checking Out This Project!** :smile:
