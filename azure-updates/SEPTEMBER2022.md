# Azure Updates 09/2022 - Highlights

### Storage

##### :flight_arrival: New Features

Azure Storage lifecycle management offers a rule-based policy that you can use to transition blob data to the appropriate access tiers or to expire data at the end of the data lifecycle. You can configure rules to move a blob to archive tier based on last modified condition. If you rehydrate a blob by changing its tier, this rule may move the blob back to the archive tier. This can happen if the last modified time is beyond the threshold set for the policy. Now you can add a new condition, daysAfterLastTierChangeGreaterThan, in your rules, to skip the archiving action if the blobs are newly rehydrated.

[Documentation](https://azure.microsoft.com/updates/generally-available-prevent-a-lifecycle-management-policy-from-archiving-a-recently-rehydrated-blob/)

### Virtual Machines

##### :boom: Preview

Ephemeral OS disk customers can choose encryption type between platform managed keys or customer managed keys for host-based encryption. The default is platform managed keys. This feature would enable our customers to meet your organization's compliance needs.

[Documentation](https://azure.microsoft.com/updates/public-preview-ephemeral-os-disks-supports-hostbased-encryption-using-customer-managed-key/)

### Storage

##### :dizzy: GA 

Resizing a disk on Azure can provide increased storage capacity and better performance for your applications. As part of our commitment to continuously add new capabilities to our Azure Disk Storage portfolio, live resize for Premium SSD and Standard SSD Disk Storage is now generally available.

With live resize, you can dynamically increase the storage capacity of your Premium SSD and Standard SSD disks without causing any disruption to your applications. To reduce costs, you can start with smaller disks and gradually increase their storage capacity without experiencing any downtime.

[Documentation](https://azure.microsoft.com/updates/generally-available-live-resize-for-premium-ssd-and-standard-ssd-disk-storage/)

### Monitor

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

### App Configuration

##### :boom: Preview

Azure Storage Explorer now offers an extension for Azure App Configuration–you can now work with Azure App Configuration resources under your Azure subscriptions directly in Storage Explorer. 

This means that with appropriate permissions,you can add, edit, or delete the key-values in your App Configuration store directly from the Storage Explorer.

[Documentation](https://azure.microsoft.com/updates/public-preview-azure-storage-explorer-support-for-azure-app-configuration-resources/)

### Functions

##### :dizzy: GA 

The Event Grid blob trigger handles events raised by a storage account and is now generally available.

The extension allows you to reduce latency by triggering on an event subscription to the same blob container. The event subscription uses Event Grid to forward changes in the blob container as events for your function to consume.

[Documentation](https://azure.microsoft.com/updates/generally-available-azure-functions-extension-for-event-grid-blob-trigger/)

### App Configuration

##### :boom: Preview

App Service and Azure Functions now support referencing configuration key-values from the Azure App Configuration service. App Configuration provides central management of configuration key-values that can span resources and deployment environments. When defining an application setting or connection string within App Service and Azure Functions, instead of providing a direct value, you can now specify a key-value in an external Azure App Configuration store. The app uses its managed identity to resolve the value from the store and expose it as an environment variable to your application.

This initial preview does not yet include support for network-restricted configuration stores or for resolution of configuration store references to Key Vault. Referenced key-values are not yet refreshed automatically, and new values will only be pulled in when the app restarts as the result of another config change such as modifying an app setting.

[Documentation](https://azure.microsoft.com/updates/public-preview-app-configuration-references-for-app-service-and-azure-functions/)

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

### API Management
##### :dizzy: GA 

Azure API Management support for the MSAL authorization library is now generally available.
You can provide a more secure OAuth 2.0 authorization code flow using PKCE when implementing user sign-in and sign-up actions 
in the developer portal through Azure Active Directory and Azure Active Directory B2C.

[Documentation](https://docs.microsoft.com/azure/api-management/api-management-howto-aad#migrate-to-msal)

---

### App Service

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

### Container Apps

##### :flight_arrival: Updated/New Features

Azure Container Apps (ACA) support for Dapr release 1.8.3 is now generally available.
All Container App Environments have been automatically upgraded to consume 1.8.3

[Dapr v1.8 release notes](https://github.com/dapr/dapr/releases/tag/v1.8.0)

[Documentation](https://docs.microsoft.com/azure/container-apps/dapr-overview?tabs=bicep1%2Cyaml)

---

### Data Explorer

##### :dizzy: GA

Azure Data Explorer (ADX) now supports ingesting data from S3 natively.

[Documentation](https://techcommunity.microsoft.com/t5/azure-data-explorer-blog/azure-data-explorer-supports-native-ingestion-from-amazon-s3/ba-p/3606746)

---

### Event Hub

##### :boom: Preview

Process your real time data streams in Azure Event Hubs using Azure Stream Analytics. 
The no code editor allows you to easily develop a Stream Analytics job without writing a single line of code. 
Within minutes, you candevelop and run a job that tackles many scenarios.

[Documentation](https://docs.microsoft.com/azure/stream-analytics/no-code-stream-processing)

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
 
---

### Azure Regions

##### :earth_africa: Region Updates

- 3 Availability Zones in UAE North
- New region: Qatar (with AZs)
              
[Documentation](https://news.microsoft.com/en-xm/2022/08/23/microsoft-launches-azure-availability-zones-to-heighten-competitiveness-of-uae-organizations)

[Azure Regions](https://azure.microsoft.com/global-infrastructure/geographies/#geographies)

---

