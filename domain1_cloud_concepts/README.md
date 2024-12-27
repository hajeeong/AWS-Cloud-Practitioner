# Domain 1 - Cloud Concepts

## What is Cloud Computing?

### Definition
**cloud com·put·ing**

*Noun*

The practice of using a network of remote servers hosted on the Internet to store, manage, and process data, rather than a local server or a personal computer.

---

### On-Premise vs Cloud Providers

#### On-Premise
- You own the servers  
- You hire the IT people  
- You pay or rent the real estate  
- You take all the risk  

#### Cloud Providers
- Someone else owns the servers  
- Someone else hires the IT people  
- Someone else pays or rents the real estate  
- You are responsible for configuring cloud services and code, someone else takes care of the rest

## Evolution of Cloud Hosting

### Server Hosting Types

#### Dedicated Server
- **One physical machine** dedicated to **a single business**.  
- Runs a single web-app/site.  
- **Advantages:**  
  - Very Expensive, High Maintenance, *High Security*.  

---

#### Virtual Private Server (VPS)
- **One physical machine** dedicated to **a single business**.  
- The physical machine is virtualized **into sub-machines**.  
- Runs multiple web-apps/sites.  
- **Advantages:**  
  - Better Utilization and Isolation of Resources.  

---

#### Shared Hosting
- **One physical machine**, shared by **hundreds of businesses**.  
- Relies on most tenants under-utilizing their resources.  
- **Advantages:**  
  - Very Cheap, Limited Functionality, Poor Isolation.  

---

#### Cloud Hosting
- **Multiple physical machines** that act as one system.  
- The system is abstracted into multiple **cloud services**.  
- **Advantages:**  
  - Flexible, Scalable, Secure, Cost-Effective, High Configurability.


## What is AWS?
Amazon Web Services

AWS was launched in 2006 is the leading cloud service provider in the world.
Cloud Service Providers can be initialized as CSPs

- **Simple Queue Service (SQS)**  
  - The first AWS service launched for public use in 2004.  

- **Simple Storage Service (S3)**  
  - Launched in March of 2006.  

- **Elastic Compute Cloud (EC2)**  
  - Launched in August of 2006.  

---

In November 2010, it was reported that all of Amazon.com's retail sites had migrated to AWS.

---

To support industry-wide training and skills standardization, AWS began offering a certification program for computer engineers in April 2013.

A **Cloud Service Provider (CSP)** is a company which:

- Provides multiple Cloud Services, e.g., tens to hundreds of services.  
- These Cloud Services **can be chained together** to create cloud architectures.  
- These Cloud Services are accessible **via a Single Unified API**, e.g., AWS API.  
- These Cloud Services utilize **metered billing** based on usage, e.g., per second, per hour.  
- These Cloud Services have rich monitoring built-in, e.g., AWS CloudTrail.  
- These Cloud Services offer **Infrastructure as a Service (IaaS)**.  
- These Cloud Services offer **automation** via Infrastructure as Code (IaC).  

---

### Example Cloud Services Architecture

- **Route53**: Domain Name  
- **ELB**: Load Balancer  
- **EC2**: Web Server  
- **RDS**: Postgres Database  
- **SES**: Send Emails  
- **QuickSight**: Analytics  
- **S3**: Stores Images  

---

### Note:
If a company offers multiple cloud services under a single UI but does not meet most or all of these requirements, it would be referred to as a **Cloud Platform**, e.g., Twilio, HashiCorp, Databricks.

### Tier-1 (Top Tier)
- **Description:** Early to market, wide offering, strong synergies between services, well-recognized in the industry.  
- **Providers:**  
  - Amazon Web Services (AWS)  
  - Microsoft Azure  
  - Google Cloud Platform (GCP)  
  - Alibaba Cloud  

---

### Tier-2 (Mid Tier)
- **Description:** Backed by well-known tech companies, slow to innovate and turned to specialization.  
- **Providers:**  
  - IBM Cloud  
  - Oracle Cloud  
  - Huawei Cloud  
  - Tencent Cloud  

---

### Tier-3 (Light Tier)
- **Description:** Virtual Private Servers (VPS) turned to offer core IaaS offering. Simple, cost-effective.  
- **Providers:**  
  - Vultr  
  - Digital Ocean  
  - Akamai Connected Cloud (Linode)  

---

### Tier-4 (Private Tier)
- **Description:** Infrastructure as a Service software deployed to run in an organization's own private data center.  
- **Providers:**  
  - OpenStack (Rackspace)  
  - Apache CloudStack  
  - *VMware vSphere*

## Common Cloud Services
A cloud service provider **can have hundreds of cloud services** that are grouped into various types of services. The four most common types of cloud services (*the 4 core*) for Infrastructure as a Service (IaaS) would be:

### 1. Compute
- **Description:** Imagine having a virtual computer that can run applications, programs, and code.

### 2. Storage
- **Description:** Imagine having a virtual hard drive that can store files.

### 3. Networking
- **Description:** Imagine having virtual networks defining internet connections or network isolations between services or outbound to the internet.

### 4. Databases
- **Description:** Imagine a virtual database for storing reporting data or a database for general-purpose web applications.

---

**Note:** AWS has over **200+ cloud services**.

## Evolution of Computing
1. Dedicated
- A physical server **wholly utilized by a single customer**.
- You have to guess your capacity.
- You’ll overpay for an underutilized server.
- You can’t vertically scale; you need a manual migration.
- Replacing a server is very difficult.
- You are limited by your Host Operating System.
- Multiple apps can result in conflicts in resource sharing.
- You have a *guarantee of security, privacy, and full utility of underlying resources*.

