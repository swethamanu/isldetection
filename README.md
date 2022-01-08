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

1. CONVERTING COLOR CHANNELS: Loaded BGR image converted to is converted to HSV 
2. INRANGE THRESHOLDING: thresholding done to segment skin areas of the image 
3. MORPHOLOGICAL TRANSFORMATIONS: applying erosion and dilation to remove noise and soften the image
4. BINARY THRESHOLDING: image is converted back to grayscale and thresholding is applied 

#### RESULT 

![image](https://user-images.githubusercontent.com/69666461/148633496-fbe32411-82d2-431d-927d-57e9772b90bc.png)

[preprocessing notebook](preprocessing_final.ipynb)

## BUILDING CNN

CNN is a kind of artificial neural network used primarily in applications that involve image processing. It allows us to apply convolutional operations to the input image to extract features before feeding it to a fully connected neural network for classification purposes 

The open source libraries keras and tensorflow were used for building, compiling and evaluating the model. 

## FITTING AND EVALUATION

The model ran for 5 epochs and an accuracy of 99.23% was obtained

[ML model notebook](ml_model_final.ipynb)

## REAL TIME EVALUATION 

![image](https://user-images.githubusercontent.com/69666461/148633976-3a03e457-5e13-49d9-8784-86d421a6c811.png)

![image](https://user-images.githubusercontent.com/69666461/148634003-2a7d2bfe-088e-47b3-8d55-722cbb589905.png)


Our model predicts most of the signs fairly well though it consistently predicts the wrong output for certain letters. It often mistakes signs for the letters O,T,S,H which look similar. It performs better on the single handed signs over the double handed ones.

[implementation notebook](app_final.ipynb)

## INFERENCE 

Though we've attained a high accuracy our model we’ve observed that it does not perform well for all signs and depends heavily on external criteria like the lighting of a place and orientation of the hand. We’ve concluded that this is most likely because of a lack of diversity in the dataset and can easily be rectified by creating a dataset with differing images for each sign. 

