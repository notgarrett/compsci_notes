---
epoch: 1740341061831
modelKey: gemini-2.0-flash|google
tags:
  - copilot-conversation
---

**user**: Please generate me a test review based off these notes:

[[Public Key Cryptography and RSA]] 
[[Random Numbers and Stream Ciphers]]

Include summarising key points and going into detail on complicated sections. Finally, generate 10 test questions as well. 
[Timestamp: 2025/02/23 15:04:21]

**ai**: Okay, here's a test review summarizing the key points from the notes on [[Public Key Cryptography and RSA]] and [[Random Numbers and Stream Ciphers]], with detailed explanations of complicated sections and 10 test questions:

## Test Review: Public Key Cryptography, RSA, Random Numbers, and Stream Ciphers

### Public Key Cryptography and RSA

*   **Misconceptions:** Public key cryptography is not more secure than symmetric key cryptography *per se*. Security depends on key length, algorithm strength, and proper implementation. It also doesn't replace symmetric key crypto, but complements it.
*   **Principles:** Uses two keys: a public key for encryption and a private key for decryption. Based on mathematical problems that are easy to compute in one direction but hard to reverse (trapdoor functions).
*   **Requirements:**

    *   It must be computationally easy for a party B to generate the pair (public key KU$_{\text{b}}$, private key KR$_{\text{b}}$)
    *   It must be computationally easy for a sender A, knowing the public key and the message to be encrypted, M, to generate the corresponding ciphertext: C = E(KU$_{\text{b}}$, M)
    *   It must be computationally easy for the receiver B to decrypt the resulting ciphertext using the private key to recover the original message: M = D(KR$_{\text{b}}$, C)
    *   It must be computationally infeasible for an opponent, knowing the public key, KU$_{\text{b}}$, to determine the private key, KR$_{\text{b}}$
    *   It must be computationally infeasible for an opponent, knowing the public key, KU$_{\text{b}}$, and a ciphertext, C, to recover the original message, M
*   **Cryptanalysis:** Focuses on finding efficient ways to compute the private key from the public key or directly decrypting ciphertexts without knowing the private key.

#### RSA Algorithm

*   **Requirements:**

    *   $p$ and $q$ must be prime
    *   $p \neq q$
    *   $n = p * q$
    *   $gcd(\phi(n), e) = 1; 1 < e < \phi(n)$
    *   $\phi(n) = (p-1)(q-1)$
    *   $d \equiv e^{-1} \mod \phi(n)$
*   **Key Generation:**

    1.  Choose two large prime numbers $p$ and $q$.
    2.  Compute $n = p \times q$. $n$ is the modulus.
    3.  Compute $\phi(n) = (p-1)(q-1)$, where $\phi$ is Euler's totient function.
    4.  Choose an integer $e$ such that $1 < e < \phi(n)$ and $gcd(e, \phi(n)) = 1$. $e$ is the public exponent.
    5.  Compute $d$ such that $d \equiv e^{-1} \pmod{\phi(n)}$. $d$ is the private exponent.
    6.  Public key: $(n, e)$. Private key: $(n, d)$.
*   **Efficient Implementation:** Uses techniques like the Chinese Remainder Theorem (CRT) to speed up decryption.
*   **Security/Attacks:**

    *   **Brute Force:** Trying all possible private keys. Infeasible with large key sizes.
    *   **Chosen Ciphertext Attacks:** Exploiting properties of RSA by choosing specific ciphertexts to decrypt.
    *   **Mathematical Attacks:** Factoring the modulus $n$ into $p$ and $q$. The most common attack.
    *   **Timing Attacks:** Measuring the time it takes to perform decryption to infer information about the private key.
    *   **Fault-Based Attacks:** Introducing faults during computation to gain information about the private key.

### Random Numbers and Stream Ciphers

*   **Use of Random Numbers:** Crucial for key generation, initialization vectors (IVs), nonces, and other cryptographic parameters.
*   **Requirements for Randomness and Unpredictability:**

    *   **Randomness:** Uniform distribution, independence.
    *   **Unpredictability:** It should be computationally infeasible to predict future random numbers based on past ones.
