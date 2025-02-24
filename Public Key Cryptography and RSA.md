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
1. Is it possible to find values of $e,d,n$ such that $M^{ed}mod(n)=M$ for all $M > n$
2. It is relatively easy to calculate $M^{e}mod(n)$ and $C^{d}mod(n)$ for all values of $M < n$
3. It is infeasible to determine $d$ given $e$ and $n$.

## Key Generation

Before the application of the public-key  
cryptosystem each participant must generate a pair of keys:  
- Determine two prime numbers p and q
- Select either e or d and calculate the other

Because the value of n = pq will be known to any potential adversary, primes must be chosen from a sufficiently large set  
- The method used for finding large primes must be reasonably efficient

## Example of RSA Algorithm

![[RSA example|100%]]o
# RSA Efficient Implementation

Both encryption and decryption in RSA involve raising an integer to an integer power, mod n

Can make use of a property of modular arithmetic:  
$$[(a\mod n) x (b \mod n)] \mod n =(a \times b) \mod n$$  
With RSA you are dealing with potentially large exponents so efficiency of exponentiation is a consideration

## Efficient Operation Using the Public Key

To speed up the operation of the RSA algorithm using the public key, a specific choice of e is usually made  

The most common choice is 65537 (216 + 1)  
- Two other popular choices are e=3 and e=17  
- Each of these choices has only two 1 bits, so the number of multiplications required to perform exponentiation is minimised  
- With a very small public key, such as e = 3, RSA becomes vulnerable to a simple attack

## Efficient Operation Using the Private Key

Decryption uses exponentiation to power d  
- A small value of d is vulnerable to a brute-force attack and to other forms of cryptanalysis.

Can use the Chinese Remainder Theorem (CRT) to speed up computation  
- The quantities $d \mod (p – 1)$ and $d \mod (q – 1)$ can be precalculated.  

End result is that the calculation is approximately four times as fast as evaluating $M = Cd \mod n$ directly.

# RSA Security and Attacks

## The Security of RSA

**Five possible approaches to attacking RSA are:**
- Brute Force
- Chosen Ciphertext Attacks
- Mathematical Attacks
- Timing Attacks
- Hardware Fault-based Attacks

## Factoring Problem

We can identify three approaches to attacking RSA mathematically:
- Factor n into its two prime factors. This enables the calculation of $\phi(n) = (p-1)\times (q-1)$ which in turn enables the determination of $d = e-1(\mod\phi(n))$
- Determine $\phi(n)$ directly without first determining $p$ and $q$. Again this enables determination of $d=e-1(\mod\phi(n))$ 
- Determine d directly without first determining $\phi(n)$

## Timing Attacks

Paul Kocher, a cryptographic consultant, demonstrated that a snooper can determine a private key by keeping track of how long a computer takes to decipher messages.  

Are applicable not just to RSA but to other public-key cryptography systems.

Are alarming for two reasons:  
- It comes from a completely unexpected direction  
- It is a ciphertext-only attack

## Countermeasures

**Constant exponentiation time:**
- Ensure that all exponentiations take the same amount of time before returning a result; this is a simple fix but does degrade performance

**Random delay:** 
- Better performance could be achieved by adding a random delay  
to the exponentiation algorithm to confuse the timing attack

**Blinding:**
- Multiply the ciphertext by a random number before performing exponentiation; this process prevents the attacker from knowing   ciphertext bits are being processed inside the computer and therefore prevents the bit-by-bit analysis essential to the timing attack

## Fault-Based Attack

An attack on a processor that is generating RSA digital signatures  
- Induces faults in the signature computation by reducing the power to the processor  
- The faults cause the software to produce invalid signatures which can then be analysed by the attacker to recover the private key  

The attack algorithm involves inducing single-bit errors and observing the results.  

While worthy of consideration, this attack does not appear to be a serious threat to RSA  
- It requires that the attacker have physical access to the target machine and is able to directly control the input power to the processor


## Chosen Ciphertext Attack

The adversary chooses a number of ciphertexts and is then given the corresponding plaintexts, decrypted with the target’s private key  
- Thus the adversary could select a plaintext, encrypt it with the target’s public key, and then be able to get the plaintext back by having it decrypted with the private key  
- The adversary exploits properties of RSA and selects blocks of data that, when processed using the target’s private key, yield information needed for cryptanalysis  

To counter such attacks, RSA Security Inc. recommends modifying the plaintext using a procedure known as optimal asymmetric encryption padding (OAEP).