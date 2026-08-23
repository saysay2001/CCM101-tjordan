# Checkpoint 4 – Research the Major Cloud Providers

## **Introduction**

Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP) are three of the leading public cloud providers. Although they use different names for their services, they provide similar infrastructure capabilities for computing, storage, networking, and identity and access management.

This comparison uses the official documentation of each cloud provider to identify equivalent services.

## **Cloud Infrastructure Service Comparison**

| **Infrastructure Component** | **Amazon Web Services (AWS)** | **Microsoft Azure** | **Google Cloud Platform (GCP)** |
|---|---|---|---|
| **Compute** | **Amazon EC2 (Elastic Compute Cloud)** – Provides scalable virtual servers for running applications and workloads. | **Azure Virtual Machines** – Provides scalable virtual machines for running applications and workloads. | **Compute Engine** – Provides scalable virtual machines running on Google's infrastructure. |
| **Storage** | **Amazon S3 (Simple Storage Service)** – Provides scalable object storage for storing and retrieving data. | **Azure Blob Storage** – Provides object storage for large amounts of unstructured data. | **Cloud Storage** – Provides scalable object storage using buckets for storing data. |
| **Networking** | **Amazon VPC (Virtual Private Cloud)** – Provides isolated virtual networks where AWS resources can be deployed using subnets, routing, and gateways. | **Azure Virtual Network (VNet)** – Provides private virtual networks with subnets, IP addressing, routing, and connectivity options. | **Virtual Private Cloud (VPC)** – Provides virtual networks, subnets, routes, and connectivity for Google Cloud resources. |
| **Identity and Access Management (IAM)** | **AWS IAM** – Controls access to AWS resources through users, groups, roles, and policies. | **Microsoft Entra ID + Azure RBAC** – Manages identities and controls access to Azure resources using roles and permissions. | **Cloud IAM** – Controls access to Google Cloud resources through identities, roles, and policies. |

## **Guide Questions**

### **1. Which cloud provider offers the broadest range of services? Explain your answer.**

**Amazon Web Services (AWS)** is generally recognized as offering the broadest range of cloud services among the three major providers. It provides services covering computing, storage, databases, networking, security, analytics, artificial intelligence, machine learning, IoT, serverless computing, and many other areas.

### **2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?**

I would recommend **Microsoft Azure** because it has strong integration with Microsoft's existing products and technologies. Organizations using Microsoft 365, Windows Server, SQL Server, and Microsoft Entra ID can benefit from Azure's integration with these services.

### **3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?**

**Google Cloud Platform (GCP)** is widely recognized for its strong AI, machine learning, and Kubernetes capabilities. Google developed Kubernetes and provides **Google Kubernetes Engine (GKE)**, along with various AI and ML services for developing and deploying intelligent applications.

### **4. What similarities did you observe among the three cloud providers?**

All three cloud providers offer equivalent fundamental infrastructure services, including virtual computing, cloud storage, networking, and identity and access management. Although their service names and specific features differ, their main purpose is to provide scalable, secure, and on-demand cloud infrastructure.

## **Conclusion**

AWS, Microsoft Azure, and Google Cloud Platform provide similar core infrastructure capabilities while using different service names and architectures. For example, **Amazon EC2, Azure Virtual Machines, and Google Compute Engine** all provide virtual computing resources, while **Amazon S3, Azure Blob Storage, and Google Cloud Storage** provide object storage.

Understanding equivalent services across cloud providers is important for cloud engineers because it makes it easier to work with different cloud platforms. The best provider for an organization depends on its existing technology ecosystem, requirements, budget, performance needs, and specialized services.

## **Official Documentation Sources**

### **Amazon Web Services (AWS)**

- Amazon EC2: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html
- Amazon S3: https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html
- Amazon VPC: https://docs.aws.amazon.com/vpc/
- AWS IAM: https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html

### **Microsoft Azure**

- Azure Virtual Machines: https://learn.microsoft.com/en-us/azure/virtual-machines/overview
- Azure Storage: https://learn.microsoft.com/en-us/azure/storage/
- Azure Virtual Network: https://learn.microsoft.com/en-us/azure/virtual-network/
- Azure RBAC: https://learn.microsoft.com/en-us/azure/role-based-access-control/overview
- Microsoft Entra ID: https://learn.microsoft.com/en-us/entra/identity/

### **Google Cloud Platform (GCP)**

- Compute Engine: https://cloud.google.com/compute/docs
- Cloud Storage: https://cloud.google.com/storage/docs
- Virtual Private Cloud: https://cloud.google.com/vpc/docs
- Cloud IAM: https://cloud.google.com/iam/docs

## **Summary**

| **Component** | **AWS** | **Microsoft Azure** | **Google Cloud** |
|---|---|---|---|
| **Compute** | Amazon EC2 | Azure Virtual Machines | Compute Engine |
| **Storage** | Amazon S3 | Azure Blob Storage | Cloud Storage |
| **Networking** | Amazon VPC | Azure Virtual Network | Google Cloud VPC |
| **IAM** | AWS IAM | Microsoft Entra ID / Azure RBAC | Cloud IAM |

The three providers follow the same fundamental cloud infrastructure concepts but implement them through different services and platforms. Learning these equivalents helps cloud engineers transfer their knowledge from one cloud provider to another.
