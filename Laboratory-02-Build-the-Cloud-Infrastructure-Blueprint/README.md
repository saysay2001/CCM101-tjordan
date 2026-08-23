# Laboratory 2 – Cloud Infrastructure Fundamentals

## **Mission Overview**

This laboratory focuses on understanding the fundamental components of cloud infrastructure through hands-on activities using a Linux environment provided by KillerCoda.

The laboratory involved examining a virtualized Linux system, identifying its compute, storage, networking, and operating system components, researching equivalent services from major cloud providers, and designing a simple cloud infrastructure for a fictional company, **Aveiro Digital Solutions**.

The activities demonstrate how physical computing resources can be abstracted into virtual infrastructure commonly used in cloud computing.

## **Objectives**

The objectives of this laboratory are to:

1. Identify the major infrastructure components present in a Linux-based cloud environment.
2. Examine compute, storage, networking, and operating system resources using Linux commands.
3. Understand how virtualization is used to provide cloud computing resources.
4. Compare equivalent infrastructure services offered by AWS, Microsoft Azure, and Google Cloud Platform.
5. Design a simple cloud infrastructure based on the resources observed in the laboratory.
6. Develop practical Linux and cloud infrastructure management skills.
7. Document technical observations and findings using Markdown.

## **Cloud Infrastructure Components**

The following infrastructure components were identified from the KillerCoda Linux environment:

| **Component** | **Observed Resource** | **Details** |
|---|---|---|
| **Compute** | Virtual CPU and RAM | 1 CPU, 1 core, 1.9 GiB RAM |
| **Virtualization** | KVM | Full virtualization |
| **Storage** | `/dev/vda` | 20 GB virtual disk |
| **Main Filesystem** | `/dev/vda1` | 19 GB total, 5.4 GB used, 13 GB available |
| **Networking** | Private IP addresses | `172.30.1.2`, `172.17.0.1` |
| **Operating System** | Ubuntu Linux | Ubuntu 24.04.4 LTS |
| **Kernel** | Linux kernel | `6.8.0-138-generic` |

### **Compute Resources**

The environment provides **1 virtual CPU with 1 core** and approximately **1.9 GiB of RAM**. These resources are used to execute Linux processes, commands, applications, and services.

The system is running under **KVM full virtualization**, demonstrating how cloud platforms can provide virtual computing resources without requiring direct access to physical hardware.

### **Storage Resources**

The system contains a **20 GB virtual disk** identified as `/dev/vda`.

The primary root filesystem is `/dev/vda1`, which has approximately **19 GB of total capacity**, with **5.4 GB used** and approximately **13 GB available**.

### **Networking Resources**

The Linux environment has the following private IP addresses:

- `172.30.1.2`
- `172.17.0.1`

These addresses allow the virtual machine and its services to communicate within the virtualized networking environment.

### **Operating System**

The operating system is:

- **Ubuntu 24.04.4 LTS**
- **Codename:** Noble Numbat
- **Linux Kernel:** `6.8.0-138-generic`

The operating system manages the available compute, memory, storage, and networking resources and provides the environment where applications and services can run.

## **Tools Used**

The following tools and resources were used during the laboratory:

| **Tool / Resource** | **Purpose** |
|---|---|
| **KillerCoda** | Provided the cloud-based Linux laboratory environment |
| **Ubuntu Linux** | Operating system used for infrastructure observation |
| **Linux Terminal** | Used to execute system administration commands |
| **Draw.io** | Used to design the cloud infrastructure diagram |
| **GitHub** | Used to store and document laboratory outputs |
| **Markdown** | Used to create technical documentation files |
| **AWS Documentation** | Used to research AWS infrastructure services |
| **Microsoft Azure Documentation** | Used to research Azure infrastructure services |
| **Google Cloud Documentation** | Used to research Google Cloud infrastructure services |

## **Linux Commands Executed**

The following Linux commands were executed to inspect the infrastructure:

### **1. Operating System Information**

