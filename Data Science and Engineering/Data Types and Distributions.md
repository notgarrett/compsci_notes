
# Going over data types and distributions

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

## Probability Distribution

### Uniform Distribution

- Probabilities for all the possible outcomes are the same or uniform
- Events that are equally likely to occur
### Bernoulli Distribution

- Many scenarios in real-world are binary
- Snow or spam email (yes/no), Games, success/failure
- Probability distribution of a binary outcome event - Bernoulli Distribution

### Binomial Distribution

- Bundle of independent and same Bernoulli experiments
- Probability of 'k' successes (one outcome) in 'n' independent Bernoulli trials

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
### Geometric Distribution

- Describes the probability of success in a series of independent trials
- Each trial is binary

**Probability of consecutive coin flips.**
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

