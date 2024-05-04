# Chess Puzzle Rating Model

## Repository Structure

This repository hosts three main notebooks. [ChessCustom.ipynb](https://github.com/pmogan77/Chess/blob/main/ChessCustom.ipynb) provides custom implementations of various regression models and then fits these models on subsets of the Lichess puzzle dataset. [ChessScikit.ipynb](https://github.com/pmogan77/Chess/blob/main/ChessScikit.ipynb) fits complimentary Scikit Learn implementations of said models. [NeuralNet.ipynb](https://github.com/pmogan77/Chess/blob/main/NeuralNet.ipynb) provides the code for most of the feature extraction done on the board. Afterwards, a neural network is fit onto the dataset using Pytorch.

In order to find pretrained results of each model, images are also included in the repository to show the effectiveness of each model. Image names correspond to their appropriate model. GS is used to indicate that the result was generated using grid search on various hyperparameters. Furthermore, these optimal hyperparameters are displayed in each image.

## Custom Chess Models

In the custom chess model file, the regression schemes implemented are:

1. Linear Regression
    - Closed Form solution
    - Gradient Descent solution
    - Batch fitting
    - L1, L2, Elastic Net Regularization
    - Momentum, RMSProp, ADAM optimization
2. Logistic Regression
    - Gradient Descent solution
    - Batch fitting
    - L1, L2, Elastic Net Regularization
    - Momentum, RMSProp, ADAM optimization
3. Polynomial Regression
    - Closed Form solution
    - Gradient Descent solution
    - Batch fitting
    - L1, L2, Elastic Net Regularization
    - Momentum, RMSProp, ADAM optimization
4. Locally Weighted Polynomial Regression
    - Closed Form solution
    - Gradient Descent solution
    - L1, L2, Elastic Net Regularization (L1 and Elastic Net only work for gradient descent solution)
    - Momentum, RMSProp, ADAM optimization
5. KNN Regression
    - Configurable K value
6. Regression Tree
    - Configurable max depth, min samples per leaf, max threshold, and min SSE for split

## Scikit Learn Chess Models

1. Linear Regression
2. Polynomial Regression
3. Random Forest Regression
4. Support Vector Regression (Bagged)
    - Grid Search on C, gamma, and kernel
5. Gradient Boosting Regression
    - Grid Search on number of estimators, learning rate, and max depth
6. AdaBoost Regression
    - Grid Search on number of estimators, learning rate, and loss
7. XGB Regression
    - Grid Search on number of estimators, learning rate, and max depth 
8. SGD Regression
    - Grid Search on alpha, l1 ratio, max iterations, tolerance, and penalty
9. KNN Regression
    - Grid Search on number of neighbors, weights, metric, and p 

## Result Interpretation

Results are shown in 4 ways: mean squared error, mean average error, line graph, and scatter plot. The mean squared error is in terms of squared ELO. The mean absolute error is in terms of ELO. The line graph plots the ascending sort of data points and then their corresponding predictions. The scatter plot graphs the actual rating against the predicted rating for each data point. A y=x line is also introduced to visualize each model's comparison against an ideal model.

### Example MSE/MAE result (XGBoost w/ Grid Search):
![XGGS](https://github.com/pmogan77/Chess/assets/60144163/071a7e32-6a0c-48f1-a3be-7c8ff4414e80)

### Example Line Graph 
![image](https://github.com/pmogan77/Chess/assets/60144163/4a427fb3-cddd-44ca-85f1-c4a81ae343de)

### Example Scatterplot:
![image](https://github.com/pmogan77/Chess/assets/60144163/19ecb547-165d-4c42-8db6-aaa8a8e734e5)


