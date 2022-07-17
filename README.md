## CAR PRICE PREDICTION

**Project report submitted to the Amrita Vishwa Vidyapeetham in partial fulfilment of the**

```
requirement for the Degree of
```
#### B.Tech. Computer Science and Engineering

#### Artificial Intelligence


### Submitted by:
```
Abhinav Pandey (AM.EN.U4AIE21088)
Abhishek. A. (AM.EN.U4AIE21003)
Anfas Hassan V (AM.EN.U4AIE21014)
Aravind MJ (AM.EN.U4AIE21017)
Rithesh R (AM.EN.U4AIE21054)
D.S.S. Sandeep Chandra (AM.EN.U4AIE21079)
```
#### July 2021


##### DEPARTMENT OF COMPUTER SCIENCE AND ENGINEERING AMRITA

##### VISHWA VIDYAPEETHAM

##### (Estd. U/S 3 of the UGC Act 1956)

##### Amritapuri Campus Kollam -

##### DEPARTMENT OF COMPUTER SCIENCE & ENGINEERING AMRITA VISHWA

##### VIDYAPEETHAM

##### (Estd. U/S 3 of the UGC Act 1956)

##### Amritapuri Campus Kollam 


## DECLARATION

##### We, Abhinav Pandey, Abishek A., Anfas Hassan, Aravind MJ, Rithesh R, D.S.S.

##### Sandeep Chandra hereby declare that this project entitled CAR PRICE PREDICTION is

##### a record of the original work done by us under the guidance of DR GEORG GUTJAHR

##### and DR GOPAKUMAR G , Dept. of Computer Science andEngineering, Amrita Vishwa

##### Vidyapeetham, that this work has not formed the basis for any

##### degree/diploma/associations/fellowship or similar awards to any candidate in any university

##### to the best of our knowledge.

##### Place: Amritapuri Date: 12 July 2022

##### Signature of the student Signature of the Project Guide


## ACKNOWLEDGEMENTS

### Humble pranams at the lotus feet of Amma, Sri Mata

### Amritanandamayi devi

##### We thank Dr Georg Gutjahr, Department of Computer Science and Engineering, Amrita

##### Vishwa Vidyapeetham, for her timely advice and constructive suggestions. We thank the

##### faculty of the CSE Department for giving us an opportunity to explore our capabilities and

##### widen our knowledge. We also thank our team members for their cooperation and hard

##### work put into this project. We also thank our batch mates for their support and our parents

##### for their support and encouragement.


## INTRODUCTION

###### An automobile company is entering the market and it is planning to set up a

###### manufacturing unit here. It also plans to produce cars locally to give competition to

###### existing companies. They have planned to do a contract with an automobile consulting

###### company to understand the factors on which the pricing of the cars depends.

###### Specifically, they want to understand the main features about a car that has more effect

###### on its pricing.

###### The company wants to know:

###### ● Which variables are significant in predicting the price of a car

###### ● How well those variables describe the price of a car

###### In our project we have planned to solve the same problem. We want to model the price

###### of cars with the available independent variables. We have split every model into a

###### training and testing set. We have used independent variables in the training set to

###### predict the price and correspondingly check the accuracy of the models with the actual

###### price in the testing set. We have made 12 different models and fit single as well as

###### multi variables in that model according to analysis. We have used many python

###### libraries such as sklearn, matplot, seaborn, etc.

###### This provides a solution for the company to manage and understand the variation of

###### prices with the variables. They can accordingly manipulate the design of the cars, the

###### business strategy etc to meet certain price levels. Further, the model will be a good

###### way for management to understand the pricing dynamics of a new market.


## DATA SET

###### Our dataset consists of 205 rows and 26 columns. The rows include the no of data per

###### car. The column includes independent variables or features of the car. The variables

###### are:

```
● Car id:
The id of the car given
Data type: int
Examples: 205, 103
```
```
● Symboling:
The degree to which the auto is more risky than its price indicates.
Data type: int
Examples: 3,2,
```
```
● Car Name :
The name of the car
Data type: object
Examples: alfa romeo stelvio, audi 100 ls
```
```
● Fuel type :
The type of fuel used in the engine
Data type: object
Examples: gas, diesel
```
```
● Car body :
Its the vehicle frame of the car
Data type: object
Examples: convertible,sedan
```
```
● Drive wheel :
Wheel and tire assembly that pushes or pulls a vehicle down the road.
Data type: object
Examples: fwd,rwd,awd
```
```
● Engine location :
The location of engine
Data type: object
Examples: front,rear
```
```
● Wheel base :
The horizontal distance between the centers of the front and rear wheels.
Data type: float
Examples: 172.2, 176.
```
```
● Car length , width and height:
The dimensions of the car
Data type: float
Examples: 168.8, 64.1, 48.
```

```
● Curb weight :
The weight of the vehicle including a full tank of fuel and all standard equipment
Data type: int
Examples: 2548, 2823
```

```
● Engine type :
The type of the engine
Data type: int
Examples: dohc,ohcv
```

```
● Cylinder number :
The number of cylinders in the car
Data type: object
Examples: four,eight
```

