---
tags:
  - comp_4312
  - "#cloud_computing"
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

## Public Cloud

**Definition:** A public cloud is a publicly accessible cloud environment owned by a third party cloud provider.

IT resources on a public cloud are generally offered to cloud consumers at a cost or are commercialised via other avenues. (Example being advertisement)

The cloud provider is responsible for the creation and on going maintenance of the public cloud and pertaining resources.

## Community Cloud

**Definition:** Similar to a public cloud, however its access is limited to a specific *community* of cloud consumers.

The community cloud may be jointly owned by the *community members* or by a *third party cloud provider* that provisions a public cloud with limited access.

## Private Cloud

**Definition:** A private cloud is owned by a **single** organisation.

Private cloud enables an organisation to use cloud computing technology as a means of centralising access to IT resources by:
- different parts
- locations
- departments of the same organisation

The actual **administration** of a private cloud environment may be carried out by internal and outsourced staff.

With a private cloud, the same organisation is both consumer and provider by definition. To differentiate these roles:
- A seperate organisation department assumes the responsibility for provisioning the cloud.
- Departments requiring access to the cloud assume the cloud consumer role.

## Hybrid Cloud

**Definition:** A cloud environment comprised of two or more different cloud deployment models.

An example: A cloud consumer may choose to deploy cloud services processing sensitive data to a private cloud and less sensitive cloud services to a public cloud.

Hybrid deployment architecture is more complex and challenging due to the potential disparity in cloud environments.

# Availability

Cloud hardware is essentially built around a large cluster of servers. Clusters are inherently highly available due to redundancy brought by independent servers used in the cluster. In case of a single server failure, the jobs running on VMs hosted in the failing server can be migrated to surviving server hosts under software control.

High availability, or HA, is desired in all server clusters. Since a cloud system is essentially built on server clusters, HA also becomes a critical requirement. 

A cluster system is highly available if:
- It has long MTTF, the average system up-time between two adjacent failures.
- It has short MTTR, the average downtime after a failure or shutdown.

```ad-info
MTTF stands for mean time to failure.
MTTR stands for mean time to repair.

$$ClusterAvailability = \frac{MTTF}{MTTF + MTTR}$$
```



