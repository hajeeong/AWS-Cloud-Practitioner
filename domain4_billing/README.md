# Domain 4: Billing, Pricing, and Support

## EC2 - Pricing Model
EC2 has for 4 pricing models
- On-Demand (Least Commitment)
  - Low cost and flexible
  - only pay per hour
  - Use case: short-term, spiky, unpredictable workloads, first time apps
  - Ideal when your workloads cannot be interrupted

- Reserved Instances (RI) upto 75% off (Best long-term)
  - Use case: steady state or predictable usage
  - Can resell unused reserved instances (Reserved Instance Marketplace)
  - Reduced Pricing is based on Term x Class Offering x Payment Option
  - Payment terms: 1 year or 3 year
  - Payment options: All upfront, Partial upfront, and No upfront
  - Class Offerings:
    - Standard up to 75% reduced pricing compared to on-demand. Cannot charge RI Attributes.
    - Convertible up to  54% reduced pricing compared to on-demand. Allows you to change RI Attributed if greater or equal in value.
    - Scheduled you reserve instances for specific time periods eg. once a week  for a few hours . Savings vary

- Spot Instances upto 90% (Biggest savings)
  - Request spare computing capacity
  - Flexible start and end times
  - Use case: can handle interruptions (server randomly stopping and starting), for non-critical background jobs
  - Instances can be terminated by AWS at anytime
  - If your instance is terminated by AWS, you don't get charged for a partial hour of usage
  - If you terminate an instance you will still be charged for any hour that it ran.

- Dedicated Host Instances (most expensive)
  - Dedicated servers
  - Can be on-demand or reserved (upto 70% off)
  - Use case: When you need a guarantee of isolate hardware (enterprise requirements)

## Free Services

- IAM
- Amazon VPC
- Organizations & Consolidated Billing
- AWS Cost Explorer

The services are free, however, they can provision AWS services which cost money
- Auto Scaling
- CloudFormation
- Elastic Beanstalk
- Opsworks
- Amplify
- AppSync
- CodeStar

## AWS Support plans
- Basic 
  - Email support only for Billing and Account
  - 7 Trusted Advisor checks
  - $0/month
- Developer
  - Tech Support via Email ~ 24 hours until reply
  - No third party support
  - General Guidance < 24hrs
  - System Imparied < 12hrs
  - 7 Trusted Advisor checks
  - $20/month
- Business
  - Tech Support via Email ~ 24 hours until reply
  - Tech Support via Chat, Phone Anytime 24/7
  - General Guidance < 24hrs
  - System Imparied < 12hrs
  - Production System Imparied < 4hrs
  - Production System Down < 1hrs
  - All Trusted Advisor Checks
  - $100/month
- Enterprise
  - Tech Support via Email ~ 24 hours until reply
  - Tech Support via Chat, Phone Anytime 24/7
  - General Guidance < 24hrs
  - System Imparied < 12hrs
  - Production System Imparied < 4hrs
  - Production System Down < 1hrs
  - Business-Critical System Down < 15m
  - Personal Concierge
  - TAM
  - All Trusted Advisor Checks
  - $15,000/month

## AWS Marketplace

- AWS Marketplace is a curated digital catalogue with 1000 of software listings from independent software vendors.

- Easily find, buy, test, and deploy software that already runs on AWS

- The product can be free to use or can have an associated charge. The charge becomes part of your AWS bill, and once you pay, AWS Marketplace pays the provider.

- The sales channel for ISVs and Consulting Partners allows you to sell your solutions to other AWS customers.

- Products can be offered as
  - Amazon Machine Images (AMIs)
  - AWS CloudFormation templates
  - Software as a Service (SaaS) offerings
  - Web ACL
  - AWS WAF rules

## AWS Trusted Advisor
Advises you on security, saving money,performance, service limits and fault tolerance

- Cost Optimization
  - Idle Load Balancers
  - Unassociated Elastic IP Addresses
- Performance
  - High Utilization Amazon EC2 Instances
- Security
  - MFA on Root Account
  - IAM Access Key Rotation
- Fault Tolerance
  - Amazon RDS Backups
- Service Limits
  - VPC

## Consolidated Billing

One bill for all of your accounts

