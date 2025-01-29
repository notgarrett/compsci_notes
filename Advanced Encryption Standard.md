---
date: 2025-01-29
tags:
  - cryptography_and_network_security
---
# Finite Field Arithmetic 

In the Advanced Encryption Standard (AES) all operations are performed on 8-bit bytes. 

The arithmetic operations of addition, multiplication, and division, are performed over the finite field of GF($2^{8}$)

The arithmetic operations in addition, subtraction, multiplication, and division without leaving the set. 

Division is defined with the following rule:
- $\frac{a}{b}=a(b^{-1})$
- An example of a finite field (one with a finite number of elements) is the set $Z_{p}$ consisting of all the integers {0,1,..., p-1}, where p is a prime number and in which arithmetic is carried out modulo p.

# Advanced Encryption Standard (AES)

Needed a replacement for 3 DES.
- 3 DES was not reasonable for long term use.

NIST called for proposals for a new AES in 1997
- Should have a security strength equal to or better than 3DES
- Significantly improved efficiency
- Symmetric block cipher
- 128 bit data and 128/192/256 bit keys

Select Rijndael in November 2001
- Published as FIPS 197

# AES Parameters

Key Size (words/bytes/bits), 4/16/128, 6/24/192, 8/32/256

Plaintext Block Size (words/bytes/bits), 4/16/128, 4/16/128, 4/16/128

Number of rounds, 10, 12, 14

Round Key Size (words/bytes/bits), 4/16/128, 4/16/128, 4/16/128

Expanded Key Size (words/bytes), 44/176, 52/208, 60/240

# Detailed Structure

Processes the entire data block as a single matrix during each round using substitutions and permutation.

The key that is provided as input is expanded into an array of forty-four 32-but words, w\[i].

```ad-note
title: Four different stages are used:
- Substituion bytes - Uses an S-box to perform a byte-by-byte subsitution of the block
- ShiftRows - a simple permutation
- MixColumns - a substitution that makes use of arithmetic over GF($2^8$)
- AddRoundKey - a simple bitwise XOR of the current block with a portion of the expanded key
```

The cipher begins and ends with an AddRoundKey stage.

Can view the cipher as alternating operations of XOR encryption (AddRoundKey) of a block, followed by scrambling of the block (the other three stages), followed by XOR encryption, and so on.

Each stage is easily reversible.

The decryption algorithm makes use of the expanded key in reverse order, however the decryption algorithm is not identical to the encryption algorithm.

State is the same for both encryption and decryption.

Final round of both encryption and decryption consists of only three stages.

# AddRoundKey Transofrmation

The 128 bits of State are bitwise XORed with the 128 bits of the round key.

Operation is viewed as a columnwise operation between the 4 bytes of a State column and one word of the round key.
- Can also be viewed as a byte-level operation.

```ad-note
title: Rationale:
- Is as simple as possible and affects every bit of State.
- The complexity of the round key expansion plus the complexity of the other stages of AES ensure security.
```

# S-Box Rationale

The S-box is designed to be resistant to known cryptanalytic attacks.

The Rijndael developers sought a design that has a low correlation between input bits and output bits and the property that the output is not a linear mathematical function of the input.

# Shift Row Rationale

The round key is applied to State column by column.
- Thus, a row shift moves an individual byte from one column to another which is a linear distance of a multiple of 4 bytes.

Transformation ensures that the 4 bytes of one column are spread out to four different columns.

# Mix Columns Rationale

Coefficients of a matrix based on a linear code with maximal distance between code words ensures a good mixing among the bytes of each column.

The mix column transformation combined with the shift row transformation ensures that after a few rounds all output bits depend on all input bits.

# AES Key Expansion

Takes as input a four-word (16 byte) key and produces a linear array of 44 words (176) bytes.
- This is sufficient to provide a four-word round key for the initial AddRoundKey stage and each of the 10 rounds of the cipher.

Key is copied into the first four words of the expanded key.
- The remainder of the expanded key is filled in four word at a time.

Each added word w\[i] depends on the immediately preceding word, w\[i - 1], and the word four positions back, w\[i - 4].
- In three out of four cases a simple XOR is used.
- For a word whose position in the w array is a multiple of 4, a more complex function is used.

# AES Implementation

AES decryption cipher is not identical to the encryption cipher.

The sequence of transformations differs although the form of the key schedules is the same.

Has the disadvantage that two seperate software or firmware modules are needed for applications that require both encryption and decryption.

# Implementation Aspects

AES can be implemented very efficiently on an 8=bit processor.

AddRoundKey is a bytewise XOR operation.

ShiftRows is a simple byte-shifting operation.

SubBytes operates at the byte level and only requires a table of 256 bytes.

MixColumns requires matrix multiplication in the field GF(28), which means that all operations are carried out on bytes.


