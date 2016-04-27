# PMML Collection
This is a collection of predictive models based on Iris data set, represented in PMML. The models in R and sklearn were represented in PMML via [`R2PMML`] (https://github.com/jpmml/r2pmml) and [`sklearn2pmml`] (https://github.com/jpmml/sklearn2pmml).

## Linear Regression
x = Sepal.Width, Petal.Length, Petal.Width

y = Sepal.Length


R: `lm {stats}`

sklearn: `sklearn.linear_model.LinearRegression()`

## Logistic Regression
x = Sepal.Length, Sepal.Width

y = Species (only 2 states; 'setosa' and 'versicolor')


R: `glm {stats}` with `family='binomial'`

sklearn: `sklearn.linear_model.LogisticRegression()`

R creates a model for each categorical state. For example, if there were two possible states in the data (A or B), R would create two models: one that would predict the likelihood of A, and another for likelihood of B. In sklearn, the decision function calculates the likelihood of state A (probability is closer to 1) or state B (probability is closer to 0).

## Random Forest
Also includes models trained on only 10 samples to make simpler models.

x = Sepal.Length, Sepal.Width

y = Species

R: `randomForest {randomForest}` with `ntree=2`

sklearn: `sklearn.ensemble.RandomForestClassifer(n_estimators = 2)`

R creates the trees in breadth-first manner, i.e. the node ids will be continuous in a breadth-first traversal. Meanwhile, sklearn outputs the trees in depth-first manner.
