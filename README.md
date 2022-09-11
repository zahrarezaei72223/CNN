# CNN
My project topic is "CNN image classification"
In this project,for dataset, I used CIFAR-10 Dataset, as it suggests, has 10 different categories of images in it. There is a total of 60000 images of 10 different
classes naming "Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship,and Truck". All the images are of size 32×32. There are in total 50000 train images
and 10000 test images.
I'm aiming to do classification using the VGG (VGG 16) model from scratch and apply all methods for increasing the performance (pre-processing, Dropout, Augmentation,
Batch Normalization,..) and at the end running a pre-trained  "Resnet" model as a transfer learning. 
VGG model Contains some main blocks and a final block that each block contains:
two Convolutional layer with a 3x3 filter and
Max-pooling to reduce volume size and final layer.
About my data, I should say, I cannot be sent it directly to my neural network. I need to process the data in order to send it to the network. 
The first thing in the process is to reduce the pixel values. Currently, all the image pixels are in a range from 1-256, and I need to reduce those values to a value
ranging between 0 and 1. This enables my model to easily track trends and efficient training. I can do this by dividing all pixel values by 255.0.
Another thing I want to do is to flatten the label values, that means(rearrange them in form of a row) by the flatten() function. 
For visualization, I used the subplot() function from matplotlib. For building my model, I used a Convolution Neural Network or CNN to train my model; it includes
using a convolution layer in this which is Conv2d layer as well as pooling and normalization methods. In the last, I had passed it into a dense layer 
and the final dense layer which is my output layer. I used ‘relu‘ activation function. The output layer uses a “softmax” function.
I used model.compile() function to compile my model. 
For the parameters, I used "adam optimizer","sparse_categorical_crossentropy as the loss function" and
metrics=[‘accuracy’].
The model will start training for 100 epochs and the Batch size is 128.
For the prediction part, I made a prediction over an image from my model using model.predict() function. Since I used data from the dataset,
I can compare the predicted output and original output.  
In the powerpoint as you can see, I compared Standardization vs. Normalization and showed how the Standardization had more useful impact.
I also, showed how using Data Augmentation increases the accuracy and Batch Normalization reduces the over fitting and so on..
In the second implementation, I used "Data Augmentation", "Data Normalization", "Regularization" and finally apply "Parameter initialization" that all the details
are in my code part.
