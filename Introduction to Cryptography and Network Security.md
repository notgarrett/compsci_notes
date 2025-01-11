---
tags:
  - cryptography_and_network_security
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

