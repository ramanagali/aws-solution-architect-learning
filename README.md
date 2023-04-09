**Solutions Architect Learning Plan Badge Assessment**

============================================== **EXAM 1** ==============================================

**Single choice**

1) A company is currently running a SQL Server database on-premises and is interested in migrating the database to Amazon Aurora.

Which of the following methods will help migrate the existing database to AWS?

1) **Use the Schema Conversion Tool to convert the existing schema for a new database engine. Once the schema is available, use the Database Migration Service to load the data into a new Amazon Aurora Database.**
1) Use the Schema Conversion Tool to create a new schema for this heterogenous migration. The schema will allow you to load the data directly to Amazon Aurora.
1) Use the Database Migration Service to directly read the data from the existing SQL Server database and load the data into a new Amazon Aurora Database.
1) Use the Schema Conversion Tool to create a new schema for this homogenous migration. A new schema will allow you to load the data directly to Amazon Aurora.




**Single choice**

2) A customer application runs on a fleet of Amazon EC2 instances. The program read and writes to Amazon DynamoDB. The application just needs last 7 days of data. However, the size of the database keeps increasing. The company needs a solution that minimizes cost and development effort.

Which solution meets these requirements?

1) Use Amazon EC2 instance to run a script to delete items that's have timestamp older than 7 days.
1) Configure Amazon DynamoDB stream to invoke AWS Lambda function when new item is created. Configure AWS Lambda to delete items in table that are older than 7 days.
1) **Configure application to add an attribute that has a value of current timestamp plus 7 days to each item created in table. Configure DynamoDB to use the attribute as TTL attribute.**
1) Use AWS CloudFormation to deploy the solution and re-deploy stack every 7 days.




**Single choice**

3) A company wants a solution to deploy and track AWS resources using dynamic templates authored in YAML format. Teams should have the ability to select frompre-defined values that change properties of AWS resources in the template.

What AWS service would you recommend that is able to meet these requirements?

1) AWS CodePipeline
1) AWS OpsWorks
1) **AWS CloudFormation**
1) AWS Elastic Beanstalk


**Single choice**

4) A company has an On-Demand Amazon EC2 instance with an attached Amazon EBS volume. There is a scheduled job that creates a snapshot of this EBS volume at 12 AM when the instance is not used. You have a production incident where you need to perform a change on both the instance and on the EBS volume at the same time when the snapshot is currently taking place.

Which of the following scenarios is valid when it comes to the usage of an EBS volume while the snapshot is in progress?

1) The volume can be used in read only mode when a snapshot is in progress.
1) The Amazon EBS volume can't be detached or attached when a snapshot is in progress.
1) The Amazon EBS volume cannot be used when a snapshot is in progress.
1) **The Amazon EBS volume can be used when the snapshot is in progress.**


**Single choice**

5) Your organization's operational lead has decided to build a cost effective centralized logging solution for multiple AWS accounts. The solution includes an Amazon S3 bucket in the centralized logging account. The logs must be deleted after three months to minimize cost.

What is the most operationally efficient way to accomplish this task?

1) Transition objects to the S3 Standard-IA storage class 30 days after creating them and delete manually/
1) Archive objects to the S3 Glacier Flexible Retrieval storage class for thee months and delete manually.
1) **Expiration actions**
1) Transition actions

**Single choice**

6) The publicly accessible website hosted on Amazon EC2 instance in GovCloud region is able to communicate with Amazon S3. Amazon DynamoDB within the same region is also able to access Amazon S3 buckets. However, the Amazon RDS database instance that uses a private subnet of a Amazon VPC hosted in the same region is unable to send SNS notifications to Amazon S3.

Which one of the following would you use to resolve the problem?

1) **VPC Endpoint**
1) Direct Connect Gateway
1) AWS Transit Gateway
1) Virtual Private Gateway


**Multiple Choice**

7) What API types are supported by Amazon API Gateway? (Select TWO)

- **WebSocket API**
- HTTPS API
- TCP
- **HTTP API**
- GraphQL API
- UDP

**Single choice**

8) A  company runs a multi-tier web application in the AWS Cloud. The application tier is hosted on Amazon EC2 instances and the backend database is hosted on an Amazon Aurora for MySQL DB cluster. For security compliance, all of the application variables such as DB hostnames, environment settings, product keys, and database passwords must be stored securely with encryption.

Which of the following options is the most cost-effective solution to meet the requirements?

1) Store the values as key-value pairs in AWS Systems Manager OpsCenter. By default, the key-value pairs will be encrypted at rest. Configure the application to retrieve the variables when it starts.
1) Store the values in a file in Amazon S3. Enable encryption on the S3 bucket and configure the application to download it.
1) Store the values by creating SecureString type parameters in AWS Systems Manager Parameter Store. Use AWS Key Management Service (AWS KMS) for the encryption. Update the application to retrieve the parameter values.
1) **Store the values by creating secrets in AWS Secrets Manager. Use AWS Key Management Service (AWS KMS) for the encryption. Update the application to retrieve the value of the secrets.**

**Single choice**

9) Your company processes and stores sensitive and private data on Amazon S3. Amazon EC2 instances process the data and then the data is sent to Amazon S3.

What design solution ensures the data does not traverse the public internet?

1) Configure a transit gateway and add a route to send the private data to Amazon S3.
1) Configure a NAT Gateway in the private subnet that sends the private data to Amazon S3.
1) **Configure an Amazon VPC endpoint and add a route to send the private data to Amazon S3.**
1) Configure an internet gateway in the public subnet to send the private data to Amazon S3.





**Single choice**

