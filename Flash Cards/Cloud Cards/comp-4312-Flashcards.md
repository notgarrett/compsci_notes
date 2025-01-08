---
tags:
  - comp_4312
  - cloud_computing
  - "#flashcards"
  - deck1
date: 2024-11-27
sr-due: 2027-11-05
sr-interval: 1072
sr-ease: 235
---

``
## Lecture 9

>[!question]
>What is Information Security
?
>>[!answer]
>>A complex ensemble of techniques, technologies, regulations, and behaviours that collaboratively protect the integrity of and accessibility to computer systems and data.
<!--SR:!2024-12-01,4,270-->

>[!question]
>IT security measures
?
>>[!answer]
>>Aim to defend against threats and interference that arise from both malicious intent and unintentional user errors.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Confidentiality
?
>>[!answer]
>>Something being made accessible only to Authorized Parties.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Integrity
?
>>[!answer]
>>Something not having been altered by an unauthorized party.
<!--SR:!2024-12-01,3,250-->

>[!question]
>What is Authenticity
?
>>[!answer]
>>Something having been provided by an Authorized Source.
>>
>> Non-repudiation
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Availability
?
>>[!answer]
>>Being accessible and usable during a specified period of time.
>>
>>In typical cloud environments, the availability of cloud services can be a responsibility that is shared by the cloud provider and cloud carrier.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Threat
?
>>[!answer]
>>A potential security violation that can challenge defences in an attempt to breach privacy and/or cause harm.
>>
>>A threat that is carried out results in an **Attack**.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Vulnerability
?
>>[!answer]
>>A weakness that can be exploited either because it is protected by insufficient security controls, or because existing security controls are overcome by an attack.
>>
>>Range of causes:
>>- Configuration
>>- Security Policy
>>- User Error
>>- Hardware/Firmware
>>- Software
>>- Architecture
<!--SR:!2024-11-30,3,250-->

>[!question]
>What is Risk
?
>>[!answer]
>>The possibility of loss or harm arising from performing an activity.
>>
>>Measured according to threat level and number of possible/known vulnerabilities.
>>
>>Two metrics:
>>- Probability of a threat occurring to exploit vulnerabilities
>>- Expectation of loss after being compromised
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are Security Controls
?
>>[!answer]
>>Countermeasures or safeguards to prevent or respond to security threats and to reduce/avoid risk.
>>
>>3 Categories:
>>- Administrative: Risk Assessments, Training Programs
>>- Technical: Firewalls, Encryption
>>- Physical: Surveillance, Locked Rooms
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are Security Mechanisms
?
>>[!answer]
>>The actual components comprising a defensive framework that protects IT resources, information, and services.
>>
>>Examples:
>>- Encryption Algorithms
>>- Access Control Mechanisms
>>- Intrusion Detection Systems
>>- Tokenization
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are some key differences between Security Controls and Security Mechanisms
?
>>[!answer]
>>**Scope**: Security controls define "what" needs to be done to secure the system, whereas security mechanisms focus on "how" those requirements will be implemented.
>>
>>**Purpose**: Controls are more about policy and governance, while mechanisms are about execution and implementation.
>>
>>**Level of Abstraction**: Controls are generally high-level and strategic, while mechanisms are more detailed and technical.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are Security Policies
?
>>[!answer]
>>Establishes a set of security rules and regulations.
>>
>>Defines how the rules and regulations are implemented and enforced.
>>
>>The positioning and usage of Security Controls and Security Mechanism can be determined by Security Policies.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are the 4 types of Threat Agents
?
>>[!answer]
>>1. Anon Attacker
>>2. Malicious Service Agent
>>3. Trusted Attacker
>>4. Malicious Insider
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is an Anonymous Attacker
?
>>[!answer]
>>A non-trusted cloud service consumer without permission in the cloud.
>>![[Pasted image 20241021121933.png]]
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Malicious Service Agent
?
>>[!answer]
>>A service agent that can intercept and forward network traffic with compromised or malicious logic.
>>![[Pasted image 20241021121856.png]]
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Trusted Attacker
?
>>[!answer]
>>Someone who shares IT resources in the same cloud environment as the cloud consumer and attempts to exploit the legitimate credentials to target cloud providers and the other tenants on the cloud.
>>
>>Attack from within.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Malicious Insider
?
>>[!answer]
>>Human threat agents acting on behalf of or in relation to a cloud provider.
>>
>>Typically current or former employees or third parties with access to the cloud provider's premises.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is the notation used to represent an attack originating from a workstation
?
>>[!answer]
>>![[Pasted image 20241021122306.png]]
<!--SR:!2024-11-29,1,215-->

## Lecture 10

>[!question]
>Cloud infrastructure mechanisms are foundational building blocks of cloud environments that establish \_\_\_\_ to form the basis of fundamental cloud technology \_\_\_\_ .
?
>>[!answer]
>>- Primary Artifacts
>>- Architecture
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are 6 Cloud Infrastructure Mechanisms?
?
>>[!answer]
>>- Logical Network Perimeter
>>- Virtual Server
>>- Cloud Storage Devices
>>- Cloud Usage Monitor
>>- Resource Replication
>>- Ready Made Environment
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Logical Network Perimeter?
?
>>[!answer]
>>- The isolation of a network from the rest of the communications network environment.
>>- It establishes a virtual network boundary to keep a group of related cloud-based physically distributed IT resources, encompassed and isolated.
>>
>>![[Pasted image 20241125135843.png]]
<!--SR:!2024-12-01,4,270-->

