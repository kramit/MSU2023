Access reviews to an application to review permissions

SAS keys provide access for a specific time

AD application proxy puts AzureAD Authenication infont of old onsite applications

Dynamic groups/users are auto removed from groups

Databricks Premium does Cred Passthrough for access to Data Lake

Need to register an App to AzureAD before you can use it for authentication, conditional access can filter on differenet criteria, including if a computer is ADJoined (owned by the company)

IP Flow verify allows you to see if traffic can flow between resources / networks

Windows Logs = event log, linux log = syslog

Polcies assiged to management group,subscription or resource group

Application need to be an enterprise app for AD application proxy for use, conditional access can force MFA on for a conneciton

ARM deployment logs go into azure activity logs

AzureAD events can be sent to Event Hubs, which then are picked up by an Azure function to be written into a Cosmos DB

Azure API mangement can support 3rd party Oauth for HTTP calls to appliations/logic apps

System logs can be passed into a log analytics workspace (LAW) from an agent that has been installed inside the VM

PIM Privileged Identity Mangement can provide just in time access or access only for the time needed to do an admin task, it will log this information. An application that needs access to an Azure resouce need a Managed Identity, this is a 'User Account' for an application so you can assign it permissions to things

A single blueprint can be assigned to multiple loctions or subscriptions

The policy needs a modify effect to be able to makes changes or add something. to be able to this it also need a managed identity with a contributer role to have the permissions to make changes/remediate thing in the subscription

SQL Insights is a feature in Azure that provides comprehensive monitoring and diagnostics for Azure SQL databases. It collects and visualizes key performance metrics. They can be sent to a storage account, a log analytics workspace or an event hub for more proccessing

Dynamic data masking is for Personal information. Dynamic data masking is a security feature that hides sensitive data in your database from non-privileged users. It automatically replaces this sensitive data with "masked" data, which is a set of random characters or empty strings. This process is dynamic because the actual database data remains unchanged; it's only masked when presented to the user. It's used to protect confidential data, such as credit card numbers, social security numbers, or personal contact information, in scenarios where users need to access a database but not necessarily all the data within it.

Blobs support SAS keys and the ability to use customer managed encryption keys

Key valt references in the application settings of an app allows the app to talk to a key vault, the get permission is equivilent to a read permission for each key without the abilty to list all the keys in teh vault

A user assigned managed ID can be shared between multiple resources but a system assigned one is locked to the resource it came with

Azure Synapse link connects a Synapse Analytics instance to data in a Cosmos DB vis the the SQL API account

Log Analytics can store data for a max of 730 days, after this you must run an application/logic app, to extract the logs to an archivable format like CSV and save them in a storage account for long long term archiving

password-based SSO supports username and password

JIT is just in time access for virtual machines, Conditional access enforces MFA

Azure Polices can enforce tags

B2B authentication you can use guest accounts for the other company to access internal resources

Azure Active Directory (AD) Entitlement Management is a service that helps organizations manage identity and access lifecycle at scale, across various groups and applications. It simplifies access request workflows, access assignments, reviews, and expiration. With Azure AD Entitlement Management, organizations can create access packages defining a bundle of related resources (like groups, applications, SharePoint sites) and policies to govern who can access these resources, under what conditions, and when access should be revoked. It's designed to reduce the workload on IT teams and improve security by ensuring that only the right people have access to necessary resources for only the necessary amount of time.

A JSON Web Token (JWT) in the context of Azure APIs is a compact, URL-safe means of representing claims to be transferred between two parties. It's a type of token that's used to authenticate users on a web application. Azure APIs often use JWTs as part of the OAuth 2.0 protocol to secure the APIs.
When a user logs into a web application, a JWT can be created which includes a set of user attributes, or "claims," and an expiration. This token is then sent to the client and included in the HTTP header for subsequent API requests. The Azure API will validate the JWT signature and check the claims within it to authenticate the user before processing the request. The use of JWTs allows for stateless, secure access to Azure APIs.

