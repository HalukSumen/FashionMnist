# Fashion Mnist 

## Exploratory Data Analysis + Data Visualization + Deep Learning Modelling 

### 1 - Abstract

In this project I made Exploratory Data Analysis, Data Visualisation and lastly Modelling .

### 2 - Data
Fashion-MNIST is a dataset of Zalando's article images consisting of a training set of __60,000__ examples and a test set of 10,000 examples. Each example is a __28x28__ grayscale image, associated with a label from __10__ labels.Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255. The training and test data sets have 785 columns. The first column consists of the class labels (see above), and represents the article of clothing. The rest of the columns contain the pixel-values of the associated image.

* To locate a pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27. The pixel is located on row i and column j of a 28 x 28 matrix.
* For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below.
* Each row is a separate image.
* Column 1 is the class label.
* Remaining columns are pixel numbers (784 total).
* Each value is the darkness of the pixel (1 to 255).

Each training and test example is assigned to one of the following labels:

* __0 T-shirt/top__
* __1 Trouser__
* __2 Pullover__
* __3 Dress__
* __4 Coat__
* __5 Sandal__
* __6 Shirt__
* __7 Sneaker__
* __8 Bag__
* __9 Ankle boot__

### 3 - Exploratory Data Analysis

Firslty, I checked data, which came two different dataset which are train and test. Later I checked distribution of labels in datasets and I create a list for expressing images for both datasets, moreover I see all the classes(labels) equally distributed. So I dont need to do Oversampling or Undersampling. 

### 4 - Data Preprocessing

For preparing datasets to the model I made data processing which is reshaping columns from (784) to (28,28,1), and for seperate vector I save label feature then process test and train data. After that I split train set into train and validation dataset. Validation set contains %30 of original train dataset and split will be 0.7/0.03. Later this process I controlled distribution of labels in train dataset and validation dataset.

### 5 - Data Visualization

!!!  IMAGES WILL UPLOAD SOON!!!

### 6 - Modelling 

I used Sequential model. The sequential model is appropriate for a plain stack of layers where each layer has exactly one input tensor and one output tensor. Then I add Conv2D layer, MaxPooling2D, Flatten and Dense. For each layer I used these parameters.

__Conv2D__
* filters = 32
* kernel_size = (3,3)
* activation function = relu 
* kernel_initializer = normal
* input_shape = (28,28,1)

__MaxPooling2D__
* pool_size = (2,2)


__Conv2D__
* filters = 64
* kernel_size = (3,3)
* activation function = relu 

__Flatten__
* A flatten operation on a tensor reshapes the tensor to have the shape that is equal to the number of elements contained in tensor non including the batch dimension and doesnt need any parameters.

__Dense__
In first Dense Layer,
* units = 128
* activation function = relu
In second Dense Layer,
* units = 10
* activation function = softmax

### 7 - Result & Future Work
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