10) You work as a solutions architect for a Healthcare company that hosts all their applications on Amazon EC2 instances. For compliance and governance perspective, the company has to take daily, weekly, and monthly snapshots of all their volumes. For auditing purpose there is a requirement to keep the snapshot for 6 months and next 6 months in grace period after which the snapshots can be deleted. To automate the snapshot creation, the organization is already using Amazon Data Lifecycle Manager (DLM) policies, so that no volume is left out from snapshot perspective. Recently you discovered that the total snapshot cost has almost doubled as compared to total volume cost.

What automated method can you take to reduce the total snapshot cost?

1) Push all the Snapshots to Amazon S3 bucket and then put a lifecycle policy on that bucket to archive the snapshots after 6 months and delete it after 1 year.
1) **Create an archival policy Amazon EBS Snapshots with Amazon Data Lifecycle Manager wherein the Snapshots will be archived after 6 months and deleted after 1 year.**
1) Leverage the SSM Run command  to delete the snapshots who have aged for 365 days.
1) Manually identify the snapshots which need to be deleted via describe snapshot API and then invoke a Delete Snapshot API based on snapshot age.

**Single choice**

11) Your company is looking to store session information from their backend Amazon EC2 instances and they want to identify the best database which can provide them durability, high availability (HA), scalability and persistence. Since they want to store session information, they want a database which can provide them microsecond latency.

Which one of the following database can best satisfy the requirements?

1) Amazon DocumentDB
1) Amazon ElastiCache with Redis cluster mode enabled
1) **Amazon MemoryDB for Redis**
1) Amazon DynamoDB


**Single choice**

12) An Amazon EC2 instance in a subnet communicates with another instance that is in a different subnet in the same Amazon VPC. It is noted that communication using the private IP addresses of the instances works.

Why does this type of behavior occur without the need to edit the route tables?

1) **This behavior is due to the Local Route in the route table, which is added to all route tables by default.**
1) This behavior is due to a 0.0.0.0/0 route in the route table.
1) This behavior is because there is no need for routing between Amazon EC2 instances within the same Amazon VPC.
1) This is the default behavior of Amazon EC2 instances.


**Multiple Choice**

13) åYour company uses an Identity Provider (IdP) for Single-sign on (SSO) and has tasked their solutions architect with connecting their AWS Account to the IdP so their users can leverage their corporate identity to access the environment.
What actions should the solutions architect take to meet these requirements? (Select TWO)

1) Create an AWS IAM User with AWS Management Console Access, attach a policy with a trust relationship with the IdP.
1) **Create an AWS IAM Identity Provider by uploading the SAML metadata document from your IdP.**
1) **Create an AWS IAM Role with a trust relationship with the IdP.**
1) Create an AWS IAM Identity Provider by uploading the JSON metadata document from your IdP.
1) Create an AWS IAM User Group, associate the User Group with the IdP and add users to the User Group.


**Multiple Choice**

14) Which of the following are benefits of integrating AWS Firewall Manager withAWS Organizations ? (Select TWO)

1) You can configure Amazon RDS database engines and Database parameters.
1) **Firewall Manager monitors for new resources created to ensure they comply with a mandatory set of security policies.**
1) **You can enable AWS WAF rules, AWS Shield Advanced protections, Amazon VPC security groups and AWS Network Firewalls.**
1) You can centrally manage Amazon S3 Lifecycle configuration on a bucket.

**Single choice**

15) A customer wants to host their domain in AWS using Amazon Route 53 service. They plan to use Amazon CloudFront for distributing their website globally. All the static assets of the website will be served from Amazon S3 and Amazon EC2 will be used for serving the dynamic content via Amazon CloudFront. The customer needs a way to integrate Amazon Route 53 with AWS CloudFront and Amazon S3.

Which strategy would you recommend that is the easiest to configure?

1) **It is possible to integrate Amazon Route53 with other AWS services like CloudFront and S3 via creating an alias record in Route 53 that points to CloudFront distributions and S3 buckets.**
1) Use an AWS Lambda function with API Gateway to redirect the API calls from Amazon Route53 to Amazon CloudFront and from there to Amazon S3 and Amazon EC2.
1) They are integrated by default.
1) It is possible, however, we need to insert the code for the integration of other AWS Services in our application which will be using Amazon Route 53.

**Single choice**

16) Your company is working on a serverless project based in Java. The developer team tested the application locally and then deployed it to AWS Lambda. While testing the application remotely, the Lambda function fails with an access denied message.

How can this issue be addressed?

1) Include an IAM policy document at the root of the deployment package and redeploy the Lambda function.
1) Redeploy the Lambda function using an account with access to the Administrator Access policy.
1) **Update the Lambda function's execution role to include the missing permissions.**
1) Update the Lambda function's resource policy to include the missing permissions.


**Multiple Choice**

17) As a cloud architect, you've been tasked with finding a way to restrict access to a specific content for all users in a specific country.
Which of the following services could be used? (Select TWO)

1) AWS Network Firewall
1) Amazon Route 53
1) AWS Shield
1) **Amazon CloudFront**
1) **AWS WAF**

**Single choice**

18) The IT Director of a company wants to set automated backup of all the Amazon Elastic Block Storage (EBS) volumes for Amazon EC2 instances as soon as possible.

What is the fastest and most cost-effective solution to automatically back up all of your EBS Volumes?

1) Create a lambda function that calls the "create-snapshot" command via the AWS SDK to take a snapshot of production EBS volumes periodically.
1) Use Amazon S3 lifecycle policy to backup EBS volumes to S3
1) Set Amazon Storage Gateway with EBS volumes as the data source and store the backups in your on-premises servers through the storage gateway.
1) **Use Amazon Data Lifecycle Manager (Amazon DLM) to automate the creation of EBS snapshots.**


**Multiple Choice**

