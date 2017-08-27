# Convolutional-Neural-Network-using-MNIST-images

Before starting the implementation, Anaconda3 and TensorFlow is installed in the computing platform. The computational neural network is implemented in jupyter notebook using TensorFlow.
## 1. Building CNN network:

### 1.1 Input data:
Initially, all the required libraries are imported from python using commands import and from. Before loading the data, configure each of the convolutional layer by defining number of filters, size of each filter and number of neurons in the fully connected layer. The MNIST data is approximately 12 MB size and it is automatically downloaded when input_data is imported from tensorflow.examples.tutorials.mnist and then run on read_data_sets(). Calculate the class number for the test labels which is the index of one-hot encoded element and all the class-labels are one-hot encoded. Then, find the dimensions for each images, classes and channels. Since the size of MNIST images are 28 pixels by 28 pixels, flatten the image to one-dimensional array with length (28x28 =784) and define ten classes (one for each of the 10 digits). Define the number of channels as 1 (we use only gray-scale images,) and verify the input data by plotting few images and true classes of MNIST images. Create a figure with 4x4 subplots to plot 16 images and write the true and predict classes for each image.
