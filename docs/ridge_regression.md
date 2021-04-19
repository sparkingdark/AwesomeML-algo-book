# Ridge regression and classification


## Regression
----------

`Ridge` regression addresses some of the problems of
`ordinary_least_squares` by imposing a penalty on the size of the
coefficients. The ridge coefficients minimize a penalized residual sum
of squares:


![img]("../images/ridge regression/equation1.png")

The complexity paramete controls the amount
of shrinkage the larger the value of , the greater the amount
of shrinkage and thus the coefficients become more robust to collinearity.

![figure]("../images/ridge regression/sphx_glr_plot_ridge_path_0011.png")

As with other linear models, `Ridge` will take in its `fit` method
arrays X, y and will store the coefficients `w` of the linear model in
its `coef_` member:

```python
    >>> from sklearn import linear_model
    >>> reg = linear_model.Ridge(alpha=.5)
    >>> reg.fit([[0, 0], [0, 0], [1, 1]], [0, .1, 1])
    Ridge(alpha=0.5)
    >>> reg.coef_
    array([0.34545455, 0.34545455])
    >>> reg.intercept_
    0.13636...

```