19) Some companies design their AWS workloads to update their components regularly, in small, reversible increments.

Which pillar of the AWS Well-Architected Framework does this design support?

1) **Operational Excellence**
1) Security
1) Reliability
1) Resilience

**Multiple Choice**

20) A solutions architect has to design an Amazon VPC with a private dual-stack subnet, running both IPv4 and IPv6 addresses, and it requires connectivity to the internet.

Which gateways can be used for both types of addresses to achieve this connectivity? (Select TWO)

1) **NAT Gateway for IPv4 addresses**
1) Egress Only Gateway for IPv4 addresses
1) Transit Gateway for both IPv4 and IPv6 addresses
1) **NAT Gateway for IPv6 addresses**
1) Egress Only Gateway for IPv6 addresses

NAT Gateways can be used for both IPv4 and IPv6 addresses in private subnets to allow outbound internet traffic.  Egress Only Gateway is only used for IPv6 addresses and Transit Gateway is used to connect multiple VPCs and on-premises networks, but it does not provide NAT functionality.

<https://aws.amazon.com/blogs/networking-and-content-delivery/dual-stack-ipv6-architectures-for-aws-and-hybrid-networks/>

**Multiple Choice**

21) Your company uses Amazon Route 53 in their networking account to manage public hosted zone records for their root domain, example.com. A developer in a different account requires the ability to create, update, or delete DNS records for their public application, app1.

How should you meet this requirement without giving the developer access to the company's networking account, or control over the root domain? (Select TWO)

1) Create an A record in the example.com Public Hosted Zone for the subdomain with the IP address from the app1.example.com Public Hosted Zone.
1) Create the example.com Public Hosted Zone in the developer’s account.
1) **Create an NS record in the example.com Public Hosted Zone for the subdomain with the name servers from the app1.example.com Public Hosted Zone.**
1) **Create the app1.example.com Public Hosted Zone in the developer’s account.**
1) Create the app1.example.com Private Hosted Zone in the developer’s account.

**Single choice**

22) A storage specialist of a company created a bucket named 'demobucket2022' for the purpose of storing files for the creation of a proof of concept (POC). After the successful implementation of proof of concept, the team wanted to leverage the bucket for the development work because of the content which was generated during POC. However, they didn't want to name it 'demobucket2022'.

What is the solution for the team to proceed with this implementation of the requirement?

1) **Amazon S3 buckets cannot be renamed once created. So, a new bucket needs to be created and copy the content using cp/sync command from the AWS CLI.**
1) Use the AWS Management Console and rename the bucket using rename bucket option.
1) Use AWS CLI and update the name of the bucket using the update bucket api.
1) Raise a support ticket and work with AWS support to rename the bucket.


**Multiple Choice**

23) A company is running a three-tier architecture on AWS. The web tier is in a public subnet, the application tier and the database are in private subnets across two availability zones. The company's security team noticed that specific IP addresses are attacking the Amazon EC2 instances in the web tier. A solutions architect must block traffic from those IP addresses from reaching the Amazon VPC.

How can this requirement be met?

1) **Block the IP addresses with Network ACLs from reaching instances in the public subnets.**
1) **Block the IP addresses with Security Groups.**
1) Block the IP address using Amazon GuardDuty.
1) Block the IP address using Amazon Inspector.

**Multiple Choice**

24) Since your company launched a new high performance computing (HPC) application in AWS, customers are complaining of latency. You, as the network engineer, have been tasked to ensure increased network performance for the application running on Amazon EC2 instances.

What should you implement to ensure the application has the lowest latency, highest network performance, and remains cost-effective?

1) **Launch multiple Amazon EC2 instances in a partition placement group across two Availability Zones.**
1) Vertical scale the Amazon EC2 instances.
1) Launch multiple Amazon EC2 instances with the current instance type and use two Availability Zones.
1) **Ensure enhanced networking is enabled on all Amazon EC2 instances running your application.**

**Multiple Choice**

25) You are a solutions architect at your company where you save backup data in Amazon S3. An employee inadvertently deleted a backup. You want to ensure that if data is deleted again, you should be able to retrieve the data and also ensure the data must not be inadvertently deleted in the future.

How can you achieve this requirement? (Select TWO)

1) Use presigned URL to protect the bucket from deletion.
1) Move the data to Amazon S3 Glacier.
1) **Configure MFA (multi-factor authentication) delete.**
1) Enable Amazon S3 default encryption.
1) **Turn on versioning in the Amazon S3 bucket.**

**Multiple Choice**

26) Which use cases are supported by Amazon S3 File Gateway? (Select TWO)

1) **Processing machine learning, big data analytics or serverless functions.**
1) Backing up on-premises file data as objects directly in Amazon EBS.
1) Migrating on-premises file data to Amazon S3, while maintaining fast local access to recently accessed data.
1) **Backing up on-premises file data as objects in Amazon S3.**
1) Backing up on-premises file data as objects directly in Amazon S3 Glacier.


**Single choice**

27) A retailer is using Amazon RDS for an online shopping store. They recently started a new sales promotion, which requires customers to access their purchase history. The database is configured in a Multi-AZ deployment. Since the primary database is used for live purchase transactions, the influx of queries is causing contention in the database, resulting in poor performance.

What is the best approach to offset the contention and improve performance with minimal effort and the least amount of downtime?

1) **Create a read replica for querying purchase history.**
1) Move the database to a larger instance size to support the increased load.
1) Use AWS Database Migration Service (DMS) to migrate the database to DynamoDB, which provides fast, consistent performance at any scale to improve overall performance.
1) Since RDS is already deployed as Multi-AZ, configure the standby database for querying purchase history, freeing the primary database for live purchase transactions.

**Single choice**

