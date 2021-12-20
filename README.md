# Fashion Mnist 
Context
 Zalando intends Fashion-MNIST to serve as a direct drop-in replacement for the original MNIST dataset for benchmarking machine learning algorithms. It shares the same image size and structure of training and testing splits.

The original MNIST dataset contains a lot of handwritten digits. Members of the AI/ML/Data Science community love this dataset and use it as a benchmark to validate their algorithms. In fact, MNIST is often the first dataset researchers try. "If it doesn't work on MNIST, it won't work at all", they said. "Well, if it does work on MNIST, it may still fail on others."

Zalando seeks to replace the original MNIST dataset

Content
Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255. The training and test data sets have 785 columns. The first column consists of the class labels (see above), and represents the article of clothing. The rest of the columns contain the pixel-values of the associated image.

To locate a pixel on the image, suppose that we have decomposed x as x = i * 28 + j, where i and j are integers between 0 and 27. The pixel is located on row i and column j of a 28 x 28 matrix.
For example, pixel31 indicates the pixel that is in the fourth column from the left, and the second row from the top, as in the ascii-diagram below.




TL;DR


## Exploratory Data Analysis + Data Visualization + Deep Learning Modelling 


### 1 - Abstract

In this project I made Exploratory Data Analysis, Data Visualisation and lastly Modelling which I did with 9 different models. In Exploratory Data Analysis I cleaned irrelevant data,NaN values and change data types for easiness. In second part, I would like to show data in plots.Such as, number of places according to their types and according to province. Later these processes I looked Pearson Correlation and Spearman Correlation which they gave very similar result as expected. Before modelling I prepared data training and testing. My testing size is __0.33__. Then I applied for each model, the algorithms I used for these project are Logistic Regression, K Neighbors Classification, Decision Tree Classification, Random Forest Classification, AdaBoost Classification, Gradient Boosting Classification, XGB Classification, ExtraTrees Classification, Bagging Classification. Finally, Random Forest Classifier gives the best result but tuning with algorithms or cleaning the data more(I believe it will decrease the size of dataset alot) can be effective.

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

Firslty, I checked data types and number of Nan in each columns. Later this process I decided which columns I will delete and which rows should I delete. So I deleted *LOCALITA - SPORT - CONGRESSI - LATITUDINE - LONGITIDUNE* columns and I deleted in NaN rows in *IN_ABITATO -SUL_LAGO - VICINO_ELIPORTO - VICINO_AEREOPORTO - ZONA_CENTRALE - VICINO_IMP_RISALITA - ZONA_PERIFERICA - ZONA_STAZIONE_FS* columns. But I keep 3 columns which contains very high number of NaN values because data they contains could be helpful for future works. 

### 4 - Data Visualization

!!!  IMAGES WILL UPLOAD SOON!!!


### 5 - Modelling 

* __5.1 - Logistic Regression__
is used to predict the categorical dependent variable using a given set of independent variables. 
* __5.2 - K Neighbors Classification__
non-parametric classification method.
* __5.3 Decision Tree Classification__
breaks the data smaller subsets in form of tree structure
* __5.4 - Random Forest Classification__
consist many decision tree but using bagging and randomness. then look at average/voting and gives the result.
* __5.5 - AdaBoost Classification__
is an meta-estimator, that begins by fitting a classifier on the original dataset and then fits additional copies of the classifier on the same dataset.
* __5.6 - Gradient Boosting Classification__
combine weak learning models to create strong model 
* __5.7 - XGB Classification__
implementation of gradient boosted decision trees but more effective in performance.
* __5.8 - ExtraTrees Classification__
implements a meta-estimator which fits number of random decision trees on various subsets of dataset and it uses average/voting to improve prediction.
* __5.9 - Bagging Classification__
an ensemble meta-estimator that fits base classifiers each on random subsets of the original dataset and then aggregate their individual predictions  to form a final prediction.

### 6 - Result & Future Work

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