AD entitement mangement can control the lifecyle of access to resources for internal or external users

An azure function that need to read logs needs permission to do so, this will be assigned based on the system-assigned managed identity of the function app

Azure entitlement management governes external users

Supported account types on the sign in endpoints of an app will provide access to an app from an external tenant

Access reviews can remove people from access if they do not responed to the request for the review

register an app in AD and delegate permissions to allow that add to perform actions

Contributer allows creation, permissions assigned to groups inherit through to groups below, only owners can change permissions

supported account typed for cross tenant authentication

entitlement management can govern external users

group things by tags for compliance reports

User admin role can create user accounts, helpdesk admin can reset passwords

API keys are text and therefore are stored as 'secrets' in a key vault and if access by an application that app need a managed identity

An azure monitor workspace can be used by multiple resources

***Case***

*Fabrikam, Inc. is an engineering company that has offices throughout Europe. The company has a main office in London and three branch offices
in Amsterdam, Berlin, and Rome.
*
- 1 tennant 2 access policies
- SQL migration NO xx Web Content NO xx metric monitoring YES
- Deploy domain controllers for corp to vnets in azure
- 1 tennant 1 custom domain 2 condtional acces policies
- Azure AD Connect Health
- Configure long-term retention policy for the database
- vCore SQL Database
- redundancy YES xx Autoscaling NO xx region fail NO

***Case***

SQL managed instance supports up to 4TB database

import/export service to move large data and then data factory to proccess that data and move it to store locations



Azure Service Bus is a cloud messaging service that connects applications, services, and devices in the cloud to enable reliable and secure asynchronous data and state transfer.

Azure Service Bus Queue: This is a basic message queue service that offers First In, First Out (FIFO) message delivery to one or more competing consumers. That means messages are received and processed by the receivers in the order they were added to the queue. This service is commonly used when you need to ensure the ordered processing of messages.
Azure Service Bus Topic: This is a more advanced publish/subscribe pattern. It enables you to send (publish) a message to a topic, and the message is then sent to all subscriptions to that topic. It's particularly useful in scenarios where multiple subscribers want to receive the same message independently. Each subscriber receives a copy of the message sent to the topic, allowing them to process the message independently from other subscribers.
In short, if you need one-to-one communication, you'd typically use a queue, while for one-to-many communications, you'd use a topic.


Block Blobs are for high transaction rate / frequently accessed data

Blob storage is for large unstructured data

elastic pools share sql resources with multiple databases that have different useage spikes

Hyperscale SQL databases support up to 100TB

Time series insights allows real time data analytics

Cosmos DB supports multi region writes and reads

Cannot send the audit logs cross region

Migrating SQL onsite-azure requires DMA data migration asisstant app, to migrate to cosmos DB you should use CosmosDB Migration Tool

Data factory can schedule move/upload of data from one place to another

Archive is cheapest tier and had a 4hour recovery time to get access to the data again

two databases on the same managed instnace can support server side transactions

Database Premium ha multiple live replicas and is cheaper than hyperscale

storage account resource lock to prevent data being modified

Data Lake is for massive data and Hyperscale is needed to proccess up to 100TB of database

Max Encryption key size is RSA 3072 for use with TDE transparrant datat encryption

IOT send data into event grid and real time analysis to be done by Time Series Insights

Synape Pools deticated to ingest data, and serverless to query to alow dynamic scale

Azure Data Lake is for big data, Hadoop is an open-source framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models, and uses HDFS hadoop file system

store images in blob and account data in a database like cosmos db

cosmosDB for noSQL supports multi master and SQL commands

burstable mysql is not right, it must be General Purpose for the high availability

Azure Cosmos DB offers various APIs for different data models. If you want to store and access data relationally while also supporting SQL queries and geo-replication, the PostgreSQL API would be the appropriate choice.

Avro data format is like JSON but better for many items of the same arrangement of data

