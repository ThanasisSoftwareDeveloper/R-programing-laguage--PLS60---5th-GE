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