- Consolidate your billing and payment methods across multiple AWS accounts into one bill
- For billing AWS treats all the accounts in an organization as if they were one account.
- You can designate one master account that pays the charges of all the other member accounts.
- Consolidated billing is offered at no additional cost
- Use Cost Explorer to visualize usage for consolidated billing

### Volume Discounts 
AWS has Volume Discounts for many services. The more you use, the more you save.
Consolidated Billing lets you take advantage of Volume Discounts

Odo's usage = 4TB
Dax's usage = 8TB
Total usage = Tier1 + Tier2

First 10 TB = $0.17 per GB
Next 40 TB = $0.13 per GB
1 TB = 1024 GB

Odo : (4 * 1024) * 0.17 = $696.32
Dax : (8 * 1024) * 0.17 = $1392.64
Unconsolidated : 696.32 + 1392.64 = $2088.96
Consolidated : ((10 * 1024) * 0.17) + ((2 * 1024) * 0.13) = $2007.04

## AWS Cost Explorer
AWS Cost Explorer lets you visualize, understand, and manage your AWS costs and usage over time. If you are have multiple AWS accounts within an AWS Organization costs will be consolidated in the master account.

- Default reports help you gain insight into your cost drivers and usage trends.

- Use forecasting to get an idea of future costs

- Choose if you want to view your data at a monthly or daily level of granularity.

- Use filter and grouping functions to dig even deeper into your data

## AWS Budgets

AWS Budgets give you the ability to setup alerts if you exceed or are approaching your defined budget

- Create Cost, Usage or Reservation Budgets
- Can be tracked at the monthly, quarterly, or yearly levels, with customizable start and end dates 
- Alerts support EC2, RDS, Redshift, and ElastiCache reservations.
- Budget based on a fixed cost or plan your upfront based on your chosen level
- Can be easily manage from the AWS Budgets dashboard or via the Budgets API.
- Get notified by providing an email or Chatbot and threshold how close to the current or forecasted budget

## TCO Calculator
The Total Cost of Ownership allows you to estimate how much you would save when moving to AWS from on-premise

- Provides you a detailed set of reports that can be used in executive presentations.
- The tool is built on underlying calculation models that generate fair assessment of value that you can achieve given the data provided.
- This TCO helps by reducing the need to invest in large capital expenditures
- The tool is for approximation purposes only

## AWS Landing Zone
- Helps Enterprises quickly setup a secure, AWS multi-account
- Provides you with a baseline environment to get started with a multi-account architecture

### AWS Account Vending Machine (AVM)
- Automatically provisions and configure new accounts via Service Catalog Template
- Uses Single Sign-on (SSO) for managing and accessing accounts
- The environment is customizable to allow customers to implement their own account baselines through a Landing Zone configuration and update pipeline

## AWS Resource Groups and Tagging
- Tags are words or phrases that act as metadata for organizing your AWS resources
- Resource Groups are a collection of resources that share one or more tags
- Helps you organize and consolidate information based on your project and the resources that you use.
- Resource Groups can display details about a group of resource based on
  - Metrics 
  - Alarms
  - Configuration Settings
- At any time you can modify the settings of your resource groups to change what resources appear.

## AWS Quick Starts
- Prebuilt templates by AWS and AWS Partners to help you deploy popular stacks on AWS 
- Reduce hundreds of manual procedures into just a few steps

A Quick Start is composed of 3 parts:
- A reference architecture for the deployment
- AWS CloudFormation templates that automate and configure the deployment
- A deployment guide explaining the architecture and implementation in detail

Most Quick Start reference deployments enable you to spin up a fully functional architecture in less than an hour

## AWS Cost and Usage Report
Generate a detailed spreadsheet, enabling you to better analyze and understand your AWS costs

- Places the reports into S3
- Use Athena to turn the report into a queryable database
- Use QuickSight to visualize your billing data as graphs



# Variation Study

## Cloud Services 
Similar names, completely different services

### CloudFormation
Infrastructure as code, set up services via templating script eg. yml, JSON

### CloudTrail
logs all api calls between aws services eg. aws s3api create-bucket --bucket my-bucket-ash-test-123

### CloudFront
Content Distribution Network, it creates a cached copy of your website and copies to servers located near people trying download webiste

### CloudWatch
is a collection of multiple services
- CloudWatch Logs: any custom log data, Memory Usage, Rails Logs, Nginx Logs
- CloudWatch Metrics: metrics that are based off of logs eg. Memory Usage
- CloudWatch Events: trigger an event based on a condition eg. ever hour take snapshot of server
- CloudWatch Alarms: triggers notifications based on metrics
- CloudWatch Dashboard: create visualizations based on metrics

