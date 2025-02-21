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

