# Cloud Infrastructure Investigation Report

## 1. Overview
This report documents the investigation of the Linux cloud server environment provided through the KillerCoda Playground. The investigation examined the operating system, kernel, compute resources, memory, storage, mounted file system, hostname, and network configuration of the server.

## 2. Operating System
**Command Used:**
cat /etc/os-release

**Findings:**
> Operating System: Ubuntu 24.04.4 LTS

> Version Codename: Noble Numbat

> Version ID: 24.04

The cloud server is running Ubuntu 24.04.4 LTS, which provides the operating system environment where applications and cloud services can run.

## 3. Kernel Version
**Command Used:**
uname -r

**Finding:**
> Kernel Version: 6.8.0-138-generic

The Linux kernel serves as the core component between the operating system and the underlying virtualized hardware resources.

## 4. CPU / Compute Resources
**Command Used:**
lscpu

**Findings:**
> Architecture: x86_64

> CPU Model: Intel Xeon E312xx (Sandy Bridge, IBRS update)

> CPU(s): 1

> CPU Cores per Socket: 1

> Socket(s): 1

> Thread(s) per Core: 1

> Hypervisor: KVM

The server is provided with one virtual CPU core. The x86_64 architecture indicates that the system uses a 64-bit processor architecture. The KVM hypervisor indicates that the server is running in a virtualized environment.

## 5. CPU Core Count
**Command Used:**
nproc

**Finding:**
> Number of CPU Cores: 1

The nproc command confirms that one processing unit is available to the Linux environment.

## 6. Memory / RAM
**Command Used:**
free -h

**Findings:**
> Total RAM: 1.9 GiB

> Used RAM: 411 MiB

> Free RAM: 870 MiB

> Available RAM: 1.5 GiB

> Swap: 1.0 GiB

The server has approximately 1.9 GiB of physical memory available to the virtual machine. It also has 1.0 GiB of configured swap space.

## 7. Disk Capacity
**Command Used:**
lsblk

**Findings:**
> Main Virtual Disk: /dev/vda

> Total Disk Capacity: 20 GB

> Root Partition: /dev/vda1 — 19 GB

> EFI Partition: /dev/vda15 — 106 MB

> Boot Partition: /dev/vda16 — 913 MB

The server uses a 20 GB virtual disk. The main 19 GB partition is used as the root filesystem.

## 8. Mounted File Systems
**Command Used:**
df -h

**Findings:**
| Filesystem | Size |  Used | Available | Mount Point |
| ---------- | ---: | ----: | --------: | ----------- |
| tmpfs      | 191M | 1000K |      190M | `/run`      |
| /dev/vda1  |  19G |  5.4G |       13G | `/`         |
| tmpfs      | 952M |   84K |      952M | `/dev/shm`  |
| tmpfs      | 5.0M |     0 |      5.0M | `/run/lock` |
| /dev/vda16 | 881M |  117M |      703M | `/boot`     |
| /dev/vda15 | 105M |  6.2M |       99M | `/boot/efi` |

The root filesystem is mounted at / and has 19 GB of allocated storage. Additional filesystems are mounted for system operations, shared memory, boot files, and EFI boot information.

## 9. Hostname
**Command Used:**
hostname

**Finding:**
> Hostname: ubuntu

The hostname identifies the Linus server within its network and system environment.

## 10. IP Address
**Command Used:**
hostname -I

**Findings:**
> IP Address: 172.30.1.2

> Additional Docker Network Address: 172.17.0.1

The 172.30.1.2 address represents the server's network address in the KillerCoda environment. The 172.17.0.1 address is associated with the Docker networking environment.

## Infrastructure Summary
The investigation shows that the KillerCoda cloud server is a virtualized Linux environment running Ubuntu 24.04.4 LTS on the KVM hypervisor.

The compute layer consists of one virtual CPU core and approximately 1.9 GiB of RAM. The storage layer consists of a 20 GB virtual disk with the primary root filesystem mounted at /. The networking layer provides the server with an IP address and additional Docker networking. The operating system and kernel provide the software foundation that manages these virtualized hardware resources.

These components work together to provide the basic infrastructure required for hosting applications and cloud-based services.

## Note: 
Screenshots of the Linux commands and their outputs are included in the screenshots directory of this laboratory folder.
