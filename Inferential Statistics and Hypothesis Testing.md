# Inferential Statistics

**Inferential Statistics:** The way of making *inferences* about *population* based on *samples*. We assume characteristics about the sample is similar to the population's statistics.

Some examples include: 
- Healthcare
	- Predictive models in healthcare (eg. predicting outbreaks).
	- Use of statistics to improve treatment.
- Decision Making
	- Consumer behaviour analysis for targeted marketing .
- Machine Learning
	- Developing models such as fraud detection.

![[InferentialDiagram.excalidraw |  5000]]


## Central Limit Theorem

**Theorem:** if you have a *population with mean $u$ and standard deviation $\sigma$* and take sufficiently large *random samples* from the population with replacement, then the *distribution of the sample means* will be approximately *normally distributed*.

- This will hold true regardless of whether or not the population is normal, or skewed. Provided that the sample size is sufficiently large (n > 30)
- If the population is *normal*, then the theorem holds true even for *samples smaller than 30*
- This means that we can use the normal probability model to quantify uncertainty when making inferences about a population mean based on the sample mean

# Hypothesis Testing

## Null and Alternate Hypothesis

**Null Hypothesis:** The data from some sample does not reflect the population itself.
**Alternate Hypothesis:**  The data from some sample does reflect the population itse

To create a hypothesis: 
- Perform some calculations on data and come up with values for a *test statistic*.
- If we assume the null hypothesis is true.
	- Test statistic should be no different that a single random variable drawn from a specific probability distribution.
	- We will test the probability that the test statistic calculated belongs to the specific theoretical distribution (*p-value*).
	- Low enough p-value is grounds to reject the null hypothesis.

## Z and T testing

### Single-sample Z-test

```ad-question
title: When do you use a Z test?
A Z test can be used when:
- You want to make inferences about the population mean
- Known variance and for unkown variance (large sample size)
```

**Example:** Suppose we want to test if a new type of energy drink changes the average reaction time of consumers. From previous data, we know that the average reaction time for people not consuming the drink is 200 ms with a standard deviation of 15 ms. 

$$\begin{align*}
\text{Population Mean} (u) &= 200 \text{ milliiseconds} \\
\text{Standard Deviation of the Population} (\sigma) &= 15 \text{ milliseconds}\\
\text{Sample Size} (n) &= 40 \text{ people (assumption for question)}\\
\text{Sample Mean} (\bar{x}) &= 190 \text{ milliseconds}
\end{align*}$$

**Step 1:** Create a *null* and *alternate* hypothesis
- Null Hypothesis (H0): The energy drink does not change the average reaction time
- Alternative Hypothesis (H1): The energy drink changes the average reaction time
**Step 2:** Choose a Significance Level
- A 0.05 sig level $\alpha = 0.05$
**Step 3:** Perform some calculations on data and come up with values for a *test statistic*
$$Z = \frac{\hat{X} - \mu}{\frac{\sigma}{\sqrt{n}}}$$
**Step 4:** Interpret the Table Value:
- One tailed tests: The p-value is the area to the right of the Z-score for positive values, to the left for negative.
- Two tailed tests: If your Z-score is positive, double the area to the right of the Z-score, if negative, double the area to the left.
**Step 5:** The calculated p-value associated with the Z-score of -4.22 is approximately 0.00003. 
**Conclusion:** Since the p-value is much less than 0.05 we reject the null hypothesis. This indicates that the difference observed in our sample is highly statistically significant. 

**If 2 Tailed:** 
**Step 4:** Determine the critical z-score
**Step 5:** Compare Z-Score with the Critical Z-Value
- Calculated Z-score = -4.22
- Critical Z-value for $\alpha=0.05 \pm 1.96$ 
**Step 6:** Since our Z-score (-4.22) is less than the negative critical Z-value (-1.96), we reject the null hypothesis. This indicates that the difference observed in our sample is highly statistically significant.

### Z vs T test

**Standard deviations:**
- Z-Test: Used when the population std is known. It's typically applied for large sample sizes (n > 30)
- T-Test: Used when the population standard deviation is unknown and estimated from the sample. It's more appropriate for small sample sizes (n <= 30) 

**Distribution:**
- Z-Test: Assumes a normal distribution
- T-Test: Based on the t-distribution, which is similar to the normal distribution but has heavier tails.
- The t-distribution accounts for the additional uncertainty due to the estimation of the standard deviation from the small sample.

### Another Example

The labels on the bars claim that each bar contains 20 grams of protein. 

Imagine we have collected a random sample of 31 energy bars from a number of different stores to represent the population of energy bars available to the general consumer. (mean = 21.39, std = 2.54)

```ad-question
Is the t-test an appropriate method to test that the energy bars have 20 grams of protein?

Our Answer: No. This is because our sample size is greater than 30, in which a Z test becomes more appropriate.
```

All same steps: 
- Compare the test statistic from the t-distribution
- Degrees of freedom = n - 1 = 30
- The critical value of t with $\alpha$ = 0.05 and 30 degree of freedom is $\pm$ 2.043
- Conclusion: Reject null hypothesis, labels are incorrect.

