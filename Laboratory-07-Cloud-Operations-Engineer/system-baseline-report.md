# System Baseline Report

## 1. Memory (RAM) Check

- **Total RAM:** 1.9 GiB
- **Used RAM:** 468 MiB
- **Free RAM:** 1.1 GiB
- **Available RAM:** 1.4 GiB
- **Swap Memory:** 1.0 GiB

The `free -h` command was used to check the server's memory usage and availability.

## 2. Disk Storage Check

- **Total Root Filesystem Storage (/):** 19 GB
- **Used Disk Space:** 5.5 GB
- **Available Disk Space:** 13 GB
- **Disk Usage:** 30%

The `df -h /` command was used to check the total and available storage capacity of the root filesystem.

## 3. CPU and Process Monitoring

The `top` command was used to observe the server's CPU utilization, system load, and active running processes.

## 4. Importance of Disk Space Monitoring

Checking disk space before a massive traffic surge is critical because increased traffic can generate more logs, temporary files, and application data, potentially filling the disk and causing application failures or service interruptions.

## 5. Screenshots

- `screenshots/memory-check.png`
- `screenshots/disk-check.png`
