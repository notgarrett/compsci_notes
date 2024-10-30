---
tags:
  - cloud_computing
  - comp_4312
date: 2024-10-18
---
# Cloud Delivery Models

**Definition:** Represents a specific, pre-packaged combination of IT resources offered by a cloud provider.

#### Common Services

| IaaS | Infrastructures-as-a-service |
| ---- | ---------------------------- |
| PaaS | Platform-as-a-service        |
| Saas | Software-as-a-service        |

## Infrastructure as a Service (IaaS)

**IaaS** model represents a self contained IT environment comprised of **infrastructure-centric IT resources** that can be accessed and managed via *cloud service based interfaces and tools*.

The environment can include:
- hardware
- storage
- network/connectivity
- "raw" IT resources

IaaS provides consumers with a **high** level of control and **responsibility** over its configuration and utilisation.

```ad-summary
IaaS is typically a virtual server, giving the user hagh level control over configuration. The user can specify hardware, memory, storage space, and build a server good for them. AWS is an example of IaaS.
```

```plantuml
cloud "Cloud Provider" as userCloud {
[physical server] .. [virtual server]
[virtual server]
}

[Cloud Contract] .. [virtual server]
[cloud consumer] -> [virtual server]
[virtual server] -> [cloud consumer]
```

## Platform as a Service (PaaS)

PaaS represents a predefined "ready to use" environment typically comprised of *already deployed and configured IT resources*.

Relies on usage of a set of pre packaged product and tools.

By working within a ready made platform, the cloud consumer is spared the administrative burden of setting up and maintaining the bare infrastructure IT resources compared to via IaaS model.

```plantuml
cloud "Cloud Provider" {
	[virtual server] .. (?)
}
[cloud consumer] <-> [virtual server]
[cloud contract] .. [virtual server]
```

```ad-summary
PaaS, or Platform as a Service, is a cloud computing model that provides a platform allowing developers to build, deploy, and manage applications without the complexity of managing the underlying infrastructure. It offers a range of tools and services, such as development frameworks, databases, and middleware, enabling developers to focus on coding and innovation.

Heroku is an example of a PaaS.
```

## Software as a Service (SaaS)

A software program positioned as a shared cloud service and made available as a product or generic utility represents the typical profile of a SaaS offering. 

Very limited administrative control for the cloud consumer. 

```ad-summary
Basically a product or utility where the user gets little to no administrative control. Discord is technically a SaaS.
```

# Cloud Development Models

- Public Cloud
- Community Cloud
- Private Cloud
- Hybrid Cloud
\shutdown now

## Public Cloud

## Community Cloud

## Private Cloud

## Hybrid Cloud

