---
date: 2025-01-29
tags:
  - cryptography_and_network_security
---
# Modes of Operation

A technique for enhancing the effect of a cryptographic algorithm or adapting the algorithm for an application.

To apply a block cipher in a cariety of applications, five modes of operation have been defined by NIST.
- The five modes are intended to cover a wide variety of applications of encryption for which a block cipher could be used.
- These modes are intended for use with any symmetric block cipher, include triple DES and AES.

# Block Cipher Modes of Operation

| Mode                             | Description                                                                                                                                                                                                   | Typical Application                                                                   |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| Electronic  <br>Codebook (ECB)   | Each block of plaintext bits is encoded independently using the same key.                                                                                                                                     | - Secure transmission of single  <br>values (e.g., an encryption key)                 |
| Cipher Block  <br>Chaining (CBC) | The input to the encryption algorithm is the XOR of the next block of plaintext and the preceding block of ciphertext                                                                                         | - General-purpose block-oriented transmission  <br>- Authentication                   |
| Cipher Feedback  <br>(CFB)       | Input is processed s bits at a time. Preceding ciphertext is used as input to the encryption algorithm to produce pseudorandom  <br>output, which is XORed with plaintext to produce next unit of ciphertext. | - General-purpose stream-oriented transmission<br>- Authentication                    |
| Output Feedback  <br>(OFB)       | Similar to CFB, except that the input to the encryption algorithm is the preceding  <br>encryption output, and full blocks are used.                                                                          | - Stream-oriented transmission over noisy channel (e.g. satellite communication)      |
| Counter (CTR)                    | Each block of plaintext is XORed with an encrypted counter. The counter is  <br>incremented for each subsequent block.                                                                                        | - General-purpose block-oriented transmission<br>- Useful for high-speed requirements |

# Criteria and properties for evaluating and constructing block cipher modes of operation that are superior to ECB:

- Overhead
- Error recovery
- Error propagation
- Diffusion
- Security

# Cipher Feedback Mode

For AES, DES, or any block cipher, encryption is performed on a block of b bits
- DES b = 64
- AES b = 128

There are three modes that make it possible to convert a block cipher into a stream cipher:
- Cipher feedback (CFB) mode
- Output feedback (OFB) mode
- Counter (CTR) mode









