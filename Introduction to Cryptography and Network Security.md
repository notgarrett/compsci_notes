---
tags:
  - "#cryptography_and_network_security"
date: 2025-01-08
---
# Cybersecurity

Cybersecurity is the collection of tools, policies, security concepts, security safeguards, guidelines, risk management approaches, actions, training, best practices, assurance, and technologies that can be used to protect the cyberspace environment and organisation and users' assets.

Organisation and users’ assets include connected computing devices, personnel, infrastructure, applications, services, telecommunications systems, and the totality of transmitted and/or stored information in the cyberspace environment. 

Cybersecurity strives to ensure the attainment and maintenance of the security properties of the organisation and users’ assets against relevant security risks in the cyberspace environment.  

The general security objectives comprise the following: availability; integrity, which may include data authenticity and non-repudiation; and confidentiality.

## Information Security

This term refers to preservation of confidentiality, integrity, and availability of information. In addition, other properties, such as authenticity, accountability, non-repudiation, and reliability can also be involved

## Network Security

This term refers to protection of networks and their service from unauthorised modification, destruction, or disclosure, and provision of assurance that the network performs its critical functions correctly and there are no harmful side effects

# Security Key Objectives

The cybersecurity definition introduces three key objectives that are at the heart of information and network security:  
- Confidentiality: This term covers two related concepts:  
	- Data confidentiality: Assures that private or confidential information is not made available or disclosed to unauthorised individuals.  
	- Privacy: Assures that individuals control or influence what information related to them may be collected and stored and by whom and to whom that information may be disclosed.

# OSI Security Architecture

![[OSI Security Architecture|100%]]

# Attacks, security services, and security mechanisms.

![[Attacks Services and Security|100%]]

# Security Attacks

## Threats and Attacks

**Threat**:
- A potential for violation of security, which exists when there is a circumstance, capability, action, or event that could breach security and cause harm. That is, a threat is a possible danger that might exploit a vulnerability.

**Attack**:
- An assault on system security that derives from an intelligent threat; that is, an intelligent act that is a deliberate attempt (especially in the sense of a method or technique) to evade security services and violate the security policy of a system.

## Types of security attacks

There are 2 types of security attacks (as classified by the X.800 and RFC 4949):
- Passive attacks
- Active attacks

A **passive** attack attempts to learn or make use of information from a system, however it does not effect the system resources. 
- Eavesdropping
- Monitoring

The goal of the attacker is to obtain transmitted information.

Examples:
- The release of message contents
- Traffic analysis

A **active** attack attempts to alter system resources or affect their operation.
- Involve some modification of the data stream or creation of a false stream
- Difficult to prevent because of the wide variety of potential physical, software, and network vulnerabilities

The goal of the defender is to detect attacks and to recover from any delays or disruptions caused.

# Security Services

## Authentication

Concerned with assuring that a communication is authentic.
- Authenticity in data means the data is transmitted from exactly where it claims it is being transmitted from.
- Involves:
	- Peer entity authentication (you are you)
	- Data origin authentication (the data comes from the origin)

## Access Control

The ability to limit and control the access to host systems and applications via communication links.

To achieve this, each entity trying to gain access must first be identified, or authenticated, so that access rights can be tailored to the individual.

## Data Confidentiality

The protection of transmitted data from passive attacks.
- Make sure your data is only able to be viewed by yourself and any recipients you want to access the data.

Protection of traffic flow from analysis.
- Requires that an attacker is blocked from observing the source and destination, frequency, length, or any other characteristics of the traffic on a communications facility.

## Data Integrity

The data is not changed without proper authorisation. 

Data Integrity Can apply to a stream of messages, a single message, or selected fields within a message.
 
Connection-oriented integrity service, one that deals with a stream of messages, assures that messages are received as sent with no duplication, insertion, modification, reordering, or replays.

A connectionless integrity service, one that deals with individual messages without regard to any larger context, generally provides protection against message modification only.

## Nonrepudiation

Prevents either sender or receiver from denying a transmitted message. 

When a message is sent, the receiver can prove the alleged sender in fact sent the message.

When a message is received, the sender can prove that the alleged receiver in fact received the message.

## Availability Service

Protects a system to insure its availability.

This service addresses the security concerned raised via denial-of-service attacks.

# Security Mechanisms

**Cryptographic algorithms:** We can distinguish between reversible cryptographic mechanisms and irreversible cryptographic mechanisms. A reversible cryptographic mechanism is simply an encryption algorithm that allows data to be encrypted and subsequently decrypted. Irreversible cryptographic mechanisms include hash algorithms and message authentication codes, which are used in digital signature and message authentication applications.  

