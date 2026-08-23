# Identify Cloud Infrastructure Components

## Introduction

  Cloud computing infrastructure is composed of several components that work together to provide computing services. The major infrastructure components observed in the KillerCoda Linux environment are compute resources, storage resources, networking resources, and the operating system.
  Based on the command executed in the Linux environment, the system is running Ubuntu 24.04.4 LTS on a virtualized KVM environment. The system has 1 CPU, approximately 1.9 GiB of RAM, a 20 GB virtual disk, and assigned IP addresses.

## 1. Compute Resources

**Observed Resources**

  The compute resources of the KillerCode environment were identified using the lscpu, nproc, and free -h commands.

*The system reported:*
> CPU Architecture: x86_64

> CPU(s): 1

> CPU Core(s): 1

> CPU Socket(s): 1

> CPU Model: Intel Xeon E312xx (Sandy Bridge, IBRS update)

> CPU Speed: Approximately 2.0 GHz based on the BIOS model information

> Virtualization: KVM

> RAM: 1.9 GiB

> Available RAM: 1.5 GiB

> Swap: 1.0 GiB

  The lscpu output specifically identifies KVM as the hypervisor vendor and the virtualization type as full virtualization. This indicates that the Linux environment is running as a virtual machine rather than directly on physical hardware.

**Purpose**

  Compute resources provide the processing capability required to execute operating-system processes, commands, applications, and services. The CPU performs calculations and instructions, while RAM provides temporary working memory for running processes.

**Importance in Cloud Computing**

  Compute resources are one of the fundamental components of cloud computing. Cloud providers allocate virtual CPUs and memory to virtual machines based on workload requirements. This allows users to obtain computing power without owning or maintaining physical servers.
  Cloud computing also allows compute resources to be scaled depending on demand. For example, an application requiring more processing power can be assigned additional CPUs or memory.

**Relation to Killercoda**

  The KillerCoda environment provides a limited amount of virtual compute resources for practicing Linux and cloud infrastructure concepts. The system has 1 virtual CPU and approximately 1.9 GiB of RAM.

*The lscpu output shows:*

> CPU(s): 1

> Core(s) per socket: 1

> Socket(s): 1

> Hypervisor vendor: KVM

> Virtualization type: full

  This demonstrates how cloud platforms can provide users with virtualized compute resources instead of direct access to physical hardware.



## 2. Storage Resources

  Storage resources were examined using the lsblk and df -h commands.

*The lsblk command identified a virtual disk:*

vda     20G  disk
├─vda1  19G  part /
├─vd
a14   4M part
├─vda15 106M part /boot/efi
└─vda16 913M part /boot

*The main filesystem was identified by df -h as:*

/dev/vda1    19G    5.4G    13G    30%    /

  Other storage areas include the /boot and /boot/efi partitions.

**Purpose**

  Storage resources provide space for permanently storing operating-system files, applications, configuration files, logs, and user data.
In the Linux environment, the virtual disk stores the Ubuntu operating system and the files required for the KillerCoda environment to operate.

**Importance in Cloud Computing**

  Storage is essential in cloud computing because applications and services need a reliable location for storing data. Cloud platforms can provide different types of storage depending on application requirements, including block storage, file storage, and object storage. 
  Virtual disks such as the one observed in KillerCoda are similar to block storage attached to a cloud virtual machine.

**Relation to KillerCoda**

  The KillerCoda environment provides a 20 GB virtual disk, represented as /dev/vda.
  The primary partition /dev/vda1 has approximately 19 GB of capacity, with 5.4 GB used and 13 GB available. This demonstrates how storage can be allocated as a virtual resource to a cloud-based or virtualized Linux machine.
  The output also shows separate partitions for /boot and /boot/efi, which support the operating system's boot process.



## 3. Networking Resources

**Observed Resources**

  Networking information was examined using the hostname -I command.

*The system returned:*

172.30.1.2

