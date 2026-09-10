# Laboratory Activity 3 – Become a Multi-Cloud Explorer

## Overview

This laboratory activity explores and compares the three major public cloud platforms:

* Amazon Web Services (AWS)
* Microsoft Azure
* Google Cloud Platform (GCP)

The activity focuses on identifying core cloud services, comparing cloud providers, analyzing business requirements, and recommending appropriate cloud solutions.

## Objectives

* Explore AWS, Microsoft Azure, and Google Cloud Platform.
* Identify core services offered by each cloud provider.
* Compare cloud services across providers.
* Analyze different business requirements.
* Recommend appropriate cloud solutions.
* Document findings using Markdown.

---

# Linux Server Investigation

For this checkpoint, a **KillerCoda Playground** was used to investigate a Linux server environment. Linux commands were executed to identify the operating system, CPU information, memory, and available disk space.

The information collected can help determine the appropriate cloud computing resources if the Linux server is migrated to a cloud platform.

---

## Linux Commands Used

### 1. Operating System

The following command was used to identify the operating system and kernel information:

```bash
uname -a
```

### 2. CPU Information

The following command was used to identify the CPU configuration:

```bash
lscpu
```

### 3. Memory

The following command was used to check the server's memory:

```bash
free -h
```

### 4. Disk Space

The following command was used to check the available disk space:

```bash
df -h
```

---

# Linux Investigation Results

The following table summarizes the information collected from the KillerCoda Playground.

| Information          | Command Used | Result                                                                                        |
| -------------------- | ------------ | --------------------------------------------------------------------------------------------- |
| **Operating System** | `uname -a`   | Ubuntu Linux, kernel 6.8.0-138-generic, x86_64 architecture                                   |
| **CPU Information**  | `lscpu`      | 1 CPU, 1 core, 1 thread, Intel Xeon E312xx (Sandy Bridge, IBRS update), approximately 2.0 GHz |
| **Memory**           | `free -h`    | 1.9 GiB total RAM, 412 MiB used, 867 MiB free, 1.5 GiB available, 1.0 GiB swap                |
| **Disk Space**       | `df -h`      | Root filesystem `/dev/vda1`: 19 GB total, 5.4 GB used, 13 GB available, 30% used              |

---

## Detailed Linux Results

### Operating System

The KillerCoda Playground is running **Ubuntu Linux** with the following information:

* **Hostname:** ubuntu
* **Kernel:** 6.8.0-138-generic
* **Architecture:** x86_64
* **Kernel Build:** #138-Ubuntu SMP PREEMPT_DYNAMIC
* **Kernel Build Date:** July 31, 2026

The system is running a 64-bit x86 Linux environment.

### CPU Information

The CPU information collected using `lscpu` shows:

* **Architecture:** x86_64
* **CPU(s):** 1
* **CPU Mode:** 32-bit and 64-bit
* **Vendor:** GenuineIntel
* **Model Name:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
* **CPU Family:** 6
* **Model:** 42
* **Socket(s):** 1
* **Core(s) per Socket:** 1
* **Thread(s) per Core:** 1
* **Approximate CPU Speed:** 2.0 GHz
* **Hypervisor:** KVM
* **Virtualization Type:** Full

This indicates that the KillerCoda Playground is a virtualized Linux server with **one virtual CPU core**.

### Memory Information

The `free -h` command reported the following:

| Memory Information |   Value |
| ------------------ | ------: |
| **Total RAM**      | 1.9 GiB |
| **Used RAM**       | 412 MiB |
| **Free RAM**       | 867 MiB |
| **Shared RAM**     | 1.1 MiB |
| **Buffer/Cache**   | 791 MiB |
| **Available RAM**  | 1.5 GiB |
| **Total Swap**     | 1.0 GiB |
| **Used Swap**      |     0 B |
| **Free Swap**      | 1.0 GiB |

The server has **1.9 GiB of total RAM**, with approximately **1.5 GiB available** at the time of investigation.

### Disk Space Information

The `df -h` command reported the following:

| Filesystem   | Size | Used | Available | Usage | Mount Point |
| ------------ | ---: | ---: | --------: | ----: | ----------- |
| `tmpfs`      | 191M | 996K |      190M |    1% | `/run`      |
| `/dev/vda1`  |  19G | 5.4G |       13G |   30% | `/`         |
| `tmpfs`      | 952M |  84K |      952M |    1% | `/dev/shm`  |
| `tmpfs`      | 5.0M |    0 |      5.0M |    0% | `/run/lock` |
| `/dev/vda16` | 881M | 117M |      703M |   15% | `/boot`     |
| `/dev/vda15` | 105M | 6.2M |       99M |    6% | `/boot/efi` |

