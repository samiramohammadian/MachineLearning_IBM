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
 
----

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
     - > <img width="631" alt="Screenshot 2023-05-29 at 12 39 31 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/5aefd63e-931c-49ce-8a09-9817d26d5aa3">
  - then we plug it into the slope equation to find theta 1 : 
    - > <img width="626" alt="Screenshot 2023-05-29 at 12 40 03 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/2c614313-a622-4b53-83f1-c59966a91fcc">
### Theta1 : 
> <img width="168" alt="Screenshot 2023-05-29 at 12 40 31 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/f6aa8cbd-577d-4b68-ba67-4594f7151af8">
### the polynomial of the line:
> <img width="198" alt="Screenshot 2023-05-29 at 12 40 45 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/c3636d7d-ffc1-4b48-88e2-bfce6eecc5bc">

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
> <img width="589" alt="Screenshot 2023-05-29 at 12 41 23 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/67ae9104-820f-4944-9010-50e24298744a">

- Pros of linear regression
   - Very fast
   - No parameter tuning 
   - Easy to understand, and highly interpretable
 
 

 ## Model Evaluation in Regression Models:
 
 The goal of regression is to build a model to accurately predict an unknown case. To this end, we have to perform regression evaluation after building the model: 
 
 - train and test on the same dataset :
   - when you test with a dataset in which you know the target value for each data point, you're able to obtain a percentage of accurate predictions for the model.
   - This evaluation approach would most likely have a high training accuracy and the low out-of-sample accuracy since the model knows all of the testing data points from the training.
 
 - train/test split:
   - > <img width="642" alt="Screenshot 2023-05-29 at 1 31 49 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/feb8b420-49c8-4548-a0ed-5f32f2a5b883">
   
 -  <img width="675" alt="Screenshot 2023-05-29 at 1 31 18 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/4a069878-75d2-487a-a9bd-d10b491ab75e">


-----
 ### Calculating the accuracy of a model : 
> <img width="486" alt="Screenshot 2023-05-29 at 1 30 47 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/d2c70373-42c6-4cad-a3d2-80c968466583">
----- 
### What is training & out-of-sample accuracy?
 - Training Accuracy
    - High training accuracy isn't necessarily a good thing
    - Result of over-fitting
    - <b>Over-fit</b>: the model is overly trained to the dataset, which may capture noise and produce a non-generalized model
    - 
 - Out-of-Sample Accuracy
    - It's important that our models have a high, out-of-sample accuracy
    - How can we improve out-of-sample accuracy?
 
----
### K-fold :
> <img width="634" alt="Screenshot 2023-05-29 at 1 30 25 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/ccf93d81-8224-4ec7-92d0-f192f6db2650">



 ## Evaluation Metrics in Regression Models:
 
-  We'll be reviewing a number of model evaluation metrics, including Mean Absolute Error, Mean Squared Error, and Root Mean Squared Error.
-  MAE , MSE , RMSE ,...
-  > <img width="745" alt="Screenshot 2023-05-29 at 1 42 13 PM" src="https://github.com/samiramohammadian/MachineLearning_IBM/assets/87034655/936a9aa9-be82-4590-b02f-6867739915d3">

 
 

