# R-programing-laguage--PLS60---5th-GE

Topic B/2:    R : Decision Trees and Support Vector Machines
-------------------------------------------------------------

B2. Show in R code the creation of the training set based on your answer to
question B1 and the creation of the predictive model of the next value of
sequence based on the algorithms: Decision Trees and Support Vector Machines. Then run the algorithm
and briefly comment on their performance in prediction, if you know
that the actual next value of the sequence is 31.3.
performance criterion is the absolute value of the difference between the prediction of the algorithm and the
actual value. Were all the algorithms able to achieve a prediction with a small deviation
from the true value? Why is it considered that any algorithm(s) underperformed?
(if, of course, this is what happened).

Hint: use the functions svm (from the {e1071} package), tree (from the package of the same name) and predict to train and invoke a support model
vector machines and decision tree respectively. For the linear regression algorithm use the lm function.




Topic C /2 :   R:  Discovery of Correlation Rules
-----------------------------------------------

C2. For the transaction table below, 

ID, Songs
1,ThisLove,7Days, WonderWall
2,WonderWall, Torn, ThisLove
3,ThisLove,7Days, BeatIt
4,WonderWall, Torn, BillieJean,7Days
5,BillieJean, BeatIt,7Days
6,ThisLove, WonderWall
7,WonderWall, Torn,7Days
8,BillieJean,7Days
9,ThisLove,7Days, WonderWall, Torn
10,BillieJean, BeatIt, ThisLove, WonderWall

using R, you are asked to view all the closed frequent elementary modules as well as the association rules that
resulting, assuming a support threshold of 0.5 and a confidence threshold of 0.5
respectively (to show the result of running the appropriate command).
Hint: you will need the {arules} package. You will create a songList.csv file with
separator of all "," (comma) and use the function
read.transactions() to read it correctly as a set of transactions.

Topic D: Clustering with the k-means algorithm and DBSCAN
---------------------------------------------------------
In this exercise we will deal with two clustering algorithms, k-means
and DBSCAN. To see their specifics we will use a synthetic corpus
data that simulates ring clusters. We will use the synthetic.csv file with
this dataset, which is provided with the pronunciation. After the
save it in a folder of your choice locally on your computer, you will load it
in R and visualize it using the following commands, after installing the
{readr}, {ggplot2}, {cluster} and {dbscan} libraries:
library(readr)
library(ggplot2)
library(gggplot(gggdr), library(cluster)
library(dbscan)
synthetic <- read_csv("[your folder]/synthetic.csv")
qplot(synthetic$att1, synthetic$att2, color = synthetic$label, data = synthetic)
As you will notice, the data is indeed (almost) organized into 3 clusters,
the core, the first_ring and the second_ring.

According to the theory (paragraph 7.2.5 from the book), the k-means algorithm is not
suitable for all types of data. Let us see how it deals with
specific data, for k=3:
kmeansCluster <- kmeans(synthetic[,1:2], center=3)
qplot(synthetic$att1, synthetic$att2, color = as.character(kmeansCluster$cluster),data =
synthetic). 
Indeed, the algorithm could not correctly cluster the data because of the
the shape of the original clusters.

D1 : Apply the DBSCAN algorithm by testing different parameters eps=
[0.5, 1, 2 or 3], minPts=[5, 15, or 20] and print a graph like the one above
showing whether DBSCAN is correctly clustering the data. Indicate for which
eps and minPts parameters achieved the best result.
Hint: use the functions and libraries listed in
The use of the libraries and libraries mentioned in the pronunciation, no other is needed.

D2: The given format of the data makes it impossible for the correct clustering by the
k-means algorithm. However, if you look more closely at the data, it can be used with a simple
trick can work perfectly. Create a new column in your data, named
mystery that calculates for each row the Euclidean distance from the origin
of the axes (0,0). Then run the k-means algorithm based only on this new column
and print the graph with the result of the clustering.
Hint: use the functions and libraries mentioned in
the pronunciation, you do not need any other.