2. VMs
- You can run **multiple Virtual Machines on one machine**.
- **Hypervisor** is the software layer that lets you run the VMs.
- A physical server shared by multiple customers.
- You are to pay for a fraction of the server.
- You’ll overpay for an underutilized Virtual Machine.
- You are limited by your Guest Operating System.
- Multiple apps on a single Virtual Machine can result in conflicts in resource sharing.
- Easy to export or import images for migration.
- Easy to **vertically** or **horizontally** scale.

3. Containers 
- **Virtual Machine running multiple containers**.
- **Docker Daemon** is the name of the software layer that lets you run multiple containers.
- You can maximize the utilization of the available capacity, which is more cost-effective.
- Your containers share the same underlying OS, so containers are more efficient than multiple VMs.
- Multiple apps can run side by side without being limited to the same OS requirements and will not cause conflicts during resource sharing.

4. Functions
- Are **managed VMs running managed containers**.
- Known as **Serverless Compute**.
- You upload a piece of code, choose the amount of memory and duration.
- Only responsible for code and data, nothing else.
- Very cost-effective; only pay for the time code is running. VMs only run when there is code to be executed.
- **Cold Starts** is a side-effect of this setup.

## Types of Cloud Computing
- SaaS (Software as a Service) for customers
- PaaS (Platform as a Service) for developers
- IaaS (Infrastructure as a Service) for Admins

## Cloud Computing Deployments Models
1. Public Cloud
- **Definition:** Everything (the workload or project) is built on the CSP.
- **Also Known As:** *Cloud-Native* or *Cloud First*.

---

2. Private Cloud
- **Definition:** Everything built on the company’s datacenters.
- **Also Known As:** On-Premise.
- **Example:** The cloud could be OpenStack.

---

3. Hybrid Cloud
- **Definition:** Using both On-Premise and a Cloud Service Provider.

4. Cross-Cloud
- **Definition:** Using Multiple Cloud Providers aka multi-cloud Amazon EKS <-> Azure Arc <-> GCP Kbernetes Engine

**Anthos** is GCP’s offering for a control plane for compute across multiple CSPs and On-Premise environments.

## Deployment Model Use Cases
# Cloud, Hybrid, and On-Premise Use Cases

## Cloud
- **Definition:** Fully utilizing cloud computing.
- **Examples:**  
  - Basecamp  
  - Dropbox  
  - Squarespace  
- **Use Cases:**  
  - Companies that are starting out today or are small enough to make the leap from a VPS to a CSP.  
  - **Types of Companies:**  
    - Startups  
    - SaaS offerings  
    - New projects and companies  

---

## Hybrid
- **Definition:** Using both Cloud and On-Premise.
- **Examples:**  
  - Deloitte  
  - CIBC  
  - CPP Investment Board  
- **Use Cases:**  
  - Organizations that started with their own datacenter but can’t fully move to the cloud due to migration effort or security compliance.  
  - **Types of Organizations:**  
    - Banks  
    - FinTech, Investment Management  
    - Large Professional Service Providers  
    - Legacy On-Premise Systems  

---

## On-Premise
- **Definition:** Deploying resources on-premises using virtualization and resource management tools, sometimes called "private cloud."
- **Examples:**  
  - AIG  
  - Government of Canada  
- **Use Cases:**  
  - Organizations that cannot run on the cloud due to strict regulatory compliance or the sheer size of their organization.  
  - **Types of Organizations:**  
    - Public Sector (e.g., Government)  
    - Super Sensitive Data (e.g., Hospitals)  
    - Large Enterprises with heavy regulations (e.g., Insurance Companies)

## Introduction and Map Overview

### Where does all this Cloud Computing Run?
69 Availability Zones within 22 Geographic Regions around the world Way More Edge Locations than AZs!

- AWS serves over **a million** active customers in **more than 190 countires**

- Streadily **expanding** global infrastructure to help customers achieve lower latency and higher throughput

- **Regions** physical location in the world with multiple Availability Zones

- **Availability Zones** one or more discrete data centers

- Edge Location datacenter owned by a trusted partner of AWS

## Regions

- A **geographically distinct** location which has multiple datacenters (AZs)

- Every region is **physically isolated** from and independent of every other region in terms of location, power, water supply

- Each region has at least two AZs

- AWS largest region is US-EAST

- Services almost always become available first in US-EAST

- Not all services are available in all regions

- US-EAST-1 is the region where you see all your billing information

## Availability Zones(AZs)

- An AZ is a datacenter owned and operated by AWS in which AWS services run
- Each region has at least two AZs
- AZs are represented by a Region Code, followed by a letter identifier eg. us-east-1a
- Multi-AZ distributing your instances across multiple AZs allows failover configuration for handling requests when one goes down
- < 10ms latency between AZs

## Edge Locations

An Edge location is a datacenter owned by a trusted partner of AWS which has direct coonnection to the AWS network.

- These locations serve requests for CloudFront and Route 53. Requests going to either of these serviecs will be routed to the nearest edge location automatically.

- S3 Transfer Acceleration traffic and API Gateway endpoint traffic also use the AWS Edge Network.

- This allows for low latency no matter where the end user is geographically located.

## GovCloud (US)

AWS GovCloud Regions allow customers to host sensitive controlled unclassified information and other types of regulated workloads.

- GovCloud Regions are only operated by employees who are US citizens on US soil.
- They are only accesible to US entities and root account holders who pass a screening process

- Customers can architect secure cloud solutions that comply with:
  - FedRAMP High baseline
  - DOJ's Criminal Justice Information Systems (CJIS) Security Policy
  - US International Traffic in Arms Regulations (ITAR)
  - Export Administration Regulations (EAR)
  - Department of Defense (DoD) Cloud Computing Security Requirements Guide