>[!question]
>What can a Logical Network Perimeter do?
?
>>[!answer]
>>- Isolate IT resources in a cloud from:
>>	- Non-authorized users
>>	- Non-users
>>	- cloud consumers
>>- Control the bandwidth that is available to isolate IT resources
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Virtual Firewall?
?
>>[!answer]
>>An IT resource that actively filters network traffic to and from the isolated network while controlling its interactions with the Internet.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Virtual Network?
?
>>[!answer]
>>Usually acquired through VLANs – it isolates the network environment within the data centre infrastructure.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125140703.png]]
?
>>[!answer]
>>One logical network perimeter contains a cloud consumer's on-premise environment.
>>
>>The other contains a cloud provider's cloud-based environment.
>>
>>The perimeters are connected through a VPN that protects communications during their transit. Since the VPN is typically implement by point-to-point encryption of the data packets sent between the communication endpoints.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Virtual Server?
?
>>[!answer]
>>A virtual server is a form of virtualization software that emulates a physical server.
>>
>>A commodity mechanism.
>>
>>Represents the most foundational building block of cloud environments.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are Virtual Servers used for?
?
>>[!answer]
>>Used by cloud providers to share the same physical server with multiple cloud consumers by providing cloud consumers with individual virtual server instances.
>>
>>Each virtual server can host numerous IT resources, cloud-based solutions, and other cloud computing mechanisms.
>>
>>Instantiation of Virtual Servers from image files is a resource allocation process that can be completed rapidly and on-demand.
>>
>>Cloud consumers that install or lease virtual servers can customize these environments independently from other cloud consumers that may be using virtual servers hosted by the same underlying physical server.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125141654.png]]
?
>>[!answer]
>>The first physical server hosts two virtual servers, while the second physical server hosts one virtual server.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125143030.png]]
?
>>[!answer]
>>A virtual server that hosts a cloud service being accessed by Cloud Service Consumer B.
>>
>>Cloud Service Consumer A accesses the virtual server directly to perform an administration task.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Virtual Infrastructure Manager (VIM)?
?
>>[!answer]
>>A virtual infrastructure manager (VIM) is an infrastructure component.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does a Virtual Infrastructure Manager (VIM) do?
?
>>[!answer]
>>It coordinates the server hardware so that virtual server instances can be created from the most convenient underlying physical server.
>>
>>Provides a range of features for administering multiple hypervisors across physical servers.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Hypervisor (AKA Virtual Machine Monitor (VMM))?
?
>>[!answer]
>>A hypervisor or VMM is a piece of computer software, firmware, or hardware that creates and runs virtual machines.
>>
>>Fundamental part of virtualization infrastructure that is primarily used to generate virtual server instances of a physical server.
>>
>>Generally limited to one physical server, and can therefore only create virtual images of that server.
>>
>>Can only assign virtual servers it generates to resource pools that reside on the underlying physical server.
>>
>>Has limited virtual server management features, such as increasing capacity or shutting it down.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What is a Host Machine?
?
>>[!answer]
>>A computer on which a hypervisor runs one or more virtual machines (each of which is called a guest machine).
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125144454.png]]
?
>>[!answer]
>>Virtual servers are created via the physical servers' hypervisors and a central VIM.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What are Cloud Storage Devices?
?
>>[!answer]
>>A cloud storage device mechanism represents storage devices designed specifically for cloud-based provisioning.
>>
>>Instances of these devices can be virtualized, similar to how physical servers can spawn virtual server images.
>>
>>Commonly able to provide fixed-increment capacity allocation in support of the pay-per-use mechanism.
>>
>>Can be exposed for remote access via cloud storage services.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are some Issues related to Storage?
?
>>[!answer]
>>- The 3 primary concerns are:
>>	- Security
>>	- Integrity
>>	- Confidentiality
>>- Legal and Regulatory implications due to relocating data across geographical or national boundaries.
>>- Large databases can have performance issues.
>>- LANs provide locally stored data with better network reliability and latency levels compared to that of WANs.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are 4 common logical units of data storage?
?
>>[!answer]
>>- Files: Collections of data are grouped into files that located in folders.
>>- Blocks: Lowest level of storage and the closest to the hardware, a block is the smallest unit of data that is still individually accessible.
>>- Datasets: Sets of data are organized into a table-based or delimited record format.
>>- Objects: Data and its associated metadata are organized as web-based resources.
<!--SR:!2024-11-30,3,250-->

>[!question]
>Describe the Cloud Storage structure.
?
>>[!answer]
>>- Network Storage
>>	- File Access
>>		- iSCSI: internet Small Computer System Inferface
>>		- FC: Fiber Channel
>>		- FCoE: Fiber Channel over Ethernet
>>		- LUN: Logical Unit Number
>>	- Block Access
>>		- POSIX: Portable Operating System Interface
>>		- NFS: Network File System
>>		- CIFS: Common Internet File System
>>- Object Storage
>>	- Object Access
>>		- CURD: Create Update Read Delete
>>		- CDM: Cloud Data Management
>>- Dataset Storage
>>	- Dataset Access
>>		- SQL: Structured Query Language
>>		- NoSQL: see above
<!--SR:!2024-11-30,3,250-->

>[!question]
>Describe Network Storage Interfaces?
?
>>[!answer]
>>Storage processing levels and threshold for file allocation are usually determined by the file system itself.
>>
>>Block storage requires data to be in a fixed format (data block), which is the smallest unit that can be stored and accessed and the storage format closest to hardware.
>>
>>Using either the logical unit number or virtual volume block-level storage will typically have better performance than file-level storage.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125163651.png]]
?
>>[!answer]
>>- 1: The cloud consumer uses the usage and administration portal to create and assign a cloud storage device to an existing virtual server.
>>- 2a: The usage and administration portal interacts with the VIM software,
>>- 2b: which creates and configures the appropriate LUN.
>>- 3a: Each cloud storage device uses a seperate LUN controlled by the virtualization platform. The cloud consumer remotely logs the virtual server directly,
>>- 3b: to access the cloud storage device.
<!--SR:!2024-11-29,1,215-->

