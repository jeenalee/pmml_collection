# PMML Collection
This is a collection of predictive models based on Iris data set, represented in PMML. The models in R and sklearn were represented in PMML via [`R2PMML`] (https://github.com/jpmml/r2pmml) and [`sklearn2pmml`] (https://github.com/jpmml/sklearn2pmml).

## Linear Regression
x = Sepal.Width, Petal.Length, Petal.Width

y = Sepal.Length


R: `lm {stats}`

sklearn: `sklearn.linear_model.LinearRegression()`

## Logistic Regression
x = Sepal.Length, Petal.Length

y = Species (only 2 states; 'setosa' and 'versicolor')


R: `glm {stats}` with `family='binomial'`

sklearn: `sklearn.linear_model.LogisticRegression()`
