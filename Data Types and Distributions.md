---
tags:
  - "#statistics"
date: 2025-01-07
---

# Data types

**Qualitative Data:** Data that is categorical. This means the data is organised by category. For example, how many people's favourite colour is blue, green, or red. 
-  *Ordinal:* The data possesses some sort of natural order. An example being high, medium, low, or A, B, C.
- *Nominal:* The data contains no natural order. Things like colours and languages fit the bill here.

**Quantitative Data:** Data that is numerical, this extends from anything that can be counted, measured, or given some numerical value. 
- *Discrete:* Data that is countable, like tickets, how many cars are parked in a parking lot. Discrete data does not have decimals.
- *Continuous:* Data that is measurable. This could be the temperature, or a scale. This is because of the measurable (and uncountable) range of values these things can represent.

![[DataDiagram.excalidraw | center | 5000 ]]

# Distributions

**Distributions:** Report the values in some dataset and how many times each value appears.

**Random Variables:** A variable whose value is subject to variations due to randomness. 

**Probability:** Likelihood that a random variable will take on a certain value. 

**Probability Distribution:** Set if all possible values a random variable can take.

## Probability Distributions

### Uniform Distribution

- Probabilities for all the possible outcomes are the same or uniform
- Events that are equally likely to occur


**Probability of outcomes on a singular dice roll**
```chart
    type: bar
    labels: ["1", "2", "3", "4", "5", "6"]
    beginAtZero: true
    series:
        - title: Probability of roll
		  data: [.16, .16, .16, .16, .16, .16]
```

### Bernoulli Distribution

- Many scenarios in real-world are binary
- Snow or spam email (yes/no), Games, success/failure
- Probability distribution of a binary outcome event - Bernoulli Distribution

### Binomial Distribution

- Bundle of independent and same Bernoulli experiments
- Probability of 'k' successes (one outcome) in 'n' independent Bernoulli trials


**Probability of consecutive coin flips**
```chart
title: 
type: bar
labels: [1, 2, 3, 4]
series:
	- title: Heads
      data: [0.5,0.25,0.125,0.0625]
    - title: Tails
      data: [0.5,0.25,0.125,0.0625]
```


### Poisson Distribution

- Frequency with which an event occurs within a specific interval
- Events are independent of each other


Probability of 'k' occurrences of a certain event over a certain period of time and space:
$$
Pr(X=k) = \frac{\lambda^{k}e^{-\lambda}}{k~!}
$$

### Gaussian Distribution

- Bell curve like style
- Arises from variables in nature
- Characteristics (position, spread)

**Average Height of people of different ages (this is not accurate)**
```chart
    type: bar
    labels: [12, 16, 20, 45, 80]
    series:
        - title: Average Height of Different Ages
	      data: [5.5,5.7,6,5.7,5.5]
```


# Descriptive Statistics

**Descriptive Statistics:** Information that describes the data. 
- Mean
- Median
- Mode
- Range
- Standard Deviation

**Mean:** The average of the data set. ($x_{i}$  refers to the $i'th$ element in the data set, $n$ represents the total number of data points)
$$\frac{\sum\limits{x_{i}}}{n}$$

**Median:** The middle value of the dataset, if there is an even number of data points, then the formula is: 
$$\frac{a+b}{2}$$
Where a and b are the 2 middle values.

**Mode:** The value that appears most often in the dataset.

**Range:**  The range is the different between the largest and the smallest value in the dataset.
$$Max(S) - Min(S)$$
Where S is our data set.

**Standard Deviation:**  The average difference between a data point and the mean. (Note that this is our variance squared. )

$$\sqrt{\frac{\sum\limits{(x_{i}-\mu)^{2}}}{N}}$$

$\mu$ represents our population mean, $N$ our population size, and $x_{i}$ our $i'th$ term in the data set.


