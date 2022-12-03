---
usemathjax: true
---
## Cross Validation

Now we know how to fit a polynomial onto a set of points. The question remains, which degree polynomial is the best? This type of check is called cross-validation, 
and while there are many different types of cross-validation, we'll look at a basic technique where we split our data into three parts:

**Training set**: The data used to fit the model.

**Validation set**: The data used to select the model.

**Test Set**: The data used to report the model's final accuracy.

The cross-validation process is as follows:

- For each potential set of features, fit a model using the training set. The error of a model on the training set is its
**training error**. 
- Check the error of each model on the validation set, called the **validation error**. Select the model that achieves the lowest
validation error.
- Calculate the **test error**, error of the final model on the test set. This is the final reported accuracy of the model.

Typically about 70% of the data goes into the training set, and 15% each for the validation and test set.
