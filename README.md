Assignment #3

1) (25 Points) Principal Component analysis (PCA)

Use Principal component analysis to summarize a multitude of health indicators into a more condensed representation. The county health rankings initiative (https://www.countyhealthrankings.org/) regularly collects health data about all counties across the USA.  There are a large number of variables and it is sometimes difficult to get a clear picture of the differences between counties. In this exercise we use PCA to come up with a more efficient representation of the county health data and then we plot the Maine counties using this representation.

Start by reading, running, and carefully looking over this notebook : https://github.com/bruceMacLeod/COS475-575/blob/main/Assignment/CHR.ipynb. Make a copy and call it CHR-PCA
For all columns, fill in missing values with the median and normalize the data by subtracting mean and dividing by the standard deviation (hint : you have done this before).
Run Principal component analysis with 5 components on the transformed data
Produce a graph that plots the ratio of explained variance (attribute of pca)  (sometimes called a skee plot).
Construct a dataframe with the principal component values for all maine counties. The head of this Dataframe should look something like :
 chr-pca-df

Obtain the values of the first two components for each of the Maine counties and plot them. Provide your observations on the plot. A picture may help :
 PCA
2) (25 Points) KMeans
Make a copy of the https://github.com/bruceMacLeod/COS475-575/blob/main/Assignment/CHR.ipynb notebook and call it PCR-KMEANS
For all columns, fill in missing values with the median and normalize the data by subtracting mean and dividing by the standard deviation (hint : you have done this before).
Run KMEANS with 5 clusters on the data
Print out the clusters that each Maine county landed in. Observations ?
Produce a few 2D graphs that plot two attribute values (ie v001, v036 : premature death, poor physical days) for Maine counties and color the counties to distinguish the group. A picture may help : kmeans
Run KMeans for a different number of clusters and plot the within cluster sum of squares (WCCS) (y-axis) as function of the number of clusters (x-axis).  Was 5 a good choice for the number of clusters ?
3) (25 Points) Neural Networks
Make a copy of the https://github.com/bruceMacLeod/COS475-575/blob/main/Assignment/CHR.ipynb notebook and call it PCR-NN
For all columns, fill in missing values with the median and normalize the data by subtracting mean and dividing by the standard deviation (hint : you have done this before).
We will attempt to predict Premature death (v001_rawvalue) from the remaining attributes. Remove any rows that do not have values for v001_rawvalue. Assign X and y variables.
Create training, validation, and test datasets
Run a linear regression on the data and compute the root mean squared error (this will be a value that we will try to beat with our NN)
Develop and train a Neural Network to predict premature death from the independent values.  Test the performance of the network against your validation set.  Experiment with different configurations (#, size of the layers). 
Choose the best network from the above and evaluate the performance against the test dataset. Did you manage to beat the linear regression result ? 
Post your network & the rmse on slack !
4) (25 Points) Continue Data exploration
a) Locate or build a dataset that you are interested in that has not been analyzed in a data science competition.  You can do this in a number of ways :

beginning of chapter 2 has a list of repositories
google search
find research papers with associated datasets
build your own ! This could include creating your own data, linking data together that has not been linked before, or pulling data or images together from google search.
b) Describe your dataset in the homework submission and describe what you would might like to do for analysis.
c) Put this dataset into your github repository and provide a link in your writeup
Handin :
Submit the three notebooks and the writeup for Problem 4 to Brightspace.
