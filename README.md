Melanoma Detection - Convolutional Neural Network
Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths.

Building A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

Built Multiclass classification model using a custom convolutional neural network in TensorFlow & Keras.

Table of Contents
General Info
Process followed
Technologies Used
Acknowledgements
General Information

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion

Process followed

Data Set is available in the Google drive as specified in the code.
# Path for train and test images
data_dir = '/content/drive/MyDrive/Data/Melanoma/Train_Data'  # Initial Training data provided
train_dir = '/content/drive/MyDrive/Data/Melanoma/Train'   # Creating train data at the ratio of 0.8 from Train_Data directory
test_dir = '/content/drive/MyDrive/Data/Melanoma/Test' # Initial Test data Provided
validation_dir = '/content/drive/MyDrive/Data/Melanoma/Validation'  # Creating Validation data at the ratio of 0.2 from Train_Data Directory

Built multiple CNN model is bulit with different layers. Accuracy summarised below.
Built Neural netwrok architecture using keras.

CNN Architecture

1. Rescaling layer to normalize the pixel values to be in the [0, 1] range
2. Two convolutional layers having 32 filters(3x3) with Relu activation followed by Batch Normalization, max pooling and Dropout of 0.25
3. Two convolutional layers having 64 filters(3x3) with Relu activation followed by Batch Normalization, max pooling and Dropout of 0.10,
4. Two convolutional layers having 128 filters(3x3) with Relu activation followed by Batch Normalization, max pooling and Dropout of 0.10,
5. Two convolutional layers having 256 filters(3x3) with Relu activation followed by Batch Normalization, max pooling and Dropout of 0.25,
6. Two convolutional layers having 512 filters(3x3) with Relu activation followed by Batch Normalization, max pooling and Dropout of 0.10 ,
7. Flatten layer,
8. Fully connected Dense layer with 1024 neurons with Relu activation, l2 regularization for both kernel and bias
9. Fully connected Dense layer with 512 neurons with Relu activation, l2 regularization for both kernel and bias
10. Fully connected Dense layer with 1024 neurons with Relu activation, l2 regularization for both kernel and bias, and finally
11. Softmax layer with 9 (num_classes) neurons
		
Used adam optimizer and categorical_crossentropy as loss function with accuracy as metric

First model: Define the Simple CNN model with 3 layers without any Regularization techniques 3 Conv + 2 FC

Second mode2: Define CNN model with 5 Conv layers and 3 FC layers Batch normalization and Regularization.

Third model: As specifed above under the label of CNN Architecture.

Python Notebook uploaded in git repo https://github.com/settumurugan/Melanoma-Detection-Assignment.

Technologies Used:
tensorlfow - 2.10.1
pandas - 2.1.1
numpy - 1.24.3
matplotlib - 3.8.0
seaborn - 0.13.2

Acknowledgements
This project was part of Upgrad-IIITB ML& AI course.
Other learning from stack-overflow on few error clarification helped to complete this study.

Contact
settu.murugan@gmail.com 