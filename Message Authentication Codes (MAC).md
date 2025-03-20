---
date: 2025-03-20
tags:
  - cryptography_and_network_security
---

# Message Authentication Requirements

Disclosure  
- Release of message contents to any person or process not possessing the appropriate cryptographic key  

Traffic analysis  
- Discovery of the pattern of traffic between parties  

Masquerade  
- Insertion of messages into the network from a fraudulent source  

Content modification  
- Changes to the contents of a message, including insertion, deletion, transposition, and modification

Sequence modification  
- Any modification to a sequence of messages between parties, including insertion, deletion, and reordering  

Timing modification  
- Delay or replay of messages  

Source repudiation  
- Denial of transmission of message by source  

Destination repudiation  
- Denial of receipt of message by destination


# Message Authentication Functions

There are two levels of message authentication functions.
- Lower-level
	- There must be some sort of function that produces an authenticator.
- Higher-level
	- Uses the lower-level function as a primitive in an authentication protocol that enables a receiver to verify the authenticity of a message.


Hash function  
- A function that maps a message of any length into a fixed-length hash value which serves as the authenticator  

Message encryption  
- The ciphertext of the entire message serves as its authenticator  

Message authentication code (MAC)  
- A function of the message and a secret key that produces a fixed-length value that serves as the authenticator

# Requirements for MACs

Taking into account the types of attacks, the MAC needs to satisfy the following:

The first requirement deals with message replacement attacks, in which an opponent is able to construct a new message to match a given MAC, even though the opponent does not know and does not learn the key.

The second requirement deals with the need to thwart a brute-force attack based on chosen plaintext.

The final requirement dictates that the authentication algorithm should not be weaker with respect to certain parts or bits of the message than others.

# MACs Based on Hash Functions: HMAC


There has been increased interest in developing a MAC derived from a cryptographic hash function.

Motivations:  
- Cryptographic hash functions such as MD5 and SHA generally execute faster in software than symmetric block ciphers such as DES  
- Library code for cryptographic hash functions is widely available  

HMAC has been chosen as the mandatory-to-implement MAC for IP security.

Has also been issued as a NIST standard (FIPS 198).

# HMAC Design Objectives

**HMAC Design Objectives RFC 2104 lists the following objectives for HMAC:**

TO use, without modification, available hash functions.

To allow for easy replace-ability of the embedded hash function in case faster or more secure hash functions are found or required.

To preserve the original performance of the hash function without incurring a significant degradation.

To use and handle keys in a simple way.

To have a well understood cryptographic analysis of the strength and the authentication mechanisms based on reasonable assumptions about the embedded hash function.
