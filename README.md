# Predicting daily bike sharing ridership
[//]: # (Image References)

[architecture]: ./assets/neural_network.png "Neural network"
[output]: ./assets/sample_output.png "Output"

The project consists of building a neural network from scratch to predict daily bike rental ridership. The dataset contains the rental number for each hour between 01/01/2011 and 31/12/2012, along with contextual information such as temperature, humidity and wind speed. Based on this dataset, the goal of the project encompasses the following steps:
* Pre-process the data
  * Convert categorical variables into dummy variables
  * Standardise variables such that they have zero mean and standard deviation of 1
* Build the neural network
  * Code both the forward pass and backward pass
  * Set appropriate hyperparameters — learning rate, number of hidden units, number of EPOCHS.
* Train the network with Stochastic Gradient Descent (SGD)
* Evaluate the model using mean squared error (MSE) on the training, validation and testing data.

The image below show the predictions for the month of December. Note the drawback of the model that fails to capture the seasonal effect related to Christmas and end-of-year holidays. A possible approach to address this problem is to extend upon the data pre-processing step, adding feature engineering that considers the [partial autocorrelation (PACF)](https://youtu.be/DeORzP0go5I).

<img src="assets/sample_output.png" alt="Predictions of the number of daily bike rentals for December" height="250"/>

## Network architecture
The network is composed of a hidden layer and an output layer. The former uses the sigmoid activation function whereas the latter has only one node used for the regression. Thus, the output layer returns its input (i.e., $f(x) = x$). The following figure illustrates the network architecture.

<img src="assets/neural_network.png" alt="Neural network architecture" height="250"/>

The code for the network implementation can be found at [my_answers.py](./my_answers.py), whereas the whole project implementation is in the [Predicting_bike_sharing_data.ipynb](./Predicting_bike_sharing_data.ipynb) Jupyter notebook.

## Project implementation
The project implementation complies with Udacity's [list of rubric points](https://review.udacity.com/#!/rubrics/2148/view) required to pass the project.

## Notes
This project contains my implementation of the "Predicting Bike-Sharing Patterns" project for the [Udacity's Deep Learning program](https://www.udacity.com/course/deep-learning-nanodegree--nd101). The baseline code has been taken from Udacity's Deep Learning [repository](https://github.com/udacity/deep-learning-v2-pytorch).
