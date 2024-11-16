---
tags:
  - cloud_computing
  - comp_4312
date: 2024-11-08
---
# Cloud Enabling Technology

Modern day clouds are under pinned by a set of primary technology components that collectively enable key features and characteristics associated with contemporary cloud computing.

These include:
- Broadband Networks and Internet Architecture
- Web Technology
- Data Centre Technology
- Virtualisation Technology
- Multi-tenant Technology
- Service Technology

# Broadband Networks and Internet Architecture

Established and deployed by ISPs (Internet Service Provider), the Internet's largest backbone networks are strategically interconnected by core routers that connect the world's multinational reworks.

ISPs can freely deploy, operate, and manage their networks. Additionally they also select partner ISPs for interconnection.

No centralised entity comprehensively governs the internet, although bodies like *Internet Corperation for Assigned Names and Numbers (ICANN)* supervise and coordinate internet communication.

The internet's topology has become a dynamic and complex aggregate of ISPs that are highly interconnected via its core protocols.

Smaller branches extend from these major nodes of interconnection, branching outwards through smaller networks until eventually reaching every internet enabled electronic device.

```ad-info
title: Tiers
 
The core Tier 1 is made of large-scale, international service providers that oversee massive interconnected global networks, which are connected to Tier 2's large regional providers.

The interconnected ISPs of Tier 2 connect with Tier 1 providers, as well as the local ISPs of Tier 3.

Cloud consumers and cloud providers can connect directly using a Tier 1 provider.
```

## Packet Switching

**End-to-end** data flows are divided into packets of a limited size that are received and processed through network switches and routers, then queued and forwarded from one intermediary node to the next.

Each packet carries the necessary location information, such as the IP or MAC address, to be processed and routed at every source intermediary, and destination node.

In circuit switching, a dedicated channel/link/connection has to be established before the call is made between users. Once established, the bandwidth of a channel/link/circuit is reserved until the call has finished.

Circuit switching can guarantee quality through dedicated bandwidth, but most of this bandwidth is wasted on "dead air".

## Router-based Interconnectivity

A router is a device that is connected to multiple networks through which it forwards packets.

Even when successive packets are part of the same data flow, routers process and forward packets individually while maintaining  the network topology information that locates the next node on the communication path between the source and destination nodes.

The internet's mesh structure connects internet hosts (end point systems) using multiple alternative network routes that are determined at runtime. 

```ad-info
title: Routing Protocols
RIP - Routing Information Protocal - used in some small networks
OSPF - Open Shortest Path First - Large enterprise networks
IS-IS - Intermediate System to Intermediate System - large service provider network backbone
BGP - Border Gateway Protocal - used among ISPS
```

## TCP/IP Internet Model

### Physical Network

IP packets are transmitted through underlying physical networks that connect adjacent nodes, such as Ethernet, SONET/OTN, 3G/4G networkds, etc. 

Physical networks comprise a data link layer that controls data transfers between neighbouring nodes, and a physical layer that transmits data bits through both wires and wireless media.

Corresponds to the Network Interface Layer in the TCP/IP model, and the physical layer + data link layer in the OSI model.

### Internet Layer

Two versions of IP (internet protocol) addressing exists today, IPv4, and IPv6. IPv4 has been around for more than 40 years, and IPv6 is being used to phase out IPv4 before complete depletion of assignable addresses bring the internet to a halt.
### Transport Layer Protocol

Transport layer protocals, such as TCP and UDP, use the IP to provide standardised, end to end communication support that facilitates the navigation of data packets across the internet. 

TCP: email, ftp, web browsing.

UDP: Some multicast and streaming applications, voice and video.

### Application Layer Protocol

Protocols such as HTTP, SMTP for email, BitTorrent for P2P, and SIP for IP telephony use transport layer protocols to standardise and enable specific data packet transferring methods over the internet. 

## Technical and Business Considerations