```
● Engine size :
The size of the engine
Data type: int
Examples: 90,
```

```
● Fuel system :
The system used in the car
Data type: object
Examples: mpfi,2bbl
```

```
● Bore ratio :
The ratio of bore to stroke
Data type: float
Examples: 3.47,2.
```

```
● Stroke :
A phase of the engine's cycle , during which the piston travels from top to bottom or vice
versa.
Data type: float
Examples: 3.47,2.
```

```
● Horsepower :
Power produced in a car
Data type: int
Examples: 154,
```

```
● Price :
The price of the specific car
Data type: float Examples: 13950 , 17450
```

## METHODOLOGY

Approach for car price prediction proposed in this paper is composed of several steps as shown

###### Data is collected from a dataset from Kaggle. It consists of 205 rows each of the car

###### and its information. It includes columns such as fueltype, horsepower, cylinder

###### number etc. But this data was not ready to be used. We have to filter and process the

###### data before we put regression on it. We first understood the structure and features of

###### the data.

###### Firstly, the company names of the cars were very vast. So, we have filtered the names

###### of cars with the actual names of the company. For instance,alfa-romeo giulia and


###### alfa-romeo stelvio arecars from same company but different name. We have only

###### considered the company name like alfa romeo.

###### Second task was to remove any errors. The company names were misspelt which

###### made them different data. So, we corrected some names as show:

```
● maxda = mazda
● Nissan = nissan
● porsche = porcshce
● toyota = toyouta
● vokswagen = volkswagen = vw
```
###### Third task was to remove the duplicates from the dataset if there were any. Fourth and

###### main task was to encode our data. We have a lot of strings in our data, but our

###### regression model cannot take strings as an input. So, we used labelEncoder to

###### transform string into int value according to the set. Now our data is filtered and ready

###### to be used.

###### We move on to data analysis and visualisation. We crossed checked every independent

###### variable and how it varies in the data set with the price. We have visualised the spread

###### of the variable with the price and accordingly selected the variable for the model.


###### ● The plot seemed to be right-skewed, meaning that the most prices in

###### the dataset are low(Below 15,000).

###### ● There is a significant difference between the mean and the median of

###### the price distribution.

###### ● The data points are far spread out from the mean, which indicates a

###### high variance in the car prices.(85% of the prices are below 18,500,

###### whereas the remaining 15% are between 18,500 and 45,400.

###### In the histogram bar graph, we can see that there is much variation in the company

###### name but the fuel type histogram is not useful as there are only two types petrol and

###### diesel.


###### Here we can analyse how much the different types of engines are varying the prices.

###### Third engine type is the most used of all the data. But the fifth is the one which has

###### highest price range and others have low price range.


###### Door-number variable is not affecting the price much. There is no significant

###### difference between the categories in it. It seems aspiration with turbo has a higher

###### price range than the std(though it has some high values outside the whiskers)


###### carwidth, carlength and curbweight seems to have a positive correlation with

###### price. carheight doesn't show any significant trend with price.

###### Now that we’ve analysed the data, we have to fit the data in the models. We’ve

###### used 12 models. 6 of them are of single variables like highwaympg, citympg,

###### horsepower, enginesize, wheelbase and boreratio. Some showed less accuracy, so

###### we are going to further use the ones which show more accuracy and less MSE.

###### Then there are 5 models which are made to test combined variables.

###### We have used the sklearn python library to split the testing and training set. There

###### is a separate table for actual price for testing of the models. We first define the

###### model, put our variable or combined variables in it and then determine the size of

###### the testing set. We have also imported LinearRegression from sklearn and used

###### that to predict the prices from the model. Then we test it in the testing set. We

###### calculate the mean squared error of the predicted and actual prices of cars. We

###### also determine the accuracy of the model.

##### Example:

##### Model(Prediction using enginesize):


## RESULTS

###### ● Prediction using highway mpg

###### ● Prediction using citympg

###### ● Prediction using horsepower

###### ● Prediction using enginesize


###### ● Prediction using wheelbase

###### ● Prediction using boreratio

###### ● Prediction using enginesize and boreratio

###### ● Prediction using enginesize and horsepower


###### ● Prediction using stroke, horsepower, enginesize

###### ● Prediction using boreratio, horsepower and enginesize

###### ● Prediction using boreratio, horsepower, enginesize and stroke


## CONCLUSION

###### Car price prediction can be a challenging task due to the high number of attributes

###### that should be considered for the accurate prediction. The major step in the

###### prediction process is collection and preprocessing of the data. In this research,

###### PHP scripts were built to normalise, standardise and clean data to avoid

###### unnecessary noise for linear regression.Then after analysing the fitting the data in

###### the models, we used it in the testing and training sets and analysed which

###### performed better.

## REFERENCES

Dataset:https://www.kaggle.com/code/goyalshalini93/car-price-prediction-linear-regression-rfe

Python Libraries:

https://scikit-learn.org/stable/

https://numpy.org

https://numpy.org

https://seaborn.pydata.org

Colab link:
https://colab.research.google.com/drive/1INp_tTRYZTZeJJY1HKyBumMJnmi2AVl9?usp=sharing


