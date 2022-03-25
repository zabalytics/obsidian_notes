#  AWS Services
I'm just going over what AWS has to offer by reading through "AWS FOR BEGINNERS: THE COMPLETE BEGINNERS GUIDE TO LEARN AND UNDERSTAND AMAZON WEB SERVICES AND ITS FUTURE IN MODERN WORLD" 

## Why AWS?
  - Companies only pay for what they use. There is no need to forecast how much you will utilize and buy the equipment because you can scale as needed.
  - You are able to migrate your existing infrastructure easily over to the cloud
  - Security and reliability can be done by Amazon, so there is no need to waste resources on these tasks

## AWS best Practices
1. plan for failure
2. before using AWS services, decouple all of your components
3. Dynamic data should be kept closer to the computer, while static data should be kept closer to the user
4. understand the security and performance tradeoffs
5. the hourly payment mechanism is used to pay for computing capacity
6. develop a habit of paying a one-time fee for every instance you would like to reserve, and you will save a lot of money on the hourly rate

## Services
Below is a list of relevant AWS services and a quick summary of what that service does. I will expand on the services that I feel we will use more in other notes.

### Compute Services
1. __[[EC2 (Elastic Computing Cloud)]]__ - Cloud based virtual machine with complete control oer the operating system
2. __LightSail__ - Deploys and manages the storage computer, and Networking resources needed to execute your applications automatically
3. __Elastic Beanstalk__ - allows for the deployment and provisioning of resources such as a massively scalable production website in an automated manner
4. __Elastic Containers Service for Kubernetes (EKS)__ - helps you run Kubernetes on Amazon's cloud without needing to install anything
5. __AWS Lambda__ - allows users to run functions inside the cloud using this AWS service. This can ultimately save money because you only pay when the functions work

### Migration 
Data is physically transferred between your data center and AWS using migration services
1. __Database Migration Services (DMS)__ - can transfer on-premises databases to AWS. Also allows migrating from one type of database to another
2. __Server Migration Services (SMS)__ - Makes transfering on-premises servers to AWS rapid and straight forward
3. __Snowball__ - Permits you to move gigabytes of data inside and outside of the AWS environment

### Storage
1. __Amazon Glacier__ - provides secure and quick data archiving and backup storage
2. __Amazon Ebs Store (EBS)__ - storage service for Amazon EC2 instances that provides block-level storage
3. __AWS Storage Gateway__ - connects on-premises software applications to cloud-based storage via this AWS service. It enables secure communication between the company's on premises storage sy stem and AWS's storage architecture

### Services of Security
1. __Identify and Access Management (IAM)__ - helps manage users, set policies, and create groups to manage numerous users.
2. __Inspector__ - A security vulnerability detection agent you may deploy on your virtual machines
3. __Certificate Manager__ - provides free SSL certificates to Route53 managed domains
4. __Web Application Firewall (WAF)__ - protects applications at the application level, allowing you to prevent SQL injection and cross-site scripting threats
5. __Cloud Directory__ - Use this service to create customizable, cloud-native directories and managing data hierarchies across various dimensions
6. __Key Management Service (KMS)__ - enables you to manage your keys. Aids in the creation and management of encryption keys, allowing you to encrypt data
7. __Organizations__ - Service handles security and automation settings for groups of AWS accounts
8. __Shield__ - a DDoS protection system service. It protects web apps hosted on AWS
9. __Macie__ - It provides a data transparency solution that assists in classifying and protecting sensitive crucial content
10. __GuardDuty__ - protects AWS accounts & workloads by detecting threats

### Services for Databases
1. __Amazon RDS__ - Database service that makes it simple to set up, run, and scale a database system in the cloud
2. __Amazon DynamoDB__ - a managed service NoSQL database service from Amazon
3. __Amazon ElastiCache__ - cloud based web service which make it simple to create, manage, and grow in the memory cache
4. __Neptune__ is a data model sergvice that is quick, dependable, and scalable
5. __Amazon Redshift__ - a data warehousing service from Amazon that can be used to do complicated OLAP queries

