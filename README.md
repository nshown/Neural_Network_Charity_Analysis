# Neural_Network_Charity_Analysis
## Overview

Given a dataset describing charities and their successfulness is it possible to predict their success using a neural network?

## Results

* **Compiling, Training, and Evaluating the Model**
  * The IS_SUCCESSFUL field is the target of the dataset.
  * The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT fields are the features to be used.
  * The EIN and NAME fields are data that can be ignored in the model.
* **Compiling, Training, and Evaluating the Model**
  * [I tried a variety of deep neural network configurations in an attempt to identify the best model](AlphabetSoupCharity_Optimization.ipynb).  I tried between 2 and 3 hidden layers.  After the features were One Hot Encoded I ended up with about 40 features  so I used between 50 and 150 nodes in each layer.  The final layer had 1 node with a sigmoid activation function because this is ideal for binary classifications.  I experimented with `relu` and `tanh` activation functions in the other hidden layers.  I experimented with `adam` and `SGD` optimizers when compiling the model.
  * The target model [performance was %75 but I was only ever able to achieve around %50](AlphabetSoupCharity_Optimization.h5).
  * I experimented with the previously mentioned settings in an attempt to get a model that was closer to the %75 target performance.

## Summary

While the target performance wasn't reached with my chosen model there are additional experiments that may achieve better results.  It may be that different activation functions improve the models performance.  It's also possible that the categories can be further binned or perhaps certain categories can be ignored entirely.  Additionally, because this is a binary classification problem, Linear Regression, SVG, and Random Forest models may perform better with this particular data set.