# Convolutional-Neural-Network-using-MNIST-images

Before starting the implementation, Anaconda3 and TensorFlow is installed in the computing platform. The computational neural network is implemented in jupyter notebook using TensorFlow.
## 1. Building CNN network:

### 1.1 Input data:
Initially, all the required libraries are imported from python using commands import and from. Before loading the data, configure each of the convolutional layer by defining number of filters, size of each filter and number of neurons in the fully connected layer. The MNIST data is approximately 12 MB size and it is automatically downloaded when input_data is imported from tensorflow.examples.tutorials.mnist and then run on read_data_sets(). Calculate the class number for the test labels which is the index of one-hot encoded element and all the class-labels are one-hot encoded. Then, find the dimensions for each images, classes and channels. Since the size of MNIST images are 28 pixels by 28 pixels, flatten the image to one-dimensional array with length (28x28 =784) and define ten classes (one for each of the 10 digits). Define the number of channels as 1 (we use only gray-scale images,) and verify the input data by plotting few images and true classes of MNIST images. Create a figure with 4x4 subplots to plot 16 images and write the true and predict classes for each image.

### 1.2 TensorFlow Graph:
Build the TensorFlow graph using the following parameters.
* Variables – to optimize for better convolutional network.
* Placeholder variables – input data to the graph.
* Cost Measure – to optimize the variables.
* Mathematical Formulas – for better convolutional network.
* An optimization method which updates the variables.
         The TensorFlow graph executes much more efficiently than NumPy because the entire computational graph is known by TensorFlow graph whereas NumPy knows only the mathematical operation at a time. Variables to optimize and mathematical formulas like gradients are well known by TensorFlow graph.

### 1.3 Weights and Biases:
Weights and biases are created using tf.variable method in TensorFlow.
* tf.Variable(tf.truncated_normal(shape, stddev=0.05))
* tf.Variable(tf.constant(0.05, shape=[length])).

### 1.4 Convolutional Layer:
Create a convolutional layer method in the computational graph using input, number of channels, filter size, number of filters and input is assumed as four-dimensional tensor with these (Image number, X-axis of image, Y-axis of image, Channels of each image) dimensions. In this method, initially create shape, weights, biases and TensorFlow operation for the convolution and strides are set to one in all dimensions. For Example, if strides = [1, 2, 2, 1], it means filter is moved by 2 pixels across x-axis and y-axis. The size of the padding is set to “SAME” because the size of the output is same and add the bias-value to each of the filter-channel. If max pooling use 2x2 filter, the height and width of the image is reduced by fifty percent. Then execute the RELU (Rectified Linear Unit) which calculates max (x, 0) for each input pixel x and finally returns layer and weights. Create a flatter layer method to reduce the 4-dimension tensor to 2-dimension because the shape of the fully connected layer is only two-dimensional. Reshape the input from [image number, image height, image width, number of channels] to [image number, number of features] where the number of features is the product of image height, image width and number of channels.

### 1.5 Fully Connected Layer and Placeholder variables:
Create a fully connected layer method with 2-dimension tensor and calculate the layers using mathematical formula weight*input + biases after initializing weights and biases. Also create placeholder variables for input images and true labels. Placeholder variables are input to the TensorFlow graph. Therefore, variables can be changed each time when the graph is executed. Initially, define the placeholder variables for input image with data type float and shape [none, image_flat] (where, none refers any number of images and image_flat is the vector length of each image). Similarly create placeholder variable for the true labels of the corresponding image and class number using argmax.
