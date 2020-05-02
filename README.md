# MSCS18037_COVID19_DLSpring2020
This repository contains code and results for COVID-19 classification assignment by Deep Learning Spring 2020 course offered at Information Technology University, Lahore, Pakistan. This assignment is only for learning purposes and is not intended to be used for clinical purposes.

# Dependencies
The code was run on Google Colab using Pytorch.

# Dataset
The dataset used is a binary dataset containing 2 classes: "Infected" and "Normal". The infected class has images of chest X-rays of Pneumonia and Covid-19 infected people while the normal class has normal chest x-ray images.

## Dataset No. 1
The dataset can be found by following the below link:
https://drive.google.com/a/itu.edu.pk/uc?id=1-HQQciKYfwAO3oH7ci6zhg45DduvkpnK

## Dataset No. 2 (For testing the effect of focal loss)
The dataset can be found by following the below link:
https://drive.google.com/file/d/1eytbwaLQBv12psV8I-aMkIli9N3bf8nO/view?usp=sharing

# VGG-16 (Normal)
The pretrained version of VGG16 on Imagenet dataset was used.

## Experiment 1

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. The training of the convolution layers (feature layers) was set to OFF. Only the final 2 FC layers were fine-tuned.
  
  The trained model can be found at models/vgg16/exp1/vgg16_2FC.pth
  
  The training and validation accuracies and loss are given as:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp1/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp1/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp1/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp1/cm_test.png)
  

## Experiment 2

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. The training of the convolution layers (feature layers) except the last convolution layer was set to OFF. So, last convolutional layer and the final 2 FC layers were fine-tuned.
  
  The trained model can be found at models/vgg16/exp2/vgg16_1C_2FC.pth
  
  The training and validation accuracies and loss are given as:
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp2/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp2/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp2/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp2/cm_test.png)
  


## Experiment 3

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. The training of the convolution layers (feature layers) except the last 6 convolution layer was set to OFF. So, last 6 convolutional layers and the final 2 FC layers were fine-tuned.
  
  The trained model can be found at models/vgg16/exp3/vgg16_6C_2FC.pth
  
  The training and validation accuracies and loss are given as:
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp3/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp3/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp3/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp3/cm_test.png)
  

## Experiment 4

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. All of the network was fine-tuned.
  
  The trained model can be found at models/vgg16/exp4/vgg16_AC_2FC.pth
  
  The training and validation accuracies and loss are given as:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp4/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp4/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp4/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/vgg16/exp4/cm_test.png)
  
# Resnet-18 (Normal)
The pretrained version of Resnet18 on Imagenet dataset was used.

## Experiment 1

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. The training of the convolution layers (feature layers) was set to OFF. Only the final 2 FC layers were fine-tuned.
  
  The trained model can be found at models/Resnet18/exp1/vgg16_2FC.pth
  
  The training and validation accuracies and loss are given as:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp1/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp1/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp1/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp1/cm_test.png)
  

## Experiment 2

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. The training of the convolution layers (feature layers) except the last layer (group of further convolutional layers) was set to OFF. So, last convolutional layer and the final 2 FC layers were fine-tuned.
  
  The trained model can be found at models/Resnet18/exp2/vgg16_1C_2FC.pth
  
  The training and validation accuracies and loss are given as:
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp2/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp2/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp2/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp2/cm_test.png)
  


## Experiment 3

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. The training of the convolution layers (feature layers) except the last 3 layers (each layer is a group of further convolutional layers) was set to OFF. So, last 3 convolutional layers and the final 2 FC layers were fine-tuned.
  
  The trained model can be found at models/Resnet18/exp3/vgg16_6C_2FC.pth
  
  The training and validation accuracies and loss are given as:
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp3/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp3/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp3/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp3/cm_test.png)
  

## Experiment 4

The following changes were made:
  1. The FC layers were removed. They were replaced with two layers. One having 470 neurons and other 2 (the output layer).
  2. All of the network was fine-tuned.
  
  The trained model can be found at models/Resnet18/exp4/vgg16_AC_2FC.pth
  
  The training and validation accuracies and loss are given as:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/cm_val.png)
  
  The testing confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/cm_test.png)

# VGG16 (Testing the Effect of Focal Loss)

## Experiment 1 (End-to-End without Focal Loss)

  In this experiment the pretrained VGG16 was taken and was fine-tuned end to end. Only the last layer was changed in order to predict 3 classes. This was taken as a multilabel classification. BCEWithLogitsLoss was used.

  The trained model can be found at https://drive.google.com/open?id=1i25ZmybjtOLiWvRx636wkDZRT97Ev89a

The training and validation accuracies and loss are given as:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/acc_loss.png)
  
  The training confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/cm_train.png)
  
  The validation confusion matrix is given below:
  
  ![alt text](https://github.com/Inaam1995/MSCS18037_COVID19_DLSpring2020/blob/master/models/Resnet18/exp4/cm_val.png)
  
## Experiment 2 (End-to-End with Focal Loss)
