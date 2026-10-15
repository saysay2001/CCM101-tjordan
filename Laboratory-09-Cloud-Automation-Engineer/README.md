# Laboratory 09 – Cloud Automation Engineer

## Mission Overview

This laboratory focuses on automating routine cloud operations using Bash scripting and cron jobs in a Linux environment. The main task was to create a script that compresses client data into a timestamped backup archive and schedule it to run automatically every day at 2:00 AM.

## Objectives

- Understand Bash scripts, variables, and cron jobs.
- Create a sample directory containing client data.
- Develop a Bash script to automate data backups.
- Use `chmod +x` to make the script executable.
- Schedule automated backups using Linux cron.
- Document the script and its configuration for future reference.

## Commands Executed

### Create Sample Data

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
```

### Create the Backup Script

```bash
nano backup.sh
```

### Make the Script Executable

```bash
chmod +x backup.sh
```

### Execute the Script

```bash
./backup.sh
```

### Check the Backup Files

```bash
ls -lh backups
```

### Verify the Backup Archive Contents

```bash
tar -tzf backups/backup_*.tar.gz
```

### Check Existing Cron Jobs

```bash
crontab -l
```

### Edit the Cron Configuration

```bash
env EDITOR=nano crontab -e
```

### Scheduled Cron Entry

```bash
0 2 * * * /root/backup.sh
```

### Verify the Installed Schedule

```bash
crontab -l
```

## Skills Learned

- **Bash scripting:** Creating scripts that execute multiple commands automatically.
- **Variables:** Storing directory paths and timestamps for easier script management.
- **Linux file permissions:** Using `chmod +x` to allow a script to execute.
- **File compression:** Using `tar` to create compressed backup archives.
- **Cron scheduling:** Configuring recurring tasks in Linux.
- **Technical documentation:** Recording commands and explaining configurations.
- **Cloud automation:** Reducing repetitive manual work and improving consistency in routine operations.

## Conclusion

This laboratory provided practical experience in automating backups using Bash scripts and cron jobs. I learned how to create a backup archive, configure file permissions, and schedule a recurring task. These skills are useful for managing cloud servers and performing routine maintenance more efficiently.