**Data integrity:** This category covers a variety of mechanisms used to assure the integrity of a data unit or stream of data units.  

**Digital signature:** Data appended to, or a cryptographic transformation of, a data unit that allows a recipient of the data unit to prove the source and integrity of the data unit and protect against forgery.  

**Authentication exchange:** A mechanism intended to ensure the identity of an entity by means of information exchange.  

**Traffic padding:** The insertion of bits into gaps in a data stream to frustrate traffic analysis attempts.  

**Routing control:** Enables selection of particular physically or logically secure routes for certain data and allows routing changes, especially when a breach of security is suspected.  

**Notarisation:** The use of a trusted third party to assure certain properties of a data exchange  

**Access control:** A variety of mechanisms that enforce access rights to resources.

# Cryptography

Cryptography is a branch of mathematics that deals with the transformation (encoding and decoding) of data.

Cryptographic algorithms are used in many ways in information security and network security.

# Cryptographic Algorithms 

![[Cryptographic algorithms|100%]]

## Keyless Algorithms

Deterministic functions that have certain properties useful for cryptography.

One type of keyless algorithm is the cryptographic hash function.
- A hash function turns a variable amount of text into a small, fixed-length value called a hash value, hash code, or digest.
- A cryptographic hash function is one that has additional properties that make it useful as part of another cryptographic algorithm, such as a message authentication code or a digital signature.

A pseudorandom number generator produces a deterministic sequence of numbers or bits that has the appearance of being a truly random sequence.

## Single-key Algorithms

Single-key cryptographic algorithms depend on the use of the secret key.

Encryption algorithms that use a single key are referred to as symmetric encryption algorithms.

Symmetric encryption algorithms take forms such as:
- Block cipher
- Stream cipher

## Asymmetric Algorithms

Encryption algorithms that use different keys for coding and decoding are referred to as asymmetric encryption algorithms.

Some examples of this are:
- Digital signature algorithm
- Key exchange
- User authentication

# Network Security

Network security is a broad term that encompasses security of the communications pathways of the network and the security of network devices and devices attached to the network.

![[elements of network security|100%]]



# Communications Security

Deals with the protection of communications through the network, including measures to protect against both passive and active attacks.

Communications security is primarily implemented using network protocols.
- A network protocol consists of the format and procedures that governs the transmitting and receiving of data between points in a network.
- A protocol defines the structure of the individual data units and the control commands that manage the data transfer

With respect to network security, a security protocol may be an enhancement that is part of an existing protocol or a standalone protocol.

# Device Security

The other aspect of network security is the protection of network devices, such as routers and switches, and end systems connected to the network, such as client systems and servers.

the primary security concerns are intruders that gain access to the system to perform unauthorised actions, insert malicious software, or overwhelm system resources to diminish availability.

Some examples of this are:
- Firewall
- Intrusion detection
- Intrusion prevention

# Standards 

**National Institute of Standards and Technology:**
- NIST is a U.S. federal agency that deals with measurement science, standards, and technology related to U.S. government use and to the promotion of U.S. private-sector innovation. Despite its national scope, NIST Federal Information Processing Standards (FIPS) and Special Publications (SP) have a worldwide impact.

**Internet Society:**
- ISOC is a professional membership society with worldwide organisational and individual membership. It provides leadership in addressing issues that confront the future of the Internet and is the organisation home for the groups responsible for Internet infrastructure standards, including the Internet Engineering Task Force (IETF) and the Internet Architecture Board (IAB). These organisations develop Internet standards and related specifications, all of which are published as Requests for Comments (RFCs).

**ITU-T:**
- The International Telecommunication Union (ITU) is an international organisation within the United Nations System in which governments and the private sector coordinate global telecom networks and services. The ITU Telecommunication Standardisation Sector (ITU-T) is one of the three sectors of the ITU. ITU-T’s mission is the development of technical standards covering all fields of telecommunications. ITU-T standards are referred to as Recommendations.

**ISO:**
- The International Organisation for Standardisation (ISO) is a worldwide federation of national standards bodies from more than 140 countries, one from each country. ISO is a nongovernmental organisation that promotes the development of standardisation and related activities with a view to facilitating the international exchange of goods and services and to developing cooperation in the spheres of intellectual, scientific, technological, and economic activity. ISO’s work results in international agreements that are published as International Standards.