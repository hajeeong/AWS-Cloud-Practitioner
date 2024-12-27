# What is cloud computing?

### Personal opinion
Cloud computing enables convenient, remote, on-demand access, to a shared pool of computing resources and services.

### AWS definition
Cloud computing is the on-demand delivery of IT resources over the internet with pay-as-you-go pricing

### NIST (National Institute of Standards and Technology) definition
Cloud computing is a model for enabling ubiquitous, convenient, on-demand network accecss to a shared pool of configurable computing resources that can be
rapidly provisioned and released with minimal management effort or service provider interaction. This cloud model is composed of five essential characteristics, three service models, and four deployment models.

# The 5 Essential Characteristics of Cloud

## On-demand self-service
The ability to create IT resources, such as compute, storage, and databases yourself, without the need to interact with other humans to do the work.

## Braod network access
The cloud resources are available to us over a network and are accessible through standard protocols like HTTP, HTTPS from a variety of client platforms.

## Resource Pooling
The cloud resources are all poolled together and they can provide these resources to serve multiple customers all at the same time

## Rapid Elasticity
The ability to quickly scale your cloud resources based on changing demands.

## Measured Service
The cloud provider has automated systems to provide transparent billing details about the cloud resources you are consuming. Allowing you, as the customer, to have monitoring and reporting capabilities of these cloud resources.

# Cloud Deployment Models

## Private Cloud
The cloud infrastructure is provisioned for exclusive use by a single organization comprising multiple consumers. It may be owned, managed, and operated by the organization, a third party, or some combination of them, and it may exist on or off premises.

## Community Cloud
The cloud infrastructure is provisioned for exclusive use by a specific community of consumers from organizations that have shared concerns. It may be owned, managed, and operated by the organization, a third party, or some combination of them, and it may exist on or off premises.

## Public Cloud
The cloud infrastructure is provisioned for open use by the general public. it may be owend, managed, and operated by a business, academic, or government organization, or some combination of them. It exists on the premises of the cloud provider.

## Hybrid Cloud
The cloud infrastructure is a composition of two or more distinct cloud infrastructures, (private, community, or public) that remain unique entities, but are bound together by standardized or proprietary technology that enables data and application portability. (Ex. Load balancing between clouds)

## Multi-Cloud

# Cloud Service Models

## IaaS (Infrastructure-as-a-Service)
### NIST definition
The capability provided to the consumer is to provision processing, storage, networks, and other fundamental computing resources where the consumer is able to deploy and run arbitrary software, which can include operating systems and applications.

### AWS definition
IaaS contains the basic building blocks for cloud IT. It typically provides access to networking features, computers (virtual or on dedicated hardware), and data storage space. 

IaaS gives you the highest level of flexibility and management control over your IT resources.

It is most similar to the existing IT resources with which many IT departments and developers are familiar.

## PaaS (Platform-as-a-Service)
### NIST definition
The capability provided to the consumer is to deploy onto the cloud infrastructure consumer‐created or acquired applications created using programming languages, libraries, services, and tools supported by the provider.

The consumer does not manage or control the underlying cloud infrastructure including network, servers, operating systems, or storage, but has control over the deployed applications and possibly configuration settings for the application‐hosting environment.

### AWS definition
PaaS removes the need for you to manage underlying infrastructure (usually hardware and operating systems), and allows you to focus on the deployment and management of your applications. This helps you be more efficient as you don’t need to worry about resource procurement, capacity planning, software maintenance, patching, or any of the other undifferentiated heavy lifting involved in running your application.

## SaaS (Software-as-a-Service)

### NIST definition
The capability provided to the consumer is to use the provider’s applications running on a cloud infrastructure. The applications are accessible from various client devices through either a thin client interface, such as a web browser, or a program interface.

The consumer does not manage or control the underlying cloud infrastructure including network, servers, operating systems, storage, or even individual application capabilities, with the possible exception of limited user-specific application configuration settings.

### AWS definition
SaaS provides you with a complete product that is run and managed by the service provider. In most cases, people referring to SaaS are referring to end-user applications (such as web-based email). With a SaaS offering, you don’t have to think about how the service is maintained or how the underlying infrastructure is managed.

You only need to think about how you will use that particular software.

<p style="color: white; background-color: blue;">Your Responsibility</p>
<p style="color: white; background-color: Red;">Provider Responsibility</p>
<table>
  <thead>
    <tr>
      <th style="color: purple; background-color: black;">On-Premesis</th>
      <th style="color: purple; background-color: black;">IaaS</th>
      <th style="color: purple; background-color: black;">PaaS</th>
      <th style="color: purple; background-color: black;">SaaS</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="color: white; background-color: blue;">APPLICATION</td>
      <td style="color: white; background-color: blue;">APPLICATION</td>
      <td style="color: white; background-color: blue;">APPLICATION</td>
      <td style="color: white; background-color: Red;">APPLICATION</td>
    </tr>
    <tr>
      <td style="color: white; background-color: blue;">DATA</td>
      <td style="color: white; background-color: blue;">DATA</td>
      <td style="color: white; background-color: blue;">DATA</td>
      <td style="color: white; background-color: Red;">DATA</td>
    </tr>
    <tr>
      <td style="color: white; background-color: blue;">RUNTIME</td>
      <td style="color: white; background-color: blue;">RUNTIME</td>
      <td style="color: white; background-color: Red;">RUNTIME</td>
      <td style="color: white; background-color: Red;">RUNTIME</td>
    </tr>
    <tr>
      <td style="color: white; background-color: blue;">GUEST OS</td>
      <td style="color: white; background-color: blue;">GUEST OS</td>
      <td style="color: white; background-color: Red;">GUEST OS</td>
      <td style="color: white; background-color: Red;">GUEST OS</td>
    </tr>
    <tr>
      <td style="color: white; background-color: blue;">VIRTUALIZATION</td>
      <td style="color: white; background-color: Red;">VIRTUALIZATION</td>
      <td style="color: white; background-color: Red;">VIRTUALIZATION</td>
      <td style="color: white; background-color: Red;">VIRTUALIZATION</td>
    </tr>
    <tr>
      <td style="color: white; background-color: blue;">PHYSICAL</td>
      <td style="color: white; background-color: Red;">PHYSICAL</td>
      <td style="color: white; background-color: Red;">PHYSICAL</td>
      <td style="color: white; background-color: Red;">PHYSICAL</td>
    </tr>
  </tbody>
</table>


# The Benefits of Cloud

## Private Cloud
- Control
- Cost
- Hardware Choice
- Software License
  - Hardware Based
  - Hardware Locked
- Security

## Public Cloud
- Scalability
- Cost Savings
- Speed
- Global Capability

## Hybrid Cloud
- Use Existing Infrastructure
- Cost Savings
- Security Requirements

## Benefits of CLoud
- Capital Expenses - CapEX
- Operational Expenses - OpEx
- Shift CapEx to OpEx
- Global Capabilities 
- Pay-as-you-Go
- Agility
- On-Demand
- Infinite Scale
- Experimentation
- Low-cost Experiments
- Security

