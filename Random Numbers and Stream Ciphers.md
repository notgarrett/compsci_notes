---
date: 2025-02-07
tags:
  - cryptography_and_network_security
---

# Use of Random Numbers

A number of network security algorithms and protocols based on cryptography make use of random binary numbers:
- Key distribution and reciprocal authentication schemes
- Session key generation
- Generation of keys for the RSA public-key encryption algorithm
- Generation of a bit stream for symmetric stream encryption

There are two distinct requirements for a sequence of random numbers:
1. Randomness
2. Unpredictability

# Requirements of Random Numbers 

## Randomness

The generation of a sequence of allegedly random numbers being random in some well-defined statistical sense has been a concern. 

Two criteria are used to validate that a sequence of numbers is random:
- Uniform distribution
	- The frequency of occurrence of ones and zeros should be approximately equal
- Independence
	- No one sub sequence in the sequence can be inferred from the others.

## Unpredictability

The requirement is not just that the sequence of numbers be statistically random, but that the successive members of the sequence are unpredictable. 

With "true" random sequences each number is statistically independent of other numbers in the sequence and therefore unpredictable. 
- True random numbers have their limitations, such as inefficiency, so it is more common to implement algorithms that generate sequences of numbers that appear to be random.
- Care must be taken that an opponent not be able to predict future elements of the sequence on the basis of earlier elements.

### Random Number Generators

![[Random Numbers Generators|100%]]

```ad-tldr
TRNG = True random number generator
PRNG = pseudorandom number generator
PRF = pseudorandom function
```

## True Random Number Generator  (TRNG)

Takes as input a source that is effectively random.

The source is referred to as an entropy source and is drawn from the physical environment of the computer.
- Includes things such as keystroke timing patterns, disk electrical activity, mouse movements, and instantaneous values of the system clock.
- The source, or combination of sources, serve as input to an algorithm that produces random binary output.

The TRNG may simply involve conversion of an anolog source to a binary output.

The TRNG may involve additional processing to overcome any bias in the source.

## Pseudorandom Numbers

Cryptographic applications typically make use of algorithmic techniques for random number generation.

These algorithms are deterministic and therefore produce sequences of numbers that are not statistically random.

If the algorithm is good, the resulting sequences will pass many tests of randomness and are referred to as pseudorandom numbers.

## Pseudorandom Number Generator


