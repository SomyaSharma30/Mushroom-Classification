# Mushroom-Classification
Mushroom Data Set Classification
Using Decision Tree, Random Forest, Naive Bayes Classifiers


Data set source: https://datarepository.wolframcloud.com/resources/Sample-Data-Mushroom-Classification

Data Preprocessing:

Data preprocessing is an important aspect of Machine Learning. It improves data quality which accelerates the accuracy, consistency, interpretability of our preprocessed data.
Steps involved in data preprocessing 

Data Cleaning: to remove noise and inconsistent data
Data Integration: where multiple data sources may be combined
Data selection: where data relevant to the analysis task are retrieved from the databases
Data Transformation: where data are transformed and consolidated into forms appropriate for applying machine learning algorithms

For the given Data Set:
It has a total of 24 attributes
Nominal Attributes
CapShape
CapSurface
CapColor
Odor
GillColor
StalkRoot
StalkSurfaceAboveRing
StalkSurfaceBelowRing
StalkColorAboveRing
StalkColorBelowRing
VeilColor
RingNumber
RingType
SporePrintColor
Population
Habitat

Binary Attributes
Bruises
GillAttachment
GillSpacing
GillSize
StalkShape
Class

Since Vell Type has only one data object, we can exclude it 
Stalkroot has more than 2000 missing values, so we can exclude it 
After taking care of Data  integration, selection, and cleaning, the next step is Encoding our data 
We encode all the data using LabelEncoder() from sklearn.preprocessing package
As Machine learning models require all input and output variables to be numeric, Encoding is an important step of data preprocessing


Training and Validation of the model 

We split data into three parts Train, Validation, Test
Then we use three classification models Decision Tree Classifier, Random Forest Classifier, and Naive Bayes on our data set

Decision Trees are constructed via an algorithmic approach that identifies ways to split a data set based on different conditions. It is one of the most widely used and practical methods for supervised learning. Decision Trees are a non-parametric supervised learning method used for both classification and regression tasks.

A Random Forest is a meta estimator that fits a number of decision tree classifiers on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. The sub-sample size is controlled with the max_samples parameter if bootstrap=True (default), otherwise the whole dataset is used to build each tree.

Naive Bayes classifiers are a collection of classification algorithms based on Bayes' Theorem. It is not a single algorithm but a family of algorithms where all of them share a common principle, i.e. every pair of features being classified is independent of each other.

We use hyperParameter selection (GridsearchCV) to find the best hyperparameter set
Then we fit the model using train set and check  their accuracy on the validation set
 The accuracy of the models on the validation set came out to be: Decision tree - 100%, Random Forest Classifier - 100%, and Naive Bayes - 86%

Testing of Model

The final accuracy after testing the models are: Decision Tree -100% and Random Forest Classifier - 100%
