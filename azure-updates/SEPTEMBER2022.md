# Azure Updates 09/2022 - Highlights


### Microsoft DevBox

##### :boom: Preview

Microsoft Dev Box is now in public preview. Microsoft Dev Box provides self-service access for developers to high-performance, 
cloud-based workstations preconfigured and ready-to-code for specific projects—all while maintaining security and corporate governance.

With Microsoft Dev Box, organizations can:
- Maximize dev productivity with ready-to-code, self-service Dev Boxes.
- Centralize governance of workstations running anywhere to maintain greater security, compliance, and cost efficiency.
- Customize dev boxes with everything developers need for their current projects.

[Documentation](https://azure.microsoft.com/blog/announcing-microsoft-dev-box-preview)

---

### Storage

##### :flight_arrival: Updated/New Features

Azure Storage lifecycle management offers a rule-based policy that you can use to transition blob data to the appropriate access tiers or to expire data at the end of the data lifecycle. You can configure rules to move a blob to archive tier based on last modified condition. If you rehydrate a blob by changing its tier, this rule may move the blob back to the archive tier. This can happen if the last modified time is beyond the threshold set for the policy. Now you can add a new condition, daysAfterLastTierChangeGreaterThan, in your rules, to skip the archiving action if the blobs are newly rehydrated.

[Documentation](https://azure.microsoft.com/updates/generally-available-prevent-a-lifecycle-management-policy-from-archiving-a-recently-rehydrated-blob/)

+++

##### :dizzy: GA 

Resizing a disk on Azure can provide increased storage capacity and better performance for your applications. As part of our commitment to continuously add new capabilities to our Azure Disk Storage portfolio, live resize for Premium SSD and Standard SSD Disk Storage is now generally available.

With live resize, you can dynamically increase the storage capacity of your Premium SSD and Standard SSD disks without causing any disruption to your applications. To reduce costs, you can start with smaller disks and gradually increase their storage capacity without experiencing any downtime.

[Documentation](https://azure.microsoft.com/updates/generally-available-live-resize-for-premium-ssd-and-standard-ssd-disk-storage/)

+++

##### :boom: Preview

Today we are releasing the ability to encrypt storage account with customer-managed keys (CMK) using an Azure Key Vault hosted on a different Azure Active Directory tenant. You can use this solution to encrypt your customers’ data using an encryption key managed by your customers.

[Documentation](https://azure.microsoft.com/updates/public-preview-encrypt-storage-account-with-crosstenant-customer-managed-keys/)

---

### Virtual Machines

##### :boom: Preview

Ephemeral OS disk customers can choose encryption type between platform managed keys or customer managed keys for host-based encryption. The default is platform managed keys. This feature would enable our customers to meet your organization's compliance needs.

[Documentation](https://azure.microsoft.com/updates/public-preview-ephemeral-os-disks-supports-hostbased-encryption-using-customer-managed-key/)

+++

##### :dizzy: GA 

The general purpose Dps v5 and Dpds v5 Azure Virtual Machines series can run popular Linux enterprise workloads such as web and application servers, open-source databases, Java and .Net applications, gaming, and media servers, and more. The new VMs provide up to 4GiBs of memory per vCPU in sizes with up to 64 vCPUs, 208GiB of memory, and 40Gbps networking, with and without local temporary storage.

The Dpls v5 and Dplds v5 VM series offer one of the lowest starting price points within the general-purpose Azure Virtual Machines portfolio, providing 2GiBs per vCPU in sizes up to 64vCPUs, 128GiBs of memory, and up to 40Gbps networking with and without local temporary storage options.

Lastly, the memory optimized Eps v5 and Epds v5 VM series feature up to 8GiBs of memory per vCPU in sizes with up to 32 vCPUs, 208GiBs of memory, 40Gbps networking, with and without local temporary storage options, and are designed to meet the requirements associated with memory-intensive Linux-based workloads including open-source databases, in-memory caching applications, and data analytics engines. 

All the VM series listed above are now generally available in multiple regions and feature the Ampere Altra Arm-based processor operating at up to 3.0GHz frequency. The Altra Arm-based processor was architected for scale-out cloud environments to deliver efficient performance and help reduce overall environmental impact of computing operations.

[Documentation](https://azure.microsoft.com/updates/generally-available-new-azure-virtual-machines-with-ampere-altra-armbased-processors/)

---

### Monitor

##### :dizzy: GA 

As part of our continued commitment to open source solutions, we are announcing the general availability of Azure Managed Grafana, a managed service that enables you to run Grafana natively within the Azure cloud platform. With Azure Managed Grafana, you can seamlessly and securely connect with and scale to businesses’ existing Azure services, enhancing observability and cloud management.

In addition to the features announced during preview, with general availability, we’re introducing new capabilities that include the latest Grafana v9.0 features with its improved alerting experience as well as zone redundancy (in preview) and API key support.

[Documentation](https://azure.microsoft.com/blog/elevate-your-visualizations-with-azure-managed-grafana-now-generally-available/)

+++


##### :dizzy: GA 

Change analysis is an observability tool that enables efficient issue triaging and root causing by centrally showing changes inside and outside of Azure web applications. Built on top of Azure resource graph, the capability securely stores resource and application configuration change data with added role-based access control (RBAC) rules on viewing sensitive information. Change analysis supports scalable queries across multiple subscriptions.

Several key change analysis capabilities and integrations have been released into general availability (GA).

Fully integrated into the Azure Monitor portal as a key data source for observability
Performance and scalability improvement for large queries on change data
Simplified change data presentations aggregated by subscription and resource-groups
Single pane of glass observability by integrating with existing workflows and tools:
Diagnose and solve problems
Activity log change history
Metrics drill-into-changelogs
Azure workbook

[Documentation](https://azure.microsoft.com/updates/generally-available-enterpriseready-azure-monitor-change-analysis-capability-released/)

+++


##### :flight_arrival: Updated/New Features

You can configure data export rules in Azure Monitor Logs and export data for application insights tables, storage accounts, and event hubs. When linking multiple applications insights components to a workspace, data export applies to data coming from all linked applications.

[Documentation](https://azure.microsoft.com/updates/generally-available-azure-monitor-logs-data-export-supports-application-insights-tables-2/)

+++

##### :flight_arrival: Updated/New Features

Azure Monitor container insights allow you to monitor your container and Kubernetes workloads. When enabling container insights, Azure Monitor deploys a containerized collection agent. This agent is being renamed from OMSAgent to Azure Monitor agent. The current OMSAgent name is a legacy name from the OMS product and does not reflect the branding for Azure Monitor. The Azure Monitor agent is being standardized as the single collection agent for Azure Monitor. The name change brings the agent’s name in line with these updates.

The changes will roll out in early September. There are no feature updates or functional changes to the agent in this release. You will see a new pod name in your clusters. Alongside that, several other related resources have also been renamed. See the “List of renamed resources” and “List of renamed labels" tables in the linked blog post for more details. Customers who use the “omsagent” string in their alerts, queries, and script must update them to avoid any issues.

[Documentation](https://azure.microsoft.com/updates/generally-available-azure-monitor-container-insights-agent-renaming/)

+++

##### :boom: Preview

Container insights now supports integration with Azure Monitor agent for AKS clusters and Arc-enabled clusters. This integration is now generally available for Linux nodes in AKS and Arc-enabled clusters. This specialized agent collects performance and event data from all nodes in the cluster, and the agent is automatically deployed and registered with the specified log analytics workspace during deployment. 

With the Azure Monitor agent, container insights also supports authentication using managed identity for AKS and Arc-enabled clusters. This is a secure and simplified authentication model where the monitoring agent uses the cluster’s managed identity to send data to Azure Monitor. It replaces the existing legacy certificate-based local authentication and removes the requirement of adding a monitoring metrics publisher role to the cluster. System-assigned identity and user-assigned identity are supported.

[Documentation](https://azure.microsoft.com/updates/public-preview-use-managed-identitybased-authentication-to-enable-azure-monitor-container-insights/)

---

### Communications Services

##### :dizzy: GA 

Azure Communication Services now supports communication experiences for Teams identities. With this capability developers can build custom standalone applications that integrate audio, video, and telephony for Teams users. 

For example, developers can build specialized line of business applications that enable calling experiences for Teams users directly into the app, develop new workflows for apps that require custom management of incoming and outgoing Teams phone calls, or even bring Teams calling capabilities into devices that are not supported with the standard Teams client. 

With this functionality developers can now start creating custom apps that: 

Make and receive Teams calls as a Teams user
Join Teams meeting as a Teams user
Manage incoming and outgoing phone calls based on Teams Phone System and integration with Teams auto attendants and call queues
Honor assigned Teams user policies

[Documentation](https://azure.microsoft.com/updates/general-availability-azure-communication-services-support-for-teams-identities/)

---

### API Management

##### :flight_arrival: Updated/New Features 

Azure API Management support for custom widgets in the developer portal is now generally available. Custom widgets make it easier to integrate with external systems and they provide a different way to represent data (e.g., a modified API reference or user profile pages) in the developer portal.  

This release also enhances custom widget development by providing “scaffolding code" in Vue, React, and native TypeScript as well as an open source npm package - removing the need to write code from scratch.

Supporting these capabilities in the managed developer portal provides you with an alternative to maintaining self-hosted portals, while offering more advanced extensibility options and better manageability and source control than available previously through the “Custom HTML” widget.

[Documentation](https://azure.microsoft.com/updates/general-availability-azure-communication-services-support-for-teams-identities/)

+++

##### :dizzy: GA 

Azure API Management support for the MSAL authorization library is now generally available.
You can provide a more secure OAuth 2.0 authorization code flow using PKCE when implementing user sign-in and sign-up actions 
in the developer portal through Azure Active Directory and Azure Active Directory B2C.

[Documentation](https://docs.microsoft.com/azure/api-management/api-management-howto-aad#migrate-to-msal)

---

### App Services

##### :flight_arrival: Updated/New Features 

Enterprise-grade edge for Azure Static Web Apps is now generally available. Enable faster page loads, enhance security, and optimize reliability for your global applications. Enterprise-grade edge combines the capabilities of Azure Static Web Apps, Azure Front Door, and Azure Content Delivery Network (CDN) into a single secure cloud CDN platform.

Key features:

Global presence in 118+ edge locations across 100 metro cities
Caching assets at the edge
Proactive protection against Distributed Denial of Service (DDoS) attacks
Native support of end-to-end IPv6 connectivity and HTTP/2 protocol.
Optimized file compression.

[Documentation](https://azure.microsoft.com/updates/generally-available-enterprisegrade-edge-for-azure-static-web-apps/)

---

### App Configuration

##### :boom: Preview

Azure Storage Explorer now offers an extension for Azure App Configuration–you can now work with Azure App Configuration resources under your Azure subscriptions directly in Storage Explorer. 

This means that with appropriate permissions,you can add, edit, or delete the key-values in your App Configuration store directly from the Storage Explorer.

[Documentation](https://azure.microsoft.com/updates/public-preview-azure-storage-explorer-support-for-azure-app-configuration-resources/)

+++

##### :boom: Preview

App Service and Azure Functions now support referencing configuration key-values from the Azure App Configuration service. App Configuration provides central management of configuration key-values that can span resources and deployment environments. When defining an application setting or connection string within App Service and Azure Functions, instead of providing a direct value, you can now specify a key-value in an external Azure App Configuration store. The app uses its managed identity to resolve the value from the store and expose it as an environment variable to your application.

This initial preview does not yet include support for network-restricted configuration stores or for resolution of configuration store references to Key Vault. Referenced key-values are not yet refreshed automatically, and new values will only be pulled in when the app restarts as the result of another config change such as modifying an app setting.

[Documentation](https://azure.microsoft.com/updates/public-preview-app-configuration-references-for-app-service-and-azure-functions/)

##### :boom: Preview

Azure App Configuration now supports replicating your configuration data in the configuration store to replicas in other Azure regions. 
Available to standard tier subscribers, any updates or additions to key/values in the configuration store or in a replica will be automatically synchronized,
using an eventual consistency model.

This delivers benefits including:
 - Increased resiliency:
   Replication across regions means that your configuration data will still be accessible should a service outage impact your store or 
   any one of the replicas.
 - Minimize latency – Now your applications can consume the data locally rather than issuing cross-region requests.
 - Optimize request distribution – Replicas and the configuration store have unique applicable request limits,
   enabling you to distribute requests efficiently to avoid exhausting the request limits on either the replicas or the configuration store.

[Documentation](https://docs.microsoft.com/azure/azure-app-configuration/concept-geo-replication)

---

### Functions

##### :dizzy: GA 

The Event Grid blob trigger handles events raised by a storage account and is now generally available.

The extension allows you to reduce latency by triggering on an event subscription to the same blob container. The event subscription uses Event Grid to forward changes in the blob container as events for your function to consume.

[Documentation](https://azure.microsoft.com/updates/generally-available-azure-functions-extension-for-event-grid-blob-trigger/)

+++

##### :boom: Preview

Azure Functions support for Node.js 18 is now in public preview. This version of Node.js is supported by Functions runtime v4.x. 

Node.js 18 is currently in the initial release stage.

[Documentation](https://azure.microsoft.com/updates/public-preview-nodejs-18-in-azure-functions/)

---

### CosmosDB

##### :flight_arrival: Updated/New Features

Use Azure Cosmos DB integrated cache to optimize read costs and latency for both point reads and queries. The Azure Cosmos DB integrated cache is an in-memory cache built-in to the Azure Cosmos DB dedicated gateway. The dedicated gateway is optional front-end compute that stores cached data and routes requests to the backend database. There’s no need to make code changes in your application to use the dedicated gateway and utilize the integrated cache. Integrated cache is currently available for Core (SQL) API only.

[Documentation](https://azure.microsoft.com/updates/general-availability-azure-cosmos-db-integrated-cache/)

---

### Databricks

##### :flight_arrival: Updated/New Features

Unity Catalog is a unified and fine-grained governance solution for all data assets including files, tables, and machine learning models in your Lakehouse.  

Unity Catalog helps simplify security and governance of your data with the following key features: 

Define once, secure everywhere: Unity Catalog offers a single place to administer data access policies that apply across all workspaces and personas. 
Standards-compliant security model: Unity Catalog’s security model is based on standard ANSI SQL and allows administrators to grant permissions at the level of catalogs, databases (also called schemas), tables, and views in their existing data lake using familiar syntax. 
Built-in auditing: Unity Catalog automatically captures user-level audit logs that record access to your data

[Documentation](https://azure.microsoft.com/updates/generally-available-unity-catalog-for-azure-databricks/)

---

### SQL Database

##### :boom: Preview

In late August 2022, the following updates and enhancements were made to Azure SQL:

•	Enable automatic key rotation for Customer Managed Key in Azure SQL Database and Azure SQL Managed Instance.
•	Expand support to standard editions of SQL Server 2019 with link feature for Azure SQL Managed Instance.

[Documentation](https://azure.microsoft.com/updates/azure-sql-public-preview-updates-for-late-august-2022/)

+++

##### :dizzy: GA 

In late August 2022, the following updates and enhancements were made to Azure SQL: 

•	Leverage an assignment of a server or instance identity with user-assigned managed Identity in Azure Active Directory for Azure SQL Database and Managed Instance.
•	Increase resiliency of Azure SQL Database Hyperscale by enabling zone redundant configuration.

[Documentation](https://azure.microsoft.com/updates/azure-sql-general-availability-updates-for-late-august-2022/)

---

### Event Hub

##### :boom: Preview

Process your real time data streams in Azure Event Hubs using Azure Stream Analytics. The no code editor allows you to easily develop a Stream Analytics job without writing a single line of code. Within minutes, you can develop and run a job that tackles many scenarios.

There are four new features which will help you build and monitor your jobs:

Managed identity: You can now use ‘managed identity’ as authentication mode in Event Hub streaming input, Cosmos DB streaming output and Azure Data Lake Storage Gen2. Managed identities eliminate the limitations of user-based authentication methods, like the need to reauthenticate because of password changes or user token expirations that occur every 90 days.
Azure Data Lake StorageGen2 reference data: You can now use Azure Data Lake Storage Gen2 as reference data in the query. Reference data is either static or changes slowly over time. It is typically used to enrich incoming streaming and do lookups in your job.
Metrics: You can now monitor the health of your job by viewing metrics within no code editor. The metrics shown are for the last one hour by default. You can select any time ranging from last 1 hour to 30 hours to view metrics for the job.
Save job: You can now save your job anytime while creating it. For starting the job, you have to configure the Event Hub, transformations, and streaming outputs for the job.

[Documentation](https://azure.microsoft.com/updates/public-preview-4-new-features-in-no-code-editor-in-azure-event-hubs/)

+++

##### :boom: Preview

Process your real time data streams in Azure Event Hubs using Azure Stream Analytics. 
The no code editor allows you to easily develop a Stream Analytics job without writing a single line of code. 
Within minutes, you candevelop and run a job that tackles many scenarios.

[Documentation](https://docs.microsoft.com/azure/stream-analytics/no-code-stream-processing)

---

### Container Apps

##### :flight_arrival: Updated/New Features

Azure Container Apps (ACA) support for Dapr release 1.8.3 is now generally available.
All Container App Environments have been automatically upgraded to consume 1.8.3

[Dapr v1.8 release notes](https://github.com/dapr/dapr/releases/tag/v1.8.0)

[Documentation](https://docs.microsoft.com/azure/container-apps/dapr-overview?tabs=bicep1%2Cyaml)

---

### Data Explorer

##### :dizzy: GA

Azure Data Explorer (ADX) now supports ingesting data from S3 natively. Prior to the S3 ingestion support in Azure Data Explorer, you had to rely on complex ETL pipelines, or orchestrators to ingest data from S3. The new feature simplifies the process and allows data ingestion from S3 in a cost effective and scalable manner.

[Documentation](https://techcommunity.microsoft.com/t5/azure-data-explorer-blog/azure-data-explorer-supports-native-ingestion-from-amazon-s3/ba-p/3606746)

---

### AKS / Kubernetes Service

##### :dizzy: GA

AKS support for Kubernetes release 1.24 is now generally available. Kubernetes 1.24 delivers 46 enhancements.
This release includes new changes such as the removal of Dockershim.

[Documentation](https://kubernetes.io/blog/2022/04/07/upcoming-changes-in-kubernetes-1-24)

+++

##### :dizzy: GA

Azure Dedicated Host is a service that provides physical servers, able to host one or more virtual machines, 
dedicated to one Azure subscription. Dedicated hosts are the same physical servers used in our data centers,
provided as a resource.
You can provision dedicated hosts within a region, availability zone, and fault domain. 
Then, you can place AKS VMs directly into your provisioned hosts, in whatever configuration best meets your needs.

Using Azure Dedicated Hosts for nodes with your AKS cluster enables:
- Hardware isolation at the physical server level. No other VMs will be placed on your hosts.
- Control over maintenance events initiated by the Azure platform. 
- With dedicated hosts, you can opt-in to a maintenance window to reduce the impact to your service.

[Documentation](https://docs.microsoft.com/azure/aks/use-azure-dedicated-hosts)

+++

##### :flight_arrival: Updated/New Features

AKS now supports key management system (KMS) plugin integration. 
This generally available capability enables encryption at rest of your Kubernetes data in etcd using Azure Key Vault. 
This means you can now store secrets in bring your own key (BYOK) encrypted etcd using KMS.

Features:  
- Use a key in Key Vault for etcd encryption
- Bring your own keys
- Provide encryption at rest for secrets stored in etcd

[Documentation](https://docs.microsoft.com/azure/aks/use-kms-etcd-encryption)

+++

##### :boom: Preview

Automated deployments simplify the process of setting up a GitHub Action and creating an automated workflow for your code releases to your Azure Kubernetes Service (AKS) cluster. Once connected, every new commit will kick off the workflow, resulting in your application being updated.

[Documentation](https://azure.microsoft.com/updates/public-preview-automated-deployments-in-aks/)

+++

##### :boom: Preview

Azure offers a unique capability of mounting Blob Storage (or object storage) as a file system to a Kubernetes pod or application using BlobFuse or NFS 3.0 options. This allows you to use blob storage with a number of stateful Kubernetes applications including HPC, Analytics, image processing, and audio or video streaming. Not only that, if your application ingests data into Data Lake storage on Azure Blobs, you can now directly mount and use it with AKS. Previously, you had to manually install and manage the lifecycle of the open-source Azure Blob CSI driver including deployment, versioning, and upgrades. 

With this preview, you can use the Azure Blob CSI driver as a managed addon in AKS with built in storage classes for NFS and BlobFuse, reducing the operational overhead and maximizing time to value.

[Documentation](https://azure.microsoft.com/updates/public-preview-blob-csi-support-in-aks-2/)

 +++

##### :flight_arrival: Updated/New Features

AKS now supports key management system (KMS) plugin integration. This generally available capability enables encryption at rest of your Kubernetes data in etcd using Azure Key Vault. This means you can now store secrets in bring your own key (BYOK) encrypted etcd using KMS.

From the Kubernetes documentation on Encrypting Secret Data at Rest:

KMS plugin for Key Vault is the recommended choice for using a third-party tool for key management. KMS plugin simplifies key rotation, with a new data encryption key (DEK) generated for each encryption, and key encryption key (KEK) rotation controlled by the user.

Features:

Use a key in Key Vault for etcd encryption
Bring your own keys
Provide encryption at rest for secrets stored in etcd
 
 [Documentation](https://azure.microsoft.com/updates/generally-available-key-management-system-integration-with-aks/)
 
 +++
  
  ##### :dizzy: GA
  
Azure Dedicated Host is a service that provides physical servers, able to host one or more virtual machines, dedicated to one Azure subscription. Dedicated hosts are the same physical servers used in our data centers, provided as a resource. 

You can provision dedicated hosts within a region, availability zone, and fault domain. Then, you can place AKS VMs directly into your provisioned hosts, in whatever configuration best meets your needs.  

Using Azure Dedicated Hosts for nodes with your AKS cluster enables:

Hardware isolation at the physical server level. No other VMs will be placed on your hosts. 
Control over maintenance events initiated by the Azure platform. With dedicated hosts, you can opt-in to a maintenance window to reduce the impact to your service.

[Documentation](https://azure.microsoft.com/updates/generally-available-azure-dedicated-host-support/)

 +++
  
  ##### :dizzy: GA
    
AKS support for Kubernetes release 1.24 is now generally available. Kubernetes 1.24 delivers 46 enhancements. This release includes new changes such as the removal of Dockershim.  

[Documentation](https://azure.microsoft.com/updates/generally-available-kubernetes-124-support/)

 +++
 
##### :boom: Preview 

The AKS DevX extension for Visual Studio Code is in public preview. This extension enhances your day-to-day life as a developer on Azure Kubernetes Service and is focused on non-cluster developer experiences. 

The first feature to be added to the DevX extension is Draft, allowing you to create Dockerfiles, deployment files, and GitHub Actions easily through Visual Studio Code.

[Documentation](https://azure.microsoft.com/updates/public-preview-aks-devx-extension-for-visual-studio-code/)

---

### Virtual Network
##### :flight_arrival: Updated/New Features

Network security groups (NSGs) support for private endpoints is now generally available. This feature enhancement provides you with the ability to enable advanced security controls on traffic destined to a private endpoint. In order to leverage this feature, you will need to set a specific subnet level property, called PrivateEndpointNetworkPolicies, to enabled on the subnet containing private endpoint resources.

At this time, Private Link network security group support is available in most public regions.

[Documentation](https://azure.microsoft.com/updates/general-availability-of-network-security-groups-support-for-private-endpoints/)

---

### Load Testing
##### :boom: Preview

Azure Load Testing now supports load testing for private endpoints. You can create an Azure Load Testing resource and enable it to generate load from within your virtual network (VNET injection).

This functionality enables the following usage scenarios:

Generate load to an endpoint that is deployed in an Azure virtual network
Generate load to a public endpoint with access restrictions, such as restricting client IP addresses
Generate load to an on-premises service, not publicly accessible, that is connected to Azure via ExpressRoute
This functionality is available in the following Azure regions: Australia East, East US, East US 2, and North Europe. This will soon be available in South Central US and West US 2.

[Documentation](https://azure.microsoft.com/updates/public-preview-microsoft-azure-load-testing-supports-private-endpoints-testing/)
 
---

### Machine Learning
##### :flight_arrival: Updated/New Features

Hierarchical forecasting eliminates the need for you to manually create individual models to produce forecasts for your hierarchy data, aiming to generate hierarchy-aware and consistent forecasts at all levels of your hierarchy.

[Documentation](https://azure.microsoft.com/updates/generally-available-hierarchical-forecasting-for-azure-machine-learning/)


+++

##### :boom: Preview

AutoML Code Generation is now available for all 10 AutoML tasks across tabular, images & text data. This feature makes AutoML a transparent solution by allowing you to select any AutoML-trained model and generate the Python training code to explore, customize, and retrain before deploying.

AutoML in Pipelines Allows you to utilize the full power of AutoML in your MLOps process.  You can prep data, funnel it into AutoML, register the resulting best model, and set up an endpoint for scoring all within one pipeline.

[Documentation](https://azure.microsoft.com/updates/azure-machine-learning-public-preview-updates-for-august-2022/)

---

### Database for MySQL
##### :flight_arrival: Updated/New Features

 Use server logs for Azure Database for MySQL - Flexible Server to enable logging for your server and save the results to a file. If you enable server logs and select the log type, you can download the logs from your server. Use the information in these logs to get detailed insights about the activities executed on your server, and then identify and troubleshoot potential issues.
 
[Documentation](https://azure.microsoft.com/updates/general-availability-server-logs-for-azure-database-for-mysql-flexible-server/)

---

### Redis Cache
##### :moneybag: Pricing Updates

Save up to 55 percent on your usage of the Enterprise and Enterprise Flash tiers of Azure Cache for Redis by purchasing reserved instances. The reservation discount will automatically apply to your matching cache resources so the process of purchasing a reservation is streamlined. Reservations are available on a one-year basis for up to a 35 percent discount or on a three-year basis for a 55 percent discount. This is a great way to maximize the cost efficiency of your Azure deployment and ensure you get the best deal.

[Documentation](https://azure.microsoft.com/updates/general-availability-reserved-instance-pricing-for-azure-cache-for-redis-enterprise/)

---

### Azure Regions
##### :earth_africa: Region Updates

- 3 Availability Zones in UAE North
- New region: Qatar (with AZs)
              
[Documentation](https://news.microsoft.com/en-xm/2022/08/23/microsoft-launches-azure-availability-zones-to-heighten-competitiveness-of-uae-organizations)

[Azure Regions](https://azure.microsoft.com/global-infrastructure/geographies/#geographies)

---



