---
date: 2025-03-05
tags:
  - cryptography_and_network_security
---
# Hash Functions

A hash function H accepts a variable-length block of data M as input and produces a fixed-size hash value. 
- $h = H(M)$
- Principal object is data integrity

Cryptographic hash function:
- An algorithm for which it is computationally infeasible to find either.
	- A) a data object that maps to a pre-specified hash result (the one-way property)
	- B) Two data objects that map to the same has result (the collision-free property)

# Message Authentication Code (MAC)

Also known as a keyed has function.

Typically used between two parties that share a secret key to authenticate information exchanged between these parts. 

Takes as input a secret key and a data block and produces a hash value (MAC) which is associated with the protected message.
- If the integrity of the message needs to be checked, the MAC function can be copied to the message and the result compared with the associated MAC value.
- An attacker who alters the message will be unable to alter the associated MAC value without knowledge of the secret key.

# Digital Signature

Operation is similar to that of the MAC.

The has value of a message is encrypted with a user's private key.

Anyone who knows the user's public key can verify the integrity of the message.

An attacker who wishes to alter the message would need to know the user's primary key.

Implications of digital signatures go beyond just message authentication.

```ad-important
Digital Signature question(s) will be on the test.
```

```ad-note
Public key encryption remove's the possibility of man in the middle attacks. 
```

# Other Hash Function Uses

Commonly used to create a one-way password file.
- When a user enters a password, the hash of the password is compared with the stored hash value for verification.
- This approach to password protection is used by most operating systems.

Can be used for intuition and virus detection.
- Store H(f) for each file on the system and secure the high values.
- One can later determine if a file has been modifidied by recomputing the H(f)
- An intruder would need to change f without changing H(f).

Can be used to output a pseudorandom function or a pseudorandom number generator. 
- A common application to a hash-based PF is the generation of a symmetric key. 

# Two Simple Hash Functions

Consider two simple insecure hash functions that operate using the following principles:
- The input is viewed as a sequence of n-bit blocks.
- The input is processed one block at a time in an iterative fashion to produce an n-bit hash function.

Bit-by-bit exclusive-OR (XOR) of every block.
- $C_{i}=b_{I}xor(b_{2})xor...xor(b_{n})$
- Produces a simple parity for each bit position and is known as a longitudinal redundancy check. 
- Reasonably effective for random data as a data integrity check.

Perform a one-bit circular shift on the hash value after each block is processed.

# Requirements for a Cryptographic Hash Function H


| Requirement         | Description |
| ------------------- | ----------- |
| Variable input size |             |
| Fixed input size    |             |
| Efficiency          |             |
| One-way property    |             |
|                     |             |
|                     |             |

# Attacks on Hash Functions

## Brute-Force Attacks

Does not depend on the specific algorithm, only depends on the bit length.

In the case of a hash function, attack depends only on the bit length of the has value.

Method is to pick values at random and try each one until a collision occurs. 

## Cryptanalysis

An attack based on weaknesses in a particular cryptographic algorithm.

Seek to explicit some property of the algorithm to perform some attack other than an exhaustive search.

# Secure Hash Algorithm (SHA)

SHE was originally designed by the National Institute of Standards and Technology (NIST) and published as a federal information processing standard (FPS) in 1993.

Was revised in 1995 as SHA-1.

Based on the hash function MDA and its design closley models ICA.

Produces 160-bit hash values.

In 2002 NIST produced a revised version of the standard that defined free new versions of SHA with hash values lengths of 256, 384, and 51. 
- Collectively known as SHA-2

