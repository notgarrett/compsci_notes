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
- Larger key size means greater security but may decrease encryption/decryption speeds.

**Number of rounds:**
- The essence of the Feistel cipher is that a single round offers inadequate security but that multiple rounds offer increasing security. 

**Subkey generation algorithm:** 
- Greater complexity in this algorithm should lead to greater difficulty at cryptanalysis. 

**Round function F:**
- Greater complexity generally means greater resistance to cryptanalysis.

**Fast software encryption/decryption:**
- In many cases, encrypting is embedding applications or utility functions in such a way as to preclude a hardware implementation; accordingly, the speed of execution of the algorithm becomes a concern. 

**Ease of analysis:**
- If the algorithm can be concisely and clearly explained, it is easier to analyse that algorithm for cryptanalysis vulnerabilities and there develop a higher level of assurance as to its strength. 

# Block Cipher Design Principles: Number of Rounds

The greater the number of rounds, the more difficult it is to perform cryptanalysis. 

In general, the criterion should be that the number of rounds is chosen to that known cryptanalytic efforts require greater effort than a simple brute-force key search attack. 

If DES had 15 or fewer rounds, differential cryptanalysis would require less effort than a brute-force key search.


# Average Time Required for Exhaustive Key Search


| Key Size (bits) | Cipher     | Number of Alternative Keys         | Time Required at $10^9$ decryption/us | Time Required at $10^{13}$ Decryption/us |
| --------------- | ---------- | ---------------------------------- | ------------------------------------- | ---------------------------------------- |
| 56              | DES        | $2^{56}\approx7.2\times10^{16}$    | $2^{55}us=1.125years$                 | 1 hour                                   |
| 128             | AES        | $2^{128}\approx3.4\times{10^{38}}$ | $2^{127}us=5.3\times{10^{21}}years$   | $5.3\times{10^{17}}$                     |
| 168             | Triple DES | $2^{168}$                          | $2^{167}us$                           | $5.8\times10^{29}years$                  |
| 192             | AES        | $2^{192}$                          | $2^{191}us$                           | $9.8\times10^{36}$                       |
| 256             | AES        | $2^{256}$                          | $2^{255}us$                           | $1.8\times10^{56}years$                  |

# Triple DES (3 DES)

Repeats basic DES algorithm three times using either two or three unique keys (168 bit/112 bit).

First standardised use in financial applications in ANSI standard x9.17 in 1985.

Attractions:
- 168-bit key length overcomes the vulnerability to brute force attack of DES
- Underlying encryption algorithm is the same as in DES 

Drawbacks:
- Algorithm is sluggish in software
- uses a 64-bit block size

