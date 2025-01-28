---
date: 2025-01-28
tags:
  - cryptography_and_network_security
---
# Stream Cipher

Encrypts a digital data stream one bit or one byte at a time. 
- Examples:
	- Autokeyed Vigenere cipher
	- Vernam cipher

In the ideal case, a one-time pad version of the Vernam cipher would be used, in which the keystream is as long as the plaintext bit stream.
- If the cryptographic keystream is random, then this cipher is unbreakable by any means other than acquiring the keystream.
- This introduces insurmountable logistical problems if the intended data traffic is very large.

For practical reasons the bit-stream generator must be implemented as an algorithmic procedure so that the cryptographic bit stream can be produced by both users. 
- It must be computationally impractical to predict future portions of the bit stream based on previous portions of the bit stream
- The two users need only share the generating key and each can produce the keystream


# Block Cipher

A block of plaintext is treated as a whole and used to produce a ciphertext block of equal length. 

Typically a block size of 64 or 128 bits is used.

As with a stream cipher, the two users share a symmetric encryption key.

The majority of network-based symmetric cryptographic applications make use of block ciphers.

# Data Encryption Standard (DES)

Until recently was the most widely used encryption scheme.
- Referred to as the Data Encryption Algorithm (DEA)
- Uses 64 bit plaintext block and 56 bit key to produce a 64 bit ciphertext block.

Strength concerns:
- Concerns about the algorithm itself
	- DES is the most studied encryption algorithm in existence.
- Concerns about the use of a 56 bit key
	- The speed of commercial off-the-shelf processors makes this key length woefully inadequate.


# DES uses Feistel Cipher Principle

Feistel proposed the use of a cipher that alternates substitutions and permutations.

**Substitutions:** Each plaintext element or group of elements is uniquely replaced by a corresponding ciphertext element or group of elements. 

**Permutation:** No elements are added or deleted or replaced in the sequence, rather the order in which the elements appear in the sequence is changed.

Is a practical application of a proposal by Claude Shannon to develop a product cipher that alternates **confusion** and **diffusion** functions.

Is the structure used by many significant symmetric block ciphers currently in use.

# Diffusion and Confusion Principle

Terms introduced by Claude Shannon to capture the two basic building blocks for any cryptographic system.
- Shannon's concern was to thwart cryptanalysis based on statistical analysis. 

**Diffusion:** 
- The statistical structure of the plaintext is dissipated into long-range statistics of the ciphertext digits.

**Confusion:** 
- Seeks to make the relationship between the statistics of the ciphertext and the value of the encryption key as complex as possible. 
- Even if the attacker can get some handle on the statistics of the ciphertext, the way in which the key was used to produce that ciphertext is so complex as to make it difficult to deduce the key.

# Feistel Cipher Design Features

**Block size:**
- Larger block sizes mean greater security but reduced encryption/decryption speed for a given algorithm. 

**Key size:** 