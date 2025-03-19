---
date: 2025-02-25
tags:
  - cryptography_and_network_security
---
# Diffie-Hellman Key Exchange

First published public-key algorithm.

A number of commercial products employ this key exchange technique.

Purpose is to enable two users to securely exchange a key that can then be used for subsequent symmetric encryption of messages.

The algorithm itself is limited to the exchange of secret values.

Its effectiveness depends on the difficulty of computing discrete logarithms.

# ElGamal Cryptography

Announced in 1984 by T. Elgamal.

Public-key scheme based on discrete logarithms closely related to the Deffie-Hellman technique.

Used in the digital signature standard (DSS) and the S/MIME e-mail standard. 

Global elements are a prime number q and a which is a primitive root of q.

Security is based on the difficulty of computing discrete logarithms.

# Elliptic Curve Arithmetic

Most of the products and standards that use public-key cryptography for encryption and digital signatures use RSA.
- The key length for secure RSA use has increased over recent years and this has put a heavier processing load on applications using RSA  

Elliptic curve cryptography (ECC) is showing up in standardization efforts including the IEEE P1363 Standard for Public-Key Cryptography.  
Principal attraction of ECC is that it appears to offer equal security for a far smaller key size.

# Abelian Group

A set of elements with a binary operation, denoted by $*$, that associates to each ordered pair (a, b) of elements in G an element $(a * b)$ in G, such that the following axioms are obeyed:

**(A1) Closure:** If $a$ and $b$ belong to $G$, then $a * b \in G$

**(A2) Associative:** $a * (b * C) = (a * b) * c$ for all $a,b,c \in G$

**(A3) Identity element:** There is an element $e \in G$ such that $a * e = e * a = a$ for all $a \in G$

**(A4) Inverse element:** For each $a \in G$ there is an element $a\prime \in G$ such that $a * a\prime = a\prime * a = e$

**(A5) Commutative:** $a * b = b * a$ for all $a,b \in G$

# Elliptic Curves Over $Z_p$

Elliptic curve cryptography uses curves whose variables and coefficients are finite

Two families of elliptic curves are used in cryptographic applications:
- Binary curves over $GF(2^{m})$
	- Variables and coefficients all take on values in $GF(2^{m})$
	- Best for hardware applications
- Prime curves over $Z_{p}$
	- Uses a cubic equation in which the variables and coefficients all take on values in the set of integers from 0 through p - 1 and in which calculations are performed modulo p.
	- Best for software applications


# Elliptic Curves Over $GF(2^m)$

Use a cubic equation in which the variables and coefficients all take on values in $GF(2^m)$ for some number m  

Calculations are performed using the rules of arithmetic in $GF(2^m)$  

The form of cubic equation appropriate for cryptographic applications for elliptic curves is somewhat different for $GF(2^m)$ than for $Z_{p}$  
- It is understood that the variables x and y and the coefficients a and b are elements of $GF(2^m)$ and that calculations are performed in $GF(2^m)$

# Elliptic Curve Cryptography (ECC)

Addition operation in ECC is the counterpart of modular multiplication in RSA.

Multiple addition is the counterpart of modular exponentiation.

To form a cryptographic system using elliptic curves, we need to find a “hard problem” corresponding to factoring the product of two primes or taking the discrete logarithm
- Q=kP, where Q, P belong to a prime curve
- Is “easy” to compute Q given k and P
- But “hard” to find k given Q, and P
- Known as the elliptic curve logarithm problem

# Security of Elliptic Curve Cryptography

Depends on the difficulty of the elliptic curve logarithm problem  

Fastest known technique is “Pollard rho method”  

Compared to factoring, can use much smaller key sizes than with RSA  

For equivalent key lengths computations are roughly equivalent  

Hence, for similar security ECC offers significant computational advantages

