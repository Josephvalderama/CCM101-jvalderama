Backup Script Guide
The Script (backup.sh)
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


What chmod +x backup.sh Did
A newly created file in Linux is treated as plain data, even when it is full
of valid shell commands. This is a safety measure that stops the system from
running arbitrary text files as programs. The chmod +x backup.sh command
adds execute permission to the file, which marks it as something Linux is
allowed to run. Without it, trying to launch ./backup.sh ends with a
"Permission denied" error.

Before and after
Running the script before changing its permissions failed:
root@ubuntu:~# ./backup.sh
bash: ./backup.sh: Permission denied

Once chmod +x backup.sh was applied, the script ran without problems and
created a compressed backup:
root@ubuntu:~# chmod +x backup.sh
root@ubuntu:~# ./backup.sh
Initiating automated backup...
Backup completed successfully at 20261015_020224!
root@ubuntu:~# ls -l backups/
total 4
-rw-r--r-- 1 root root 178 Oct 15 02:02 backup_20261015_020224.tar.gz
Cron Expression Breakdown: 0 2 * * * /root/backup.sh
| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | Runs at the top of the hour (minute 0) |
| Hour | 2 | Runs during the 2 AM hour (02:00 in 24-hour time) |
| Day of Month | * | Matches every day of the month |
| Month | * | Matches every month of the year |
| Day of Week | * | Matches every day of the week |

Combined, these fields tell the system to launch /root/backup.sh by itself
every night at exactly 2:00 AM, with nobody needing to start it.

Installed schedule (crontab -l)
...
# m h  dom mon dow   command
0 2 * * * /root/backup.sh

