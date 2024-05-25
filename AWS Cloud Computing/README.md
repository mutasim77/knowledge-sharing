<img width="100%" alt="banner" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/45788179-cb6b-4af4-a039-50f5d31fab31">

# AWS Cloud Computing Repository ☁️ 
Welcome to the AWS Cloud Computing Repository! This repository serves as a hub for information, guides,
and resources related to cloud computing with a focus on Amazon Web Services (AWS). Whether you're a beginner 
looking to explore cloud technologies or an experienced AWS user seeking advanced insights, this repository 
aims to provide valuable content and foster a collaborative learning environment.

## Table of Contents 📜
- [Introduction to Cloud Computing ☁️ ](#introduction-to-cloud-computing-)
- [Amazon Web Services 💎](#amazon-web-services-)
  - [AWS IAM 🔐](#aws-iam-)
  - [AWS Storage 🗄️](#aws-storage-)
  - [AWS Compute 💻](#aws-compute-)
  - [AWS Databases 🛢️](#aws-databases-)
  - [AWS Networking Services 🌐](#aws-networking-services-)
  - [Auto Scaling and Monitoring 🍟](#auto-scaling-and-monitoring-)

### Introduction to Cloud Computing ☁
![image](https://github.com/mutasim77/knowledge-sharing/assets/96326525/9b554614-3f33-4a83-b46b-f8745a356404)

#### What is Cloud Computing? 🤓
Cloud computing is like renting a computer, storage, or software over the internet instead of owning and maintaining your own physical hardware. Instead of running programs or storing data on your local computer, you can do it online through servers hosted by a third party.

#### Why Do We Need Cloud Computing? 👀
1. **Cost-Efficiency:** With cloud computing, you pay for what you use, avoiding the need to invest in expensive hardware upfront.
2. **Scalability:** It allows you to easily scale up or down based on your needs without the hassle of buying and installing new equipment.
3. **Accessibility:** You can access your data and applications from anywhere with an internet connection, making collaboration and remote work more efficient.
4. **Massive Economies of scale:** Because of aggregate usage from all customers, AWS can achieve higher economies of scale and pass savings on to customers.

#### Types of Cloud Computing ✨:
1. **Infrastructure as a Service (IaaS):** Provides virtualized computing resources over the internet. Users can rent virtual machines and storage.
2. **Platform as a Service (PaaS):** Offers a platform allowing customers to develop, run, and manage applications without dealing with the underlying infrastructure.
3. **Software as a Service (SaaS):** Delivers software applications over the internet, eliminating the need for users to install, maintain, and run the software.
<img width="944" alt="Screenshot 2024-01-31 at 7 12 08 AM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/05ccc209-77e5-4fb6-adba-4947d8ece333">


#### Types of Deployment Models 🪄:
1. **Public Cloud** ☁️:
  - **Explanation:** Imagine renting a virtual space on the internet. Many people, like you and others, share this space for various needs.
  - **Real-world Example:** Using Gmail or Google Drive, where you access and store your emails and documents on Google's servers that are shared with millions of users.

2. **Private Cloud** 🏠: 
  - **Explanation:** This is like having your own exclusive club. Everything is just for your use. It's more private and customizable.
  - **Real-world Example:** A company might have its own servers that only its employees can use for storing and accessing files.
   
3. **Hybrid Cloud** 🔄:
  - **Explanation:** Think of it as having a mix of both public and private spaces. Some things are shared with everyone, and some are just for your exclusive use.
  - **Real-world Example:** A business might use a public cloud for customer-facing apps and a private cloud for confidential business files.

4. **Community Cloud** 🏘️:
  - **Explanation:** It's like a shared neighborhood where certain houses (organizations) share common spaces. These houses have similar needs and work together.
  - **Real-world Example:** Different healthcare providers sharing a cloud platform for patient data exchange while ensuring privacy and compliance.

![image](https://github.com/mutasim77/knowledge-sharing/assets/96326525/a7c00828-503c-4c12-b3ba-b5dbd7a768f7)

#### Major Cloud Providers 💎:
1. **Amazon Web Services (AWS):** Offers a wide range of cloud services, including computing power, storage, and databases.
2. **Microsoft Azure:** Provides a variety of services, from computing to analytics and storage, integrated with Microsoft products.
3. **Google Cloud Platform (GCP):** Offers cloud computing, storage, and machine learning services, backed by Google's infrastructure.

![image](https://github.com/mutasim77/knowledge-sharing/assets/96326525/1c49ce7e-0f88-48aa-bc92-ce0da38190df)

> In summary, cloud computing is a flexible, cost-effective solution that allows individuals and businesses to access and use computing resources over the internet. It offers various services and deployment models to suit different needs, and major providers like AWS, Azure, and GCP make these resources easily accessible to a global audience.


## Amazon Web Services 💎
> Below, I'll provide some services and categories of AWS, but it's important to note that these are not the only ones available. AWS offers a wide range of services across various categories to cater to different business needs. The services mentioned here are just a subset of the comprehensive suite of solutions provided by AWS. Let's explore some of them below.

### What are Web Services ?
Web services are software systems designed to support interoperable machine-to-machine interaction over a network. In the context of AWS, they refer to cloud-based services accessible over the internet, providing computing power, storage, and other functionalities on-demand.

### Amazon Web Services Categories:
- **Storage Services 🗄️:**
<img width="600" alt="Screenshot 2024-02-08 at 2 12 34 PM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/2ee41109-f2b2-4aca-9c31-8429bbd1b071">

  - **Amazon S3 (Simple Storage Service):** Scalable object storage designed to store and retrieve any amount of data.
  - **Amazon EBS (Elastic Block Store):** Persistent block storage volumes for use with Amazon EC2 instances.
  - **Amazon EFS (Elastic File System):** Fully managed file storage for use with EC2 instances.
  - **Amazon Glacier:** Low-cost storage for data archival and long-term backup.

---

- **Compute Services 💻:**
<img width="600" alt="Screenshot 2024-02-08 at 2 12 21 PM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/295b954d-997b-422f-8797-89c900d33808">

  - **Amazon EC2 (Elastic Compute Cloud):** Scalable virtual servers in the cloud.
  - **AWS Lambda:** Serverless computing service for running code in response to events.
  - **Amazon ECS (Elastic Container Service):** Highly scalable container management service.
  - **Amazon EKS (Elastic Kubernetes Service):** Managed Kubernetes service for container orchestration.
  - **Amazon EC2 Auto Scaling:** Enables you to automatically add or remove EC2 instances according to conditions that you define.
  - **Amazon Elastic Container Registry (Amazon ECR):** A fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.
  - **AWS Elastic Beanstalkis:** A service for deploying and scaling web applications and services on familiar servers such as Apache and Microsoft Internet Information Services (IIS).
  - **AWS Fargate:** Serverless compute engine for containers.

---

- **Database Services🛢️ :**
<img width="600" alt="Screenshot 2024-02-08 at 2 11 57 PM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/c3b14fb3-73e7-49d5-a329-c02c10e3d41e">

  - **Amazon RDS (Relational Database Service):** Managed relational database service.
  - **Amazon Aurora:** High-performance relational database compatible with MySQL and PostgreSQL.
  - **Amazon Redshift:** Fully managed data warehouse service.
  - **Amazon DynamoDB:** A key-value and document database that delivers single-digit millisecond performance at any scale, with built-in security, backup and restore, and in-memory caching.

---

- **Networking Services: 🌐**
<img width="600" alt="Screenshot 2024-02-08 at 2 11 43 PM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/bc71e18e-b90a-4eb9-9c71-0cce55671bc5">

  - **Amazon VPC (Virtual Private Cloud):** Isolated cloud resources and customizable networking environment.
  - **Elastic Load Balancing:** Automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions.
  - **Amazon CloudFront:** Global content delivery network (CDN) service.
  - **AWS Transit Gateway:** Centrally manage and scale connectivity across VPCs and on-premises networks.
  - **Amazon Route 53:** Scalable DNS (Domain Name System) web service.
  - **AWS Direct Connect:** Dedicated network connection from on-premises to AWS.
  - **AWS VPN (Virtual Private Network):** Securely connect on-premises networks to AWS.

---
    
- **Security Services: 🔒**
<img width="600" alt="Screenshot 2024-02-08 at 2 11 30 PM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/bd317e57-a59e-4f4e-9cf9-ecab62645c9b">

  - **AWS IAM (Identity and Access Management):** Securely control access to AWS services and resources.
  - **AWS Organizations:** Allows you to restrict what services and actions are allowed in your accounts.
  - **Amazon Cognito:** Lets you add user sign-up, sign-in, and access control to your web and mobile apps.
  - **AWS Artifact:** Provides on-demand access to AWS security and compliance reports and select online agreements.
  - **AWS Key Management Service (AWS KMS):** Enables you to create and manage keys. You can use AWS KMS to control the use of encryption across a wide range of AWS services and in your applications.
  - **AWS Shield:** Managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS.

---
    
- **Cost Management Services: 💰**
<img width="600" alt="Screenshot 2024-02-08 at 2 13 06 PM" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/df2f8265-c07e-4f91-96ff-7f5cd6a8a403">

  - **AWS Cost and Usage Report:** Contains the most comprehensive set of AWS cost and usage data available, including additional metadata about AWS services, pricing, and reservations
  - **AWS Budgets:** Set custom cost and usage budgets.
  - **AWS Cost Explorer:** Visualize, understand, and manage AWS costs and usage.

---

- **Management and Governance Services: 🛠️**
<img width="600" alt="Management and Governance Services" src="https://github.com/mutasim77/knowledge-sharing/assets/96326525/9f83a9f4-f283-4907-b266-c2615bd734b5">

  - **AWS Management Console:** Provides a web-based user interface for accessing your AWS account.
  - **AWS Config:** Assess, audit, and evaluate the configuration of AWS resources.
  - **AWS CloudWatch:** Monitor and log AWS resources and applications.
  - **AWS Auto Scaling:** Provides features that allow you to scale multiple resources to meet demand.
  - **AWS Command Line Interface:** Provides a unified tool to manage AWS services.
  - **AWS Trusted Advisor:** Optimize AWS resources for performance, security, and cost-effectiveness.
  - **AWS Well-Architected Tool:** Review and improve your workloads based on AWS best practices.
  - **AWS CloudTrail:** Tracks user activity and API usage


## AWS IAM 🔐
Think of IAM as the security gatekeeper for your AWS account. It controls `who (users, groups, applications)` can do `what (actions)` and to `what (resources)`.

### Shared Responsibility Model 📜:
Imagine a pie cut in half.
- **AWS's half:** They manage the underlying infrastructure (hardware, software, facilities) and its security.
- **Your half:** You're responsible for securing your resources (data, applications, configurations) within the AWS account.

### Key Points 🔑:

1. **Shared responsibility:**
   - AWS takes care of the "cloud infrastructure," you manage your "stuff within the cloud."
2. **IAM helps you assign access securely:**
   - Create users, groups, and roles.
   - Define what each can do (permissions) and which resources they can access.
3. **Securing your account:**
   - Use strong passwords, rotate them regularly.
   - Enable multi-factor authentication (MFA) for extra security.
   - Monitor your account activity and investigate suspicious behavior.
  
> You and AWS are partners in securing your cloud environment. By understanding and managing your share of the responsibility, you can keep your data and applications safe.

## AWS Storage 🗄
Amazon offers several storage services that businesses and individuals can use to store their data securely and access it whenever they need to. Here are the main ones:

![AWS Storage](https://www.awsgeek.com/AWS-Storage-Gateway/AWS-Storage-Gateway.jpg)

### Amazon S3 (Simple Storage Service) 🦋:
  - Think of it as a big digital warehouse where you can store any type of data, like documents, images, or videos.
  - For example, if you have a website, you can store all your images and files on S3, so they're safe and easy to access.

### Amazon EBS (Elastic Block Store) 🦄:
  - It's like having a hard drive in the cloud. You can store data that you need to access quickly, like operating systems or database files.
  - Imagine you're running a website with a database. You can use EBS to store the database files securely and ensure quick access whenever someone visits your site.

### Amazon EFS (Elastic File System) 🐹:
  - This is like having a shared network drive in the cloud. Multiple users or systems can access the same files simultaneously.
  - For example, if you're working on a project with your team, you can store all project files in EFS, and everyone can access and work on them together from different locations.

### Amazon S3 Glacier 🐌:
  - It's a storage service for data that you don't need to access frequently but still want to keep for long-term storage.
  - Think of it as a vault for your digital files. For instance, you might use Glacier to store old backups or archives of your company's documents that you need to keep for legal reasons.

> Amazon storage services are like different types of storage units you can rent in the cloud. Depending on your needs, you can choose the one that best fits what you want to store and how you want to access it.

## AWS Compute 💻
Amazon provides various compute services that allow you to run your applications and processes in the cloud efficiently. Here are the main ones:

![AWS Compute](https://td-mainsite-cdn.tutorialsdojo.com/wp-content/uploads/2020/05/AWS-Compute-Overview.png)

### AWS EC2 (Elastic Compute Cloud) ⛅️:
- This is like renting virtual computers in the cloud. You can configure these instances with the exact amount of CPU, memory, and storage you need.
- For example, if you have a website, you can use EC2 to host it. You choose the instance type that suits your website's requirements, like how much traffic it gets and how much processing power it needs.

### Container Services 🫙:
Containers are like lightweight, portable packages that contain everything your application needs to run. ECS and EKS help you manage and orchestrate these containers at scale.

#### Amazon ECS (Elastic Container Service) 🔆:
- ECS is a fully managed container orchestration service that allows you to easily run, stop, and manage Docker containers on a cluster.
- With ECS, you can define your application as a collection of tasks and services, which are then scheduled and run on a cluster of EC2 instances or AWS Fargate.
- It provides features like automatic scaling, load balancing, and service discovery, making it easier to deploy and manage containerized applications at scale.
- For example, if you have a microservices architecture for your application, you can use ECS to deploy and manage each microservice as a separate container, ensuring efficient resource utilization and easy scalability.

#### Amazon EKS (Elastic Kubernetes Service) 〽️:
- EKS is a fully managed Kubernetes service that allows you to run Kubernetes clusters on AWS without the complexity of managing the underlying infrastructure.
- Kubernetes is an open-source container orchestration platform that automates the deployment, scaling, and management of containerized applications.
- With EKS, you can take advantage of Kubernetes' rich ecosystem of tools and resources, including support for advanced features like custom networking, storage, and security policies.
- It simplifies the process of running Kubernetes clusters by handling tasks such as cluster provisioning, upgrading, and patching, allowing you to focus on developing and deploying your applications.
- For example, if you have a large, complex application with multiple components that need to be deployed and managed across different environments, you can use EKS to orchestrate and scale these components efficiently, ensuring high availability and reliability.

### AWS Lambda 🐏:
- Lambda allows you to run code without provisioning or managing servers. You just upload your code, and Lambda takes care of running it whenever it's triggered.
- For instance, let's say you have a mobile app that needs to resize images when users upload them. Instead of setting up servers to handle this, you can use Lambda to automatically resize the images as soon as they're uploaded.

### AWS Elastic Beanstalk 🚸:
- This service makes it easy to deploy and manage your applications in the cloud without worrying about the underlying infrastructure.
- Think of it as a platform that handles all the heavy lifting of deploying, scaling, and monitoring your application. You just upload your code, and Elastic Beanstalk takes care of the rest.

> Amazon's compute services offer different ways to run your applications in the cloud, whether you need virtual machines, containers, serverless computing, or a managed platform for your apps. Each service caters to different needs and preferences, giving you flexibility and scalability for your projects.

## AWS Databases 🛢
Amazon offers a range of database services that cater to various needs, from traditional relational databases to NoSQL and data warehousing solutions. These services provide scalable, reliable, and managed database solutions for different types of applications and workloads.

### Amazon RDS (Relational Database Service) 🔗:
- RDS is a fully managed relational database service that supports popular database engines like MySQL, PostgreSQL, Oracle, SQL Server, and MariaDB.
- It simplifies database administration tasks such as provisioning, patching, backup, and scaling, allowing you to focus on developing your applications.
- For example, if you're building a web application that requires a relational database, you can use RDS to easily deploy and manage a MySQL or PostgreSQL database instance without worrying about server management.

### Amazon DynamoDB 🪄:
- DynamoDB is a fully managed NoSQL database service that offers low-latency, high-performance, and scalable storage for applications that require flexible data models.
- It provides features like automatic scaling, built-in security, and seamless integration with other AWS services, making it ideal for modern web and mobile applications.
- For instance, if you're developing a real-time analytics platform that needs to handle large volumes of data with low latency, you can use DynamoDB to store and query the data efficiently.

### Amazon Redshift 🐠:
- Redshift is a fully managed data warehousing service that allows you to analyze large datasets using SQL queries.
- It's optimized for data warehousing workloads, with features like columnar storage, parallel query execution, and advanced compression techniques for high performance and cost-effectiveness.
- For example, if you're running an e-commerce platform and need to analyze sales data to make business decisions, you can use Redshift to store and query terabytes of data quickly and cost-effectively.

### Amazon Aurora 🤓:
- Aurora is a fully managed relational database engine that is compatible with MySQL and PostgreSQL, offering the performance and availability of commercial databases at a fraction of the cost.
- It's designed for applications that require high throughput, low latency, and scalability, with features like automatic failover, continuous backup, and read scalability.
- For instance, if you're running a mission-critical application that requires high availability and scalability, you can use Aurora to achieve performance levels comparable to commercial databases like Oracle or SQL Server at a lower cost.

> Amazon's database services provide flexible and scalable solutions for various types of applications and workloads, enabling you to focus on building and scaling your applications without worrying about database management tasks. Whether you need a traditional relational database, a NoSQL database, or a data warehousing solution, Amazon has a service to meet your needs.


## AWS Networking Services 🌐
Amazon provides a comprehensive set of networking services to help you build a robust, scalable, and secure network infrastructure. These services enable you to connect your cloud resources, manage network traffic, and ensure the security and reliability of your applications.

### Amazon VPC (Virtual Private Cloud) 🛠️
- VPC allows you to create a logically isolated network in the AWS cloud.
- You have full control over your virtual networking environment, including IP address ranges, subnets, and routing tables.
- For example, you can use VPC to create a private network for your web application, separating public-facing servers from internal databases.

### Amazon CloudFront 🌍

## Auto Scaling and Monitoring 🍟
It's crucial to ensure that your applications are not only available but also responsive to changing demands. That's where Auto Scaling and Monitoring come into play.

**Auto Scaling 🎚️** allows you to automatically adjust the number of resources, such as compute instances, based on the workload. This means you can seamlessly handle fluctuations in traffic without manual intervention, ensuring your applications remain responsive and cost-efficient.

**Monitoring 📺** is the process of keeping an eye on the health, performance, and security of your AWS resources and applications. By collecting and analyzing data from various sources, you can gain valuable insights into how your systems are performing and detect any issues before they impact your users.

### Elastic Load Balancing 🧬
- Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses, to ensure optimal resource utilization and high availability.
- Think of it as a traffic cop for your applications. It monitors the health of your instances and redirects traffic away from unhealthy instances, ensuring that your application remains available and responsive.
- For example, if you have a web application hosted on multiple EC2 instances, ELB can evenly distribute incoming web requests to these instances, preventing any single instance from becoming overwhelmed with traffic.

### Amazon CloudWatch ⏰
- CloudWatch is a monitoring and observability service that provides real-time insights into the performance and health of your AWS resources and applications.
- It collects and tracks metrics, monitors logs and events, and sets alarms to notify you of any changes or issues in your environment.
- Imagine CloudWatch as a dashboard for your AWS services. It gives you visibility into how your resources are performing, allowing you to troubleshoot problems, optimize resource usage, and ensure the reliability of your applications.

### Amazon EC2 Auto Scaling 🍗
- EC2 Auto Scaling automatically adjusts the number of EC2 instances in your fleet based on demand, ensuring that you have the right amount of capacity to handle your workload at all times.
- It allows you to define scaling policies based on metrics like CPU utilization or request count, so your application can scale in or out dynamically in response to changes in traffic.
- Picture it as an elastic rubber band for your EC2 instances. When traffic increases, EC2 Auto Scaling adds more instances to handle the load, and when traffic decreases, it removes excess instances to save costs.

> Elastic Load Balancing, Amazon CloudWatch, and Amazon EC2 Auto Scaling work together to ensure that your applications are highly available, scalable, and performant in the AWS cloud. ELB distributes incoming traffic, CloudWatch monitors your resources and applications, and EC2 Auto Scaling automatically adjusts your capacity to match demand, providing a seamless and efficient experience for your users.
