
Elasticity is the ability to acquire resources as you need them and release resources when you no longer need them. Think of Auto Scaling and adding and removing instances as needed.

Vertical scaling is increasing the size and computing power of a single instance or node without increasing the number of nodes or instances.

VPCs are associated to a single Region. You cannot span a VPC across Regions, nor can you peer with a VPC in another Region.

AWS logically groups its Regions into geographic locations. Each Region is spread out and fully independent and isolated from other Regions. If there's a flood, tsunami or earthquake in 1 Region, the other Regions will not be impacted. Because of this, it makes sense to deploy your application to multiple Regions.

Serverless is a way to build and run applications without having to manage infrastructure. Fargate is considered serverless.

Serverless is a way to build and run applications without having to manage infrastructure. Lambda is considered serverless.

Serverless is a way to build and run applications without having to manage infrastructure. S3 is considered serverless.

Serverless is a way to build and run applications without having to manage infrastructure. DynamoDB is considered serverless.

EC2 is not serverless because there is a server that you directly manage.

While CloudFront speeds up the global delivery of static content, it alone doesn't ensure high availability.

Multi-Region deployments are best for applications that have extremely high availability requirements.

Deploying applications to multiple AZs replicates applications across multiple data centers in the same Region, supporting high availability.

Fault Tolerant systems are designed to operate through failures of key components. These systems avoid loss of service by reducing or managing failures.

AWS recommends enabling multiple Availability Zones for all load balancers. With an Application Load Balancer, however, it is a requirement that you enable at least two or more Availability Zones. This configuration helps ensure that the load balancer can continue to route traffic. If one Availability Zone becomes unavailable or has no healthy targets, the load balancer can route traffic to the healthy targets in another Availability Zone.

A CloudWatch alarm can be set up to monitor CPU utilization and trigger further action. Further action could be an Auto Scaling group adding another EC2 instance and/or using SNS to notify team members of the occurrence.

Trusted Advisor provides real-time guidance to help you provision your resources following AWS best practices. https://aws.amazon.com/premiumsupport/technology/trusted-advisor/

With elasticity, the company doesn't have to plan ahead of time how much capacity they'll need - elasticity allows them to match the supply of resources with changing workload demands.

The Auto Scaling group can be used to scale out and scale in the instances as the demand dictates. This will save money and avoid having instances sitting idle for long periods of time. AWS Auto Scaling monitors your applications and automatically adjusts your capacity to maintain steady, predictable performance at the lowest possible cost. Using AWS Auto Scaling, it’s easy to set up application scaling for multiple resources across multiple services in minutes. https://aws.amazon.com/autoscaling/

The company can utilize Elastic Load Balancing to evenly distribute incoming traffic across all their EC2 instances.

An edge location uses cached copies of your content for fast delivery to users. Don't forget CloudFront speeds up delivery using edge locations.

A Region is a geographical area of the world that is a collection of data centers logically grouped into Availability Zones. 

If the developer uses a serverless architecture (for example, one that includes Lambda), the developer will not have to worry about managing servers or the underlying infrastructure.

Elasticity allows the developer to match the supply of resources with changing workload demands.

You pay only when you access it and only for what you use, which allows you to spread costs over time since there are no huge upfront investments.

Customers benefit from massive economies of scale and achieve lower variable costs than they can get on their own due to volume discounts.

AWS Organizations provides central governance and management for multiple accounts. Organization SCPs allow you to create permissions guardrails that apply to all accounts within a given organization. Service control policies (SCPs)

AWS Organizations provides central governance and management for multiple accounts. Organization SCPs allow you to create permissions guardrails that apply to all accounts within a given organization. Service control policies (SCPs)

While configuration management is a shared responsibility between the customer and AWS, AWS is responsible for configuration of infrastructure devices.

AWS maintains the configuration of its infrastructure devices. Don't forget AWS is responsible for its global infrastructure elements: Regions, edge locations, and Availability Zones.

The IAM credential report lists all the users and the status of their various credentials, including passwords, access keys, server certificates, and MFA devices.

Artifact offers on-demand access to AWS security and compliance reports.

KMS allows you to generate and store encryption keys.

Secrets Manager allows you to manage and retrieve secrets (passwords or keys).

This Performance Efficiency pillar focuses on the effective use of resources to meet demand. In this pillar, you would use the information gathered through the evaluation process to actively drive adoption of new services or resources. You would also define a process to improve workload performance, and you would need to stay up-to-date on new resources and services.

You are responsible for patching the guest operating system.

The principle of least privilege involves giving a user the minimum access required to get the job done. https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#grant-least-privilege

Config allows you to assess, audit, and evaluate the configurations of your resources over time. Config works with EC2 instances, servers running on-premises, and servers and VMs in environments provided by other cloud providers.

The company will need to create a role that grants access to S3 and associate it with the instance.