>[!question]
> Describe Object Storage Interfaces?
?
>>[!answer]
>>Various types of data can be referenced and stored as Web Resources (or just resources).
>>
>>This is referred to as object storage, which is based on technologies that can support a range of data and media types.
>>
>>Mechanisms that implement this interface can typically be accessed via REST or Web service-based cloud services using HTTP as the prime protocol.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125163715.png]]
?
>>[!answer]
>>1. The cloud consumer interacts with the usage and administration portal to create a cloud storage device and define access control policies.
>>2. The usage and administration portal interact with the cloud storage software to create the cloud storage device instance and apply the required access policy to its data objects.
>>3. Each data object is assigned to a cloud device and all of the data objects are stored in the same virtual storage volume. The cloud consumer uses the proprietary cloud storage device UI to interact directly with the data objects.
<!--SR:!2024-11-29,1,215-->

>[!question]
>Describe Database Storage Interfaces?
?
>>[!answer]
>>Typically support a query language in addition to basic storage operations.
>>
>>Management is carried out using standard API or an admin UI.
>>
>>Divided into 2 main categories:
>>- Relational Data Storage (SQL)
>>- Non Relational Data Storage (NoSQL)
<!--SR:!2024-12-01,4,270-->

>[!question]
>Describe Relational Storage? What are some of its issues?
?
>>[!answer]
>>Rely on tables to organize similar data into rows and columns.
>>
>>Based on any number of commercially available database products:
>>- Oracle Database
>>- Microsoft SQL Server
>>- MySQL
>>
>>Traditionally, on-premise IT environments store data using relational database management systems (RDBMSs).
>>
>>Issues:
>>- Scaling vertically can be more complex and less cost-effective than horizontal scaling.
>>- Complex relationships and/or large volumes of data can be afflicted with higher processing overhead and latency, especially when accessed remotely via cloud services.
<!--SR:!2024-11-30,2,230-->

>[!question]
>Describe Non-Relational Storage? What are some of its issues?
?
>>[!answer]
>>Establishes a "looser" structure data with less emphasis on defining relationships and data normalization.
>>
>>Can be more horizontally scalable than relational databases.
>>
>>Trade-off is loses of much of the native form and validation due to the limited or primitive schemas or data models.
>>
>>Don't tend to support relational database functions like transactions or joins.
>>
>>Motivation is to avoid the potential complexity and processing overhead imposed by relational databases.
>>
>>Issues:
>>- Normalized data exported into a non-relational storage repository will usually become de-normalized, meaning that the size of the data will typically grow.
>>- Cloud providers often offer non-relational storage that provides scalability and availability of stored data over multiple server environments.
<!--SR:!2024-11-29,1,210-->

>[!question]
>What is a Cloud Usage Monitor?
?
>>[!answer]
>>A cloud usage monitor mechanism is a lightweight and autonomous processing module responsible for collecting and processing IT resource usage data.
>>
>>Depending on the type of usage metrics cloud usage monitors can exist in different formats.
>>
>>Each can be designed to forward collected usage data to a log database for post-processing and reporting purposes.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are 3 common agent-based implementation formats for the cloud usage monitor mechanism?
?
>>[!answer]
>>- Monitoring Agent
>>- Resource Agent
>>- Polling Agent
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Monitoring Agent?
?
>>[!answer]
>>A monitoring agent is an intermediary, event-driven program that exits as a service agent and resides along existing communication paths to transparently monitor and analyse data flows.
>>
>>Commonly used to measure network traffic and message metrics.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125160612.png]]
?
>>[!answer]
>>- 1: A cloud service consumer sends a request message to a cloud service.
>>- 2: The monitoring agent intercepts the message to collect relevant usage data,
>>- 3a: before allowing it to continue to the cloud service.
>>- 3b: The monitoring agent stores the collected usage data in a log database.
>>- 4: The cloud service replies with a response message.
>>- 5: The message in sent back to the consumer without being intercepted by the monitoring agent.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Resource Agent?
?
>>[!answer]
>>A resource agent is a processing module designed to collect usage data by having event-driven interactions with specialized resource software.
>>
>>Commonly used to measure observable events at the resource software level, for example:
>>- Initiating
>>- Suspending
>>- Resuming
>>- Vertical Scaling
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125160628.png]]
?
>>[!answer]
>>1. The resource agent is actively monitoring a virtual server and detects an increase in usage.
>>2. The resource agent receives a notification from the underlying resource management program that the virtual server is being scaled up and stores the collected usage data in a log database, as per its monitoring metrics.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Polling Agent?
?
>>[!answer]
>>A polling agent is a processing module that collects cloud service usage data by polling IT resources.
>>
>>Commonly used to periodically monitor IT resource status, such as uptime and downtime.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125160644.png]]
?
>>[!answer]
>>1. A polling agent monitors the status of a cloud service hosted by a virtual server by sending periodic polling request messages and receiving polling response messages that report usage status "A" after a number of polling cycles, until it receives a usage status of "B".
>>2. Upon which the polling agent records the new usage status in the log database.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is Resource Replication?
?
>>[!answer]
>>The creation of multiple instances of the same IT resource, replication is typically performed when an IT resource's availability and performance need to be enhanced.
>>
>>Virtualization technology is used to implement the resource replication mechanism to replicate cloud-based IT resources.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125155753.png]]
?
>>[!answer]
>>A hypervisor replicates several instances of a virtual server, using a stored virtual server image.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Ready-Made Environment?
?
>>[!answer]
>>A ready-made cloud environment mechanism represents a pre-defined, cloud-based platform comprised of a set of already installed IT resources, ready to be used and customized by a cloud consumer.
>>
>>Typically includes a complete software development kit (SDK) enabling cloud consumers programmatic access to whatever SDK comprise its programming stack.
>>
>>A defining component of the PaaS cloud delivery model.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241125160047.png]]
?
>>[!answer]
>>A cloud consumer accesses a ready-made environment hosted on a virtual server.
<!--SR:!2024-11-29,1,215-->

