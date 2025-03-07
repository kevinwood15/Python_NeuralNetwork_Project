# Python_NeuralNetwork_Project
In this project, I use PyTorch to build a neural network and evaluate the CIFAR-10 dataset. 

I load the data, flatten the images, and specify a Cross Entropy loss function and Stochastic Gradient Descent optimizer. 
I train the data on a GPU accessible through Udacity, since this modeling is computationally intensive. I run 30 epochs until the test accuracy converges to around 50% (achieved at about epoch 22).
The testing loss and validation loss began to diverge around 15 to 30 epochs with an accuracy of 45%, so the model overfits to some extent. 

Overall, The model is a simple application of deep learning to image classification. I simply converted my images to tensors rather than specifying a more complication transformation with normalization, etc. 
Pursuing these more compliated transformation could improve accuracy.

My model has 5 layers, starting with an input of 3072 (3x32x32 from the tensor dimensions) and reducing down to the 10 outputs, one for each class of image. 
Each layer utilizes a rectified linear unit function. I specified a cross entropy loss function and utilized stochastic gradient descent with a learning rate of 0.1. 
The model could be improved with a more granular learning rate (for example 0.01, 0.001, ...), but this would involve more computational power.
