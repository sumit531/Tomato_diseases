# Tomato_diseases
#Problem Statement:To predict whether a leaf sample taken is going to grow without any hindarances.Useful in Agriculture Scenarios.

Created an image classifier on the basis of previous found samples out of which several bad as well as good samples were taken.The sample images were digitally taken and then sent for further analysis(which weeds out the non-descripit one).Then using Deep Learning modules,We obtained a score of 0.9044.

And then when an altogether new image was given to the model,it is able to correctly predict whether the new tomato leaf sample taken is going to sprout defectively or not.

Steps-:

1.)Importing necessary libraries
2.)Setup the batch file ,image size,channel,epochs
3.)Import data into tensorflow dataset object
4.)Finding class names belonging to images
5.)Function to Split Dataset
  Dataset should be bifurcated into 3 subsets, namely:
  Training: Dataset to be used while training 
  Validation: Dataset to be tested against while training 
  Test: Dataset to be tested against after we trained a model

6.)Cache, Shuffle, and Prefetch the Dataset

7.)Building the Model
  Creating a Layer for Resizing and Normalization

  Before we feed our images to network, we should be resizing it to the desired size. Moreover, to improve model performance, we should   normalize the image pixel value (keeping them in range 0 and 1 by dividing by 256). This should happen while training as well as        inference. Hence we can add that as a layer in our Sequential Model.

  You might be thinking why do we need to resize (256,256) image to again (256,256). You are right we don't need to but this will be       useful when we are done with the training and start using the model for predictions. At that time somone can supply an image that is    not (256,256) and this layer will resize it
  
8.)Data Augmentation
  Data Augmentation is needed when we have less data, 
  this boosts the accuracy of our model by augmenting the data.

 9.)Applying Data Augmentation to Train Dataset

 10.)Compiling the Model
  We use adam Optimizer, SparseCategoricalCrossentropy for losses, accuracy as a metric

11.)  Plotting the Accuracy and Loss Curves

12.)loss, accuracy, val loss etc are a python list 
  containing values of loss, accuracy etc at the end of each epoch

  13.)Run prediction on a sample image

14.)Write a function for inference,Now run inference on few sample images
