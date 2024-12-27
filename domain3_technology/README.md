# Domain 3: Cloud Technology and Services

## Organizations and Accounts

- Organizations allow you to centrally manage billing, control access, compliance, security, and share resources across your AWS accounts.

- Root Account User is a single sing-in identity that has complete access to all AWS services and resources in an account. Each Account has a Root Account User
- Organization Units are a group of AWS accounts within an organization which can also contain other organizational units - creating a hierarchy
- Service Control Policies give central control over the allowed permissions for all accounts in your organization, helping to ensure your accounts stay within your organization's guidelines.

## AWS Networking

- Region: the geographical location of your network
- AZ: the data center of your AWS resources
- VPC: a logically isolated section of the AWS Cloud where you can launch AWS resources
- Internet Gateway: enables access to the Internet
- Route Tables: determine where network traffic from your subnets are directed
- NACLs: acts as a firewall at the subnet level
- Security Groups: acts as firewall at the instance level
- Subnets: a logical partition of an IP network into multiple, smaller network segments

![Description of Image](/Users/hajeong/Desktop/Coding/AWS_cloud_practitioner/Screenshot 2024-12-27 at 1.56.44 AM.png)

## Database Services
- DynamoDB: NoSQL key/value database
- DocumentDB: NoSQL Document database that is MongoDB compatible
- RDS: Relational Database Service that supports multiple engines
  - Engines: MySQL, PostgreSQL, Maria DB, Oracle, Microsoft SQL Server, Aurora
- Aurora: MySQL(5x faster) and PSQL(3x faster) database fully managed
- Aurora Serverless: only runs when you need it, like AWS Lambda
- Neptune: managed Graph Database
- Redshift: Columnar database, petabyte warehouse (1000TB = 1PB) 
- ElastiCache: Redis or Memcached database

## Provisioning
What is provisioning?
The allocation or creation of resources and services to a customer

- Elastic Beanstalk: service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker
- OpsWorks: configuration management service that provides managed instances of Chef and Puppet
- CloudFormation: infrastructure as code, JSON or YAML
- AWS QuickStart: pre-made packages that can launce and configure your AWS compute, network, storage, and other services required to deploy a workload on AWS
- AWS Marketplace: a digital catalogue of thousands of software listings from independent software vendors you can use to find, buy, test, and deploy software.

## Computing
- EC2: Elastic Compute Cloud, highly configurable server eg. CPU, Memory, Network, OS
- ECS: Elastic Container Service, Docker as a Service highly scalable, high-performance container orchestration service that supports Docker containers, pay for EC2 instances
- Fargate: Microservices where you don't think about the infrastructure. Play per task
- EKS: Kubernetes as a Service, easy to deploy, manage, and scale containerized applications using Kubernetes
- Lambda: serverless functions run code without provisioning or managing servers. You pay only for the compute time you consume
- Elastic Beanstalk: orchestrates various AWS services, including EC2, S3, Simple Notification Service(SNS), CloudWatch, autoscaling, and Elastic Load Balancers
- AWS Batch: plans, schedules, and executes your batch computing workloads across the full range of AWS compute service and features, such as Amazon EC2 and Spot Instances

## Storage
- S3: Simple Storage Service (object storage)
- S3 Glacier: low cost storage for archiving and long-term backup
- Storage Gateway: hybrid cloud storage with local caching
  - File Gateway
  - Volume Gateway
  - Tape Gateway
- EBS(Elastic Block Storage): hard drive in the cloud you attach to EC2 instances (SSD, IOPS SSD, Throughput HHD, Cold HHD)
- EFS(Elastic File Storage): file storage mountable to multiple EC2 instances at the same time
- Snowball: Physically migrate lots of data via a computer suitcase 50-80 TB
  - Snowball Edge: A better version of Snowball - 100TB
  - Snowmobile: Shipping container, pulled by a semi-trailer truck - 100PB

  ## Business Centric Services
  - Amazon Connect(Call Center): Cloud-based call center service you can setup in just a few clicks, based on the same proven system used by the Amazon customer service teams.
  - WorkSpaces(Virtual Remote Destop): Secure managed service for provisioning either Windows or Linux desktops in just a few minutes which quickly scales up to thousands of desktops
  - WorkDocs: A content creation and collaboration service, easily create, edit, and share content saved centrally in AWS (AWS version of Sharepoint)
  - WorkMail: managed business email, contacts, and calendar service with support for existing desktop and mobile email client applications (IMAP)
  - Pinpoint: Marketing campaign management system you can use for sending targeted email, SMS, push notifications, and voice messages
  - SES(Simple Email Service): A cloud-based email sending service designed for marketers and application developers to send marketing, notification, and emails
  - QuickSight: A Business Intelligence(BI) service. Connect multiple datasource and quickly visualize data in the form of graphs with little to no programming knowledge.

## Enterprise Intergration
- **Direct Connect**
A dedicated Gigabit network connection from your premises to AWS. Imagine having a direct fibre optic cable running straight to AWS.

---

- **VPN**
Establish a **secure** connection to your AWS network:

- **Site-to-Site VPN**: Connecting your on-premise to your AWS network.
- **Client VPN**: Connecting a Client (a laptop) to your AWS network.

---

- **Storage Gateway**
A hybrid storage service that enables your on-premises applications to use AWS cloud storage. You can use this for:

- Backup and archiving
- Disaster recovery
- Cloud data processing
- Storage tiering
- Migration

---

- **Active Directory**
The AWS Directory Service for Microsoft Active Directory, also known as **AWS Managed Microsoft AD**, enables your directory-aware workloads and AWS resources to use managed Active Directory in the AWS Cloud.

## Logging Services
- **CloudTrail**
Logs all **API calls** (SDK, CLI) between AWS services (who can we blame):

- **Who created this bucket?** - Detect developer misconfiguration
- **Who spun up that expensive EC2 instance?**- Detect malicious actors
- **Who launched this SageMaker Notebook?**- Automate responses

---

- **CloudWatch**
A collection of multiple services:

- **CloudWatch Logs**: Performance data about AWS Services (e.g., CPU Utilization, Memory, Network In), Application Logs (e.g., Rails, Nginx), Lambda logs.
- **CloudWatch Metrics**: Represents a time-ordered set of data points. A variable to monitor.
- **CloudWatch Events**: Triggers an event based on a condition (e.g., every hour take a snapshot of the server).
- **CloudWatch Alarms**: Triggers notifications based on metrics.
- **CloudWatch Dashboard**: Creates visualizations based on metrics.

