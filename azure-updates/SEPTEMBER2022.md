# Azure Updates 09/2022 - Highlights

### Storage

Azure Storage lifecycle management offers a rule-based policy that you can use to transition blob data to the appropriate access tiers or to expire data at the end of the data lifecycle. You can configure rules to move a blob to archive tier based on last modified condition. If you rehydrate a blob by changing its tier, this rule may move the blob back to the archive tier. This can happen if the last modified time is beyond the threshold set for the policy. Now you can add a new condition, daysAfterLastTierChangeGreaterThan, in your rules, to skip the archiving action if the blobs are newly rehydrated.

[Documentation](https://azure.microsoft.com/updates/generally-available-prevent-a-lifecycle-management-policy-from-archiving-a-recently-rehydrated-blob/)

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

