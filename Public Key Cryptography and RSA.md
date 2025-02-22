---
date: 2025-02-21
tags:
  - cryptography_and_network_security
---

# Misconceptions Concerning Public-Key Encryption

Public-key encryption is more secure from cryptanalysis than symmetric encryption.

Public-key encryption is a general-purpose technique that has made symmetric encryption obsolete.

There is a feeling that key distribution is trivial when using public-key encryption, compared to the cumbersome handshaking involved with key distribution centers for symmetric encryption.

# Principles of Public-Key Cryptosystems

The concepts of public-key cryptography evolved from an attempt to attack two of the most difficult problems associated with symmetric encryption:

**Key distribution:**
- How to have secure communications in general without having to trust a KDC with your key.

**Digital signatures:** 
- How to verify that a message comes intact from the claimed sender.

Whitfield Diffie and Martin Hellman from Stanford University achieved a breakthrough in 1976 by coming up with a method that addressed both problems and was radically different from all previous approaches to cryptography.

# Public-Key Cryposystems

A public-key encryption scheme has six ingredients:

- Plaintext
- Encryption algorithms
- Public key
- Private key
- Ciphertext
- Decryption algorithm

# Conventional and Public-key Encryption

## Conventional Encryption

Needed to work:
1. The same algorithm with the same key is used for encryption and decryption.
2. The sender and receiver must share the algorithm and the key.

Needed for Security:
1. The key must be kept secret.
2. It must be impossible or at least impractical to decipher a message if the key is kept secret.
3. Knowledge of the algorithm plus samples of ciphertext must be insufficient to determine the key. 

## Public-Key Encryption

Needed to Work:
1. One algorithm is used for encryption and a related algorithm for decryption with a pair of keys, one for encryption and one for decryption.
2. The sender and receiver must each have one of the matched pair of keys. (not the same one).

Needed for Security:
1. One of the two keys must be kept secret.
2. It must be impossible or at least impractical to decipher a message if one the keys is kept secret. 
3. Knowledge of the algorithm plus one of the keys plus samples of ciphertext must be insufficient to determine the other key.


## Public-Key Requirements

A one-way function is one that maps a domain into a range such that every function value has a unique inverse, with the condition that the calculation of the function is easy, whereas the calculation of the inverse is infeasible.  
- Y = f(X) easy  
- X = f–1(Y) infeasible  
Need a trap-door one-way function for asymmetric encryption.  

A trap-door one-way function is a family of invertible functions fk, such that:
- Y = fk(X) easy, if k and X are known
- X = fk–1(Y) easy, if k and Y are known  
- X = fk–1(Y) infeasible, if Y known but k not known  

A practical public-key scheme depends on a suitable trap-door one-way function.

## Public-Key Cryptanalysis

A public-key encryption scheme is vulnerable to a brute-force attack.
- Countermeasure: use large keys.
- Key size must be small enough for practical.encryption and decryption.
- Key sizes that have been proposed result in encryption/decryption speeds that are too slow for general-purpose use.
- Public-key encryption is currently confined to key management and signature applications.

Another form of attack is to find some way to compute the private key given the public key  
- To date it has not been mathematically proven that this form of attack is infeasible for a particular public-key algorithm  

Finally, there is a probable-message attack  
- This attack can be thwarted by appending some random bits to simple messages

# Rivest-Shamir-Adleman (RSA) Algorithm

Developed in 1977 at MIT by Ron Rivest, Adi Shamir & Len Adleman.

Most widely used general-purpose approach to public-key encryption.

Is a cipher in which the plaintext and ciphertext are integers between 0 and n – 1 for some n.
- A typical size for n is 1024 bits, or 309 decimal digits

RSA makes use of an expression with exponentials. 

Plaintext is encrypted in blocks with each block having a binary value less than some number n.

Encryption and decryption are of the following form, for some plaintext block M and ciphertext block C.

$$\begin{align*}
C &= M^{e}mod(n)\\
M &= C^{d}mod(n)=(M^{e})dmod(n)=M^{ed}mod(n)
\end{align*}$$

Both sender and receiver must know the value of n.

The sender knows the value of e, and only the receiver knows the value of d.

This is a public-key encryption algorithm with a public key of $PU=\{e,n\}$ and a private key of $PR=\{d,n\}$

## Algorithm Requirements

For this algorithm to be satisfactory for public-key encryption, the following requirements must be met:
1. Is it possible to find values of $e,d,n$ such that $$