Azure site recovery does a 15 min failover RTO recovery time objective as it is constantly backing up

36 months for policy backup and a 1 day RPO

Two machines in two regions with a traffic manager profile will provide redundency with 2 virtual machines that are running and indipendent .NET application

Premium file shares are fast and are supported up to ZRS for redundency, they do not support GRZ when running in premium for the extra speed

BlockBlob with Premium is fast and gen purposeV2 has the most features

Gen purpose v2 supports immutable storage (legal hold preventing hard deletion)

Front door supports SSl when used infront of an AKS cluster

Gen purpose storage supports storage tiers

Key vaults are redundent to a paired region by default and will fail over to the paired region, when running from the failover region you cannot modify data (delete data) until the original region is back online

Azure site recovery is for failing to a second on prem data center, Azure backup can archive data for a long time for finance or legal data, you can use both in the same solution at the same time


Azure SQL Managed Instance Business Critical provides a high-availability solution with several replicas in a separate cluster, and it uses the Always On technology, which guarantees no data loss during failover (a requirement in your case).
Business Critical tier also supports zone-redundant configuration, which ensures the database remains operational during a zone outage.
While Business Critical is not the cheapest option, it is the one that meets all the specified requirements. The Basic and General Purpose tiers do not offer the same high availability and zero data loss features. The Premium tier for Azure SQL Database does offer these, but it is generally more expensive than Managed Instance Business Critical. So, in terms of cost-efficiency while still meeting all requirements, Business Critical is the best option.
Azure SQL Database Premium tier provides a feature called "Active Geo-Replication" which allows you to configure up to four readable secondary databases in the same or different data center locations. This provides regional failover with no data loss.

In the event of a zone outage, you can manually failover to one of your secondary databases. Also, Azure SQL Database Premium supports Zone Redundant Configuration in regions that provide Availability Zones, further enhancing the high availability of the database.

While the Premium tier might have higher costs than Basic or General Purpose, it's the only option among the ones given that meets all the requirements of no data loss on failover and high availability in the event of a zone outage. Hyperscale is a great option for large databases, but it doesn't provide automatic failover with no data loss like the Premium tier does.


SQL serverless is the least costly option that provides a zone redundent configuration

In Azure SQL Database, you have options for both Active and Standard Geo-Replication to ensure business continuity in the event of a regional outage or disaster.

Active Geo-Replication: This is a high-availability feature that allows you to create up to four readable secondary replicas of your database in the same or different Azure region. The secondary replicas are always online and accessible for read operations, making this ideal for load balancing read-only traffic. In the event of a regional outage, you can manually failover to one of your secondary databases.

Standard Geo-Replication: This feature is available for databases in the Standard pricing tier. It provides geo-redundancy by creating a single secondary replica in a different region. However, unlike Active Geo-Replication, the secondary database created with Standard Geo-Replication is not readable and does not allow for load balancing of read operations. The secondary database only becomes available (for read and write operations) after failover.

Both Active and Standard Geo-Replication provide a recovery point objective (RPO) of less than five seconds, meaning minimal data loss in the event of a failover. However, the choice between them mainly depends on whether you need to balance read-only traffic across multiple regions (Active) or simply need a standby secondary database for disaster recovery (Standard).

Always On Availability Groups is a high-availability and disaster-recovery feature of Microsoft SQL Server that provides an enterprise-level alternative to database mirroring. It enables a failover environment for a set of user databases, known as availability databases.

This feature consists of two or more replicas that host a set of databases. One replica, the primary replica, serves the clients, while the other replicas, known as secondary replicas, are kept in sync with the primary replica. In the event of a failure, one of the secondary replicas automatically becomes the primary replica to minimize downtime.

In terms of Azure SQL, the Always On feature is available in the Business Critical tier for both Azure SQL Database and Azure SQL Managed Instance. This tier implements a technology similar to SQL Server Always On Availability Groups on the backend, providing automatic failover within the same Azure region and a high level of resilience to faults.

