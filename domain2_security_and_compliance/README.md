# Domain 2 - Security and Compliance

## Shared Responsibility Model

### Customer Responsibilities: Security **in** the Cloud
Customers are responsible for:

- **Data**
- **Configuration**

---

### AWS Responsibilities: Security **of** the Cloud
AWS is responsible for:

- **Hardware**
- **Operation of Managed Services**
- **Global Infrastructure**

## AWS Compliance Programs
A set of internal policies and procedures of a company to comply with laws, rules, and regulations or to uphold business reputation.

---

### Health Insurance Portability and Accountability Act (HIPAA)
- United States legislation that provides data privacy and security provisions for safeguarding medical information.

### Payment Card Industry Data Security Standard (PCI DSS)
- Required when you want to sell things online and need to handle credit card information.

---

### Other Compliance Programs:
- **CJIS**: Criminal Justice Information Services
- **Department of Defense**: Defense compliance
- **FedRAMP**: Federal Risk and Authorization Management Program
- **FIPS**: Federal Information Processing Standards (Cryptography)
- **AICPA SOC**: Service Organization Controls (SOC)
- **TÜV Austria**: Security certifications
- **ITAR**: International Traffic in Arms Regulations
- **CSA**: Cloud Security Alliance
- **FDA**: Food and Drug Administration compliance
- **Gov.uk**: UK Government compliance
- **IRAP**: Information Security Registered Assessors Program
- **NIST**: National Institute of Standards and Technology

## AWS Artifact
### Key Features
- **No cost, self-service portal** for on-demand access to AWS’ compliance reports.
- On-demand **access to AWS’ security and compliance reports** and select online agreements.
- These checks are based on **global compliance frameworks**.

### Supported Frameworks
How do we prove AWS meets a compliance?
--
- No cost, self-service portal for on-demand access to AWS' compliance reports
- On-demand access to AWS' security and compliance reports** and select online agreements
- These checks are based on **global compliance frameworks**:
  - **AICPA SOC**
  - **ISO 27001**
  - **PCI DSS**
  - **C5**
  - **IRAP**
  - **FedRAMP**

### Example: Government of Canada (GC) Partner Package
- **Reporting Period**: Valid beginning 08/25/2017.
- The package includes:
  - Partner Package
  - Controls Implementation Summary (CIS)
  - Customer Responsibility Matrix (CRM)
  - PBMM Security Assessment
  - Letter of Attestation

### Process
1. Retrieve artifact via **self-service portal**.
2. Download as a **PDF**.
3. Export to **XLSX** for further use.

## Amazon Inspector
How do we prove an EC2 Instance is harden?
--
Hardening: The act of eliminating as many security risks as possible.
-- 
- AWS Inspector runs a security benchmark against specific EC2 instances.
- You can run a variety of security benchmarks
- Can perform both Network and Host assessment
  1. Install the AWS agent on your EC2 instances.
  2. Run as assessment for your assessment target.
  3. Review your findings and remediate security issues.
--
One very popular benchmark you can run is by CIS(Center for Internet Security) which has 699 checks

## AWS WAF
- AWS Web Application Firewall protect your web applications from common web exploits
- Write your own rules to ALLOW or DENY traffic based on the contents of an HTTP requests
- Use a ruleset from a trusted AWS Security Partner in the AWS WAF Rules Marketplace
- WAF can be attached to either CloudFront or an Application Load Balancer

--
Protect web applications from attacks covered in the OWASP Top 10 most dangerous attacks:
- Injectino
- Broken Authentication
- Sensitive data exposure
- XML External Entities (XXE)
- Broken Access control
- Security misconfigurations
- Cross Site Scripting (XSS)
- Insecure Deserialization
- Using Components with know vulnerabilities
- Insufficient logging and monitoring

## AWS Shield
AWS Shield is a managed DDoS(Distributed Denial of Service) protection service that safeguards applications running on AWS