## Lecture 11

>[!question]
>What is a Automated Scaling Listener?
?
>>[!answer]
>>A service agent that monitors and keeps track of communication between service consumers and services for load balancing purposes.
>>
>>It resides within the cloud, typically near the firewall, from where it automatically tracks load status information.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are 2 different types of responses to load fluctuation conditions that a Automated Scaling Listener may provide?
?
>>[!answer]
>>1. Automatically scale out or scale in IT resources based on parameters previously defined by the cloud consumer (Auto-Scaling).
>>2. Automatically notify the cloud consumer when loads exceed current threshold or are falling below allocated resources.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126140920.png]]
?
>>[!answer]
>>1. Three cloud service consumers attempt to access one cloud service simultaneously.
>>2. The automated scaling listener scales out and initiates the creation of three redundant instance of the service.
>>3. A fourth cloud service consumer attempts to use the cloud service.
>>4. Programmed to allow up to only three instance of the cloud service, the automated scaling listener rejects the fourth attempt and notifies the cloud consumer that the requested workload limit has been exceeded.
>>5. The cloud consumer's cloud resource administrator accesses the remote administration environment to adjust the provisioning setup and increase the redundant instance limit.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Load Balancer?
?
>>[!answer]
>>A runtime agent with pre-programmed logics – Primarily for horizontal scaling.
>>
>>A common purpose of horizontal scaling is workload balancing across two or more IT resources to increase the performance and the capacity that a single IT resource cannot provide.
>>
>>Performs a range of specialized runtime workload distribution functions:
>>- Asymmetric Distribution: Issuing larger workloads to IT resources with higher processing capacities.
>>- Workload Prioritization: Scheduling, queuing, discarding, and distributing workloads according to their priority levels.
>>- Content-Aware Distribution: Distributing requests to different IT resources as dictated by the content of each request.
<!--SR:!2024-11-29,1,210-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126135900.png]]
?
>>[!answer]
>>A load balancer implemented as a service agent transparently distributes incoming workload request messages across two redundant cloud service implementations, which in turn maximizes performance for the cloud service consumers.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What are 4 different Load Balancer mechanisms
?
>>[!answer]
>>- Multi-Layer Network Switch
>>- Dedicated Load Balancer Hardware Appliance
>>- Dedicated Software-Based
>>- Service Agent
<!--SR:!2024-12-01,4,270-->

>[!question]
>How does Load Balancing work as a Service?
?
>>[!answer]
>>Enables networking to distribute incoming requests evenly among designated instances.
>>
>>Distribution ensures that the workload is shared predictably among instances and enables more effective use of system resources.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are 3 Load Balancing methods to distribute incoming requests?
?
>>[!answer]
>>- Round Robin: Rotates requests evenly between multiple instances.
>>- Source IP: Requests from a unique source IP address are consistently directed to the same instance.
>>- Least Connection: Allocates request to the instance with the least number of active connections.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126140547.png]]
?
>>[!answer]
>>New instances of the cloud services are automatically created to meet increasing usage requests. The load balancer uses round-robin scheduling to ensure that the traffic is distributed evenly among the active cloud services.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Service Level Agreement Monitor?
?
>>[!answer]
>>Specifically used to observe the runtime performance of cloud services to ensure that they are fulfilling contractual quality-of-service (QoS) requirements, as published in the service level agreement.
>>
>>The data collected by the SLA monitor is prcessed by an SLA management system to be aggregated into SLA reporting metrics.
>>
>>The system can also proactively repair or failover cloud services when exceptions conditions occur, such as when the SLA monitor reports a cloud service as "down".
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126141440.png]]
?
>>[!answer]
>>Step 1: "up-time": The SLA monitor polls the cloud service sending polling request messages $M_{REQ_{1}}$ to $M_{REQ_{N}}$; and receives the respective polling response messages $M_{REP_{1}}$ to $M_{REP_{N}}$ reporting that the service is 'up' at each polling cycle (1a). The SLA monitor stores the 'up' time period (time it takes to poll cycles 1 to N) in the log database (1b).
>>
>>Step 2: "down-time": The SLA monitor polls the cloud service sending polling request messages $M_{REQ_{N+1}}$ to $M_{REQ_{N+M}}$ and polling response messages are not received (2a). While the response messages keep timing out, the SLA monitor stores the 'down' time period (time it takes the poll cycles N+1 to N+M) in the log database (2b).
>>
>>Step 3: "up-time": The data collected by the SLA monitor is usually processed by a SLA management system that is responsible for processing the data collected during usage and aggregate it in more manageable and meaningful SLA metrics.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Pay-Per-Use Monitor?
?
>>[!answer]
>>Implemented as a resource agent.
>>
>>Measures cloud-based IT resource usage based on predefined parameters in pricing plans and generates usage logs for fee calculations.
>>
>>The data collected is processed by a billing system that calculates payment fees.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are 3 monitoring variables collected by the Pay-Per-Use Monitor?
?
>>[!answer]
>>- Request/Response message quantities (how many are sent)
>>- Transmitted data volume (how much is sent)
>>- Bandwidth consumption
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126211210.png]]
?
>>[!answer]
>>1. A cloud consumer requests the creation of a new instance of a cloud service.
>>2. The IT resource is instantiated and the pay-per-use monitor receives a "start" event notification from the resource software.
>>3. The pay-per-use monitor stores the value timestamp in the log database.
>>4. The cloud consumer later requests that the cloud service to instance be stopped.
>>5. The pay-per-use monitor receives a "stop" event notification from the resource software and...
>>6. stores the value timestamp in the log database.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126211530.png]]
?
>>[!answer]
>>- 1: A cloud service consumer sends a request message to the cloud service.
>>- 2: The pay-per-use monitor intercepts the message.
>>- 3a: forwards it to the cloud service.
>>- 3b: and stores the usage information in accordance with its monitoring metrics.
>>- 4: The cloud service forwards the response message back to the cloud service consumer to provide the requested service.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is an Audit Monitor?
?
>>[!answer]
>>A specialized cloud usage monitor that is used for collecting data for network and system audits.
>>
>>The data is commonly called audit track data.
>>
>>The data collected is usually specified by the auditing requirements, required by regulatory, compliance, and consumer-provider contact conditions.
>>
>>Data can be chosen from a broad selection of monitoring data types.
<!--SR:!2024-11-30,3,250-->

