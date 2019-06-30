# Skin-Lesion-Classifier-HAM10000

Classification of 7 types of skin Lesions namely:
1.	Melanocytic nevi
2.	Melanoma
3.	Benign keratosis-like lesions
4.	Basal cell carcinoma
5.	Actinic keratoses
6.	Vascular lesions
7.	Dermatofibroma


For this HAM1000 dataset was used ("Human Against Machine with 10000 training images").Ham10000 is a collection dermatoscopic images from different populations, acquired and stored by different modalities. The final dataset consists of 10015 dermatoscopic images.
The data set was obtained from here : https://www.kaggle.com/kmader/skin-cancer-mnist-ham10000
From the HAM10000 data set we will be using only HAM10000_metadata.csv and HAM10000_images_part1 and HAM10000_images_part2 which have to be unzipped for accessing the images in the folders through the os module 

DataPreprocessing:
Separated directories were created and for train and test data within which 7 directories corresponding to 7 different types of lesions were created.
Test and train were split in the ratio 10:90 i.e 9013 samples in the training set and 1002 samples in test set. Both the folders containing the images(i.e HAM10000_images_part1 and HAM10000_images_part2) were accessed  and their corresponding class was obtained form HAM10000_metadata.csv ‘dx’ column and were copied into their respective folders(one of the 7 classes ) in the respective directories (train or test)


Model:
This is a simple Lenet model with 3 conv layers and 3 maxpool layers.
Here the validation set was the same as the test set 
The model gave an accuracy of around 74% in the test set, 20 epochs was taken with anything more the more was seen to overfitting 
The graphs below give the loss and accuracy in the training and validation set 


![alt text](https://github.com/dhruv-shindhe/Skin-Lesion-Classifier-HAM10000/blob/master/loss.png)

![alt text](https://github.com/dhruv-shindhe/Skin-Lesion-Classifier-HAM10000/blob/master/accuracy.png) 


Improvements :
1.Different validation and test set
2.Data augmentation
3.Tranfer learning using MOBILENet