28) Which scaling considerations do not change when migrating from traditional cloud-based architectures to Serverless?

1) Designing horizontally scaled architectures with Auto Scaling Groups and Monitoring.
1) **Providing the best user experience, optimizing costs, and performing well under load.**
1) Designing for High Availability
1) Pre-provisioning capacity to handle an increase in expected workload.

**Multiple Choice**

29) Which open source databases are compatible with Amazon Aurora? (Select TWO)

1) SQL Server
1) Redis
1) **PostgreSQL**
1) **MySQL**
1) MariaDB


**Multiple Choice**

30) Your CEO decided to migrate your data center to AWS. You are engaged as the AWS migration specialist to create a business case and decide to use AWS Migration Evaluator.

Which of the following are included in the business case report? (Select THREE)

1) **A breakdown of what went into the on-premises costs.**
1) Recommendation on how to automatically converting your source servers from physical, virtual, or cloud infrastructure to run natively on AWS
1) Recommend AWS services required for your target architecture.
1) **Recommendation for the customer on next steps for a successful migration.**
1) **An executive summary of the savings across a combination of scenarios applied to different workloads.**
1) Provide configuration data about your on-premises servers.


**Multiple Choice**

31) Some Amazon EC2 instances are started to be added in an Amazon VPC and the Security Group and Network Access Control List (NACL) by default are being used.
How do these Amazon VPC security features behave?

1) **Security Group denies inbound traffic and allows all traffic outbound. NACL allows both incoming and outgoing traffic, to start denying the default configuration must be edited**.
1) Security Groups allow both inbound and outbound traffic. NACL allows both incoming and outgoing traffic, to start denying the default configuration must be edited.
1) Security Groups deny both inbound and outbound traffic. NACL allows both incoming and outgoing traffic, to start denying the default configuration must be edited.
1) Security Groups deny inbound and outbound. NACL denies both incoming and outgoing traffic, to start allowing the default configuration must be edited.

**Multiple Choice**

32) You have deployed a multi tier web application and placed it in an Amazon VPC.The web tier is in subnet A, the application tier is in subnet B, and the database tier is in subnet C.

What series of steps should you take to ensure that the application tier can only receive traffic via HTTPS from the web tier and only send traffic via MySQL to the database tier? (Select TWO)

1) **Add an outbound rule to your application tier security group on TCP port 3306 with a destination of the database tier**
1) Create a database tier security group with an inbound rule on TCP port 3306 with the source of the application tier.
1) Add a managed NAT gateway to connect your application tier with your database tier
1) Create a database tier security group with a deny rule for application tier on all ports except TCP 3306.
1) **Create an application tier security group with an inbound rule on HTTPS port 443 with the source of the web tier**

**Single choice**

33) A company operates in a highly regulated industry. The company stores log files in Amazon S3. Industry policy requires that the company must not delete or overwritten the log files for at least 6 months.

What should a solutions architect do to meet these requirements?

1) Use presigned URL to protect the bucket from deletion.
1) Enable Amazon S3 Intelligent-Tiering
1) **Create a new bucket and enable object lock.**
1) Configure MFA (multi-factor authentication) delete.


**Single choice**

34) As an AWS solutions architect, you review this AWS CLI command line used to create a PostgreSQL-compatible Amazon RDS database cluster:

aws rds create-db-cluster 
--db-cluster-identifier sample-pg-cluster 
--engine aurora-postgresql 
--master-username master 
--master-user-password secret99 
--db-subnet-group-name default 
--vpc-security-group-ids sg-0b9130572daf3dc16

You notice that a retention period for the automated backup was not set.
What retention period, in days, will be used by this PostgreSQL-compatible Amazon RDS database cluster?

1) 7
1) 35
1) **1**
1) 0

**Single choice**

35) Your company is exploring cloud computing and wants to start by building a small, event-driven application that supports Marketing campaigns. The campaign will consist of workflow that involves several discrete steps and target a small customer base. The Marketing group wants the developers to build it quickly and have it ready for customers as soon as possible. The developers want a visual way to track the individual steps in the campaign.

Which compute option would be best?

1) **Run the application on AWS Batch. Organize the steps in the batch with AWS Step Functions for compute.**
1) Configure an Amazon EC2 instance and deploy the application to run there. Write another service to run the application components when requested on another EC2.
1) Use AWS Lambda for compute. Organize the Lambdas to run within AWS Step Functions.
1) Run the application on AWS Batch. Set up Batch to call the Lambda for compute.


**Single choice**

36) As the solutions architect in an organization, you are given an assignment to build an application in AWS which is required to be deployed in an Auto Scaling group of On-Demand Amazon EC2 instances and a MongoDB database. It is expected that the database will have high-throughput workloads performing small, random I/O operations.

Which of the following is the most performant Amazon EBS type to use for your database?

1) General Purpose SSD - gp2
1) Cold HDD - sc1
1) Throughput Optimized HDD - st1
1) **Provisioned IOPS SSD - io1**

**Single choice**

37) Your company is looking to migrate its data-heavy, flagship video processing application to AWS. The application runs across multiple Linux servers on-premises. The application requires a high performance file system, as the instances need to share the data at a very fast rate.

Which recommendation best meets the requirements?

- **Host your application on multiple Amazon EC2 Linux instances. Use Amazon FSx for Lustre for file system storage.**
- Host your application on multiple Amazon EC2 Linux instances. Use Amazon FSx for Windows File Server for file system storage.
- Host your application on Amazon S3 and utilize S3 for file system storage.
- Host your application on Amazon S3. Use Amazon EFS for file system storage.


**Single choice**

38) A solutions architect has been asked to help troubleshoot a Step Function's execution of a state machine. The users are noticing that occasionally, a task doesnt return a response and it creates a situation where the state machine has to be reset.