>[!question]
>![[Pasted image 20241126211743.png]]
?
>>[!answer]
>>1. A cloud service consumer requests access to a cloud service by sending a login request message with security credentials.
>>2. The audit monitor intercepts the message.
>>3. and forwards it to the authentication service.
>>4. The authentication service processes the security credentials. A response message is generated for the cloud service consumer, in addition the results from the login attempt.
>>5. The audit monitor intercepts the response message and store the entire collected login event details in the log database, as per the organization's audit policy requirements.
>>6. Access has been granted, and a response is sent back to the cloud service consumer.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Failover System?
?
>>[!answer]
>>Increases reliability and availability by using established clustering technology to provide redundant implementations of software programs.
>>
>>Configured to switch automatically over to a redundant or standby IT resource instance whenever the currently active IT resource becomes unavailable.
>>
>>Commonly used for mission-critical programs or for reusable services that can introduce a single point of failure for multiple applications.
>>
>>Can span more than one geographical region so that each location hosts one or more redundant implementations of the same IT resource.
>>
>>Relies on the resource replication mechanism to supply the redundant IT resource instances, that are actively monitored to detect errors and unavailability conditions.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are the two basic configurations for Failover Systems? *ASK*
?
>>[!answer]
>>1. Active-Active: Redundant implementations actively serves the workload synchronously. (SWAP-N-STAY)
>>2. Active-Passive: Standby or inactive implementation is activated to take over the processing when they become unavailable. (SWAP-N-BACK)
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Resource Cluster?
?
>>[!answer]
>>A logically combined group of geographically diverse IT resources.
>>
>>A cluster mechanism is used to group multiple IT resource instances so that they can be operated as a single IT resource.
>>
>>Increases combined computing capacity, load balancing, and availability of the clustered IT resources.
>>
>>![[Pasted image 20241126172137.png]]
>>
>>Rely on high-speed dedicated network connections between IT resource instances (nodes) to communicate for workload distribution, task scheduling, data sharing, and system synchronization.
<!--SR:!2024-11-29,1,210-->

>[!question]
>What is a Cluster Management Platform?
?
>>[!answer]
>>Runs as distributed middleware in all of the cluster nodes and is usually responsible for Resource Clustering activities.
>>
>>Implements a coordination function that allows distributed IT resources to appear as one IT resource, and also executes IT resources inside the cluster.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are 3 common resource cluster types?
?
>>[!answer]
>>- Server Cluster
>>- Database Cluster
>>- Large Dataset Cluster
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Server Cluster?
?
>>[!answer]
>>Physical and Virtual servers alike are clustered to increase the performance and availability (within IaaS environments).
>>
>>Hypervisors running at different physical servers can be configured to share the virtual server execution state in order to establish clustered virtual servers.
>>
>>In virtual cluster environments, virtual servers are able to live-migrate from one physical server to another.
>>
>>The virtualization platform suspends the execution of a given virtual server at one physical server and resumes it on another.
<!--SR:!2024-11-30,2,230-->
 
>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126173001.png]]
?
>>[!answer]
>>A loosely coupled server cluster that incorporates a load balancer. There is no shared storage. Resource Replication is used to replicate cloud storage devices through the network by the cluster software.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Database Cluster?
?
>>[!answer]
>>High-availability cluster with a synchronization feature that maintains the consistency of data being stored at different storage devices used in the cluster.
>>
>>The redundant capacity is usually based on an active-active or active-passive failover system committed to maintaining the synchronization conditions.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What is a Large Dataset Cluster?
?
>>[!answer]
>>Data partitioning and distribution is implemented so that the target dataset can be efficiently partitioned without compromising data integrity or computing accuracy.
>>
>>Each cluster node processes workloads without communicating with other nodes as much as in other cluster types.
<!--SR:!2024-12-01,4,270-->