172.17.0.1

These are private IP addresses assigned to network interfaces within the virtualized environment.

**Purpose**

  Networking resources allow the Linux system to communicate with other systems, services, and networks. They provide connectivity that allows applications to exchange data and access external resources.

**Importance in Cloud Computing**  

  Networking is essential to cloud computing because cloud resources rarely operate independently. Virtual machines, databases, applications, containers, and users need to communicate with each other.

*Cloud networking provides features such as:*

> IP addressing

> Network interfaces

> Routing

> Private networks

> Internet connectivity

> Communication between cloud services

  Networking also plays an important role in security because cloud environments can separate resources into private and public networks.

**Relation to KillerCoda**

*The KillerCoda Linux environment has private IP addresses:*

> 172.30.1.2

> 172.17.0.1

  The 172.30.1.2 address represents connectivity within the environment's virtual network, while 172.17.0.1 is commonly associated with Docker's default bridge network.
  The presence of these addresses demonstrates that the environment uses virtual networking to allow the Linux system and its services to communicate within the virtualized infrastructure.



## 4. Operating System

**Observed Operating System**

*The KillerCoda environment is running:*

> Ubuntu 24.04.4 LTS

> Codename: Noble Numbat

**The Linux kernel version is:*

> 6.8.0-138-generic

*This information was obtained using:*

> cat /etc/os-release

> uname -r

**Purpose**

  An operating system manages the computer's hardware and software resources. It provides the environment where applications and services can run.

*Linux manages resources such as:*

> CPU processes

> Memory

> Storage

> Network interfaces

> Users and permissions

> System services

> Hardware and virtual devices

**Importance in Cloud Computing**

  The operating system is an important layer of cloud infrastructure because applications and services generally run on top of an operating system.
  Linux is widely used in cloud environments because it is open-source, flexible, stable, efficient, and supports a large ecosystem of server applications and management tools.


**Relation to KillerCoda**

  KillerCoda provides an Ubuntu 24.04.4 LTS Linux environment. Users can interact with the operating system through the command line and use standard Linux commands to inspect and manage infrastructure resources.

*The following output confirms the operating system:*

> PRETTY_NAME="Ubuntu 24.04.4 LTS"

> VERSION_ID="24.04"

> VERSION_CODENAME=noble

*The environment uses the Linux kernel:*

< 6.8.0-138-generic

  This gives students practical experience managing a Linux-based environment similar to those commonly used for cloud servers.



## Summary of Observed Infrastructure

| Component            | Observed Example     | Details                                   |
| -------------------- | -------------------- | ----------------------------------------- |
| **Compute**          | Virtual CPU and RAM  | 1 CPU, 1 core, 1.9 GiB RAM                |
| **Virtualization**   | KVM                  | Full virtualization                       |
| **Storage**          | `/dev/vda`           | 20 GB virtual disk                        |
| **Main Filesystem**  | `/dev/vda1`          | 19 GB total, 5.4 GB used, 13 GB available |
| **Networking**       | Private IP addresses | `172.30.1.2`, `172.17.0.1`                |
| **Operating System** | Ubuntu Linux         | Ubuntu 24.04.4 LTS                        |
| **Kernel**           | Linux kernel         | `6.8.0-138-generic`                       |



## Conclusion

  The KillerCoda environment demonstrates the main infrastructure components used in cloud computing. The compute resources provide CPU and memory for running processes, while the storage resources provide space for the operating system and data. The networking resources allow the environment to communicate with other systems and services, and the Ubuntu operating system manages these resources and provides the platform for applications and administrative tasks.

  The identification of KVM virtualization is particularly important because it demonstrates how cloud computing can abstract physical hardware into virtual resources. Instead of directly interacting with a physical server, the user works with a virtual Linux machine that has allocated CPU, memory, storage, and networking resources. This is a practical example of how cloud infrastructure provides computing resources as virtualized services.