### CloudSearch
Search engine, you have an ecommerce website and you want to add a search bar

## Connect Services

### Direct Connect
Dedicated Fiber Optics Connections from DataCenter to AWS
- A large enterprise has their own datacenter and they need an insanely fast connection directly AWS. If you need to security you can apply a VPN connect on-top of Direct Connect

### Amazon Connect (Call Center Service)
Get a toll free number, accept inbound and outbound calls, setup automated phone systems.

### Media Connect (New Version of Elastic Transcoder, Coverts Videos to DIfferent Video Types)
You have 1000 of videos you and you need to transcode them into different videos format, maybe you need to apply watermarks, or insert introduction video in front of every video

## Elastic Transcoder vs MediaConvert
Both services transcodes videos

### Elastic Transcoder
- The old way
- Transcodes videos to streaming formats

### AWS Elemental MediaConvert
- The new way
- Transcodes videos to streaming formats
- Overlays images
- Insert videos clips
- Extracts captions data
- Robust UI

## SNS vs SQS
The both Connect Apps vis Messages

### SNS (Simple Notifications Service)
Pass Alongs Messages eg. PubSub

--

- Send notifications to subsribers of topics via multiple protocol eg. HTTP, Email, SQS, SMS

- SNS is generally used for sending plain text emails which is triggered via other AWS services. The best example of this is billing alarms.
- Can retry sending in case of failure for HTTPS
- Really good for webhooks, simple internal emails, triggering lambda functions

### SQS (Simple Queue Service)
Queue Up Messages, Guaranteed Delivery

--

- Places messages into a queue. Applications pull queue using AWS SDK
- Can retain a message for up to 14 days
- Can send them in sequential order or in parallel
- Can ensure only one message is sent
- Can ensure messages are delivered at least once
- Really good for delayed tasks, queueing up emails

## Amazon Inspector vs AWS Trusted Advisor
Both are security tools and they both perform audits

### Amazon Inspector
- Audits a single EC2 instance that you've selected
- Generates a report from a long list of security checks i.e 699 checks

### Trusted Advisor
- Trusted Advisor doesn't generate out a PDF report
- Gives you a holistic view of recommendations across multiple services and best practices eg. you have open ports on these security groups
- You should enable MFA on your root account when using trusted advisor

## ALB vs NLB vs CLB

All three of these can attach Amazon Certification Manager(ACM) SSL Certificate

### Application
- Layer 7 Requests
- HTTP and HTTPS traffic
- Routing Rules, more usability from one load balancer
- Can attatch WAF

### Network
- Layer 4 IP protocol data
- TCP and TLS traffic where extreme performance is required
- Capable of handling millions of requests per second while maintaining ultra-low latencies
- Optimized for sudden and volatile traffic patterns while using a single static IP address per Availability Zone

### Classic (Old)
- Layer 4 and Layer 7
- Intended for applications that were built within the EC2-Classic network
- Doesn't use Target Groups

## SNS vs SES

### SNS (Simple Notifications Service)
Practical and Internal

--

- Send notifications to subsribers of topics via multiple protocol eg. HTTP, Email, SQS, SMS

- SNS is generally used for sending plain text emails which is triggered via other AWS services. The best example of this is billing alarms.

- Most exam quesitons are going to be talking about SNS beacuse lots of services can trigger SNS for notifications.

- You need to know what are Topics and Subscriptions regarding SNS

### Simple Email Service
Professional, Marketing, Email

- A cloud based email service eg. SendGrid
- SES send html emails, SNS cannot
- SES can receives inbound emails
- SES can create Email Templates
- Custom domain name email
- Monitor your email reputation

## AWS Artifact vs AWS Inspector

Both Artifact and Inspector compile out PDFs

### AWS Artifact
- Why should an enterprise trust AWS?
- Generates a security report that's based on global compliance frameworks such as:
  - Service Organization Control (SOC)
  - Payment Card Industry (PCI)

### AWS Inspector
- How do we know this EC2 instance is secure? prove it?
- Runs a script that analyze your EC2 instance, then generates a PDF report telling you which security checks passed.
- Audit tool for security of EC2 instances.