*cat /etc/os-release*

This command was used to identify the operating system and its version.

### **2. Linux Kernel Version**

*uname -r*

This command was used to identify the Linux kernel currently running on the system.

### **3. CPU and Virtualization Information**

*lscpu*

This command was used to inspect the CPU architecture, CPU count, cores, processor information, and virtualization details.

### **4. Number of Processing Units**

*nproc*

This command was used to determine the number of available processing units.

### **5. Memory Information**

*free -h*

This command was used to examine the available RAM and swap memory.

### **6. Block Storage Information**

*lsblk*

This command was used to identify the available storage devices, partitions, sizes, and mount points.

### **7. Filesystem Disk Usage**

*df -h*

This command was used to determine the amount of storage space currently being used and the amount available.

### **8. IP Address Information**

*hostname -I*

This command was used to identify the IP addresses assigned to the Linux environment.

### **9. Hostname**

*hostname*

This command was used to identify the hostname of the server.



## **Skills Learned**
Through this laboratory, several technical skills and cloud computing concepts were developed.

**Linux System Administration**

The laboratory provided hands-on experience using Linux commands to inspect system resources, including CPU, memory, storage, networking, and operating system information.

**Infrastructure Identification**

The activities improved the ability to identify the major components of cloud infrastructure and understand the purpose of each component.

**Virtualization**

The lscpu command revealed that the environment uses KVM full virtualization. This helped demonstrate how physical computing resources can be presented as virtual resources to users.

**Compute Resource Management**

The laboratory provided experience in identifying CPU cores, CPU architecture, RAM, and available processing resources using commands such as lscpu, nproc, and free.

**Storage Management**

Using lsblk and df -h provided practical experience in identifying disks, partitions, mount points, storage capacity, and filesystem usage.

**Networking**

The use of hostname -I demonstrated how to identify IP addresses assigned to a Linux environment and helped develop an understanding of virtual networking.

**Cloud Provider Comparison**

Researching AWS, Microsoft Azure, and Google Cloud Platform helped demonstrate that different cloud providers may use different names for services that perform similar infrastructure functions.

Examples include:
| **Infrastructure Component** | **AWS**    | **Microsoft Azure**             | **Google Cloud** |
| ---------------------------- | ---------- | ------------------------------- | ---------------- |
| **Compute**                  | Amazon EC2 | Azure Virtual Machines          | Compute Engine   |
| **Storage**                  | Amazon S3  | Azure Blob Storage              | Cloud Storage    |
| **Networking**               | Amazon VPC | Azure Virtual Network           | Google Cloud VPC |
| **IAM**                      | AWS IAM    | Microsoft Entra ID / Azure RBAC | Cloud IAM        |

**Cloud Architecture Design**

The laboratory also developed the ability to translate technical infrastructure observations into a simple cloud architecture. The proposed Aveiro Digital Solutions infrastructure connects a user through the Internet to a private virtual network containing a compute resource and storage resource.

**Technical Documentation**

Creating Markdown files and organizing laboratory results in GitHub improved the ability to document technical information in a structured and readable format.


## **Challenges Encountered**

One of the main challenges I encountered was **familiarizing myself with cloud infrastructure concepts**. At first, terms like compute, storage, networking, and virtualization were unfamiliar, but using the Linux environment helped me understand how these concepts work in an actual system.

Another challenge was **creating a cloud architecture from scratch**. It was difficult at first to decide how the user, Internet, network, compute, and storage should connect. Designing the infrastructure for **Aveiro Digital Solutions** helped me see how these components work together in a real-world company.

I also found it challenging to **understand the different services offered by AWS, Azure, and Google Cloud** because they use different names for similar services. Comparing them helped me understand that the important thing is knowing what a cloud service does, not just memorizing its name.

Overall, the laboratory challenged me to move from **simply knowing cloud concepts to actually applying them**. It helped me become more familiar with Linux, virtualization, cloud services, and basic cloud architecture.