### Services for Analytics
1. __Athena__ - analytics solution that allows you to find files using perm SQL queries in your S3 bucket
2. __CloudSearch__ - to construct a fully managed web browser for your website, use this AWS service
3. __ElasticSearch__ - a search engine that works similarly to CloudSearch but with additional functionality such as application monitoring
4. __Kinesis__ - service that enables you to stream and analyze real-time data at a large scale
5. __QuickSight__ - tool for analyzing company data. Allows you to generate data visualizations in AWS dashboard from S3, DynamoDB, and so on
6. __Elastic Map Reduce (EMR)__ - service mostly used for big data processing, such as Spark, Splunk, and Hadoop
7. __Data Pipeline__ - allows us t omove information from one point to another. For instance, moving over DynamoDB to S3

### Services for Management
1. __CloudWatch__ - allows you to keep track of AWS environments (i.e. EC2, RDS, and CPU usage) it also allows you to set alarms based on criteria
2. __CloudFormation__ - technique for converting infrastructure to the cloud
3. __CloudTrail__  provides a simple way to audit AWS resources. It assists you in keeping track of all changes
4. __OpsWorks__ - allows users to run Chef/Puppet in an AWS environment easily
5. __Configuration__ - AWS service keeps track of your environment. When users break certain defined configs, the program sends you an alert.
6. __AWS Auto Scaling__ - allows users to scale up and down their resources based on __CloudWatch__ measurements
7. __Manager of Systems__ - Use this AWS service to organize your resources. It enables you to spot problems and take action
8. __Managed Services__ - it manages your AWS infrastructure 
9. __Service Catalog__ - Large organizations can use this service to authorize which services will be used and which will not

### Services for Applications
1. __Step Functions__ - A way to see what is in the application and which microservices it is using
2. __Simple Workflow Service (SWF)__ - Service aids in the coordination of both automated and human-driven tasks
3. __Simple Notification Service (SNS)__ - Use this service to get email and SMS notifications depending on AWS services
4. __SQS (Simple Queuing Service)__ - Decouple your apps with this service. It works on a pull basis
5. __Elastic Transcoder__ - Service utility that allows you to modify the format and resolution of a video to support various devices such as tablets, smartphones, etc.

### Management and Deployment 
1. __AWS CloudTrail__ - monitors AWS API calls and sends you backlog files
2. __Amazon Cloudwatch__ - AWS resources, such as EC2 and RDS DB Servers, are monitored via Amazon CloudWatch. It also lets you keep track of custom metrics generated by users' apps and services
3. __AWS CloudHSM__ - Using Hardware Security Module (HSM) equipment inside the AWS environment, this solution allows you to meet corporate, regulatory, and contractual compliance needs for data security

### Tools for Developers
1. __CodeStar__ - used to create, manage, and collaborate on various software projects over AWS
2. __Code Commit__ - AWS version control tool
3. __CodeBuild__ - simplifies the process of compiling and building your code
4. __CodeDeploy__ - tool for automatically deploying your code to EC2 instances
5. __CodePipeline__ - aids in the creation of deployment pipeline that includes testing, building, authentication, and deployment in both dev and prod environments
6. __Cloud9__ - IDE in AWS

### Streaming from Desktop Apps
1. __Workspaces__ - virtual desktop infrastructure. Enables you to use cloud-based remote desktops
2. __AppStream__ - web-based method of delivering desktop programs to your consumers. (i.e. using MS word with google chrome)

### Artificial Intelligence
1. __Lex__ - platform to help you quickly create chatbots
2. __Polly__ - produce audio versions for your notes using text-to-speech tech
3. __Rekognition__ - face recognition service. Aids in recognizing faces and objects in photos and videos
4. __SageMaker__ - ML platform that helps develop, train, and deploy models at any scale
5. __Transcribe__ - speech-to-text service
6. __Translate__ - tool that works like google translate allowing you to translate text from one language to another

### Customer Interaction
1. __Amazon Connect__ - enables you to set up a customer service center in the cloud
2. __Pinpoint__ - tool that helps you understand and interact with your consumers
3. __Simple Email Service (SES)__ - assists in sending mass emails to customers
