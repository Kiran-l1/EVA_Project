When we are building a convolution neural network. We need to do the basic data pre-processing that helps in processing the image faster. 
•	So, we start with Image normalization first, typically image normalization helps in achieving convergence faster.
•	We will start building the CNN with 3x3 Convolutions, they are the kernels which help in feature extraction. 
•	Typically, 3x3 convolutions & convolution layers alone won’t be sufficient due to hardware limitations. To solve this, we have introduced the transition layers which help by reducing the dimensions of the images.
•	In transitions layers, we have two major elements, MaxPooling & 1x1 Convolutions.
•	Maxpooling helps in reducing the dimensions of the images and taking the max value from the local receptive field.
•	1x1 convolution is a “feature pooling” technique which helps in dimension reduction.
•	Positioning of transition layer is done such that it is not there in the first 2-3 layers or last 2-3 layers.
•	We need to build the CNN in such a way that at that last layer the global receptive field can cover the complete input image.
•	We stop convolutions with the standard 3x3 when we are near the last layer, while there is no specific place to stop. We can manually check the images by zooming in upto 11x11 or 13x13 or a different dimension to see till where we can read/understand the image and then use a large kernel at that place. 
•	Softmax is an activation function, it is exponential and enlarges the difference pushing one result closer to 1 and others to 0.
•	Batch Normalization typically helps in having higher learning rates, networks train faster even though individual epochs take longer due to normalization calculations.
•	Dropouts are used in case of overfitting. We know overfitting is occurring when training accuracy is larger than test accuracy. So, to avoid overfitting, we drop a small percentage of nodes in each randomly to increasing the performance of the network.
•	Epochs is nothing but passing the entire dataset forward and backward once through the network. We start with a small number of epochs, however if the training accuracy is showing increasing trend and not plateauing then we increase the number of epochs
•	Batch Size is typically taken at a number of 2 power, as the memory is allocated as a 2 power. With increase in batch size the time taken for one epoch to be training decreases
•	We know that our network is doing well or not very early by looking at the second and third epoch training and test accuracy. They are a good indication of how our network will perform.
•	Learning rate controls how much we are adjusting the weights of our network wrt. Loss. 
•	Typically, lr is constant throughout the network, however ideally, we need to decrease the rate as the loss is decreasing.
•	LR Schedule is created to reduce the learning rate as the number of epochs are increased.
•	Adaptive Moment Estimation (Adam) or Stochastic Gradient Descent (SGD), they are both optimizers. Adam is faster and SGD is more generalized.