>[!question]
> What is a Multi-Device Broker?
?
>>[!answer]
>>Facilitates runtime data transformation so as to make a cloud service accessible by a wider range of cloud service consumer programs and devices.
>>
>>An individual cloud service may need to be accessed by different types of cloud service consumers, some of which may be incompatible with the cloud service's published service contract.
>>
>>Mapping logic needs to be created to transform (convert) information that is exchanged at runtime.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126174007.png]]
?
>>[!answer]
>>A multi-device broker contains the mapping logic necessary to transform data exchanges between a cloud service and different types of cloud service consumer devices. This scenario depicts the multi-device broker as a cloud service with its own API. This mechanism can also be implemented as a service agent that intercepts messages at runtime to perform necessary transformations.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What are 3 common gateway components?
?
>>[!answer]
>>- XML: transmits and validates XML data.
>>- Cloud Storage: transforms cloud storage protocols and encodes storage devices to facilitate data transfer and storage.
>>- Mobile Device: transforms the communication protocols used by mobile devices.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are the 4 levels at which transformation logic can be created?
?
>>[!answer]
>>- Transport Protocols
>>- Messaging Protocols
>>- Storage Device Protocols
>>- Data Schemas/Data Models
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a State Management Database?
?
>>[!answer]
>>A storage device used to temporarily persist state data for software programs.
>>
>>Alternative to caching state data in memory.
>>
>>Software programs can off-load state data to the database in order to reduce the amount of runtime memory they consume.
>>
>>Increases scalability.
>>
>>Commonly used by cloud services, especially those involved in long-running runtime activities.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What do the following diagrams describe?
>![[Pasted image 20241126212229.png|500]]
>![[Pasted image 20241126212240.png|500]]
?
>>[!answer]
>>The first diagram shows: During the lifespan of a cloud service instance it may be required to remain stateful and keep state data cached in memory, even when idle.
>>
>>The second diagram shows: By deferring state data to a state repository, the cloud service is able to transition to a stateless condition (or a partially stateless condition), thereby temporarily freeing system resources.
<!--SR:!2024-11-29,1,215-->

## Lecture 12

>[!question]
>What is a Remote Administration System?
?
>>[!answer]
>>Provides tools and UIs for external cloud resource administrators to configure and administer cloud-based IT resources.
>>
>>Acts as a portal for access to administration and management features of various underlying systems, including:
>>- Resource management
>>- SLA management
>>- Billing management
>>
>>Tools and APIs provided are generally used by the cloud provider to develop and customize online portals that provide cloud consumers with a variety of administrative controls.
>>
>>Attractive options for those who would like to centrally administer on-premise and cloud-based IT resources from a single console.
<!--SR:!2024-11-29,1,210-->

>[!question]
>What are 2 Remote Administration Portals?
?
>>[!answer]
>>- Usage and Administration Portal: General purpose portal that centralizes management controls to different cloud-based IT resources and can further provide IT resource usage reports.
>>	- Part of numerous cloud technology architectures.
>>- Self-Service Portal: Shopping portal that allows the cloud consumer to search an up-to-date list of cloud services and IT resources that are available from a cloud provider.
>>	- Primarily associated with the rapid provisioning architecture.
>>	- Consumer submits its chosen items to the cloud provider for provisioning.
<!--SR:!2024-11-30,2,230-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126213200.png]]
?
>>[!answer]
>>1. A cloud resource administrator uses the usage and administration portal to configure an already leased virtual server (not shown) to prepare it for hosting.
>>2. The cloud resource administrator then uses the self-service portal to select and request the provisioning of a new cloud service.
>>3. The cloud resource administrator then accesses the usage and administration portal again to configure the newly provisioned cloud service that is hosted on the virtual server.
>>4. Throughout these steps, the remote administration system interacts with the necessary management systems to perform the requested actions.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What are some common tasks performed via a Remote Administration Console?
?
>>[!answer]
>>- Configuring and setting up cloud services
>>- Provisioning and releasing IT resources for on-demand cloud services
>>- Monitoring cloud service status, usage, performance, QoS, SLA fulfillment
>>- Managing leasing costs, usage fees, user accounts, security credentials, authorization, and access control
>>- tracking internal and external access to leased services
>>- planning and assessing IT resource provisioning
>>- capacity planning
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241126213606.png]]
?
>>[!answer]
>>Standardized APIs published by remote administration systems from different clouds enable a cloud consumer to develop a custom portal that centralizes a single IT resource management portal for both cloud-based and on-premise IT resources.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Resource Management System?
?
>>[!answer]
>>Helps coordinate IT resources in response to management actions performed by both cloud consumers and cloud providers.
>>
>>Virtual Infrastructure manager (VIM) is the Core.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are some tasks that are typically automated and implemented in a Resource Management System?
?
>>[!answer]
>>- Managing virtual IT resource templates that are used to create pre-built instances, such as virtual server images.
>>- Allocating and releasing virtual IT resources into the available physical infrastructure in response to the starting, pausing, resuming, and termination of virtual IT resource instances.
>>- Coordinating IT resources in relation to the involvement of other mechanism, such as resource replication, load balancing, and failover systems
>>- Enforcing usage and security policies throughout the life-cycle of cloud service instances.
>>- Monitoring operational conditions of IT resources
<!--SR:!2024-11-29,1,210-->

