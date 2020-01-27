# Histopathologic-cancer-detection
Python Jupyter Notebook leveraging **Transfer Learning** and **Convolutional Neural Networks** implemented with [Keras](https://keras.io/).

Part of the [Kaggle competition](https://www.kaggle.com/).

Submitted [Kernel](https://www.kaggle.com/c/histopathologic-cancer-detection/submissions) with 0.9374 score.

Check out corresponding Medium article:

[Histopathologic Cancer Detector - Machine Learning in Medicine](https://towardsdatascience.com/histopathologic-cancer-detector-finding-cancer-cells-with-machine-learning-b77ce1ee9b0a)


# Introduction

There are millions of datasets already trained on the image net which does a great job in the classification task.
My idea was to use **CNN** architecture of these pre-trained models to capture shape, texture, color, etc. of my dataset as they are not data specific.
Afterward, I added my fully connected neural networks at the end of this CNN architecture and fine tunned them to make them data specific.
The pre-trained model I used here is known as [Xception](https://towardsdatascience.com/review-xception-with-depthwise-separable-convolution-better-than-inception-v3-image-dc967dd42568).

Then I used a technique known as **Image augmentation**, which increases the data set by applying: rotation, shift, flip, etc on the original images. It increased the variance of my dataset and thus increased the test accuracy.

For the optimization purpose, I used [Adam optimizer](https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/)
As dataset was of 6 GB for memory management, batches of 16 images were formed and then image augmentation was applied to them.


# Data


Dataset: [Link](https://www.kaggle.com/c/histopathologic-cancer-detection/data)

Description: *Binary classification* whether a given histopathologic image contains a tumor or not.


# Model


![alt text](https://github.com/kulgarima/Histopathologic-cancer-detection/blob/master/model.jpg)


![alt text](https://github.com/kulgarima/Histopathologic-cancer-detection/blob/master/model.png)


# Training Log-loss and Accuracy curves

![alt text](https://github.com/kulgarima/Histopathologic-cancer-detection/blob/master/training.png)


# Result

Kaggle score: **0.9374**