What can be added to the process flow in the state machine to help recover automatically from a stuck condition created by an un-returned result from a task?

1) Create a cron job that will automatically retrigger the state machine after a certain amount of time.
1) Create a Pass process flow to bypass the problem task.
1) **Use timeouts to avoid stuck executions.**
1) Remove the problem task from the state machine.


**Multiple Choice**

39) As the AWS solutions architect, you need to explore whether Amazon ECS is the right choice to build sophisticated application architectures on a microservices model.

Which of the following is true for Amazon ECS? (Select THREE)

1) Easier to manage since your entire application need to be on a single task definition.
1) **Amazon ECS has built-in security; all of the images are stored in a container registry that is only accessible through HTTPS.**
1) Amazon ECS supports multi-cloud integration.
1) **A cluster may contain a mix of tasks hosted on AWS Fargate, Amazon EC2 instances, or external instances.**
1) Amazon ECS manages your cluster resources for all launch types.
1) **Amazon ECS provides service discovery for a microservice architecture.**

**Single choice**

40) A multi-national company has services across the globe which has a web application as its customer-facing frontend. One of the features of the app is to allow users to be able to upload huge amounts of files. As part of their architecture, they use a single bucket in the us-east-1 region and all the data from users is uploaded to this bucket. Now, as the demand for applications has grown, more and more users are using the application, which has led to an increase in file uploads. Because the users are across the globe, the upload takes time when the users are geographically far from the us-east-1region, which leads to a degraded user experience. You need to improve the upload experience without making major code level changes.

Which is the best service that you could use to achieve this requirement?

1) AWS DataSync
1) Amazon Partner Network
1) AWS Transfer Family
1) **Amazon S3 Transfer Acceleration**


**Multiple Choice**

41) Your company is looking for a solution to manage backups for their workloads running in AWS. They are interested in the AWS Backup service, but are trying to determine the cost of the service.

Which of the following factors would need you to look at to determine the actual cost of AWS Backup? (Select TWO)

1) **The amount of storage used to store the backups.**
1) The backup frequency.
1) The service(s) being protected,
1) **The retention period.**


**Multiple Choice**

42) Your company uses an Amazon EC2 instance in a public subnet to host a web application. The Amazon EC2 instance uses a default security group. The network ACL is configured to block all traffic to the instance. You must allow incoming traffic on port 443 to access the application from any source.

Which combination of steps will accomplish this requirement? (Select TWO)

1) In the security group, add a rule to allow TCP connections on port 443 from the source 0.0.0.0/0
1) In the security group, add a rule to allow TCP connections on port 443 to destination 0.0.0.0/0
1) **In the network ACL add rules to allow both inbound and outbound TCP connection on port 443 from source 0.0.0.0/0 and destination 0.0.0.0/0**
1) In the network ACL, add a rule to allow inbound TCP traffic on port 443 from source 0.0.0.0/0 and outbound traffic on port 1024-65535 to the destination 0.0.0.0/0
1) **In the network ACL, add a rule to allow outbound TCP traffic on port 1024 - 65535 to destination 0.0.0.0/0**

**Single choice**

43) A healthcare company has strict security requirements and they need to make sure that data in Amazon S3 buckets is not publicly accessible. However, one of their team members inadvertently made a bucket publicly available. The Security team of the company wants to implement a solution that would prevent public access to any buckets requiring minimal administrative effort.

What settings needs to be implemented by the Security team to achieve the requirement?

1) **Implement block public access level setting at the account level.**
1) Implement block public access level setting at the bucket level.
1) Implement a Config rule named 's3-bucket-public-write-prohibited' which will prevent public access to all the buckets.
1) Configure an AWS Lambda function which periodically identifies any publicly accessible buckets and remediates the issue.

**Single choice**

44) A company is using SQL to query their self hosted PostgreSQL server. The IT architect wants to migrate their database to AWS purpose built databases and use a serverless database as their workloads are very unpredictable.

Which service will meet their needs?

1) DynamoDB
1) Amazon ElastiCache
1) **Amazon Aurora**
1) Amazon RDS


**Single choice**

45) You are a cloud security engineer and have been tasked with ensuring that confidential data is not accessible publicly. To ensure compliance with this mandate, you are interested in turning on Amazon S3 Block Public Access (BPA) feature.

Which of the following statements best describes the AWS concept of public access?

1) Any bucket or object that grants permissions to any resources located outside AWS.
1) Any bucket or object that grants permissions to AllUsers OR AuthenticatedUsers groups.
1) Any bucket or object that grants permissions to any resource in another AWS account.
1) **Any bucket or object accessible by any source other than the bucket or object owner.**


**Single choice**

46) Your team is deploying a new solution on Amazon ECS. Since your team is new to the cloud, your director wants you to use AWS provided permissions to ensure reusability and automatic updates.

Which type of AWS provided permission policy should you use to enable principals to create, manage, and describe Amazon EC2 Auto Scaling resources?

1) **Managed policy**
1) Multi-factor authentication
1) Custom policy
1) Inline policy


**Multiple Choice**

47) A company wants to allow their existing Active Directory users access to AWS without having to recreate AWS IAM user accounts for every person.

Which of the following methods is the most cost effective solution to meet the requirements? (Select TWO)

1) Amazon Directory Services
1) Cognito Identity Pool
1) **SAML 2.0**
1) X.509 Certificate
1) **OpenID Connect**

**Multiple Choice**

48) A company is working on a new product launch. Both production and test environments are using similar Amazon EC2 instances with attached Amazon EBS volumes. The Billing team will need a solution to monitor the costs of both environments to identify any unexpected charges.

What should a solutions architect implement to ensure that the Billing team can identify the charges for each environment? (Select TWO)

