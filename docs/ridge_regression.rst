.. _ridge_regression:

Ridge regression and classification
===================================

Regression
----------

:class:`Ridge` regression addresses some of the problems of
:ref:`ordinary_least_squares` by imposing a penalty on the size of the
coefficients. The ridge coefficients minimize a penalized residual sum
of squares:


.. math::

   \min_{w} || X w - y||_2^2 + \alpha ||w||_2^2


The complexity parameter :math:`\alpha \geq 0` controls the amount
of shrinkage: the larger the value of :math:`\alpha`, the greater the amount
of shrinkage and thus the coefficients become more robust to collinearity.

![img](./images/ridge regression/sphx_glr_plot_ridge_path_0011.png)


As with other linear models, :class:`Ridge` will take in its ``fit`` method
arrays X, y and will store the coefficients :math:`w` of the linear model in
its ``coef_`` member::

    >>> from sklearn import linear_model
    >>> reg = linear_model.Ridge(alpha=.5)
    >>> reg.fit([[0, 0], [0, 0], [1, 1]], [0, .1, 1])
    Ridge(alpha=0.5)
    >>> reg.coef_
    array([0.34545455, 0.34545455])
    >>> reg.intercept_
    0.13636...

