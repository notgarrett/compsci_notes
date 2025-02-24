---
date: 2025-01-22$
tags:
  - cryptography_and_network_security
---

# Definitions

**Plaintext:** An original message.

**Ciphertext:** The coded message.

**Enciphering/encryption:** The process of converting from plaintext to ciphertext.

**Deciphering/decryption:** Restoring the plaintext from the ciphertext.

**Cryptography:** The area of study of the many schemes used for encryption.

**Cryptographic system/cipher:** A scheme.

**Cryptanalysis:** Techniques used for deciphering a message without any knowledge of the enciphering details.

**Cryptology:** The area of cryptography and cryptanalysis

# Categories of Cryptographic Systems

Characterised along three independent dimensions:

The type of operations used for transforming plaintext to ciphertext:
- Substitution
- Transposition

The number of keys used:
- Symmetric, single-key, secret-key, conventional encryption
- Asymmetric, two-key, or public-key encryption

The way in which the plaintext is processed:
- Block cipher
- Stream cipher

# Symmetric Cipher Model


![[Symmetric Cipher Model|100%]]

There are two requirements for secure use of conventional encryption:
- A strong encryption algorithm and large key size
- Sender and receiver must have obtained copies of the secret key in a secure fashion and must keep the key secure


# Encryption Scheme Security and attacks

## Cryptanalysis and Brute-Force Attack

**Cryptanalysis:**
- Attack relies on the nature of the algorithm plus some knowledge of the general characteristics of the plaintext
- Attack exploits the characteristics of the algorithm to attempt to deduce a specific plaintext or to deduce the key being used

**Brute-force-attack:**
- Attacker tries every possible key on a piece of ciphertext until an intelligible translation into plaintext is obtained
- On average, half of all possible keys must be tried to achieve success.

## Types of Cryptanalytic Attacks


| Type of Attack    | Known to Cryptanalyst                                                                                                                                                                                                                                                                    |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Ciphertext Only   | - Encryption algorithm<br>- Ciphertext                                                                                                                                                                                                                                                   |
| Known Plaintext   | - Encryption algorithm<br>- Ciphertext<br>- One of more plaintext-ciphertext pairs formed with the secret key                                                                                                                                                                            |
| Chosen Plaintext  | - Encryption algorithm<br>- Ciphertext<br>- Plaintext message chosen by cryptanalyst, together with its corresponding ciphertext generated with the secret key                                                                                                                           |
| Chosen Ciphertext | - Encryption algorithm<br>- Ciphertext<br>- Ciphertext chosen by cryptanalyst, together with its corresponding decrypted plaintext generated with the secret key                                                                                                                         |
| Chosen Text       | - Encryption algorithm<br>- Ciphertext<br>- Plaintext message chosen by cryptanalyst, together with its corresponding ciphertext generated with the secret key<br>- Ciphertext chosen by cryptanalyst, together with its corresponding decrypted plaintext generated with the secret key |

## Encryption Scheme Security

Unconditionally secure
- No matter how much time an opponent has, it is impossible for them to decrypt the the ciphertext imply because the required information is not there.

Computationally secure
- The cost of breaking the cipher exceeds the value of the encrypted information
- The time required to break the cipher exceeds the useful lifetime of the information

## Strong Encryption

The term strong encryption refers to encryption schemes that make it impractically difficult for unauthorised persons or systems to gain access to plaintext that has been encrypted

Properties that make an encryption system strong are:
- Appropriate choice of cryptographic algorithm
- Use of sufficiently long key lengths
- Appropriate choice of protocols
- A well-engineered implementation
- Absence of deliberately introduced hidden flaws

# Transposition Ciphers

## Rail Fence Cipher

Simplest transposition cipher.

Plaintext is written down as a sequence of diagonals and then read off as a sequence of rows.

To encipher the message "meet me after the toga party" with a rail fence of depth 2, we would write:

m e m a t r h t g p r y
  e t e f e t e o a a t

Encrypted message is: MEMATRHTGPRYETEFETEOAAT

## Row Transposition Cipher

Is a more complex transposition.

Write the message in a rectangle, row by row, and read the message off, column by column, but permute the order of the columns.

The order of the columns then becomes the key to the algorithm.

```ad-tip
The key length will always determine the row length.
```

4 3 1 2 5 6 7
a t t a c k p
o s t p o n e
d u n t i l t
w o a m x y z

Our ciphertext here is: TTNAAPTMTSUOAODWCOIXKNLYPETZ

# Substitution ciphers

## Substitution Technique

Is one in which the letters of plaintext are replaced by other letters or by numbers or symbols.

If the plaintext is viewed as a sequence of bits, then substitution involves replacing plaintext bit patterns with ciphertext bit patterns.

## Caesar Cipher

Simplest and earliest known use of a substitution cipher.

Used by Julius Caesar. (The goat)

Involves replacing each letter of the alphabet with the letter standing three places further down the alphabet.

Alphabet is wrapped around so that the letter following Z is A.

Plaintext: meet me after the toga party
Cipher: PHHW PH DIWHU WKH WRJD SDUWB

Encryption algorithm expression:
$$c = E(k,p)=(p + k)mod(26)$$
where k is the shift and p is the letter (as a numerical value).

