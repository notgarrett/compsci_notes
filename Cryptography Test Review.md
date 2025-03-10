---
epoch: 1740364713426
modelKey: gemini-2.0-flash|google
tags:
  - copilot-conversation
  - cryptography_and_network_security
---

**user**: Based on the notes [[Random Numbers and Stream Ciphers]] amd [[Public Key Cryptography and RSA]]

Generate me a test review based on these two notes
[Timestamp: 2025/02/23 21:38:33]

**ai**: Okay, here's a test review based on the notes [[Random Numbers and Stream Ciphers]] and [[Public Key Cryptography and RSA]]. This review is designed to test your understanding of the core concepts, definitions, and applications of these topics.

**I. Random Numbers and Stream Ciphers**

1.  **Random Number Requirements:**
    *   Explain the two distinct requirements for a sequence of random numbers used in cryptographic applications.
    *   Describe the criteria used to validate that a sequence of numbers is random.
    *   Why is unpredictability important, and how does it relate to true random sequences versus algorithm-generated sequences?

2.  **Random Number Generators:**
    *   Differentiate between True Random Number Generators (TRNGs), Pseudorandom Number Generators (PRNGs), and Pseudorandom Functions (PRFs). Provide examples of sources of entropy for TRNGs.
    *   Explain the role of a seed in a PRNG. What are the implications if an adversary knows the algorithm and the seed?
    *   What is the difference between a PRNG and a PRF?

3.  **PRNG Requirements:**
    *   What is the basic security requirement for a PRNG or PRF used in cryptographic applications?
    *   Explain the three characteristics that NIST SP 800-22 specifies for randomness testing.
    *   Describe the purpose of the Frequency Test, Runs Test, and Maurer's universal statistical test.

4.  **Unpredictability and Seed Requirements:**
    *   Differentiate between forward and backward unpredictability in the context of PRNGs.
    *   Why is it important for the seed of a PRNG to be secure and unpredictable? How is the seed typically generated?

5.  **PRNG Algorithms:**
    *   Briefly explain the Linear Congruential Generator (LCG). What parameters are critical for a good random number generator using this method?
    *   What is a Cryptographically Secure Pseudorandom Bit Generator (CSPRBG)? What is the security of the Blum Blum Shub (BBS) generator based on?
    *   Describe two approaches that use a block cipher to build a PRNG.

6.  **Stream Ciphers:**
    *   Draw and explain the general architecture of a stream cipher. Define the components: Plaintext ($p_i$), Ciphertext ($c_i$), Keystream ($z_i$), Key ($K$), Initialisation Value ($IV$), State ($\sigma_i$), Next-state function ($f$), Keystream function ($g$).
    *   Discuss the design considerations for stream ciphers, including period, keystream properties, and key length.
    *   What is a potential advantage of stream ciphers compared to block ciphers?

**II. Public Key Cryptography and RSA**

1.  **Public-Key Cryptosystems:**
    *   Explain the key distribution and digital signature problems that public-key cryptography aims to solve.
    *   List and briefly describe the six ingredients of a public-key encryption scheme.
    *   Compare and contrast conventional (symmetric) and public-key encryption in terms of what is needed to work and what is needed for security.

2.  **One-Way Functions and Trapdoors:**
    *   Define a one-way function and a trap-door one-way function. Why are trap-door one-way functions important for asymmetric encryption?

3.  **RSA Algorithm:**
    *   Describe the Rivest-Shamir-Adleman (RSA) algorithm. Explain the encryption and decryption formulas.
    *   What are the requirements for the RSA algorithm to be satisfactory for public-key encryption?
    *   Outline the steps involved in RSA key generation. Why must the prime numbers $p$ and $q$ be chosen from a sufficiently large set?

4.  **RSA Implementation and Security:**
    *   Explain how the property of modular arithmetic, $ [(a \mod n) \times (b \mod n)] \mod n = (a \times b) \mod n $, is used to make RSA more efficient.
    *   What is a common choice for the public exponent $e$ to speed up RSA, and why? What is a vulnerability of using a very small public key?
    *   How can the Chinese Remainder Theorem (CRT) be used to speed up RSA decryption?

5.  **RSA Attacks and Countermeasures:**
    *   List and briefly describe five possible approaches to attacking RSA.
    *   Explain the mathematical attacks on RSA related to factoring.
    *   Describe timing attacks and three countermeasures against them.
    *   What is a fault-based attack, and how does it work?
    *   Explain the chosen ciphertext attack and the countermeasure recommended by RSA Security Inc.

**III. General Knowledge**

1.  What are some misconceptions concerning public-key encryption?
2.  What is the difference between a block cipher and a stream cipher?
3.  What is the difference between diffusion and confusion in the context of cryptography?
4.  What is the purpose of the S-box in AES?
5.  What is the purpose of the ShiftRows transformation in AES?
6.  What is the purpose of the MixColumns transformation in AES?
7.  What is the purpose of the AddRoundKey transformation in AES?

This review should give you a good starting point for preparing for a test on these topics. Remember to study your notes and understand the underlying concepts. Good luck!


#### Sources:
- [Random Numbers and Stream Ciphers](obsidian://open?vault=compsci_notes&file=Random%20Numbers%20and%20Stream%20Ciphers)
- [Public Key Cryptography and RSA](obsidian://open?vault=compsci_notes&file=Public%20Key%20Cryptography%20and%20RSA)
- [Introduction to Cryptography and Network Security](obsidian://open?vault=compsci_notes&file=Introduction%20to%20Cryptography%20and%20Network%20Security)
- [Block Ciphers and the Data Encryption Standard](obsidian://open?vault=compsci_notes&file=Block%20Ciphers%20and%20the%20Data%20Encryption%20Standard)
- [Classical Encryption Techniques](obsidian://open?vault=compsci_notes&file=Classical%20Encryption%20Techniques)
- [Advanced Encryption Standard](obsidian://open?vault=compsci_notes&file=Advanced%20Encryption%20Standard)
- [Random Numbers Generators](obsidian://open?vault=compsci_notes&file=Random%20Numbers%20Generators)
- [Cryptographic algorithms](obsidian://open?vault=compsci_notes&file=Cryptographic%20algorithms)
- [RSA example](obsidian://open?vault=compsci_notes&file=RSA%20example)
[Timestamp: 2025/02/23 21:38:53]