*   **TRNGs (True Random Number Generators):** Use physical phenomena (e.g., thermal noise, radioactive decay) to generate random numbers.
*   **PRNGs (Pseudo-Random Number Generators):** Deterministic algorithms that produce sequences of numbers that appear random.
*   **PRF (Pseudo-Random Function):** A function that is computationally indistinguishable from a truly random function.
*   **PRNG Requirements:**

    *   Long period (the sequence shouldn't repeat too soon).
    *   Good statistical properties (should pass randomness tests).
    *   Unpredictability.
*   **Randomness Tests:**

    *   **Frequency Test:** Checks if the number of 0s and 1s in a sequence is approximately equal.
    *   **Runs Test:** Checks the number of runs (sequences of consecutive identical bits) of different lengths.
    *   **Maurer's Universal Statistical Test:** A more sophisticated test that looks for patterns in the sequence.
*   **Seed Requirements:** The seed must be chosen randomly and kept secret.
*   **Purpose-Built Algorithms:**

    *   **Linear Congruential Generator (LCG):** A simple PRNG of the form $X_{n+1} = (aX_n + c) \mod m$.
    *   **Blum Blum Shub (BBS):** A more secure PRNG based on the quadratic residuosity problem.
*   **PRNG using Block Ciphers:** Using a block cipher in counter mode to generate a pseudo-random sequence.
*   **Stream Cipher Architecture and Design Considerations:**

    *   **Architecture:** A stream cipher encrypts data one bit or byte at a time. It consists of a key stream generator and a mixing function (usually XOR).
    *   **Design Considerations:** Key stream should be unpredictable, have a long period, and be resistant to correlation attacks.

### Detailed Explanation of Complicated Sections

#### RSA Security and Attacks

The security of RSA relies on the difficulty of factoring large numbers. Mathematical attacks, such as the Quadratic Sieve and the General Number Field Sieve (GNFS), are the most significant threats. The complexity of these algorithms is sub-exponential, but they are still computationally intensive for sufficiently large numbers (e.g., 2048 bits or more).

Timing attacks exploit the fact that the time it takes to perform the modular exponentiation operation in RSA decryption can depend on the value of the private key bits. By carefully measuring these timings, an attacker can infer information about the private key. Countermeasures include using constant-time exponentiation algorithms and adding random delays.

#### PRNG Security

The security of a PRNG depends on its ability to resist prediction. Simple PRNGs like LCG are easily predictable if the parameters are known. More sophisticated PRNGs like BBS and those based on block ciphers are more resistant to prediction, but they are not foolproof. It's crucial to choose a PRNG that is appropriate for the security requirements of the application and to seed it with a truly random value.

### Test Questions

1.  Explain the difference between symmetric and public key cryptography. What are the advantages and disadvantages of each?
2.  Describe the RSA algorithm, including key generation, encryption, and decryption.
3.  What are the requirements for choosing the prime numbers $p$ and $q$ in RSA? Why are these requirements important?
4.  Explain how the Chinese Remainder Theorem (CRT) can be used to speed up RSA decryption.
5.  Describe the different types of attacks that can be mounted against RSA. What are the countermeasures for each type of attack?
6.  What are the requirements for a good random number generator in cryptography?
7.  Explain the difference between TRNGs and PRNGs. What are the advantages and disadvantages of each?
8.  Describe the Linear Congruential Generator (LCG). Why is it not suitable for cryptographic applications?
9.  Explain how a block cipher can be used to construct a PRNG.
10. What are the key design considerations for a stream cipher? What are some of the attacks that can be mounted against stream ciphers?


#### Sources:
- [Task-2-0698370-COMP4476-01](obsidian://open?vault=compsci_notes&file=Task-2-0698370-COMP4476-01)
- [Task-1-0698370-COMP4476-01](obsidian://open?vault=compsci_notes&file=Task-1-0698370-COMP4476-01)
- [Home](obsidian://open?vault=compsci_notes&file=Home)
[Timestamp: 2025/02/23 15:04:55]