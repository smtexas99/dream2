# Under the Hood of a Neural Network

## Part 1: Explaining Neural Network

The code in [short_nn.py](src/short_nn.py) has been given to you as a (very) short and minimal implementation of a neural network. Our goal is to understand and improve the code.

To start, explore the code. Your exploration may include:
* changing the value in the for-loop
* adding print statements to explore what various variables contain
* use the debugger and step through line by line

## Part 2: Make the Code Better

1. Determine which variable contains the predicted output of the neural network? It may help to look at the shape of the various variables for as a step in the right direction. Add a comment or rename this variable so it is transparent that this variables holds the model output/predictions

2. Determine what difference it makes that we set the random number seed. Add a comment describing the purpose of this line.

3. Determine which variable contains the values of nodes in the first hidden layer. Add a comment to indicate this.

4. Move all the code implementing the neural network into a separate function. The code setting up raw data should be left out of this function. The function should take the X data, y data and number of iterations as arguments. It should initialize the weights and update them the requested number of iterations. Then it should return the network's predictions.

5. You will now apply the neural network function you created to the churn.csv file in the data directory.

Read this file using `pd.read_csv()`. Drop the State and Phone columns. Convert the other columns to numerical representations (e.g. convert binary variables to 0 or 1).

Normalize all columns by subtracting the column means and dividing by the column standard deviations. Use [`sklearn.feature_selection.SelectKBest`](http://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html#sklearn.feature_selection.SelectKBest) to pick 8 variables that are related to churn. 

Apply the neural network function you created to the 8 columns of data and get predicted churn. Report the accuracy of the model. Note that we haven't used proper validation, but we'll get to that when we use a more complete neural network library this afternoon.
