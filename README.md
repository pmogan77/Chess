# Chess Puzzle Rating Model
## Repository structure
This repository hosts two main notebooks. [ChessCustom.ipynb](https://github.com/pmogan77/Chess/blob/main/ChessCustom.ipynb) provides custom implementations of various regression models and then fits these models on subsets of the Lichess puzzle dataset. [ChessCustom.ipynb](https://github.com/pmogan77/Chess/blob/main/ChessCustom.ipynb) fits complimentary Scikit Learn implementations of said models. 

In order to find pretrained results of each model, images are also included in the repository to show the effectiveness of each model. Image names correspond to their appropriate model. GS is used to indicate that the result was generated using grid search on various hyperparameters. Furthermore, these optimal hyperparameters are displayed in each image.

## Custom Chess Models
In the custom chess model file, the regression schemes implemented are:

 1. Linear Regression
	 a. Closed Form solution
	 b. Gradient Descent solution
	 c. Batch fitting
	 d. L1, L2, Elastic Net Regularization
	 e. Momentum, RMSProp, ADAM optimization
 2. Logistic Regression
	 a. Gradient Descent solution
	 b. Batch fitting
	 c. L1, L2, Elastic Net Regularization
	 d. Momentum, RMSProp, ADAM optimization
 3. Polynomial Regression
	 a. Closed Form solution
	 b. Gradient Descent solution
	 c. Batch fitting
	 d. L1, L2, Elastic Net Regularization
	 e. Momentum, RMSProp, ADAM optimization
 4. Locally Weighted Polynomial Regression
	 a. Closed Form solution
	 b. Gradient Descent solution
	 c. L1, L2, Elastic Net Regularization (L1 and Elastic Net only work for gradient descent solution)
	 d. Momentum, RMSProp, ADAM optimization
 5. KNN Regression
	 a. Configurable K value
 6. Regression Tree
	 b. Configurable max depth, min samples per leaf, max threshold, and min SSE for split

## Scikit Learn Chess Models

 1. Linear Regression
 2. Polynomial Regression
 3. Random Forest Regression
 4. Support Vector Regression (Bagged)
	 a. Grid Search on C, gamma, and kernel
 5. Gradient Boosting Regression
	 a. Grid Search on number of estimators, learning rate, and max depth
 6. AdaBoost Regression
	 a. Grid Search on number of estimators, learning rate, and loss
 7. XGB Regression
	 a. Grid Search on number of estimators, learning rate, and max depth 
 8. SGD Regression
	 a. Grid Search on alpha, l1 ratio, max iterations, tolerance, and penalty
 9. KNN Regression
	 a. Grid Search on number of neighbors, weights, metric, and p 

## Result Interpretation
Results are shown in 4 ways: mean squared error, mean average error, line graph, and scatter plot. The mean squared error is in terms of squared ELO. The mean absolute error is in terms of ELO. The line graph plots the ascending sort of data points and then their corresponding predictions. The scatter plot graphs the actual rating against the predicted rating for each data point. A y=x line is also introduced to visualize each model's comparison against an ideal model.