-- 
What is a DDOS attack?
- A malicious attempt to disrupt normal traffic by flooding a website a large amount of fake traffic
-- 
All AWS customers benefit from the automatic protections of AWS Shield Standard, at no additional cost
--
When you route your traffic through Route53 or CloudFront you are using AWS Shield Standard
--
Protects you against Layer 3, 4 and 7 attacks 
- 7 Applications
- 4 Transport
- 3 Network

--
### Shield Standard (Free)
For protection against most common DDoS attacks, and access to tools and best practices to build a DDoS resilient architecture. Automatically available on all AWS services.

### Shield Advanced ($3000/year)
For additional protection against larger and more sophisticated attacks, visibility into attacks, and 24/7 access to DDoS experts for complex cases.
--
Available on:
- Amazon Route 53
- Amazon CloudFront
- Elastic Load Balancing
- AWS Global Accelerator
- Elastic IP (Amazon Elastic Compute Cloud and Network Load Balancer)

## Penetration Testing
What is PenTesting?:
An autorized simulated cyberattack on a computer system, performed to evaluate the security of the system.
--
Can you perform PenTesting on AWS? YES
--

- Permitted Services:
  - EC2 instances, NAT Gateways, ELB
  - RDS
  - CloudFront
  - Aurora
  - API Gateways
  - AWS Lambda and Lambda@Edge functions
  - Lightsail resources
  - Elastic Beanstalk environment
- Prohibited Activities:
  - DNS zone walking via Amazon Route 53 Hosted Zones
  - Denial of Service (DoS), Distributed Denial of Service (DDoS), Simulated DoS, Simulated DDoS
  - Port flooding
  - Protocol flooding
  - Request flooding(login request flooding, API request flooding)

--
For other simulated events you will need to submit a request to AWS. A reply could take up to 7 days.

## Amazon Guard Duty
What is IDS/IPS?
Intrusion Detection System and Intrusion Protection System.
--
A device or software application that monitors a network or systems for malicious activity or policy violations.
--
How do we detect if someone is attempting to gain access to our AWS account or resources?
--
Guard Duty is a threat detection service that continuously monitors for malicious, suspicious activity and unauthorized behavior. It uses Machine Learning to analyze the following AWS logs:
- CloudTrail Logs
- VPC Flow Logs
- DNS logs
--
It will alert you of Findings which you can automate a incident response via CloudWatch Events or with 3rd Party Services.

## Key Management Service (KMS)
A managed service that makes it easy for you to create and control the encryption keys used to encrypt your data.
- KMS is a multi-tenant HSM(Hardware Security Module)
- Many AWS services are integrated to use KMS to encrypt your data with a simple checkbox
- KMS uses Envelope Encryption
--
Envelope Encryption:
When you encrypt your data, your data is protected, but you have to protect your encryption key. When you encrypt your data key with a master key as an additional layer of security.

## Amazon Macie
Macie is a fully managed service that continuously monitors S3 data access activity for anomalies, and generates detailed alerts when it detects risk of unauthorized access or inadvertent data leask.

-- 
Macie works by uses Machine Learning to analyze your CloudTrail logs
-- 
Macie has a variety of alerts
- Anonymized Access
- Config Compliance
- Credential Loss
- Data Compliance
- File Hosting
- Identity Enumeration
- Information Loss
- Location Anomaly
- Open Permissions
- Privilege Escalation
- Ransomware
- Service Disruption
- Suspicious Access

--
Macies's will identify your most at-risk users which could lead to a compromise

## Security Groups vs NACLs

### Security Groups
- Acts as a firewall at the instance level
- Implicitly denies all traffic.
- You create Allow rules eg. Allow an EC2 instance access on port 22 for SSH

### NACLs (Network Access Control Lists)
- Acts as a firewall at the subnet level
- You create Allow and Deny rules eg. Block a specific IP address known for abuse

## Virtual Private Network (VPN)
- lets you establish a secure and private tunnel from your network or device to the AWS global network

### AWS Site-to-Site VPN
Securely connect on-premises network or branch office site to VPC

### AWS Client VPN
Securely connect users to AWS or on-premises networks