IAM allows you to create and manage access keys for an IAM user.

A bucket access policy can be attached directly to an S3 bucket to limit access to specific users.

CloudWatch can monitor the state of your AWS resources and can notify you when an EC2 is approaching 100% utilization.

AWS is responsible for the Lambda runtime environment.

By default, all subnets within a VPC can communicate with each other, without needing any other resources or configuration. https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Subnets.html

NAT gateways work in different scenarios to allow your subnet to communicate with the internet and are not required to communicate between subnets.

Polly turns text into speech.

AWS Application Discovery Service helps you gather information about your on-premises environment and is considered a migration tool. https://aws.amazon.com/cloud-migration/

Config allows you to assess, audit, and evaluate the configurations of your resources.

Snowball helps you migrate massive amounts of data into cloud, so it is considered a migration tool. https://aws.amazon.com/cloud-migration/

Auto Scaling allows you to automatically add or remove EC2 instances based on conditions you specify - these can include such things as at a specific time, or depending on how busy your application is. Auto Scaling cannot change the size of existing instances, nor can it add or change storage on an instance. https://aws.amazon.com/autoscaling/

Auto Scaling adds or removes instances — it does not change the sizing of instances.

Enterprise Support provides access to a Technical Account Manager (TAM) who helps coordinate access to subject matter experts among other things.

The Business level support plan provides 1 hour or less response time support for production-level failures. https://aws.amazon.com/premiumsupport/plans/

Organizations allows you to centrally manage multiple AWS accounts under 1 umbrella. You can allocate resources and apply policies across accounts.

Trusted Advisor provides real-time guidance to help you provision your resources following AWS best practices.

Control Tower helps you ensure your accounts conform to company-wide policies. Control Tower actually sits on top of Organizations.

The Pricing Calculator provides an estimate of AWS fees and charges. Since the company knows the workload details, the AWS Pricing Calculator can also help with calculating the total cost of ownership.

Tightly coupled components are highly dependent on each other and should be avoided.

Loose coupling helps reduce the risk of cascading failures between components.

Trusted Advisor doesn't check if any AWS is down. However, you can easily find this information on the AWS Service Health Dashboard.

Trusted Advisor checks Amazon S3 buckets for open-access permissions, which allow anyone to access the bucket's contents. It also checks for bucket policies that might override these permissions, giving unintended users access to the bucket.

Security groups act like built-in firewalls for your virtual servers — the rules you create define what is allowed to talk to your instances and how. Although network access control lists can be used to block or deny traffic, these operate at the subnet level (covering all instances in the subnet with the same ruleset), not per instance as the question specifies. Route tables tell traffic where it should go next to reach its destination, and an Availability Zone is a collection of data centers — which isn't relevant in this question

Under the Shared Responsibility Model, AWS takes responsibility for managing all the hardware (including access, patching, and other maintenance) and software required to deliver the service — which in this case is the EC2 instance. Anything to do with the instance itself is the responsibility of the customer.

Application is a valid load balancer type AWS offers
Classic is a valid load balancer type AWS offers
Network is a valid load balancer type AWS offers

CloudTrail allows you to track the username.
CloudTrail tracks the AWS Region that the request was made to, such as us-east-1.

A NAT gateway is required to allow resources in a private subnet to access the internet

NACLs ensure proper traffic is allowed in the subnet. By themselves, they do not enable access to the internet, but they need to be properly configured to let traffic bound for the internet out.

Lex helps you build conversational interfaces like chatbots.

A CloudFront origin can be an S3 bucket, an elastic load balancer, or a valid domain name

Cost savings is a benefit of AWS Organizations. You'll receive volume discounts since usage is combined across accounts.
Account governance is a benefit of AWS Organizations. You have a quick and automated way to create accounts or invite existing accounts.
Consolidated billing is a benefit of AWS Organizations. The advantage of consolidated billing is that you receive 1 bill for multiple accounts.

Infrastructure Event Management offers architecture guidance and operational support during the preparation and execution of planned events, such as shopping holidays, product launches, and migrations.

Trusted Advisor has a service limit dashboard that helps you monitor service limits.

CloudWatch Alarms can be used to determine the percentage of utilization versus the limit.

Amazon Redshift provides the best solution for performing queries based on a predefined set of dimensions. Redshift organizes data for high performance based on user-specified distribution schemes. Amazon ElastiCache provides in-memory performance, but no data organization assistance. Amazon Aurora and Amazon DynamoDB are good solutions, but Redshift's columnar storage gives it the edge


Snowmobile transports multi-petabyte or exabyte-scale data.
Snowball is a petabyte-scale data transport solution.

Redshift is at times the recipient of streaming data, but it can not itself stream data in real time

Kinesis allows you to analyze data and video streams in real time. 

