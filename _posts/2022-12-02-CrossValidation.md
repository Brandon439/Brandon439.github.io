## Cross Validation

Now we know how to fit a polynomial onto a set of points. The question remains, which degree polynomial is the best? This type of check is called cross-validation, 
and while there are many different types of cross-validation, we'll look at a basic technique where we split our data into three parts:

**Training set**: The data used to fit the model.

**Validation set**: The data used to select the model.

**Test Set**: The data used to report the model's final accuracy.

The cross-validation process is as follows:

- 