>[!question]
>How are Resource Management Systems accessed by cloud resource administrators?
?
>>[!answer]
>>They can be accessed by cloud resource administrators employed by the cloud provider or cloud consumer.
>>
>>Direct access can be granted through the resource management system's native console.
>>
>>Expose APIs that allow cloud providers to build remote administration system portals.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127113615.png]]
?
>>[!answer]
>>1. The cloud consumer's cloud resource administrator accesses a usage and administration portal externally to administer a leased IT resource.
>>2. The cloud provider's cloud resource administrator uses the native UI provided by the VIM to perform internal resource management tasks.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is an SLA Management System?
?
>>[!answer]
>>Represents a range of commercially available cloud management products that provide features pertaining to the administration, collection, storage, reporting, and runtime notification of SLA data.
>>
>>Generally includes a repository used to store and retrieve collected SLA data based on pre-defined metrics and reporting parameters.
>>
>>Relies on one or more SLA monitor mechanisms to collect the SLA data.
>>
>>The metrics monitored are aligned with the SLA guarantees in corresponding cloud provisioning contracts.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127114137.png]]
?
>>[!answer]
>>- 1: A cloud service consumer interacts with a cloud service.
>>- 2a: An SLA monitor intercepts the exchanged messages, evaluates the interaction, and collects relevant runtime data in relation to QoS guarantees defined in the cloud service's SLA.
>>- 2b: The data collected is stored in a repository.
>>- 3: that is part of the SLA management system.
>>- 4: Queries can be issued and reports can be generated for an external cloud resource administrator via a usage and administration portal
>>- or for an internal cloud resource administrator via the SLA management system's native UI.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Billing Management System?
?
>>[!answer]
>>Dedicated to the collection and processing of usage data as it pertains to cloud provider accounting and cloud consumer billing.
>>
>>Relies on pay-per-use monitors to gather runtime usage data that is stored in a repository that the system components then draw from for billing, reporting, and invoicing purposes.
>>
>>Allows for the definition of different pricing policies, as well as custom pricing models on a per cloud consumer and/or per IT resource basis.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are some pricing models for Billing Management Systems?
?
>>[!answer]
>>- Traditional Pay-Per-Use
>>- Flat-Rate
>>- Pay-Per-Allocation
>>- Combos
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are two billing arrangements for Billing Management Systems?
?
>>[!answer]
>>- Pre-usage
>>- Post-usage
>>
>>Pre-defined limits can be put on post-usage, or it can be unlimited which are usually in the form of usage quotas (which will block the consumer).
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127115115.png]]
?
>>[!answer]
>>- 1: A clodu service consumer exchanges messages with a cloud service.
>>- 2a: A pay-per-use monitor keeps track of the usage and collects data relevant to billing
>>- 2b: which is forwarded to a repository that is part of the billing management system.
>>- 3: The system periodically calculates the consolidated cloud service usage fees and generates an invoice for the cloud consumer.
>>- 4: the invoice may be provided to the cloud consumer through the usage and administration portal.
<!--SR:!2024-11-29,1,215-->

## Lecture 13

>[!question]
>What is Encryption?
?
>>[!answer]
>>A digital coding system dedicated to preserving the confidentiality and integrity of data.
>>
>>Encodes plaintext data into a protected and unreadable format, which is paired with a string of characters called an encryption key.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is a Cipher?
?
>>[!answer]
>>A standardized algorithm that transforms plaintext data into encrypted data, which is then referred to as ciphertext.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does encryption help counter?
?
>>[!answer]
>>- Traffic Eavesdropping
>>- Malicious Intermediary
>>- Insufficient Authorization
>>- Overlapping Trust Boundary Security Threats
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127120520.png]]
?
>>[!answer]
>>A malicious service agent is unable to retrieve data from an encrypted message. The retrieval attempt may furthermore be revealed to the cloud service consumer.
>>
>>Note: Lock symbol indicates the message has been encrypted.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What are two types of Encryption?
?
>>[!answer]
>>- Symmetric
>>- Asymmetric
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Symmetric Encryption?
?
>>[!answer]
>>Uses the same key for both encryption and decryption.
>>
>>AKA: Secret Key Cryptography.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Asymmetric Encryption?
?
>>[!answer]
>>Relies on the use of two different keys, namely a private key and a public key.
>>
>>A document that was encrypted with a private key can only be decrypted with the corresponding public key (and vice-versa).
>>
>>AKA: Public Key Cryptography.
>>
>>Almost always slower than Symmetric Encryption.
<!--SR:!2024-12-01,4,270-->

case study

>[!question]
>What is Hashing?
?
>>[!answer]
>>A one-way, non-reversible form of data protection.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127121247.png]]
?
>>[!answer]
>>A hashing function is applied to protect the integrity of a message that is intercepted and altered by a malicious service agent, before it is forwarded. The firewall can be configured to determine that the message has been altered thereby enabling it to reject the message before it can proceed to the cloud service.
<!--SR:!2024-11-29,1,215-->

case study

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127121553.png]]
?
>>[!answer]
>>1. A hashing procedure is invoked when the PaaS environment is accessed.
>>2. The applications that were ported to this environment are checked,
>>3. and their message digests are calculated.
>>4. The message digests are stored in a secure on-premise database, and a notification is issued if any of their values are not identical to the ones in storage.
<!--SR:!2024-11-29,1,215-->

>[!question]
>What is a Digital Signature?
?
>>[!answer]
>>A means of providing data authenticity and integrity through authentication and non-repudiation.
>>
>>A message is assigned a digital signature prior to transmission, which is then rendered invalid if the message experiences any subsequent, unauthorized modifications.
>>
>>Evidence that the message received is the same as the one created by its rightful sender.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What Security Mechanisms are involved in the creation of a digital signature?
?
>>[!answer]
>>- Hashing
>>- Asymmetrical Encryption
>>
>>A message digest that was encrypted by a private key and appended to the original message.
>>
>>The recipient decrypts the digital signature, which produces the message digest.
>>
>>The hashing mechanism is applied to the original message to produce the digest.
>>
>>If both procedures have an identical result, the message has maintained its integrity.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127122951.png]]
?
>>[!answer]
>>Cloud service consumer B sends a message that was digitally signed but was altered by trusted attacker cloud service consumer A. Virtual server B is configured to verify digital signatures before processing incoming messages even if they are within its trust boundary. The message is revealed as illegitimate due to its invalid digital signature, and is therefore rejected by virtual server B.
<!--SR:!2024-11-29,1,215-->

