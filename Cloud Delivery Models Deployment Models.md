---
tags:
  - cloud_computing
  - comp_4312
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


## Software as a Service (SaaS)
