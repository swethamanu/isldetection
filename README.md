# INDIAN SIGN LANGUAGE DETECTION
 
Indian Sign language (ISL) is used by millions of specially abled people all across the country to communicate effectively. In this project we’ve used computer vision, machine learning and deep learning techniques to build a model that can detect alphabets and digits in Indian Sign Language in real time.

## CONTENTS

1. Identifying the dataset
2. Preprocessing
3. Building CNN
4. Fitting and Evaluation
5. Inference


## IDENTIFYING THE DATASET

We searched the web and found a suitable dataset on Github by user [Karthikeyu](https://github.com/Karthikeyu) who had developed a similar application. It is a self created dataset and all the images were captured by him. It included signs for alphabets (A-Z) and digits (1-9), a total of 35 classes. 

#### TEST-TRAIN SPLIT

TOTAL NUMBER OF IMAGES → 42000

NUMBER OF CLASSES → 35 

IMAGES PER CLASS → 1200 

NUMBER OF IMAGES USED FOR TRAINING → 31500

NUMBER OF IMAGES USED FOR TESTING → 10500

###### link to the dataset ---> [datset](https://drive.google.com/drive/folders/1keWr7-X8aR4YMotY2m8SlEHlyruDDdVi)

## PREPROCESSING

#### PROCEDURE 

1. CONVERTING COOLOR CHANNELS: Loaded BGR image converted to is converted to HSV 
2. INRANGE THRESHOLDING: thresholding done to segment skin areas of the image 
3. MORPHOLOGICAL TRANSFORMATIONS: applying erosion and dilation to remove noise and soften the image
4. BINARY THRESHOLDING: image is converted back to grayscale and thresholding is applied 

#### RESULT 

![image](https://user-images.githubusercontent.com/69666461/148633496-fbe32411-82d2-431d-927d-57e9772b90bc.png)

[preprocessing notebook](isldetection/preprocessing_final.ipynb)

## BUILDING CNN








