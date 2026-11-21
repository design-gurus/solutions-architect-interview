# AWS vs. Azure vs. GCP: Service Translation Table

The three large cloud platforms offer the same building blocks under different names. A candidate who knows one platform can translate most designs to another with the table below. Interviewers at each company expect their own service names, each with a reason for the choice.

Providers rename services often. Check a name against the provider's documentation before an interview.

## Compute

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Virtual machines | EC2 | Virtual Machines | Compute Engine |
| Managed Kubernetes | EKS | AKS | GKE |
| Containers without servers to manage | Fargate | Container Apps | Cloud Run |
| Functions | Lambda | Azure Functions | Cloud Run functions |

## Storage

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Object storage | S3 | Blob Storage | Cloud Storage |
| Block storage (disks for servers) | EBS | Managed Disks | Persistent Disk |
| Shared file storage | EFS | Azure Files | Filestore |

## Databases

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Managed relational database | RDS, Aurora | Azure SQL Database | Cloud SQL, AlloyDB |
| Key-value and document database | DynamoDB | Cosmos DB | Firestore, Bigtable |
| In-memory cache | ElastiCache | Azure Cache for Redis | Memorystore |

## Networking

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Private network | VPC | Virtual Network | VPC |
| Load balancing | Elastic Load Balancing | Load Balancer, Application Gateway | Cloud Load Balancing |
| Content delivery network | CloudFront | Front Door | Cloud CDN |
| DNS | Route 53 | Azure DNS | Cloud DNS |
| Dedicated link to a data center | Direct Connect | ExpressRoute | Cloud Interconnect |

## Messaging

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Message queue | SQS | Service Bus | Pub/Sub |
| Publish and subscribe | SNS | Event Grid | Pub/Sub |
| Event streaming | Kinesis | Event Hubs | Pub/Sub |

## Identity and security

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Identity and access control | IAM | Microsoft Entra ID | IAM |
| Encryption keys | KMS | Key Vault | Cloud KMS |
| Secrets | Secrets Manager | Key Vault | Secret Manager |

## Analytics

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Data warehouse | Redshift | Synapse Analytics | BigQuery |
| Data pipelines | Glue | Data Factory | Dataflow |
| Monitoring | CloudWatch | Azure Monitor | Cloud Monitoring |

## AI

| Building block | AWS | Azure | Google Cloud |
|---|---|---|---|
| Access to foundation models | Bedrock | Azure OpenAI | Vertex AI |
| Machine learning platform | SageMaker | Azure Machine Learning | Vertex AI |

## Where the translation is not exact

The table maps names, not behavior. Four differences come up in interviews.

1. **Messaging on Google Cloud.** Pub/Sub covers the queue, the publish and subscribe service, and much of the streaming role. AWS and Azure use separate services for each.
2. **Identity on Azure.** Microsoft Entra ID manages users and sign-in. Permissions on resources are assigned through a separate role system. AWS and Google Cloud both call their permission system IAM, but the models differ.
3. **Networks on Google Cloud.** A Google Cloud VPC is global, with subnets in regions. An AWS VPC and an Azure Virtual Network each belong to one region.
4. **The warehouse on Google Cloud.** BigQuery has no cluster to size. Redshift and Synapse offer both sized and serverless forms.

## How to use the table in an interview

State the building block first, then the service, then the reason.

- **Weak:** "I would use DynamoDB."
- **Strong:** "The cart needs lookups by one key at a few thousand requests a second. A key-value database fits, which is DynamoDB here. The team also has nobody to run a database cluster."

The strong form still works if the candidate forgets a name. "A managed key-value database" is a complete answer, and the name is a detail.

## Go deeper

- [Grokking the Solutions Architect Interview](https://www.designgurus.io/course/grokking-the-solutions-architect-interview?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-aws-vs-azure-vs-gcp-services) has a cloud foundations chapter with a service mapping lesson and guidance on choosing compute, storage, databases, and networking.
- [Grokking System Design Fundamentals](https://www.designgurus.io/course/grokking-system-design-fundamentals?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-aws-vs-azure-vs-gcp-services) explains each building block independent of any vendor.
- Use the names in the [technical screen](../rounds/technical-screen.md).
- Free answer: [Cloud-based system design interview questions for AWS, Azure, and GCP](https://www.designgurus.io/answers/detail/cloud-based-system-design-interview-questions?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-aws-vs-azure-vs-gcp-services), design questions that use these services.
- Free answer: [How do you architect multi-cloud portability vs. lock-in?](https://www.designgurus.io/answers/detail/how-do-you-architect-multicloud-portability-vs-lockin?utm_source=github&utm_medium=repo&utm_campaign=solutions-architect-interview&utm_content=cheat-sheets-aws-vs-azure-vs-gcp-services), when a design should stay portable across providers.
