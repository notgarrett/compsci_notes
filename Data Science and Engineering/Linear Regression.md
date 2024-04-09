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