The decryption algorithm can be expressed as:
$$$$
$$p = D(k, C)=(C-k)mod(26)$$


```ad-warning
Don't use this to secure important data!
The caesar cipher can easily be bruteforced, because there is only 26 keys (each of length 2 or less).
```

## Mono-alphabetic Cipher

It is the permutation of a finite set of elements S is an ordered sequence of all the elements in S, with each element appearing exactly once.

If the cipher line can be any permutation of the 26 alphabetic characters, then there are 26! or greater than $4 \times 10^{26}$ possible keys.
- This is 10 orders of magnitude greater than the key space for DES
- Approach is referred to  as a mono alphabetic substitution cipher because a single cipher alphabet is used per message


UZQSOVUOHXMOPVGPOZPEVSGZWSZOPFPESXUDBMETSXAIZ  
VUEPHZHMDZSHZOWSFPAPPDTSVPQUZWYMXUZUHSX  
EPYEPOPDZSZUFPOMBZWPFUPZHMDJUDTMOHMQ

```ad-question
title: How would you decode this?

How you would decode this is to relate the frequencies of each of these letters, to the common frequencies of letters in the English alphabet. Then with some guess work you would translate this cipher. No character corresponds to a space, you have to figure thouse out yourself.
```

The cipher above translates to:

"it was disclosed yesterday that several informal but direct contacts have been made with political representatives of the Viet cong in Moscow"

## Playfair Cipher

Best known multiple letter encryption cipher.

Treats diagrams in the plaintext as single units and translates these units into ciphertext diagrams.

Based on the use of a 5 x 5 matrix of letters constructed using a keyword.

Invented by British scientist Sir Charles Wheatstone in 1854.

Used as the standard field system by the British Army in World War 1, and the US army and other allied forced in World War 2.

## Playfair Key Matrix

Fill in letters of keywords (minus duplicates) from left to right and from top to bottom, then fill in the remainder of the matrix with the remaining letters in alphabetic order.

Using the keyword MONARCHY

M O N A R 
C H Y B D
E F G I/J K
L P Q S T 
U V W X Z

1. Repeating plaintext letters that are in the same pair are separated with a filler letter, such as x, so that balloon would be treated as balxloon.
2. Two plaintext letters that fall in the same row of the matrix are each replaced by the letter to the right, with the first element of the row circularly following the last. For example, ar is encrypted as RM.
3. Two plaintext letters that fall in the same column are each replaced by the letter beneath, with the top element of the column circularly following the last For example, mu is encrypted as CM.
4. Otherwise, each plaintext letter in a pair is replaced by the letter that lies in its own row and the column occupied by the other plaintext letter. Thus, hs becomes BP and ea becomes IM (or JM, as the encipherer wishes).


## Hill Cipher

Developed by the mathematician Lester Hill in 1929.

Strength is that it completely hides single-letter frequencies.
- The use of a larger matrix hides more frequency information.
- A 3x3 hill cipher hides not only single-letter but also two-letter frequency information.

Strong against a ciphertext-only attack but easily broken with a known plaintext attack.

\[3x3\] plaintext, key, ciphertext

$$C = E(K,P) = PKmod(26)$$
$$P = D(K,C) = CK^{-1}mod(26)=PKK^{-1}=P$$

## Polyalphabetic Ciphers

Polyalphabetic substitution cipher.
- Improves on the simple monoalphabetic technique by using different monoalphabetic substitutions as one proceeds through the plaintext message.

```ad-note
All these techniques have the following features in common:
- A set of related monoalphabetic substituion rules is used.
- A key determines which particular rule is chosen for a given transformation.
```


## Vigenere Cipher

Best known and one of the simplest polyalphabetic substitution ciphers.

In this scheme the set of related monoalphabetic substitution rules consists of the 26 Caesar ciphers with shifts of 0 through 25.

Each cipher is denoted by a key letter which is the ciphertext letter that substitutes for the plaintext letter a.

$$Ci=(p_{i}+k_{i})mod(26)$$
$$\pi= (C_{i}-k_{i})mod(26)$$

This is just like the Caesar cipher, but your key is the translation for every letter.

## Vernam Cipher

Basically, it uses a generator to generate a key for the plaintext, and a generator that will eventually repeat the generated key for the decryption. 

## One-Time Pad

Improvement to the Vernam cipher proposed by an Army Signal Corp officer, Joseph Mauborgne.

Use a random key that is as long as the message so that the key need not be repeated.

Key is used to encrypt and decrypt single message and then is discarded.

Each new message requires a new key of the same length as the new message.

Scheme is unbreakable:
- Produces random output that bears no statistical relationship to the plaintext.
- Because the ciphertext contains no information whatsoever about the plaintext, there is simply no way to break the code.

```ad-danger
title: Difficulties
The one=time pad offers complete security butm in practice, has two fundamental difficulties:
- There is the practical problem of making large quantities of random keys
	- Any heavily used system might required millions of random characters on a regular basis
- Mammoth key distribution problem
	- For every message to be sent, a key of equal length is needed by both sender and receiver

Because of these difficulties, the one-time pad is of limited utility.
- Useful primarily for low-bandwidth channels requireing very high security
```

The one-time pad is the only cryptosystem that exhibits perfect secrecy.