# Backup Script Guide

### 1. Overview

This document explains the automated backup script created for CloudNova Technologies. The script backs up client data by compressing the `app-data` directory into a timestamped archive. A Linux cron job is configured to execute the script automatically every day at 2:00 AM.

### 2. Complete Backup Script

The following is the Bash script saved as `backup.sh`.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

### 3. Explanation of chmod +x

The command used was:

```bash
chmod +x backup.sh
```

The `chmod` command changes file permissions, while `+x` adds execute permission. This allows the script to be executed directly using `./backup.sh` instead of manually running each command inside the file.

### 4. Cron Job Configuration

The following cron entry was installed:

```bash
0 2 * * * /root/backup.sh
```

This schedules the backup script to run every day at 2:00 AM, based on the system's configured time and timezone.

### 5. Breakdown of the Cron Expression

| Time Field | Value | Explanation |
|---|---|---|
| Minute | `0` | Runs at minute zero. |
| Hour | `2` | Runs at 2 AM. |
| Day of Month | `*` | Runs every day of the month. |
| Month | `*` | Runs every month. |
| Day of Week | `*` | Runs every day of the week. |

The asterisk (`*`) means every applicable value for that field.

### 6. How the Backup Process Works

1. The script identifies the source directory containing the client data.
2. It defines the directory where backups will be stored.
3. It generates a timestamp to create a unique backup filename.
4. It creates the backup directory if it does not exist.
5. The `tar -czf` command compresses the source directory into a `.tar.gz` archive.
6. The cron job runs the script automatically according to the configured schedule.

### 7. Conclusion

This task demonstrates how Bash scripting and cron scheduling can automate routine backup operations. Automation reduces manual work and helps maintain consistent backups. In a production environment, the script should use verified absolute paths, log its results, and store additional copies of backups in a separate secure location.