Customers on the Developer Support plan can submit support cases for account and billing questions, service limit increases, and technical support cases via email only.

Consolidated billing has the benefit of combining usage across all accounts in the organization to share the volume pricing discounts, Reserved Instance discounts, and Savings Plans. This can result in a lower charge for your project, department, or company than with individual standalone accounts.

AWS maintains networking components: generators, uninterruptible power supply (UPS) systems, computer room air conditioning (CRAC) units, fire suppression systems, and more.

Coupling defines the interdependencies or connections between components of a system. Loose coupling helps reduce the risk of cascading failures between components.

AWS customers are welcome to carry out security assessments or penetration tests against their AWS infrastructure without prior approval for Amazon EC2 instances, NAT gateways, elastic load balancers, and 7 other services.

Inspector works with EC2 instances to uncover and report vulnerabilities.

Trusted Advisor is a tool that provides real-time guidance to help you provision resources following AWS best practices. It will check security groups for rules that allow unrestricted access (0.0.0.0/0) to specific ports.

The IAM credential report lists all the users and the status of their various credentials, including passwords, access keys, server certificates, and MFA devices.

WAF helps protect your web applications against common web attacks.

AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS. Shield Standard protects against layer 3 and 4 attacks. Shield Advanced protects against layer 3, 4, and 7 attacks.

An internet gateway enables resources inside your VPC to reach the internet, as long as route tables and IP addresses are correctly configured in your environment.

NACLs ensure proper traffic is allowed in the subnet.

Installing the database directly to EC2 gives the customer complete control over the database and its management.

RDS does provide a lot of value, like automated backups and software patching, but it does not provide the complete control and flexibility needed by the customer.

With a Savings Plan, you commit to specific usage, but this commitment doesn't reserve capacity.

A Reserved Instance is a reservation of resources and capacity for either 1 or 3 years. A capacity reservation offers assurance that the customer will be given preference if there is ever a capacity constraint in a Region.

On-Demand Capacity Reservations enable you to reserve compute capacity for your Amazon EC2 instances for any duration.

A Reserved Instance is a reservation of resources and capacity for either 1 or 3 years. A capacity reservation offers assurance that the customer will be given preference if there is ever a capacity constraint in a Region.

Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost. https://aws.amazon.com/autoscaling/


On-Demand Instances are charged equally per-hour, regardless of how long they're run for.

EC2 Reserved Instances offer significant discounts for a contracted term-of-service, up to 72% off.

Spot Instances are a great choice for this use case. Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS Cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices. The key phrase in this question is, "It is alright if there are interruptions in the application." If the application could not accept interruptions, then the best option would be On-Demand.

With On-Demand Instances, you pay for compute capacity by the second with no long-term commitments. This is, however, not the best option for this scenario. 


A multi-Region deployment will best ensure global availability. While it can be the most expensive, as well as complex to configure, multi-Regional architectures will ensure that even if all Availability Zones in a single Region fail due to a catastrophic event, your data will remain accessible.

Edge locations host a content delivery network called CloudFront. https://aws.amazon.com/about-aws/global-infrastructure/

To enable the option for selecting an object to be public you first need to disable the Block Public Access setting on the S3 bucket. This setting is in place to prevent accidental configuration of the S3 bucket and objects being visible from anywhere on the internet.

EMR helps you process large amounts of data using big data frameworks like Hadoop.

CloudWatch provides events and alarms, and could potentially be set up to be triggered when an EC2 instance is terminated but will not provide detailed information over who and when the action was taken.

CloudTrail provides the event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command line tools, and other AWS services.

Elastic Beanstalk monitors application health via a health dashboard.

Load balancers monitor the health of EC2 instances and route the traffic to only instances that are in a healthy state.

Route 53 can be used to configure DNS health checks to route traffic to healthy endpoints or to monitor the health of your applications.

Kinesis helps collect, process, and analyze real-time streaming data.

Redshift allows you to run complex analytic queries against petabytes of structured data, using sophisticated query optimization, columnar storage on high-performance local disks, and massively parallel query execution.

Spot Instances are usually the most cost-effective solution for workloads that can be interrupted. On-Demand and Reserved Instances are both more expensive in this use case, and Custom Instances do not exis

EMR is a service that makes it easy to process large amounts of data efficiently

The IAM policy simulator allows you to test and troubleshoot identity-based policies, IAM permissions boundaries, service control policies (SCPs), and resource-based policies.

While CodeDeploy can deploy code to the cloud and on-premises, it is not used to automate the configuration of servers like OpsWorks.

OpsWorks allows you to use Chef or Puppet to automate the configuration of your servers and deploy code on-premises or the cloud.

IAM entities are the users (IAM users and federated users) and roles that are created and used for authentication.

An identity is an IAM resource object that is used to identify and group. You can attach a policy to an IAM identity. These include users, groups, and roles.