1) Cost Allocation Tag
1) **Budgets**
1) **Cost Explorer**
1) AWS Trusted Advisor
1) Savings Plans

**Single choice**

49) The finance team in your organization needs to send data to your team's backend workflow. You want to filter inbound traffic at the subnet level while allowing returning traffic back to the finance team's service.

What do you need to setup to complete this workflow?

1) **Create a Security Group.
   Enable inbound connections from the other team. Since Security Group is stateful, it will automatically enable outbound returning traffic.**
1) Create a Network Access Control List (NACL).
   Enable inbound traffic from the other team's service. Since NACL is stateful, it will automatically enable outbound returning traffic.
1) Create a Network Access Control List (NACL).
   Enable inbound traffic from the other team's service; enable outbound traffic to return data to the other team's service
1) Create a Security Group.
   Enable inbound connections from the other team. Enable outbound returning traffic to the other team's service


**Single choice**

50) Your company has an internal knowledge base which has large number of files. 1000s of new files are added to the knowledge base every week and once a month outdated files are removed.The total storage requirements for the knowledge base can vary greatly based on additions, removals and modifications of the files.The knowledge base is accessed via a web application which runs on multiple Amazon EC2 instances behind an application load balancer. Every EC2 instance needs to access all of the files.

What is the most suitable storage solution?

1) Amazon S3
1) Amazon FSx for Lustre
1) **Amazon EFS**
1) Amazon EBS




============================================== **EXAM 2** ==============================================

**Multiple Choice**

1) VPC Peering between two Amazon VPCs has just been activated and accepted. After that a solutions architect finds that they still have no communication between the workloads that are in both VPCs.
What additional step can help to provide effective communication between VPCs?

1) A Transit Gateway needs to be added between both VPCs to allow communication.
1) **Edit both route tables on the Amazon VPCs to add routes to the other VPC to which you want to connect.**
1) A Virtual Private Gateway needs to be added between both VPCs to allow communication.
1) Additional configurations need to be made directly in VPC Peering.


**Single choice**

2) A company is using AWS Lambda to process small number of images that are uploaded to Amazon S3. Suddenly, they uploaded a large number of image files (several thousands) in S3 bucket. As a result, an error was generated by AWS Lambda (status code 429).
What is the MOST likely cause of this error?

1) **The concurrency execution limit for the account has been exceeded.**
1) The event source mapping has not been configured.
1) AWS Lambda cannot process multiple files simultaneously
1) Amazon S3 could not handle the sudden burst in traffic.


**Single choice**

3) A customer has two AWS accounts. One of them is a devtest account used by their development and QA teams and the other one is a production account where currently all their production workloads are running. The customer has several Amazon VPCs in both the accounts. The customer is using Amazon Route 53 as DNS service in both of their AWS accounts and planning to have Private Hosted Zones created. The customer is looking for a solution with which they could have ease of management and efforts for the Private Hosted Zones.

Which of the following options has the least administrative efforts and ease of management for the customer to associate VPCs and Private Hosted Zones with Route 53 service?

1) Amazon VPCs from the different AWS account are associated by default with the Private Hosted Zone in the other account as both accounts belongs to the same customer.
1) Create Private Hosted Zones in both the AWS accounts separately and associate their respective Amazon VPCs with their corresponding Private Hosted Zones.
1) **Associate VPCs belonging to different accounts with a single hosted zone.**
1) Customer could write a script for the Amazon VPCs in one account to be associated with the Private Hosted Zone of the other AWS Account and host that script on AWS Lambda which can perform the job for the customer.

**Single choice**

4) A solutions architect must find the gateway that a database in an Amazon EC2 instance on a private subnet that can initiate a session to the internet, but must not allow a session from the internet to initiate back to the database.

What gateway is it recommended to use for this private subnet directly for this behavior for the Internet connectivity?

1) **NAT Gateway**
1) Transit Gateway
1) Virtual Private Gateway
1) Direct Connect Gatewa


**Multiple Choice**

6) Which of the following Amazon EBS data persistence statements are correct? (Select THREE)

1) **A non-root EBS volume persists, by default, on instance termination.**
1) Both root and non-root EBS volume data is persisted by default regardless of the EC2 instance state is started/stopped/terminated
1) **A non-root EBS volume "DeleteOnTermination" attribute is set to false, by default.**
1) **EBS volume's "DeleteOnTermination" attribute value can be changed while instance is running.**
1) A non-root EBS volume is deleted when an instance is rebooted.
1) EBS volume's "DeleteOnTermination" attribute value can only be set during EC2 instance creation and cannot be changed while instance is running.

**Single choice**

7) Over the past three months, AWS costs have been steadily rising. In an attempt to improve visibility and manage costs, the company wants to set up a system to send notifications if the current spending is over budget.

Which of the following services can help facilitate this process?

1) AWS Cost & Usage Report
1) AWS Billing console
1) **AWS Budgets**
1) AWS Cost Explorer

**Multiple Choice**

9) You can configure an application to use AWS Lambda ephemeral storage.
How can you configure storage between 512MB and 10,240MB, in 1MB increments? (Select TWO)

1) **AWS Lambda API**
1) **AWS Lambda console**
1) Amazon EventBridge
1) AWS Fargate

**Multiple Choice**

10) Your company has a private Amazon VPC in their AWS account that cannot be connected to the internet due to data sensitivity concerns. A solutions architect needs a way to interactively troubleshoot an Amazon EC2 Instance running in this VPC.

What should the solutions architect do in order to gain access to the Amazon EC2 instance, without provisioning any type of internet connectivity? (Select TWO)

