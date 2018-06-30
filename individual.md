# Deep Learning in Python

Large neural networks (aka Deep Learning) are the current hot-topic in machine learning. In this assignmnet, you will learn to build and evaluate alternative neural network models.

There are many relatively new libraries for using neural networks, but there isn't yet a single standard. We will use keras, which is arguably the most popular library for machine learning.

You can find the data [here](data/).

## Part 1: Getting comfortable with Keras

1. Install keras using the command `pip install keras`

2. Read the example code for [Multilayer Perceptron](http://keras.io/examples/) (that's a fancy name for the standard feedforward neural network).

    There is a lot going on in this code. Take the time to make sure you understand what is going on. As with many high level APIs there is a learning curve involved in aligning your understanding with the interface provided by the API. There are also more examples on that page and in kera's GitHub [repository](https://github.com/fchollet/keras/tree/master/examples) if you're looking for more examples/context.

## Part 2: Building and testing Neural Network models

You will now use keras to build neural networks for a range of predictive modeling problems. Over the course of the afternoon, you should use at least two of the following datasets:

* churn.csv (which you have used previously, and is also in today's data directory).
  * For this data you will be doing binary classification, this means that the final layer in your network should have one node with sigmoid activation (just like we had in logistic regression) and that the loss function should be binary cross entropy.
* The MNIST dataset. Each observation in this dataset depicts a handwritten digit. The first column (called 'label') describes what number the writer was trying to write. The images of the digits were scanned onto a 28x28 grid, and the darkness on each part of the grid is depicted as a number. The darkness of these parts of the grids are called pixel intensities, and each predictive column represents the darkness of a single pixel. This dataset is also in the data directory.
  * For this data you will be doing multiclass classification, this means that the final layer in your network should have the same number of nodes as there are classes with softmax activation (this is generalization of sigmoid function) and that the lass function should be categorical cross entropy.

For each problem/dataset, create a train/test split where 70% of your data is used for training (and 30% is used for testing). You will also need to choose an evaluation metric appropriate for the problem at hand. Use only a single evaluation metric, and justify (in writing) why it is a good metric to use.

You will now experiment with different neural network architectures (e.g. number and size of hidden layers), levels of dropout, and number of variables entering the network. 

Every time you try a new network, write down your predictions for how this network's performance will compare to your previous networks' performance in terms of:

* execution speed
* training error
* validation error

The models take a while to run. So you can write your predictions while they run. After the model runs, give a 1-sentence summary of how the model performance compared to your expectations. Optionally, compare your model to previous models you have learned (random forest, and either linear or logistic regression.)