The main root filesystem is `/dev/vda1`, which has **19 GB of total storage**, **5.4 GB used**, and **13 GB available**.

---

# Cloud Migration Analysis

If this Linux server were migrated to the cloud, it could be hosted using virtual machine services provided by AWS, Microsoft Azure, or Google Cloud Platform.

Based on the investigation, the server currently has approximately:

* **Operating System:** Ubuntu Linux
* **Architecture:** x86_64
* **CPU:** 1 virtual CPU core
* **Memory:** 1.9 GiB RAM
* **Root Storage:** 19 GB
* **Available Root Storage:** 13 GB

The cloud virtual machine selected should provide resources that are at least comparable to the current server.

---

## AWS

The equivalent AWS service is **Amazon Elastic Compute Cloud (Amazon EC2)**.

Amazon EC2 provides virtual servers that can run Linux operating systems. CPU, memory, storage, and networking resources can be configured according to the requirements of the workload.

### Possible AWS Service

* **Amazon EC2** – Hosts the Linux server as a cloud-based virtual machine.
* **Amazon EBS** – Provides persistent block storage for the Linux server.

A suitable starting configuration would provide at least **1 vCPU and approximately 2 GiB of memory**, with at least **20 GB of storage** to accommodate the current disk requirement and future growth.

---

## Microsoft Azure

The equivalent Microsoft Azure service is **Azure Virtual Machines**.

Azure Virtual Machines allows organizations to deploy Linux-based virtual machines in the cloud. The virtual machine can be configured with the required CPU, memory, storage, networking, and operating system.

### Possible Azure Service

* **Azure Virtual Machines** – Hosts the Linux server as a cloud-based virtual machine.
* **Azure Managed Disks** – Provides persistent storage for the virtual machine.

A suitable starting configuration would provide at least **1 vCPU and approximately 2 GiB of memory**, with at least **20 GB of storage**.

---

## Google Cloud Platform

The equivalent Google Cloud service is **Google Compute Engine**.

Google Compute Engine provides configurable virtual machines that can run Linux operating systems and applications. CPU, memory, storage, and networking resources can be selected according to the workload requirements.

### Possible Google Cloud Service

* **Google Compute Engine** – Hosts the Linux server as a cloud-based virtual machine.
* **Persistent Disk** – Provides persistent storage for the virtual machine.

A suitable starting configuration would provide at least **1 vCPU and approximately 2 GiB of memory**, with at least **20 GB of storage**.

---

# Cloud Service Comparison

| Cloud Provider            | Cloud Service              | Starting Resource Consideration             | Purpose                                             |
| ------------------------- | -------------------------- | ------------------------------------------- | --------------------------------------------------- |
| **AWS**                   | **Amazon EC2**             | At least 1 vCPU, ~2 GiB RAM, 20+ GB storage | Hosts Linux-based virtual machines and applications |
| **Microsoft Azure**       | **Azure Virtual Machines** | At least 1 vCPU, ~2 GiB RAM, 20+ GB storage | Hosts Linux-based virtual machines and applications |
| **Google Cloud Platform** | **Google Compute Engine**  | At least 1 vCPU, ~2 GiB RAM, 20+ GB storage | Hosts Linux-based virtual machines and applications |

> **Note:** The suggested resources are based on the current KillerCoda server configuration. The exact VM or instance size should be selected based on the application's workload, performance requirements, pricing, and future resource needs.

---

# Migration Considerations

When migrating the Linux server to the cloud, the operating system, CPU requirements, memory requirements, and disk space should be considered.

Based on the KillerCoda investigation, the server currently uses **1 CPU core, 1.9 GiB of RAM, and 19 GB of root disk space**.

The selected cloud virtual machine should provide enough computing resources to run the Linux operating system and its applications. Storage should also be sufficient for the operating system, applications, logs, databases, backups, and future data.

Other factors such as **cost, network performance, security, availability, scalability, and existing infrastructure** should also be considered when selecting a cloud provider.

---

# Recommended Cloud Platform

For a general-purpose Linux server, **Amazon Web Services (AWS)** would be a suitable choice because Amazon EC2 provides flexible virtual machine configurations and a broad range of additional cloud services.

However, **Microsoft Azure** and **Google Cloud Platform** are also capable of hosting the same Linux server. The final choice should depend on the organization's budget, technical requirements, existing infrastructure, and preferred cloud ecosystem.