1) **Attach an AWS IAM Instance Profile with the necessary permissions for AWS SSM Session Manager to the Amazon EC2 instance. Use AWS SSM Session Manager to access the Amazon EC2 Instance.**
1) Create an SSH key pair, use the key pair to SSH into the Amazon EC2 instance from their workstation.
1) **Create Amazon VPC Interface Endpoints for SSM, SSMMessages, and EC2Messages.**
1) Create an SSH key pair, use the SSH key pair to SSH into the AWS EC2 instance from AWS SSM Session Manager.
1) Create Amazon VPC Interface Endpoints for EC2, EC2Messages, and a VPC Gateway Endpoint for S3.


**Single choice**

11) You are in charge of securely managing Amazon S3 buckets on AWS. One bucket currently receives requests to read or write over the public internet. A potential risk exists where person in the middle attacks or eavesdropping attempts may occur.

Which of the following options below would address this risk regardless of where the request comes from?

1) Create an IAM User policy with a condition that will only allow users to upload or read from the designated bucket if as:SecureTransport is True.
1) **Create a bucket policy for the designated bucket and create a condition using as:SecureTransport to only allow encrypted connections over HTTPS.**
1) Create a SCP policy for the organization with a condition using as:SecureTransport to only allow encrypted connections over HTTPS.
1) Create a SCP policy for the organization with a condition to only write to the bucket if the data is encrypted.




**Single choice**

13) A customer wants to host their domain in AWS using Amazon Route 53 service. They plan to use Amazon CloudFront for distributing their website globally. All the static assets of the website will be served from Amazon S3 and Amazon EC2 will be used for serving the dynamic content via Amazon CloudFront. The customer needs a way to integrate Amazon Route 53 with AWS CloudFront and Amazon S3.

Which strategy would you recommend that is the easiest to configure?


1) Use an AWS Lambda function with API Gateway to redirect the API calls from Amazon Route53 to Amazon CloudFront and from there to Amazon S3 and Amazon EC2.
1) **It is possible to integrate Amazon Route53 with other AWS services like CloudFront and S3 via creating an alias record in Route 53 that points to CloudFront distributions and S3 buckets.**
1) It is possible, however, we need to insert the code for the integration of other AWS Services in our application which will be using Amazon Route 53.
1) They are integrated by default.

**Single choice**

14) Your team has an application that they would like to move to the cloud. The application and its logic are complex. It processes the departments accounting information and adjusts calculations in a stateful manner. As such, it needs to run for a large amount of compute time. The application runs long during the second and fourth week of the month to process additional payments. Because it is calculating many payments and makes requests to multiple external systems, it utilizes complex networking and needs access to the underlying files in the operating system to run.

Which compute option is best for this workload?

1) Rewrite the application to put part of the calculations into containers on an EKS cluster with AWS Fargate for the main application and scheduling
1) Rewrite the application into a Lambda serverless application. Lambda will automatically scale based on need for the second and fourth week of the month.
1) **Host the application on Amazon EC2 instances. Enable autoscaling for the EC2 instances when needed for the second and fourth week of the month.**
1) Put the application into a container. Containers are optimized for complex networking, and long compute times make sense for container workloads


**Single choice**

16) You have a large customer base spread across three geographic areasthe US East Coast, India and Western Europe. The high performance web application serving customers in three regions requires data with minimum latency and no downtime.

What would be the best way to fulfil this requirement?

1) **Use Amazon DynamoDB Global Tables.**
1) Amazon DynamoDB with provisioned capacity mode.
1) Amazon RDS with cross region replication.
1) Aurora DB with multi AZ enabled.


**Multiple Choice**

17)

You been asked to explore whether AWS Shield Advanced is the right solution to protect internet facing applications against Distributed Denial of Service (DDoS) attacks.

Which of the following is true for AWS Shield Advanced? (Select TWO)

1) It detects layers 1 thru 7  attacks, and mitigates layer 7 attacks.
1) **It mitigates against  layer 3, 4, and detects layer 7 attacks.**
1) It is available only to customers at the Business and Enterprise Premium support plans.
1) It is enabled automatically when you use select AWS services.
1) **It charges a monthly fee, plus a usage fee based on data transfer out from select services.**






**Single choice**

18) An IT organization is looking for a way to migrate their container workloads to the cloud to reduce administrative and maintenance tasks. Their Windows workloads are the highest priority to migrate onto AWS, and convenience and ease is the top priority to free up administrative time.

Which AWS managed service will meet your companys requirements?

1) Amazon ECS
1) AWS Lambda
1) **AWS Fargate**
1) Amazon EKS


**Single choice**

21) Your operational team wants to automate and centralize Amazon EBS volumes backup. You decided to use AWS Backup and created a backup plan based on a template provided by AWS Backup. Your operational team has now decided to configure a new custom Backup plan from scratch. You have to delete the backup plan.

What will happen if a backup plan is deleted?

1) **Existing Amazon EBS volumes backups are not deleted.**
1) Only unencrypted Amazon EBS volumes backups are deleted.
1) You need sign in as the root user to delete a backup plan once it is created.
1) Existing Amazon EBS volumes backups are also deleted.




**Single choice**

24) A highly regulated company has deployed their web application on AWS which comprises an Auto scaling group of Amazon EC2 instances, an Application Load Balancer and a PostgreSQL RDS instance. To ensure data confidentiality, you are tasked to validate that RDS can only be accessed using an instance profile for Amazon EC2 instance via authentication token.


How would you secure the solution to meet the above requirement?

1) Configure SSL in your application to encrypt the database connection to Amazon RDS.
1) Create an AWS IAM Role and assign it to your Amazon EC2 instance which will grant exclusive access to your Amazon RDS instance.
1) Use a combination of AWS IAM and STS to restrict access to your Amazon RDS instance via a temporary token.
1) **Enable the AWS IAM DB Authentication.**


