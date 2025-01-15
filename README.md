# Melanoma-Detection

## Melanoma Detection Using a CNN-Based Model
> 
elanoma, a type of skin cancer, is a serious health concern with potentially life-threatening consequences if not detected early. With the advancements in deep learning and computer vision,
 building a CNN-based model has become a promising approach for accurate melanoma detection.In this project, we will explore the steps involved in creating a CNN-based model that can 
 effectively identify melanoma, providing a valuable tool for early diagnosis and treatment.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)



## General Information,
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. 
A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

Data Source : The dataset is from the International Skin Imaging Collaboration (ISIC) , which consists of 2K+ images of malignant and benign oncological diseases, which are already pre classified .
The data set contains the following diseases:

1) Actinic keratosis
2) Basal cell carcinoma
3) Dermatofibroma
4) Melanoma
5) Nevus
6) Pigmented benign keratosis
7) Seborrheic keratosis
8) Squamous cell carcinoma
9) Vascular lesion


## Conclusions
Initial analysis(Model 1)
*  Both training and validation accuracies are relatively low, which suggests the model is not performing well on either the training data or unseen data. This is an indicator of underfitting.
*  The validation loss (1.7741) is significantly higher than the training loss (1.3694). A large difference between training and validation loss can indicate overfitting, however, in this case, since both accuracies are low, it is likely due to the model not having learned enough general patterns from the data.

Model 2 with Augmentation :
Since underfitting indicates the model hasn't learned enough general patterns from the data, we need to increase the diversity and size of the training data without fundamentally changing the original data distribution.Below augmentation can be used:

*  Random Rotation: Rotate images randomly by a small angle (e.g., within +/- 10 degrees). This helps the model become invariant to slight rotations of the skin lesions.
*  Random Horizontal/Vertical Flip: Flip images horizontally or vertically. This increases the variety of perspectives the model sees.
*  Random Zoom: Zoom in or out on images randomly. This exposes the model to different scales of the skin lesions.

It was observed under fitting was answered to an extent with augmented data with good improvement in validation score to 52% but accuracy is still also was just above 51% .This could be beacuse of smaller dataset and class imbalance.

Model 3 ( Augemented data with and resolving class imbalance):
Augementor was used to add another 500 sample accross all classes as such no class have fewer sample
* With help of Augmentor generated data, Overall Accuracy increased to great extent.

  Training Accuracy - 95%
  Validation Accuracy - 77%

* Overall Loss

  Training Loss - less than .15
  Validation Loss - less then 1.17

Although Model seems overfitting a bit, but can be fine tuned by modifying hyper parameters






<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- tensorflow import keras
- tensorflow.keras import layers
- tensorflow.keras.models import Sequential
- SparseCategoricalCrossentropy:  Suitable for multi-class classification problems.
- Adam : As it offers adaptive learning rate along with speed and accuracy
- Augemntor for adding samples


## Contact
Created by [@saksham7786] -  