case study + dia

>[!question]
>What is Public Key Infrastructure (PKI)?
?
>>[!answer]
>>A common approach for managing the issuance of asymmetric keys.
>>
>>A system of protocols, data formats, rules, and practices that enable large-scale systems to securely use public key cryptography.
>>
>>Associates public keys with their corresponding key owners (public key identification).
>>
>>Rely on digital certificates: digitally signed data structures that bind public keys to certificate owner identities, as well as other info (like validity periods).
>>
>>Usually digitally signed by a third-party certificate authority (CA).
<!--SR:!2024-11-30,2,230-->

case study + dia

>[!question]
>What is Identity and Access Management?
?
>>[!answer]
>>Encompasses the components and policies necessary to control and track user identities and access privileges for IT resources, environments, and systems.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What are the 4 main components of Identity and Access Management?
?
>>[!answer]
>>1. Authentication
>>2. Authorization
>>3. User Management
>>4. Credential Management
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Authentication (IAM)?
?
>>[!answer]
>>A combination of Username and Password are the most common forms of user autherntication.
>>
>>Also supports:
>>- Digital Signatures
>>- Digital Certificates
>>- Biometric Hardware (Fingerprint Reader)
>>- Specialized Software (Voice Recog.)
>>- Locking to registered IP/MAC addresses
<!--SR:!2024-11-30,3,250-->

>[!question]
>What is Authorization (IAM)?
?
>>[!answer]
>>The correct granularity for access controls and oversees the relationship between identities, access control rights, and IT resource availability.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is User Management (IAM)?
?
>>[!answer]
>>Responsible for:
>>- Creating new user identities
>>- Access Groups
>>- Resetting Passwords
>>- Defining Password Policies
>>- Managing Privileges
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Credential Management (IAM)?
?
>>[!answer]
>>Establishes identities and access control rules for defined user accounts, which mitigates the threat of insufficient authorization.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Single Sign On (SSO)?
?
>>[!answer]
>>Enables one cloud service consumer to be authenticated by a security broker, which establishes a security context that is persisted while the cloud consumer accesses other cloud services or cloud-based IT resources.
>>
>>That way you don't need to re-authenticate itself with every subsequent request.
<!--SR:!2024-12-01,4,270-->

>[!question]
>How does SSO work?
?
>>[!answer]
>>The credentials initially provided by the cloud service consumer remain valid for the duration of the session, while its security context information is shared.
>>
>>The security broker manages the mechanism and is especially useful when a cloud service consumer needs to access cloud services residing on different clouds.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127141012.png]]
?
>>[!answer]
>>1. A cloud service consumer provides the security broker with login credentials.
>>2. The Security broker responds with an authentication token (message with small lock symbol) upon successful authentication, which contains cloud service consumer identity information.
>>3. That is used to automatically authenticate the cloud service consumer across cloud services A, B, and C.
<!--SR:!2024-11-29,1,215-->

case study + dia

>[!question]
>What are Cloud Based Security Groups?
?
>>[!answer]
>>Barriers between IT resources that increase data protection.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What is Cloud Resource Segmentation?
?
>>[!answer]
>>A process by which separate physical and virtual IT environments are created for different users and groups.
>>
>>Determined through security policies.
>>
>>Used to enable virtualization by allocating a variety of physical IT resources to virtual machines.
>>
>>Needs to be optimized for public cloud environments, since organizational trust boundaries from different cloud consumers overlap when sharing the same underlying physical IT resources.
<!--SR:!2024-11-30,3,250-->

>[!question]
>How are Networks segmented?
?
>>[!answer]
>>Into logical cloud-based security groups that form logical network perimeters.
>>
>>Each resource is assigned to at least one logical cloud-based security group.
>>
>>Each logical cloud-based security group is assigned specific rules that govern the communication between the security groups.
<!--SR:!2024-11-30,3,250-->

>[!question]
>How are Virtual Servers segmented?
?
>>[!answer]
>>Multiple virtual servers running on the same physical server can become members of different logical cloud-based security groups.
>>
>>Virtual servers can be further separated into public-private groups, development-production groups, or any other designation configured by the cloud resource administrator.
<!--SR:!2024-12-01,4,270-->

dia - case - dia

>[!question]
>What is an example of Cloud Resource Segmentation?
?
>>[!answer]
>>An organization's WAN can be partitioned according to individual network security requirements. One network can be established with a resilient firewall for external Internet access, while a second is deployed without a firewall because its users are internal and unable to access the Internet.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What are Hardened Virtual Server Images?
?
>>[!answer]
>>Hardening is the process of stripping unnecessary software from a system to limit potential vulnerabilities that can be exploited by attackers.
>>
>>A template for virtual service instance creation that has been subjected to a hardening process. This generally results in a virtual server template that is significantly more secure than the original standard image.
<!--SR:!2024-11-30,3,250-->

>[!question]
>What is an example of the Hardening process?
?
>>[!answer]
>>Removing redundant programs, closing unnecessary server ports, and disabling unused services, internal root accounts, and guest access.
<!--SR:!2024-12-01,4,270-->

>[!question]
>What does the following diagram describe?
>![[Pasted image 20241127141857.png]]
?
>>[!answer]
>>A cloud provider applies its security policies to harden its standard virtual server images. The hardened image template is saved in the VM images repository as part of a resource management system.
<!--SR:!2024-11-29,1,215-->

dia + case