Remember, the actual term "Always On Availability Groups" is specific to SQL Server, while Azure SQL Database and Managed Instance use similar but not identical technology to provide the same high availability and fault tolerance.


Business Critical for redundency, always encrypted for specific columns that contain PII

Geo-redundent backupt for mySQL flex server for failover

Basic Azure Virtual WAN does not support express route

Azure function apps can run powershell code, logic apps will alow you to send and email and operate on a schedule or trigger

Azure AD domain services (AADDS) is on-site active directory (old LDAP) running in the cloud as a service

Function apps premium plan has the ability to communicate with a private IP

file share and file sync to centralise a file share distribution

on-prem data gateway will allow access to an isolated SQL server and connects to a connection gateway resource

VPN is not required for API access as it is exposed externally over the internet

application gateway is layer 7 and includes a web application firewall

Azure API management premium allows rate limitation of calls

app services can run .net apps and are cheaper than a scale set or a vm

Parent firewall policies are required to be in the same region as the child policies

vCore based can be serverless and only run at specific times

service bus is a queue service to allow asynchronous messages to communicate in XML 

Azure migrate tool can scan services on site to produce a report of what is on site to be migrated

CycleCloud manages HPC (high performance compute) clusters

Traffic manager does DNS load balancing redirection for high availability, with the setting of priority traffic routing it will auto fail over to an alternate location


***multi***
You need to design an access solution for the app. The solution must meet the following replication requirements:
- Support rate limiting.
- Balance requests between all instances.
- Ensure that users can access the app in the event of a regional outage

**front door**

***muti***

premium file shares for speed and GRS is the highest tier of redundency. A private endpoint will give the storage account an IP allowing communication contained entirely within the express route connection and not over the publuic internet.

Both Private Endpoint and Service Endpoint are networking features provided by Azure to secure your services. However, they operate differently:
Private Endpoint: This is a network interface that connects you privately and securely to a service powered by Azure Private Link. The private endpoint uses an IP address from your VNet address space, and it provides a secure connection between clients on your VNet and the Azure service, both situated on the Microsoft backbone network. Traffic between your VNet and the service travels over the Microsoft backbone network, eliminating exposure from the public Internet.
Service Endpoint: This extends your virtual network private address space and the identity of your VNet to the Azure services, over a direct connection. Endpoints allow you to secure your critical Azure service resources to only your virtual networks by whitelisting the VNet identity. Traffic from your VNet to the Azure service always remains on the Microsoft Azure network.

HTTP GET only is needed to read with no write operatios auth level need to be anon as people are accesing it publicly over the internet

Azure policys can restrict access to SKUs or deployment locations


A gateway subnet needs only a /27 at a minimum to work

Azure data factory transforms data for storage based on rules or pipelines that you create. It can transform the data automaticly as things are uploaded or moved into a storage location.

The AKS clustercan be scaled with a cluster autoscaler, the underlying compute power for an AKS cluster comes from an azure scale set

self hosted intergration runtime and a pipeline

In Azure Data Factory, a Self-hosted Integration Runtime is like a bridge. It's a tool you install in your local network (or on a virtual machine) that helps Azure connect to your local data.
It's used for three main things:
Moving data: It lets you transfer data securely between your local network and Azure.
Running tasks: It can manage tasks on machines in your local network or virtual network.
Running SSIS packages: If you're using SQL Server Integration Services (SSIS) packages to transform your data, a Self-hosted Integration Runtime can run those tasks in Azure.
So, if you have data in your local network that you want to move to Azure, or tasks that you want to run in Azure but manage locally, you would use a Self-hosted Integration Runtime.

virtual nodes : A Virtual Node in the context of Azure Kubernetes Service (AKS) is an add-on that enables Kubernetes nodes to be based on Azure Container Instances (ACI). It allows for rapid provisioning of pods, and enables Kubernetes clusters to burst and scale out quickly without the need for additional servers or infrastructure.




