# Regression 
week2

##  introduction to regression: 
 
- Regression is the process of preicting a continuous value . 
- In regression there are two types of variables: a dependent variable and one or more independent variables.
  - The dependent variable can be seen as the state, target, or final goal we study and try to predict. (Y)
  - independent variables, also known as explanatory variables, can be seen as the causes of those states. (X)
  
>  <img width="645" alt="Screenshot 2023-05-29 at 10 47 07 AM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/40b45d63-2cc9-46bf-b763-3e83a6178e49">


+ The key point in the regression is that our dependent value should be continuous and cannot be a discrete value. However, the independent variable, or variables, can be measured on either a categorical or continuous measurement scale. 

- Type of Regression model : 

  - Simple Regression: 
    - Simple Linear Regression
    -  Simple Non-Linear Regression
    -  
  - Multiple Regression:  --> be more than an independent comparison in the process
    - Multiple Linear Regression
    - Multiple Non-Linear Regression

- Applications of regression : 
   - Sales forecasting
   - Satisfaction analysis
   - Price estimation
   - Employment income

- Regression algorithms
  - Ordinal regression
  - Poisson regression
  - Fast forest quantile regression
  - Linear, Polynomial, Lasso, Stepwise, Ridge regression
  - Bayesian linear regression
  - Neural network regression
  - Decision forest regression
  - Boosted decision tree regression
  - KNN (K-nearest neighbors)
 

##  Simple Linear Regression:
 
 - the Co2 emission of different cars -> It includes engine size, cylinders, fuel consumption and Co2 emissions for various car models.

- we have two Linear regression topology :
 
   - Simple Linear Regression:
     - Predict <b>co2emission</b> vs <b>EngineSize</b> of all cars
       - Independent variable (x): EngineSize
       - Dependent variable (y): co2emission
   
   - Multiple Linear Regression:
     - Predict <b>co2emission</b> vs <b>EngineSize</b> and <b>Cylinders</b> of all cars
       - Independent variable (x): EngineSize, Cylinders, etc
       - Dependent variable (y): co2emission
   
 
 > <img width="635" alt="Screenshot 2023-05-29 at 12 34 48 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/b5a2d6e7-d52b-4ccd-a3ff-8251f3414658">
 

 ### FIT LINE: 
> <img width="781" alt="Screenshot 2023-05-29 at 11 58 01 AM 2 2" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/32e165c9-b4a9-4ac1-8bb8-dfb187ba0aac">
- we must calculate theta 0 and theta 1 to find the best line to fit the data.
------
> <img width="609" alt="Screenshot 2023-05-29 at 12 35 55 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/55092079-a098-4b91-9da4-93302752c0ff">
- MSE : Mean Squared Error that should be minimized .  ->  we should find the best parameters theta 0 and theta 1 :
  - we have two options here: 
    -  Option one, we can use a mathematic approach, 
    -  or option two, we can use an optimization approach
 ----- 
### Theta 0:
  -  we calculate the mean of the independent and dependent or target columns from the data set: 
     - > <img width="832" alt="Screenshot 2023-05-29 at 12 16 13 PM" src="https://github.com/samiramohammadian/MachineLearningWithPython_IBM/assets/87034655/1be1b4f7-98b2-47df-954d-cd531cfa5186">
  - then we plug it into the slope equation to find theta 1 : 
    - > <img width="824" alt="Screenshot 2023-05-29 at 12 17 20 PM" src="https://github.com/samiramohammadian/MachineLearningWithPython_IBM/assets/87034655/3847f6b5-4468-4185-a9eb-8fc90143bee8">
### Theta1 : 
> <img width="220" alt="Screenshot 2023-05-29 at 12 18 19 PM" src="https://github.com/samiramohammadian/MachineLearningWithPython_IBM/assets/87034655/6916205c-1fcd-4ba7-89e6-edda55a706b1">
### the polynomial of the line: 
> <img width="254" alt="Screenshot 2023-05-29 at 12 20 36 PM" src="https://github.com/samiramohammadian/MachineLearningWithPython_IBM/assets/87034655/acb768a5-4dbe-43f4-a473-061c306ee30e">
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 <img width="794" alt="Screenshot 2023-05-29 at 12 24 51 PM" src="https://github.com/samiramohammadian/MachineLearningWithPython_IBM/assets/87034655/20a4ecaf-e8c4-4011-8baf-8ba0ce85aacc">

- Pros of linear regression
   - Very fast
   - No parameter tuning 
   - Easy to understand, and highly interpretable
 
 




