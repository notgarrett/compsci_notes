
# Regression Analysis

A simple linear regression model for a *response variable y* and *predictor variable x* is one in which we seek coefficients (or parameters) $\beta_{0}$ and $\beta_{1}$, such that, informally:

$$y \approx \beta_{0}+\beta_{1}x$$
$$\hat{Y}_{i}=b_{0}+b_{1}X_{i}$$

Ordinary Least Squares Method:
$$b1 = \frac{\sum\limits^{n}_{i=1}(X_{i}-\bar{X})(Y_{i}-\bar{Y})}{\sum\limits^{n}_{i=1}(X_{i}-\bar{X})^{2}}$$

$$b_{0}= \overline{Y} - b1\overline{X}$$

Quantitative indicator of the relationship: $R^{2}$
$$R^{2}-1 = \frac{SSR}{SST}$$
- Relationship between variation (*fitted line*) and variation (*data mean*). 
	- *Variation* of the data *explained* by the relationship between two variables
	- The remainder of the variability is explained by variables not included in the model or by inherent randomness in the data

```chart
type: line
labels: [1,2,3,4,5,6,7,8,9]
series:
  - title: Data
    data: [1,2,3,5,7,5,6,8,7,9]
tension: 0.41
width: 80%
labelColors: false
fill: false
beginAtZero: false
bestFit: true
```

$R^{2}$ is the square of the correlation coefficient the proportion of variation in the response explained by the explanatory variable. 

Regression lines that predict y from x is only for predicting y from x. Not *x from y*. 

Correlation does not distinguish between x and y. For regression, the two variables play different roles and are not interchangeable.

Conditions for a simple linear regression model
- Linearity
- Constant variability - points should nearly scatter evenly around the zero line.

## Outliers

**Outliers:** Points that lie away from the cloud of points. 
- A point is *influential* if including or excluding the point would considerably change the slope of the regression line. 

```ad-question
title: Do influential points always reduce $R^{2}$?
Our answer is no, as an outlier can actually lay closer to the line of best fit, as opposed to always further away.
```

## Multiple Linear Regression

A simple linear regression model for a response variable y and predictor variable x is one in which we seek coefficients or parameters $B_{0}$ and $B_{1}$, such that:
$$y \approx B_{0}+B_{1}x$$
$$\hat{Y}_{i}=b_{0}+b_{1}X_{i}$$

Multiple linear regression however, has multiple variables, like so: 
$$\hat{y}_{i}=b_{0}+b_{1}x_{i1}+b_{2}x_{i2}+...+b_{p}x_{ip}$$

The *$i^{th}$ residual*, the difference between the observed and the predicted response.
$$\begin{align*}
e_{i}&=\text{observed response - predicted response}\\
&= y_{i}-\hat{y}_{i}\\
&= y_{i}-b_{0}-b_{1}x_{i1}-b_{2}x_{i2}-...-b_{p}x_{ip}
\end{align*}$$

Applying the *method of least squares:*
- Determine values of b's such that the sum of squared residuals is minimised
$$\sum\limits(y_{i}-b_{0}-b_{1}x_{i1}-...-b_{p}x_{ip})^{2}$$

## Inference

Simple linear regression:
- Regression on x is of no value for predicting the response y or,
- There is no straight-line relationship between x and y

Multiple linear regression:
- $x_{1}$ is of no value for predicting y or,
- predictor $x_{1}$ contains no additional information over or above the contained other predictors useful to predict y

The standard deviation $\sigma$ in the model 
- estimated by the regression standard error, *s*. 
$$\begin{align*}
s^{2}&= \frac{\sum\limits{e_{i}^{2}}}{n-p-1}\\ \\
&= \frac{\sum\limits(y_{i}-\hat{y_{i}})^{2}}{n-p-1}
\end{align*}$$
$$$$
Quantity $n - p - 1$ is the degrees of the freedom. 
- For simple linear regression: p = 1
- For multiple linear regression: p = number of explanatory variables

### F Test

The **F Test** provides an *overall assessment* of the model to explain the response. 

The individual t tests assess the importance of a single variable, given the presence of the other variables in the model.

The sum of squares represent sources of variation
- Both the sums of squares and their degrees of freedom add:

$$SST = SSM + SSE$$
$$DFT = DFM + DFE$$


| Source | Degrees of freedom | Sum of squares                       | Mean square | F       |
| ------ | ------------------ | ------------------------------------ | ----------- | ------- |
| Model  | $p$                | $\sum\limits(\hat{y_i}-\bar{y})^{2}$ | SSM/DFM     | MSM/MSE |
| Error  | $n-p-1$            | $\sum\limits(y_{i}-\hat{y_{i}})^{2}$ | SSE/DFE     |         |
| Total  | $n-1$              | $\sum\limits(y_{i}-\bar{y})^{2}$     | SST/DFT     |         |

