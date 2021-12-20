# Fashion Mnist 

## Exploratory Data Analysis + Data Visualization + Deep Learning Modelling 

### 1 - Abstract

In this project I made Exploratory Data Analysis, Data Visualisation and lastly Modelling .

### 2 - Data
Fashion-MNIST is a dataset of Zalando's article images consisting of a training set of __60,000__ examples and a test set of 10,000 examples. Each example is a __28x28__ grayscale image, associated with a label from __10__ labels.Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255. The training and test data sets have 785 columns. The first column consists of the class labels (see above), and represents the article of clothing. The rest of the columns contain the pixel-values of the associated image.

* To locate a pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27. The pixel is located on row i and column j of a 28 x 28 matrix.
* For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below.

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




* __Each row is a separate image.__
* __Column 1 is the class label.__
* __Remaining columns are pixel numbers (784 total).__
* __Each value is the darkness of the pixel (1 to 255).__

### 3 - Exploratory Data Analysis

Firslty, I checked data, which came two different dataset which are train and test. Later I checked distribution of labels in datasets and I create a list for expressing images for both datasets, moreover I see all the classes(labels) equally distributed. So I dont need to do Oversampling or Undersampling. 

### 4 - Data Preprocessing

For preparing datasets to the model I made data processing which is reshaping columns from (784) to (28,28,1), and for seperate vector I save label feature then process test and train data. After that I split train set into train and validation dataset. Validation set contains %30 of original train dataset and split will be 0.7/0.03. Later this process I controlled distribution of labels in train dataset and validation dataset.

### 5 - Data Visualization

!!!  IMAGES WILL UPLOAD SOON!!!


### 6 - Modelling 


### 7 - Result & Future Work

* __Logistic Regression Score:__ 0.6460699681962744
* __K Neighbors Classifier Score:__ 0.6338028169014085
* __DecisionTree Classifier Score:__ 0.8391640163562017
* __Random Forest Classifier Score:__ 0.8727850976828714
* __AdaBoost Classifier Score:__ 0.5483870967741935
* __Gradient Boosting Classifier Score:__ 0.8714220808723308
* __XGB Classifier Score:__ 0.7878237164925034
* __ExtraTree Classifier Score:__ 0.8632439800090868
* __Bagging Classifier Score:__ 0.8514311676510677

According the scores,Random Forest Classifier gives best result with __0.872785__. Also Gradient Boosting is gives very close to Random Forest Classifier with __0.871422__, and finally AdaBoost is give the worst performance with __0.548387__. In the end Random Forest Classifier gives the best result but maybe tuning with XGB increase its score.  
