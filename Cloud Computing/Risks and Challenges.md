# Risks and Challenges

## Increased Security Vulnerabilities

Shared data with cloud providers introduces more vulnerabilities. 

More opportunities for bad actors to attack resources and steal or damage information.

Unreliable cloud providers may not maintain the guarantees it makes in the SLAs (service level agreements).

![[UnreliableNetworkChallenge.excalidraw | center]]

## Limited portability between Cloud Providers

Due to a lack of established *industry standards* within the cloud computing industry, public clouds are commonly proprietary to various extents.

There are challenges in moving from one cloud provider to another.

Commonly, services don't tend to match up one for one. Different security technologies as well.

## Multi Regional Compliance and Legal Issues

Third party providers frequently establish data centres in affordable or convenient geographical locations. 

Example: Due to laws, UK requires personal data on their citizens to be kept in the country, creating legal complications with centres outside the country.

Countries have laws that require some types of data to be disclosed to certain government agencies For example, a European cloud consumer’s data that is located in the U S can be more easily accessed by government agencies(due to the U S Patriot Act) when compared to data located in many European Union countries.

# Roles, Boundaries, and Characteristics

## Roles

### Cloud Provider

Organisation that provides cloud based IT resources. 
The organisation is responsible for making *cloud services* available to cloud consumers as per agreed upon **SLA** guarantees.

### Cloud Consumer

Organisation or person that has a formal contract or agreement with the cloud provider to use IT resources. 

### Cloud Resource Administrator

A person or organisation responsible for administrating a cloud based IT resource.

The cloud resource admin can be the cloud consumer or provider within which the cloud service resides.

### Additional Roles
- Cloud auditor
	- Conducts independent assessments of cloud environments. Evaluates security, privacy, and performance.
- Cloud broker
	- Responsibility of managing and negotiating usage of cloud services between providers and consumers.
- Carrier
	- Responsible for providing the wire level connectivity between cloud consumers and cloud providers.

## Boundaries

### Organisational Boundary
An organisational boundary represents the physical perimeter that surrounds a set of IT resources that are owner and governed by an organisation.

### Trust Boundary
When an organisation assumes the role of cloud consumer to access cloud based IT resources, it needs to extend its trust beyond the physical boundary of the organisation to include parts of the cloud environment.

## Characteristics

### On Demand Usage

A cloud consumer can access cloud based IT resources with the freedom to self provision IT resources.

Once configured, usage of the self provisioned IT resources can be on demand and automated.

This characteristic enables the service based and usage driven features in mainstream clouds.

### Ubiquitous Access

Ubiquitous access represents the ability for a cloud service to be **widely accessible**.

From different locations, and different devices.

### Multi-tenancy

The characteristic of a software program that enables an instance of the program to serve different consumers (whereby each is isolated from the other), is referred to as multi-tenancy.

Multi-tenancy relies on the use of virtualisation technologies.

Through multi-tenancy, IT resources can be dynamically assigned and reassigned, according to cloud service consumer demands.

Resource pooling allows cloud providers to **pool large scale IT resources** to serve multiple cloud consumers. It is achieved through multi-tenancy technology.

### Elasticity

Elasticity is the automated ability of a cloud to transparently **scale IT resources** as required in response to runtime conditions or predetermined by the cloud consumer or provider.

Elasticity is often considered a core justification for the adoption of cloud computing related to the benefit of reduced investment and proportional cost.

Cloud providers with the vast IT resources can offer the greatest range of elasticity.

### Measured Range

The measured usage characteristic represents the ability of a cloud platform to keep track of the usage of its IT resources.

The cloud provider can charge c cloud consumer only for the IT resources actually used and/or for the time frame during which access to the IT resources was granted.

Measured usage is not limited to tracking statistics for billing purposes. It also encompasses the general monitoring of IT resources and relate usage reporting (for both cloud provider and cloud).

### Resiliency

Resilient computing is a form of fail over that distributes redundant implementations of IT resources across physical locations.

IT resources can be reconfigured so that if one becomes deficient, processing is automatically handled over to another redundant implementation.

Within cloud computing, the characteristic of resiliency can refer to redundant IT resources within the same cloud (but in different physical locations).


