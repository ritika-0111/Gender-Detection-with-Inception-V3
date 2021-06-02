# Gender-Detection-with-Inception-V3  

## Dataset
In this project, we will use the CelebA dataset (http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html), which is available on Kaggle.
You can download dataset from Kaggle (https://www.kaggle.com/jessicali9530/celeba-dataset):

## Overall  
The dataset contains:  

   202,599 number of face images of various celebrities  
   10,177 unique identities, but names of identities are not given  
   40 binary attribute annotations per image  
   5 landmark locations  
   
## Data Files
*imgalignceleba.zip:* All the face images, cropped and aligned

*listevalpartition.csv:* Recommended partitioning of images into training, validation, testing sets. Images 1-162770 are training, 162771-182637 are validation, 182638-202599 are testing

*listbboxceleba.csv:* Bounding box information for each image. "x1" and "y1" represent the upper left point coordinate of bounding box. "width" and "height" represent the width and height of bounding box

*listlandmarksalign_celeba.csv:* Image landmarks and their respective coordinates. There are 5 landmarks: left eye, right eye, nose, left mouth, right mouth

*listattrceleba.csv:* Attribute labels for each image. There are 40 attributes. "1" represents positive while "-1" represents negative

## Modelling and structure
Using Inception V3 model
I am using a pretrained Inception V3 model for which I will retrain some layers and fix the first layers. I will also attach new output layers to perform the new classification task.

## Target variable
As my target variable, I only use the gender feature available in the dataset and detect if the image shows a man or a woman.

## Strategy:

*Importing libraries and reading Data*    
*Data Visualization*  
*Separating Training, Testing and Validation Data*  
*Data Augmentation*  
*Importing Inception V3 model*  
*Adding Custom Layers*  
*Create and compile final model*  
*Plotting loss functiona and accuracy through epochs*  
*Prediction on Testing Data to check accuracy*  
*Generating new predictions*  


### Note:  
1. The inception model (https://keras.io/api/applications/inceptionv3/) is available from Keras. We can either download pre-trained model or else can connect the notebook with the dataset using "imagenet" as weights.  
2. Keras ImageDataGenerator and flow_from_dataframe is used to avoid loading all images in memory and fit the model on the entire dataset.