**Single choice**

25) After a budget review, you have noticed your Amazon EBS charges make up a significant portion of your bill. Currently, all EBS volumes are in use and required to stay active. All unattached volumes have been deleted after creating snapshots. Snapshots are managed with lifecycle policies and a review has found no issue with retention.

Which of the following options will best help you to reduce your EBS spending?

1) **Review the Amazon EBS volume size to make sure you did not over provision EBS volumes.**
1) Generate snapshots of all volumes and only create and Amazon EBS volume when the data is requested.
1) Manually delete snapshots you are not currently using or anticipate using within the next year.
1) Detach the Amazon EBS volume from the Amazon EC2 instance. This will make sure you are not being charged unless you are using the EBS volume by attaching it to an EC2 instance.

**Multiple Choice**

26) Which of the following requirements must be met before you use Amazon S3 File Gateway? (Select TWO)

1) **Configure Microsoft Active Directory (AD).**
1) Configure Amazon Athena to count number of files transferred to Amazon S3 bucket.
1) **Configure your private networking, VPN, or AWS Direct Connect between your Amazon Virtual Private Cloud (Amazon VPC) and the on-premises environment where you are deploying your gateway.**
1) Make sure your gateway can resolve the name of your AWS IAM Identity Center.


**Single choice**

28) A company runs a batch application in the AWS Cloud hosted on 200+ Amazon EC2 instances. As a solutions architect, you are asked to push debug logs to an Amazon S3 bucket every 2:00 AM for all the EC2 instances.

What is the best possible solution from an operation point of view?

1) Use Systems Manager Distributor to transfer the logs every 2:00 AM on all the AWS Systems Manager Managed instances.
1) Use SSM Session Manager to run a shell script on all Amazon EC2 instances 2:00 AM in the morning.
1) **Create a schedule in AWS Systems Manager Maintenance window to move the logs to S3 bucket every 2:00 AM in the morning.**
1) Inject a user script via Ops Work to all of the Amazon EC2 instances that will push the logs to this Amazon S3 bucket.

**Multiple Choice**

32) A solutions architect needs to capture IP traffic logs going in and out of the network interfaces of the Amazon EC2 instances inside of an Amazon VPC. The records need to capture network internet protocol (IP) traffic flow transmitted by a 5-tuple. This information must be publishable in Amazon CloudWatch Logs.

What service function would you use to cover all the subnets that belong to the same VPC?

1) Network Access Analyzer
1) VPC Reachability Analyzer
1) VPC IP Address Manager (IPAM)
1) **VPC Flow Logs**

**Single choice**

36) A company currently stores critical data in Amazon S3. The customer wants a mechanism to recover individual objects to an earlier state due to overwrites.

Which of the following is the simplest way to recover the objects from overwrite?

1) Copy Amazon S3 objects periodically to Amazon Elastic Block Storage (EBS) volume as a backup.
1) Configure bucket policy (Permissions -> Bucket Policy) that will Deny s3:DeleteObject action.
1) Create a snapshot of the Amazon S3 bucket.
1) **Enable versioning for Amazon S3 buckets.**




**Single choice**

38) The data science team wants to efficiently run distributed training jobs using the latest Amazon EC2 GPU-powered instances, and deploy training and inferences using open source distribution, such as Kubeflow.
Which service is suitable for this use case?

1) AWS CodeBuild
1) **Amazon Elastic Kubernetes Service (EKS)**
1) AWS Fargate
1) AWS Elastic Beanstalk

**Multiple Choice**

41) You have to design a hybrid network architecture for an AWS Direct Connect link for connecting to a customer's on-premise site.
What gateways can you use to make this connection? (Select THREE)

1) Internet Gateway
1) **Transit Gateway**
1) NAT Gateway
1) **Virtual Private Gateway**
1) **Direct Connect Gateway**
1) Egress only Gateway




**Single choice**

42) Your company has an on-premises contact center. Your CTO is looking to migrate to the cloud to reduce operational workloads and costs.
Which AWS managed service will meet the companies requirements?

1) Amazon Chime
1) Alexa for business
1) Amazon Monitron
1) **Amazon Connect**

**Single choice**

44) For which of the following Amazon RDS database engines is the disk I/O activity suspended on the primary database during backup for a Multi-AZ deployment?

1) Oracle
1) MySQL
1) None. Backups are taken on the primary for Multi-AZ deployments
1) **SQL Server**


**Multiple Choice**

45) Which of the following is a serverless NoSQL database for applications that need high performance at any scale? (Select TWO)

1) **Amazon DocumentDB**
1) Amazon Aurora
1) Amazon ElastiCache
1) **Amazon DynamoDB**
1) Amazon RDS

**Single choice**

46) A solutions architect needs to choose a gateway to make a hybrid network connection between 3 Amazon VPCs and 1 AWS Site-to-Site VPN.
Which gateway could make these connections on the same gateway?

1) Virtual Private Gateway
1) **AWS Transit Gateway**
1) Internet Gateway
1) Direct Connect Gateway


Multiple Choice

47) As an AWS solutions architect, you've been asked to scale out write performance across multiple Availability Zones within an AWS Region. You've decided to deploy the Aurora Multi-Master.

Which of the following are features of an Amazon Aurora Multi-Master deployment option? (Select THREE)

1) **Supports up to four READ/WRITE nodes.**
1) **Available with Amazon Aurora MySQL-Compatible edition.**
1) Available with Amazon Aurora PostgreSQL-Compatible edition.
1) Features high availability with brief downtime during failover.
1) **Features continuous availability with no failover when a writer DB instance becomes unavailable.**
1) You can enable cross-Region replicas from multi-master clusters.
